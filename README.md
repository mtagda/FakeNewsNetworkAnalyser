# FakeNewsNetworkAnalyser


# NewsGraph.de


We can’t combat fake news by ourselves but we can give people tool that enables them to better understand what mechanisms stand behind it. This tool will reveal and analyse the social networks structures standing behind the spread of the fake news, and name it’s most important actors. We need to give one an ability to instantly visualize the data, in order to deduct key insights, and enable the export of the data to further analysis. This tool needs to be easily accessible through useful Web User Interface, and highly efficient in computation of graphs. We will be then able to store the network graphs, and finally, we want to try to apply ML algorithms that will look for similarities in our collected Graph Database in order to better show the hidden patterns.

#Workflow

Die Analyse von Fake News Netzwerke müssen wir um eine Soziale Netzwerke verankern. Twitter wäre dafür ein guter Ausgangspunkt, weil dieser Mikroblogging Dienst einen umfangreichen API-Zugriff bietet und man in der Lage ist die Verbindungen zwischen einzelnen Beiträgen gut nachzuvollziehen. Später könnten wir daran denken, wie wir zum Beispiel Facebook-Daten greifen und als Graph darstellen könnten (Graph API) .

Zunächst wird die Datenextraktion von Twitter-Daten durchgeführt, damit man für die Analyse notwendige Informationen erhält. Es wird ein Graph von Twitter-Interaktionen (Retweet, Quote Tweet, Reply, Likes) zwischen einem Tweet (insbesondere Fake Tweet) und anderen Benutzer erstellt.  Es werden dann Signalstärke als auch andere Scores berechnet die wichtige Informationen darüber liefern, wie weit ein Tweet verbreitet ist. Wir müssen noch passende Scoring-Algorithme ausdenken die unseren Bedürfnissen entsprechen, dh. es sollten richtige und aussagekräftige Aussagen über jeden einzelnen Tweet getroffen werden.

Eine andere nützliche Methode für die Datenanalyse könnte Clusteranalyse sein. Unter Clusteranalyse versteht man die Einteilung von Datenpunkten in Gruppen, sogenannte Cluster. Dabei sollen möglichst ähnliche Daten dem gleichen Cluster zugeordnet werden und sehr verschiedene Daten unterschiedlichen Clustern. Das Ziel hier wäre herauszufinden, welche Twitter-Nutzern-Gruppen ein bestimmtes Tweet verbreitet haben.  Zum Thema Community Detection wurde schon bereits vieles entwickelt. Es gibt versichernde Algorithmen die in der Lage sind, unterschiedliche Community Types (interaction based, topic based etc.) zu bestimmen. 

Die ganze Logik können wir dann in Python schreiben, und per AWS deployen. Wir bräuchten noch eine Web UI, oder genauer Content Management System um die Logik zur Analyse von eingegebenen Daten durchzuführen und auszugeben. Als Eingangstor sollte eine MEAN.JS applikation dienen wo wird das Ganze logik zum Nutzer/Projektverwaltung abgelegt. WebUI sollte für die schwierige analysen den AWS Lambda deployed backend ansprechen .Die Ergebnisse (Graphen (insbesondere interaktive Visualisierung, Scores etc.) stellen wir dann übersichtlich vor(JavaScript d3.js three.js) , mit einer einfachen Exportierung-Möglichkeit. Wir könnten auch die Ergebnisse die mit Fake News verbunden sind speichern und dann miteinander vergleichen sowie nach Ähnlichkeiten suchen (mit hilfe des maschinellen Lernens, oder andere Graph Analysis tools wie neo4j ...). 




Tomasz Tkaczyk(github:gniewsus)
Magdalena Trzeciak (github: mtagda)

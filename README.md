# digraph
Render directed graphs in Qlik Sense

This Extension builds on top of the javascript version viz.js of graphviz (see: https://github.com/mdaines/viz.js/wiki/API) from Mike Daines. It can be used for plotting directed graphs in Qlik Sense to display processes, networks, (material) flow and basically any (directed) relation between nodes.

# Usage

Download the zip file and extract it to your local Qlik Sense Desktop Extension folder or import it to a Qlik Sense Server via QMC. Drag&Drop the new Digraph extension to your canvas. Digraph needs 2 dimensions (nodes: "from" and "to") and 1 measure (value for edge).

# Beware

Graphviz is fast, but due to it's nature to try to draw graphs according to force models trying to minimize crossing edges there IS a limit (not a hard limit, more a practical one) of nodes/edges, which can be plotted inside of Qlik Sense. This depends on the used renderer and the complexity of the DOT representation, as well. Max number of nodes can get as low as less than 100, in contrast I successfully plotted a graph with A LOT more nodes/edges. It heavily relies on the use case. Weird node names or edge values might break the DOT syntax. 

The standalone non-JS version is far more robust and offers higher performance (see: https://www.graphviz.org/ for further information).

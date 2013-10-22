# Study notes

These are the study notes that I made as I worked through this chapter.

## Day 1

### Neo4J is Whiteboard Friendly

Neo4J speaks to me more than the other databases because it models data in the same way that I do, as graphs of interconnected nodes.

The sideEffect function doesn't appear to work.

craig = g.addVertex(['name':'Craig'])
toni = g.addVertex(['name':'Toni'])
g.addEdge(craig, toni, 'married_to')
charlotte = g.addVertex(['name':'Charlotte'])
g.addEdge(craig, charlotte, 'father')
g.addEdge(toni, charlotte, 'mother')
kiera = g.addVertex(['name':'Kiera'])
g.addEdge(craig, kiera, 'father')
g.addEdge(toni, kiera, 'mother')

martin = g.addVertex(['name':'Martin'])
g.addEdge(martin, craig, 'father')
carol = g.addVertex(['name':'Carol'])
g.addEdge(carol, craig, 'mother')
g.addEdge(martin, carol, 'married_to')

tony = g.addVertex(['name':'Tony'])
g.addEdge(tony, toni, 'father')
glynis = g.addVertex(['name':'Glynis'])
g.addEdge(glynis, toni, 'mother')
g.addEdge(tony, glynis, 'divorced_from')

bernie = g.addVertex(['name':'Bernie'])
g.addEdge(tony, bernie, 'married_to')

john = g.addVertex(['name':'John'])
g.addEdge(john, glynis, 'divorced_from')
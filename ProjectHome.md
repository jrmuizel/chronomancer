The [Chronicle](http://code.google.com/p/chronicle-recorder) framework provides complete register and memory-level recording of Linux processes and efficient queries over the recorded traces. Chronomancer builds on Chronicle by providing a UI for inspecting and querying traces --- effectively an extremely powerful debugger. Chronomancer can display program state for any chosen point in time; find the last write to any given memory location; display the execution path taken through a function (no more stepping!); display correct call stacks in the presence of tail calls or stack corruption; and much more!

Chronomancer supports debugging C and C++ programs with DWARF2/3 debug information such as is generated by gcc. It is implemented in Java as an Eclipse plugin and can integrate with the Eclipse CDT. It offers extension points so other plugins can define new commands, views, event queries, and custom data renderers.

Chronomancer is small, about 10K lines of code, quite new, and has many rough edges and missing features. (There are many features that would be easy to add that no other debugger has ever offered.) However, it can already be used to debug interesting problems; it has already been used to successfully analyze a difficult Firefox garbage collection bug.

Chronomancer is released with the permission of the Mozilla Foundation. Thanks MF!
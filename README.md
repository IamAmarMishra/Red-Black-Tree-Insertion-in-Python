# Advance-Data-Structures
This is python 3 code for creating or inserting a new node and searching a value in RB Tree.

The value of nodes is provided in the form space seprated values in a line and after providing the values press enter to execute the insertion operation.

After creating the RB Tree, search function is called to find the path of any node in the tree, to stop the searching function enter any character from keyboard.

# Algorithm for Insertion
Following is detailed algorithm. The algorithms has mainly two cases depending upon the color of uncle. If uncle is red, we do recoloring. If uncle is black, we do rotations and/or recoloring.

Color of a NULL node is considered as BLACK.

Let x be the newly inserted node.
1) Perform standard BST insertion and make the color of newly inserted nodes as RED.

2) If x is root, change color of x as BLACK (Black height of complete tree increases by 1).

3) Do following if color of x’s parent is not BLACK and x is not root.
….a) If x’s uncle is RED (Grand parent must have been black from property 4)
……..(i) Change color of parent and uncle as BLACK.
……..(ii) color of grand parent as RED.
……..(iii) Change x = x’s grandparent, repeat steps 2 and 3 for new x.
redBlackCase2

….b) If x’s uncle is BLACK, then there can be four configurations for x, x’s parent (p) and x’s grandparent (g) (This is similar to AVL Tree)
……..i) Left Left Case (p is left child of g and x is left child of p)
……..ii) Left Right Case (p is left child of g and x is right child of p)
……..iii) Right Right Case (Mirror of case i)
……..iv) Right Left Case (Mirror of case ii)

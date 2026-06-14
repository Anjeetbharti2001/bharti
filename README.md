# bharti
this is my 
<br>
<p> Every day self improve coder life ,<br> i understanding that little code name of the code</p>
<p>something facing the error in code</p>


class Node {<br>
    int data;<br>
    Node left;<br>
    Node right;<br>

    Node(int data) {
        this.data = data;
        this.left = null;
        this.right = null;
    }
}

public class Tree {

    static class BnTree {
        static int idx = -1;

        public static Node buildTree(int nodes[]) {
            idx++;

            if (nodes[idx] == -1) {
                return null;
            }

            Node newNode = new Node(nodes[idx]);
            newNode.left = buildTree(nodes);
            newNode.right = buildTree(nodes);

            return newNode;
        }
    }

    public static void main(String args[]) {
        int nodes[] = {1, 2, 4, -1, -1, 5, -1, -1, 3, -1, 6, -1, -1};

        BnTree tree = new BnTree();
        Node root = tree.buildTree(nodes);

        System.out.println(root.data);
    }
}

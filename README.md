# Trees
### To create the tree nodes

`

    public class BTree {
    static Root root;

    private class Root {
        private Root left;
        private Root right;
        int val;

        public Root(int val) {
            this.val = val;
        }
    }
    
        public void createTree() {
            Root r = new Root(2);
            Root rl = new Root(4);
            Root rr = new Root(4);
            root = r;
            r.left = rl;
            r.right = rr;
        }

        public void printTree(Root root) {
            if (root == null) return;
            printTree(root.left);
            System.out.println(root.val);
            printTree(root.right);
        }

        public static void main(String[] args) {
           BTree bt=new BTree();
           bt.createTree();
           bt.printTree(bt.root);
       }
    }
  
`

 

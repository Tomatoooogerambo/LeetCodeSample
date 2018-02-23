### Binary Tree Preorder traversal
#### 1. Recursive
```
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public List<Integer> preorderTraversal(TreeNode root) {
        List<Integer> pre = new LinkedList<Integer>();
        helper(root, pre);
        return pre;
    }
    public void helper(TreeNode root, List<Integer> pre){
        if (root == null) return;
        pre.add(root.val);
        helper(root.left, pre);
        helper(root.right, pre);
    }
}
```

#### 2.Iteratively
```
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public List<Integer> preorderTraversal(TreeNode root) {
        List<Integer> list = new ArrayList<Integer>();
        Stack<TreeNode>  stack = new Stack<TreeNode>();
        TreeNode tempNode = new TreeNode();
        if(root != null)
            stack.push(tempNode);
        while(root != null) {
            if(!stack.isEmpty()) 
                list = stack.pop().val;
            if(root.left != null)
                tempNode = 
        }
    }
}
```
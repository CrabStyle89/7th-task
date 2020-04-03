/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     public int val;
 *     public TreeNode left;
 *     public TreeNode right;
 *     public TreeNode(int x) { val = x; }
 * }
 */
public class Solution {
    public bool IsSymmetric(TreeNode root) 
    {
        if (root != null)
			{
				int a = root.left.val;
				int b = root.right.val;
				if (a==b)
                {
                   IsSymmetric(root.left);
                    a= root.left.val;
                   IsSymmetric(root.right); 
                    b=root.right.val;
                }
                else return false;
			}
else return false;
        return true;
        
    }
}

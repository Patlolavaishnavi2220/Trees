#0 based index
class Node:
    def __init__(self,data):
        self.data=data
        self.left=None
        self.right=None
def createbt(arr,i,n):
    if i>=n:
        return None
    root=Node(arr[i]) 
    root.left=createbt(arr,2*i+1,n)
    root.right=createbt(arr,2*i+2,n)
    return root
def preorder(root): 
    if root:
        print(root.data,end=" ")
        preorder(root.left)
        preorder(root.right)
def level(root):
    if not root:
        return[]
    q=[root]
    res=[]
    while q:
        node=q.pop(0)
        res.append(node.data)
        if node.left:
            q.append(node.left)
        if node.right:
            q.append(node.right)
    return res
def presearch(root,ele):
    if root is None:
        return False
    if root.data==ele:
        return True
    return presearch(root.left,ele) or presearch(root.right,ele)
def levelsearch(root,ele):
    if not root:
        return False
    q=[root]
    while q:
        node=q.pop(0)
        if node.data==ele:
            return True
        if node.left:
            q.append(node.left)
        if node.right:
            q.append(node.right)
arr=list(map(int,input().split()))
btree=createbt(arr,0,len(arr))
preorder(btree)
print(level(btree))
print(presearch(btree,4))

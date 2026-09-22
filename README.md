# Swapping-Nodes-in-a-Linked-List
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def swapNodes(self, head: Optional[ListNode], k: int) -> Optional[ListNode]:
        if head is None:
            return None
        temp=head
        n=0
        while temp:
            n+=1
            temp=temp.next
        temp=head
        for i in range(k-1):
            temp=temp.next
        a=temp
        temp=head
        for i in range(n-k):
            temp=temp.next
        b=temp
        a.val,b.val=b.val,a.val
        return head

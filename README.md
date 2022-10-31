# FirstProgram

class Solution:
    def detectCycle(self, head: Optional[ListNode]) -> Optional[ListNode]:
        current=head
        pre=head
        first=head
        if (head!=None and head.next!=None):
            
            while (current.next and current.next.next):
                pre=pre.next
                current=current.next.next
                if (current==pre):
                    while (pre!=first):
                        pre=pre.next
                        first=first.next
                    return first
            
        

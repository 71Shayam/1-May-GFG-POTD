 struct Node* arrangeCV(Node* head) {
        // Code here
        Node *vowel=new Node('a'),*con=new Node('b');
        Node *vowelH=vowel,*conH=con;
        while(head){
            char temp = head->data;
            if(temp=='a' or temp=='e' or temp=='i' or temp=='o' or temp=='u'){
                vowel->next=head;
                vowel=vowel->next;
            }
            else{
                con->next=head;
                con=con->next;
            }
            head=head->next;
        }
        con->next=NULL;
        vowel->next=conH->next;
        return vowelH->next;
    }

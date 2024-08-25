#include <stdio.h>
#include <stdlib.h>

struct node {
    int data;
    struct node *next;
};

void insert_after(struct node *head) {
    struct node *p, *current;
    int key;

    printf("Enter the element after which you want to add a new element: ");
    scanf("%d", &key);

    current = head;
    while (current != NULL && current->data != key) {
        current = current->next;
    }
    
    if (current != NULL) {
        p = (struct node *)malloc(sizeof(struct node));
        printf("Enter the value of the new node: ");
        scanf("%d", &p->data);
        p->next = current->next;
        current->next = p;
    } 
}

int main() {
    struct node *head, *p, *q;
    char ch;

    head = (struct node *)malloc(sizeof(struct node));
    printf("Enter the value of the first node: ");
    scanf("%d", &head->data);
    head->next = NULL;

    p = head;
    do {
        q = (struct node *)malloc(sizeof(struct node));
        printf("Enter the value of the next node: ");
        scanf("%d", &q->data);
        q->next = NULL;
        p->next = q;
        p = q;
        while (getchar() != '\n');

        printf("Press 'y' to add another node\n ");
        ch = getchar();
    } while (ch == 'y');

    insert_after(head);


    printf("The linked list is:\n");
    p = head;
    while (p != NULL) {
        printf("%d\n", p->data);
        p = p->next;
    }

    p = head;
    while (p != NULL) {
        q = p->next;
        free(p);
        p = q;
    }

    return 0;
}

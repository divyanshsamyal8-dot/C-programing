#include <stdio.h>
#include <stdlib.h>
#define MAX 100

int list[MAX];
int n = 0;

/* Insert at Beginning */
void insertInBeg(int value) {
    if (n == MAX) {
        printf("List is full!\n");
        return;
    }
    for (int i = n; i > 0; i--) {
        list[i] = list[i - 1];
    }
    list[0] = value;
    n++;
}

/* Insert at End */
void insertAtEnd(int value) {
    if (n == MAX) {
        printf("List is full!\n");
        return;
    }
    list[n++] = value;
}

/* Insert at Position */
void insertAtPos(int value, int pos) {
    if (n == MAX || pos < 0 || pos > n) {
        printf("Invalid position or list full!\n");
        return;
    }
    for (int i = n; i > pos; i--) {
        list[i] = list[i - 1];
    }
    list[pos] = value;
    n++;
}

/* Delete from Beginning */
void deleteFromBeg() {
    if (n == 0) {
        printf("List is empty!\n");
        return;
    }
    for (int i = 0; i < n - 1; i++) {
        list[i] = list[i + 1];
    }
    n--;
}

/* Delete from End */
void deleteFromEnd() {
    if (n == 0) {
        printf("List is empty!\n");
        return;
    }
    n--;
}

/* Delete from Position */
void deleteFromPos(int pos) {
    if (n == 0 || pos < 0 || pos >= n) {
        printf("Invalid position!\n");
        return;
    }
    for (int i = pos; i < n - 1; i++) {
        list[i] = list[i + 1];
    }
    n--;
}

/* Display */
void display() {
    if (n == 0) {
        printf("List is empty!\n");
        return;
    }
    for (int i = 0; i < n; i++) {
        printf("%d ", list[i]);
    }
    printf("\n");
}

/* Search */
void search(int key) {
    for (int i = 0; i < n; i++) {
        if (list[i] == key) {
            printf("Element found at index %d\n", i);
            return;
        }
    }
    printf("Element not found!\n");
}

/* Update */
void update(int pos, int value) {
    if (pos < 0 || pos >= n) {
        printf("Invalid position!\n");
        return;
    }
    list[pos] = value;
}

/* Sort (Bubble Sort) */
void bubbleSort() {
    if(n == 0)
        printf("List is Empty!!\n");
    else{
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {
                if (list[j] > list[j + 1]) {
                    int temp = list[j];
                    list[j] = list[j + 1];
                    list[j + 1] = temp;
                }
            }
        }
        printf("Element Sorted!!\n");
    }
}

int main() {
    int choice, value, pos;

    while (1) {
        printf("\n1. Insert in Beginning");
        printf("\n2. Insert at End");
        printf("\n3. Insert at Any Position");
        printf("\n4. Delete from Beginning");
        printf("\n5. Delete from End");
        printf("\n6. Delete from Given Position");
        printf("\n7. Display List");
        printf("\n8. Search Element in List");
        printf("\n9. Update Element of List");
        printf("\n10. Sort Element of List");
        printf("\n11. Exit");

        printf("\nEnter Choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Enter value: ");
                scanf("%d", &value);
                insertInBeg(value);
                break;
            case 2:
                printf("Enter value: ");
                scanf("%d", &value);
                insertAtEnd(value);
                break;
            case 3:
                printf("Enter value and position: ");
                scanf("%d %d", &value, &pos);
                insertAtPos(value, pos);
                break;
            case 4:
                deleteFromBeg();
                break;
            case 5:
                deleteFromEnd();
                break;
            case 6:
                printf("Enter position: ");
                scanf("%d", &pos);
                deleteFromPos(pos);
                break;
            case 7:
                display();
                break;
            case 8:
                printf("Enter value to search: ");
                scanf("%d", &value);
                search(value);
                break;
            case 9:
                printf("Enter position and new value: ");
                scanf("%d %d", &pos, &value);
                update(pos, value);
                break;
            case 10:
                sort();
                printf("List sorted!\n");
                break;
            case 11:
                return 0;
            default:
                printf("Invalid Choice!\n");
        }
    }
}

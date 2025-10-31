#include <stdio.h>
#include <ctype.h>  

int findLargest(int arr[], int size) {
    int largest = arr[0];
    for (int i = 1; i < size; i++) {
        if (arr[i] > largest) {
            largest = arr[i];
        }
    }
    return largest;
}

int countVowels(char str[]) {
    int count = 0;
    for (int i = 0; str[i] != '\0'; i++) {
        char ch = tolower(str[i]);
        if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
            count++;
        }
    }
    return count;
}

int main() {
   
    int n;
    printf("Enter number of elements in the array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    int largest = findLargest(arr, n);
    printf("The largest element in the array is: %d\n\n", largest);

    while (getchar() != '\n');

    char str[1000];
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    int vowelsCount = countVowels(str);
    printf("The number of vowels in the string is: %d\n", vowelsCount);

    return 0;
}

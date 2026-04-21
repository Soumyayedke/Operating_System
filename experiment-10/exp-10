#include <stdio.h>

int main() {
    int n, m, i, j, k;
    
    printf("Enter number of processes: ");
    scanf("%d", &n);
    printf("Enter number of resource types: ");
    scanf("%d", &m);
    
    int allocation[n][m], max[n][m], need[n][m], available[m];
    int finish[n], safeSeq[n];
    
    // Input allocation matrix
    printf("Enter Allocation Matrix (process x resource):\n");
    for(i = 0; i < n; i++)
        for(j = 0; j < m; j++)
            scanf("%d", &allocation[i][j]);
    
    // Input max matrix
    printf("Enter Max Matrix (process x resource):\n");
    for(i = 0; i < n; i++)
        for(j = 0; j < m; j++)
            scanf("%d", &max[i][j]);
    
    // Input available vector
    printf("Enter Available Resources (vector):\n");
    for(i = 0; i < m; i++)
        scanf("%d", &available[i]);
    
    // Calculate Need matrix
    for(i = 0; i < n; i++)
        for(j = 0; j < m; j++)
            need[i][j] = max[i][j] - allocation[i][j];
    
    // Initialize finish array
    for(i = 0; i < n; i++)
        finish[i] = 0;
    
    int count = 0;
    while(count < n) {
        int found = 0;
        for(i = 0; i < n; i++) {
            if(finish[i] == 0) {
                int canAllocate = 1;
                for(j = 0; j < m; j++) {
                    if(need[i][j] > available[j]) {
                        canAllocate = 0;
                        break;
                    }
                }
                if(canAllocate) {
                    for(k = 0; k < m; k++)
                        available[k] += allocation[i][k];
                    safeSeq[count] = i;
                    count++;
                    finish[i] = 1;
                    found = 1;
                }
            }
        }
        if(!found) {
            printf("\nSystem is NOT in a safe state.\n");
            return 0;
        }
    }
    
    printf("\nSystem is in a safe state.\nSafe sequence: ");
    for(i = 0; i < n; i++)
        printf("P%d ", safeSeq[i]);
    printf("\n");
    
    return 0;
}

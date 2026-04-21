#include <stdio.h>

int main() {
    int n, i, j, time, tq;
    int wt = 0, tat = 0; // total waiting time and turnaround time
    printf("Enter number of processes: ");
    scanf("%d", &n);

    int bt[n], at[n], rem_bt[n], pid[n];
    for (i = 0; i < n; i++) {
        pid[i] = i + 1;
        printf("Enter burst time for process %d: ", i + 1);
        scanf("%d", &bt[i]);
        printf("Enter arrival time for process %d: ", i + 1);
        scanf("%d", &at[i]);
        rem_bt[i] = bt[i]; // initialize remaining burst time
    }

    printf("Enter time quantum: ");
    scanf("%d", &tq);

    int t = 0; // current time
    int done;
    printf("\nGantt Chart:\n");
    do {
        done = 1;
        for (i = 0; i < n; i++) {
            if (rem_bt[i] > 0 && at[i] <= t) {
                done = 0;
                if (rem_bt[i] > tq) {
                    printf("| P%d ", pid[i]);
                    rem_bt[i] -= tq;
                    t += tq;
                } else {
                    printf("| P%d ", pid[i]);
                    t += rem_bt[i];
                    wt += t - at[i] - bt[i];
                    tat += t - at[i];
                    rem_bt[i] = 0;
                }
            }
        }
    } while (!done);

    printf("|\n");

    printf("\nAverage Waiting Time = %.2f\n", (float)wt / n);
    printf("Average Turnaround Time = %.2f\n", (float)tat / n);

    return 0;
}

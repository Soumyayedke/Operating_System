#include <stdio.h>
#include <unistd.h>
#include <sys/wait.h>

int main() {
    pid_t pid;

    printf("Parent Process Started\n");
    printf("Parent PID: %d\n", getpid());

    pid = fork();

    if (pid < 0) {
        printf("Process creation failed\n");
    }
    else if (pid == 0) {
        printf("\nChild PID: %d\n", getpid());
        printf("Parent PID (from child): %d\n", getppid());

        execl("/bin/ls", "ls", "-l", NULL);

        // This runs only if execl fails
        perror("execl failed");
    }
    else {
        wait(NULL);
        printf("\nChild process completed\n");
        printf("Parent process exiting\n");
    }

    return 0;
}

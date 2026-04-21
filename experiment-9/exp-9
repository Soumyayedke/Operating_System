#include <stdio.h>

int main() {
    int n, frames, i, j, k, page_faults = 0, flag, index = 0;
    
    printf("Enter number of pages: ");
    scanf("%d", &n);
    int pages[n];
    printf("Enter page reference string:\n");
    for(i = 0; i < n; i++) {
        scanf("%d", &pages[i]);
    }
    
    printf("Enter number of frames: ");
    scanf("%d", &frames);
    int frame[frames];
    
    // Initialize frames to -1
    for(i = 0; i < frames; i++) {
        frame[i] = -1;
    }
    
    printf("\nPage replacement process:\n");
    for(i = 0; i < n; i++) {
        flag = 0;
        // Check if page is already in frame
        for(j = 0; j < frames; j++) {
            if(frame[j] == pages[i]) {
                flag = 1; // page hit
                break;
            }
        }
        
        if(flag == 0) { // page fault
            frame[index] = pages[i];
            index = (index + 1) % frames; // FIFO replacement
            page_faults++;
            
            // Print current state of frames
            printf("Page %d caused a page fault. Frames: ", pages[i]);
            for(k = 0; k < frames; k++) {
                if(frame[k] != -1) printf("%d ", frame[k]);
                else printf("- ");
            }
            printf("\n");
        } else {
            printf("Page %d hit. No page fault.\n", pages[i]);
        }
    }
    
    printf("\nTotal page faults: %d\n", page_faults);
    
    return 0;
}

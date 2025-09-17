# Employee-management-system
Mini project
#include <stdio.h>
#include <string.h>

// Define Employee structure
struct Employee {
    int id;
    char name[50];
    char department[50];
    float salary;
};

// Function to display employee details
void displayEmployee(struct Employee e) {
    printf("\nEmployee ID: %d", e.id);
    printf("\nName: %s", e.name);
    printf("\nDepartment: %s", e.department);
    printf("\nSalary: %.2f\n", e.salary);
}

int main() {
    int n, i;

    printf("Enter number of employees: ");
    scanf("%d", &n);

    struct Employee emp[n];  // Array of employees

    // Input employee details
    for (i = 0; i < n; i++) {
        printf("\nEnter details of Employee %d\n", i + 1);
        printf("ID: ");
        scanf("%d", &emp[i].id);
        printf("Name: ");
        scanf(" %[^\n]", emp[i].name);  // reads string with spaces
        printf("Department: ");
        scanf(" %[^\n]", emp[i].department);
        printf("Salary: ");
        scanf("%f", &emp[i].salary);
    }

    // Display all employees
    printf("\n--- Employee Records ---\n");
    for (i = 0; i < n; i++) {
        displayEmployee(emp[i]);
    }

    return 0;
}

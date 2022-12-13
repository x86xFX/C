# C

```c
#include <stdio.h>

int main() {
  char roomType, paymentMethod, decision;
  int noOfRooms, noOfNights;
  float roomPrice = 0;
  float totalPrice = 0;

  printf("Input the room type : ");
  scanf(" %c", & roomType);

  switch (toupper(roomType)) {
  case 'D':
    roomPrice = 31000.00;
    printf("\tDelux");
    break;

  case 'S':
    roomPrice = 35000.00;
    printf("\tSuperior Deluxe");
    break;

  case 'C':
    roomPrice = 50000.00;
    printf("\tClub Suites");
    break;

  case 'E':
    roomPrice = 75000.00;
    printf("\tExecutive Suites");
    break;

  case 'P':
    roomPrice = 100000.00;
    printf("\tPresidential Suite");
    break;

  default:
    printf("\tInvalid Room Type");
    exit(0);
  }

  printf("\nInput number of rooms : ");
  scanf("%d", & noOfRooms);

  printf("\nInput number of nights : ");
  scanf("%d", & noOfNights);

  printf("\nInput paying method : ");
  scanf(" %c", & paymentMethod);

  if (toupper(paymentMethod) == 'C') {
    totalPrice = noOfRooms * noOfNights * roomPrice;
    totalPrice = totalPrice - (totalPrice * 0.1);
    printf("Total amount : %.2f\n", totalPrice);

  } else if (toupper(paymentMethod) == 'M') {
    totalPrice = noOfRooms * noOfNights * roomPrice;
    printf("Total amount : Rs.%.2f\n", totalPrice);

  } else {
    printf("Wrong Payment Type, Abort...");
    exit(0);
  }
  
  printf("\nYour total room charge is: %.2f\n \nDo you want to continue?(y/n): ", totalPrice);
  scanf("%d", & decision);

  if(toupper(decision) == 'Y') {
      printf("Purchase Approved");
      
  } else {
      printf("Purchase cancelled");
      exit(0);
  }
  
  return 0;
}
```

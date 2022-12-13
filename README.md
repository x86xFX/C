# C

```c
#include <stdio.h>

int main() {
  char roomType, paymentMethod;
  int noOfRooms, noOfNights;
  float roomPrice = 0;
  float totalPrice = 0;

  printf("Input the room type : ");
  scanf(" %c", & roomType);

  switch (toupper(roomType)) {
  case 'D':
    roomPrice = 31000.00;
    printf("Delux");
    break;

  case 'S':
    roomPrice = 35000.00;
    printf("Superior Deluxe");
    break;

  case 'C':
    roomPrice = 50000.00;
    printf("Club Suites");
    break;

  case 'E':
    roomPrice = 75000.00;
    printf("Executive Suites");
    break;

  case 'P':
    roomPrice = 100000.00;
    printf("Presidential Suite");
    break;

  default:
    printf("Invalid Room Type");
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
    printf("Total amount : %.2f\n", totalPrice);

  } else {
    printf("Wrong Payment Type, Abort...");
    exit(0);
  }

  return 0;
}
```

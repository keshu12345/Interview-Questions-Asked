# Interview-Questions-Asked

## Car24

public enum AsyncActionName {
  order_create,
  order_refund,
  order_payment_done,
  order_booking_type_change
}


/// SOLID 

// Single responsibility

orderEventService.orderBookingTypeChanged(asyncObject.getOrder());
 orderEventService.postOrderCreation(asyncObject.getOrder());
  orderEventService.postOrderCreation(asyncObject.getOrder());
  orderEventService.postOrderRefund(asyncObject.getOrder());


Interface PaymantOrder {


   private OrderEventService orderEventService;

PaymantOrder( OrderEventService orderEventService){

This.orderEventService=orderEventService

}



Class PlaymentOrderFactory{



  PaymantOrder getOrderInstance(String name){

switch(name){

Case “ order_create”

}

}

}


getOrder(){

Return orderEventService.

}

}

Class  OrderBooking {


   private OrderEventService orderEventService;




}

Class OrderRefund{


   private OrderEventService orderEventService;


}

Class OrderPaymentDone{

   private OrderEventService orderEventService;


}

Class OrderBookingTypeChange{

   private OrderEventService orderEventService;



}



//  
public class AsyncProcessor {
  @Autowired 
   private OrderEventService orderEventService;



  // Processing all the async event according to asyn actionName
  public void processAsyncCall(AsyncActionRequest asyncObject) {
    if (AsyncActionName.order_booking_type_change.equals(asyncObject.getActionName())) {
      orderEventService.orderBookingTypeChanged(asyncObject.getOrder());
    } else if (AsyncActionName.order_create.name().equalsIgnoreCase(asyncObject.getActionName().name())) {
      orderEventService.postOrderCreation(asyncObject.getOrder());

    } else if (AsyncActionName.order_payment_done
        .name()
        .equalsIgnoreCase(asyncObject.getActionName().name())) {
      orderEventService.postOrderConfirmation(asyncObject.getOrder());
    } else if (AsyncActionName.order_refund
        .name()
        .equalsIgnoreCase(asyncObject.getActionName().name())) {
      orderEventService.postOrderRefund(asyncObject.getOrder());
    } 
  }
}


Question :10 beans   want to create based on periorty bases

@Component
Class A {
@Transaction()
public void method1(){
//db work
}

public void method2(){
this.method1();
}
}


@Component
Class B {
@Autowired
private A a;

public void method3() {
a.method1()
}

}




Employee 
Id, name, dept_id, salary_range_id  ra
1, one, 1, 1
2, two, 2, 2
3, three, 1, 1
4, four, 2, 2
5, five, 2, 1
.
.
department
Id, name 
1, IT
2, Finance


salary_range
Id, range
1, 1-10000
2, 10001-20000



Want number of emplo

count , dept, range
2,  IT,  1-10000
2, FINANCE,   10001-20000
1, FINANCE,  1-10000

Select  count(name),dept,range 
From (Select *

From Employee as e

Inner join  salary_range as sr on sr.id=e.salary_range_id))
Inner join  salary_range as sr on sr.id=e.salary_range_id)AND Inner Join  department  as dep On

Group by(d.name)


Given index -> c1, c2,c3 - composite index 



1. where c1 = x and c2 = y and c3 = z
2. where c3= x and c1= y and c2 = z
3. where c3=x
4. where c1 = x and c2 = y
5. where c3 = x and c1  = y

which one is query using composite query??


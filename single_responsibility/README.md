One of foundation to SOLID is Single Responsibility. Let’s talk directly by an Example how we can implement Single responsibility inside our code below. Within sample program there are two solutions to find Volume of rectangular prism.

### First solution within RectangularPrismOne class
- We embedding Rectangle inside RectangularPrism class.
- We count total area of rectangle and count volume for rectangular prism (two things).
### Second solution within RectangularPrismTwo class
- Using two classes to get the result.
- Class Rectangle responsible to count total area
- Class RectangularPrismTwo responsible only count volume
- RectangularPrismTwo receive an rectangle object as params
- Let rectangle object to count total area (responsible is within Rectangle class) and get the result to get volume (responsible is within RectangularPrism)
Test 1:

<img width="562" height="313" alt="image" src="https://github.com/user-attachments/assets/9a85e3cf-5989-44d0-a246-9fe750e34944" />

<img width="300" height="121" alt="image" src="https://github.com/user-attachments/assets/adb94454-bf38-4b91-9bd7-9635444c254b" />

Test 2:

<img width="562" height="314" alt="image" src="https://github.com/user-attachments/assets/b63606c2-5bcc-41e6-afbd-b95208619524" />

<img width="300" height="121" alt="image" src="https://github.com/user-attachments/assets/ce35b077-7cda-45ec-ae2f-158db6ed7afc" />

Test 3:

<img width="561" height="315" alt="image" src="https://github.com/user-attachments/assets/83f2485a-b03a-4dc8-9a3e-65a26d924207" />

<img width="300" height="121" alt="image" src="https://github.com/user-attachments/assets/352fca35-00ac-428f-8ed5-2be2ff35458f" />

Test 4:

<img width="564" height="317" alt="image" src="https://github.com/user-attachments/assets/688256ec-7f66-4ad6-9f97-c7ded0445846" />

<img width="300" height="121" alt="image" src="https://github.com/user-attachments/assets/a36b4443-455b-4b8d-a627-45442364a7c0" />

Test 5:

<img width="561" height="316" alt="image" src="https://github.com/user-attachments/assets/6ee18d3e-1e57-4263-982f-6a4e59592ad9" />

<img width="300" height="121" alt="image" src="https://github.com/user-attachments/assets/7eb23fa4-2a2b-4fc6-82d0-333ea29a01ac" />

Test 6:

<img width="562" height="314" alt="image" src="https://github.com/user-attachments/assets/cea2971b-044d-4ccc-9a32-f98987bdd333" />

<img width="300" height="121" alt="image" src="https://github.com/user-attachments/assets/713034f4-dc6e-4ab0-a2aa-999a321a7d62" />

I tried with 6 different positions and it detected a shoe in all of them, even when I put a handbag in the background to confuse the model. This demonstrates that the model is robust and deals well with different positions and challenges due to the use of a highly accurate model as a base (ResNet50).

The last test I did was to check the limits of the model by using an incomplete shoe and a handbag in the background. In that case, the handbag was detected. It probably was detected in that way because the incomplete shoe doesn't show any laces or characteristics to be detected as one. To the model, it could well be a random object flying around when the photo was taken. When that happened, the model saw the handbag in the background and determined that it must be the principal object to detect and classify it. However, if we see the code, as we are only classifying handbags and shoes, the default response could have been set to handbag. To take that theory to the test, I have taken a photo in complete blank and checked the result.

Test 7:

<img width="535" height="300" alt="image" src="https://github.com/user-attachments/assets/4bf728c3-c0d9-47b9-a909-9b1832e77ccd" />

<img width="298" height="118" alt="image" src="https://github.com/user-attachments/assets/1b326ffa-2ec2-4e5d-9758-be66b0f0c644" />

Test 8:

<img width="533" height="300" alt="image" src="https://github.com/user-attachments/assets/c769a6ce-8fd8-48f1-a1f3-0d9bfb9ec236" />

<img width="298" height="118" alt="image" src="https://github.com/user-attachments/assets/dc61f27f-b578-4f70-bc21-1b1a0c6f1ad8" />

As we can see, the blank photo has been classified as a handbag, concluding that the default value is indeed a handbag. To improve the model and if the use case needs it, we should add a third category to answer to us when no handbag and no shoe is in the photo or simply don't classify it in either.

**OTP Text Field**

**otp_text_field** is a Flutter widget for creating **stylish OTP input fields**. It allows entering multi-digit OTPs in individual boxes with callbacks.



```yaml
#add dependency to pubspec.yaml
dependencies:
  otp_text_field: 

#package url: https://pub.dev/packages/otp_text_field
```

```dart
//implementation
OTPTextField(
          length: 6,
          width: MediaQuery.of(context).size.width,
          fieldWidth: 40,
          style: TextStyle(fontSize: 17),
          textFieldAlignment: MainAxisAlignment.spaceAround,
          fieldStyle: FieldStyle.box,
          onCompleted: (pin) {
            print("Entered OTP: $pin");
          },
        )

``
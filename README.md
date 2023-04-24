# CustomToast-Android

To create a custom Toast in Android Studio, follow these steps:

1. Create a custom layout for the Toast message. Open the XML layout file where you want to design the custom Toast layout. Add the UI elements you want to display in the Toast message. For example, you could create a LinearLayout with a TextView and an ImageView. Save this layout file with a name like "custom_toast.xml".

2. Create a Toast object and set its custom view. In the activity or fragment where you want to display the Toast message, create a Toast object and call its setView() method to set the custom view you created in step 1.

            LayoutInflater inflater = getLayoutInflater();
            View layout = inflater.inflate(R.layout.toast, (ViewGroup)findViewById(R.id.toastHolder));
            TextView tv = layout.findViewById(R.id.t1);
            tv.setText("Custom Toast Demo");

            Toast toast = new Toast(getApplicationContext());
            toast.setView(layout);
   
 3. Customize the Toast appearance and duration. You can further customize the Toast message by calling methods on the Toast object. For example, you can set the duration of the Toast message using the setDuration() method, or set a gravity for the Toast message using the setGravity() method.  
            
            toast.setDuration(Toast.LENGTH_LONG);
            toast.setGravity(Gravity.CENTER_VERTICAL, 0, 700);
            toast.show();
          
4. Test the custom Toast message. Run your app and trigger the Toast message to display. You should see your custom layout appear instead of the default Toast message.
5. On click button then custom Toast show in lauched Screen.

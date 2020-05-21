# CameraAbort
相机相关问题
```
        // 裁减图片时传递的return-data设置为true，在onActivityResult的Intent中data的值会带一个Bitmap对象，如果图片太大或者裁减图片目标尺寸过大，
        // 就会出现android.os.TransactionTooLargeException: data parcel size 642356 bytes错误，因为Intent之前传递Parcel对象有大小限制。
        // 这个时候只能通过MediaStore.EXTRA_OUTPUT设置裁减图片保存位置，只传递图片路径，不直接传bitmap对象。
        intent.putExtra("return-data", false);
```

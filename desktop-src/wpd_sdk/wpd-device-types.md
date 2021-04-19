---
description: WPD \_ 裝置 \_ 類型列舉類型說明不同的 Windows 可攜式裝置 (WPD) 類型通常用來判斷可攜式裝置的基本分類和視覺外觀。
ms.assetid: 51714e0f-e9b7-4474-a8bb-da3875ef5399
title: 'WPD_DEVICE_TYPES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3e71acf200a95bba05b7298a5824bfa353e4a90b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999078"
---
# <a name="wpd_device_types-enumeration"></a>WPD \_ 裝置 \_ 類型列舉

**WPD \_ 裝置 \_ 類型** 列舉類型說明不同的 WINDOWS 可攜式裝置 (WPD) 類型通常用來判斷可攜式裝置的基本分類和視覺外觀。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_DEVICE_TYPES { 
  WPD_DEVICE_TYPE_GENERIC                       = 0,
  WPD_DEVICE_TYPE_CAMERA                        = 1,
  WPD_DEVICE_TYPE_MEDIA_PLAYER                  = 2,
  WPD_DEVICE_TYPE_PHONE                         = 3,
  WPD_DEVICE_TYPE_VIDEO                         = 4,
  WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER  = 5,
  WPD_DEVICE_TYPE_AUDIO_RECORDER                = 6
} WPD_DEVICE_TYPES;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**WPD \_ 裝置 \_ 類型 \_ 泛型**
</dt> <dd>

泛型 WPD，包含不屬於其他 [**WPD \_ 裝置 \_ 類型**](wpd-device-types.md) 列舉值的多功能裝置。

</dd> <dt>

<span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**WPD \_ 裝置 \_ 類型 \_ 相機**
</dt> <dd>

攝影機裝置，例如數位靜止相機。

</dd> <dt>

<span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**WPD \_ 裝置 \_ 類型 \_ 媒體 \_ 播放機**
</dt> <dd>

支援播放音訊、影片或觀賞圖片的 media player 裝置，例如便攜音樂播放機或便攜媒體中心。 並非所有這項功能都分類為 WPD \_ 裝置 \_ 類型的 \_ MEDIA \_ PLAYER。 例如，可移植音樂播放機裝置會分類為 WPD \_ 裝置 \_ 類型 \_ 媒體 \_ 播放機。

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**WPD \_ 裝置 \_ 類型 \_ 電話**
</dt> <dd>

電話裝置，例如行動電話。

</dd> <dt>

<span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**WPD \_ 裝置 \_ 類型 \_ 影片**
</dt> <dd>

影片裝置。

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**WPD \_ 裝置 \_ 類型 \_ 個人 \_ 資訊 \_ 管理員**
</dt> <dd>

個人資訊管理員裝置。

</dd> <dt>

<span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**WPD \_ 裝置 \_ 類型 \_ 音訊 \_ 錄製器**
</dt> <dd>

音訊錄製器裝置。

</dd> </dl>

## <a name="remarks"></a>備註

**WPD \_裝置 \_ 類型** 會使用 [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) 介面來讀取。 WPD 應用程式可能會使用這些值來判斷裝置的一般視覺外觀。 也就是，針對類似相機的裝置會顯示相機圖片，會針對類似電話的裝置顯示行動電話圖片等等。

> [!Note]  
> WPD 應用程式必須使用可攜式裝置的功能來判斷功能，而不是 **WPD \_ 裝置 \_ 類型** 值。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 





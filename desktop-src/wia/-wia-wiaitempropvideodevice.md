---
description: 標準 Windows 映像取得 (WIA) video 驅動程式 (wiavusd.dll) 支援串流處理影片裝置的下列屬性。
ms.assetid: 24fa7e02-c409-49ec-b1a9-309f7c95e292
title: '影片 WIA 裝置屬性常數 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPV_LAST_PICTURE_TAKEN
- WIA_DPV_IMAGES_DIRECTORY
- WIA_DPV_DSHOW_DEVICE_PATH
- WIA_DPF_MOUNT_POINT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f02991cb5c2b8cc15eb89e335ef1e46442c89510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113260"
---
# <a name="video-wia-device-property-constants"></a>影片 WIA 裝置屬性常數

標準 Windows 映像取得 (WIA) video 驅動程式 (wiavusd.dll) 支援串流處理影片裝置的下列屬性。

> [!Note]  
> WIA 不支援 Windows Server 2003、Windows Vista 或更新版本中的影片裝置。 針對這些版本的 Windows，請使用 [DirectShow](/previous-versions//ms783323(v=vs.85)) 從影片取得影像。

 

前置詞 "WIA \_ DPV \_ " 表示影片裝置的裝置屬性，而且是 C/c + + 中使用的命名慣例。 針對腳本用途，這些常數會使用前置詞 "VideoDevice"，而且是 [WiaItemPropertyId](-wia-wiaitempropertyid.md) 列舉型別的一部分。 來自該腳本列舉的對應成員名稱，會出現在下列清單中 C/c + + 常數名稱旁邊的括弧中。



| 常數/值                                                                                                                                                                                                                                                                           | Description                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <dt>**WIA \_DPV \_ 上一 \_ 張 \_ 拍攝**</dt> <dt>VideoDeviceLastPictureTaken</dt>的圖片 </dl> | 這個屬性是用來通知 WIA 驅動程式已新增新的映射。 應用程式應該將這個屬性的值設定為成功呼叫 [**IWiaVideo：： TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) 方法所建立之影像檔案的名稱。 <br/> 類型： VT \_ BSTR，存取：讀取/寫入<br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <dt>**WIA \_DPV \_ IMAGES \_ 目錄**</dt> <dt>VideoDeviceImagesDirectory</dt> </dl>         | 這個屬性是由標準的 WIA video 使用者模式驅動程式 (wiavusd.dll) 所公開。 這個屬性的值是 WIA 視頻驅動程式預設放置影像的目錄完整路徑。 應用程式應該將 [**IWiaVideo：： ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) 屬性設定為此值。 <br/> 類型： VT \_ BSTR、Access： Read Only<br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <dt>**WIA \_DPV \_ DSHOW \_ 裝置 \_ 路徑**</dt> <dt>VideoDeviceDShowDevicePath</dt> </dl>     | DirectShow 裝置的完整路徑。 <br/> 類型： VT \_ BSTR、Access： Read Only<br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <dt>**WIA \_DPF \_ 裝入 \_ 點**</dt> <dt>FileDeviceMountPoint</dt> </dl>                              | 未實作。 <br/> 類型： **VT \_ I4**、存取：唯讀、有效的值： [WIA \_ 類別 \_ 無](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wiadef。h</dt> </dl> |



 

 

---
description: 以逆時針方向指定影片框架的旋轉。
ms.assetid: 7C0911A6-6D7C-4510-891F-A6F56CE1EC2B
title: 'MF_MT_VIDEO_ROTATION 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf3d909b29757a02d46cc842b30f04bfb0463d6f734eecb74bfb957fa206fb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876698"
---
# <a name="mf_mt_video_rotation-attribute"></a>MF \_ MT \_ 影片 \_ 旋轉屬性

以逆時針方向指定影片框架的旋轉。

## <a name="data-type"></a>資料類型

**MFVideoRotationFormat** 儲存為 **UINT32**

## <a name="remarks"></a>備註

掌上型裝置的影片（例如行動電話）通常會以90、180或270度旋轉。 如果相機將方向以中繼資料的形式儲存在影片檔案中，則在播放時可以調整影像。

如果此屬性設定為 **MFVideoRotationFormat \_ 90**，則表示內容已以逆時針方向旋轉90度。 如果內容在順時針方向旋轉90度，則屬性值會是 **MFVideoRotationFormat \_ 270**。

此屬性支援的值會在 [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat)中列舉。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型](media-types.md)
</dt> </dl>

 

 





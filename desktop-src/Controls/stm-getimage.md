---
title: 'STM_GETIMAGE 訊息 (Winuser .h) '
description: 應用程式會傳送 STM \_ GETIMAGE 訊息，以抓取與靜態控制項相關聯之影像的控制碼 (圖示或點陣圖) 。
ms.assetid: eb5fe67a-09be-4c13-89c6-0e2f23e8c081
keywords:
- STM_GETIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- STM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77fe0c3d00a2a957530160a5ce5a21b8a1cf84e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024649"
---
# <a name="stm_getimage-message"></a>STM \_ GETIMAGE 訊息

應用程式會傳送 **STM \_ GETIMAGE** 訊息，以抓取與靜態控制項相關聯之影像的控制碼 (圖示或點陣圖) 。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定要取出的影像類型。 這個參數可以是下列其中一個值：



| 值                                                                                                                                                                     | 意義                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**影像 \_ 點陣圖**</dt> </dl>                | 點陣圖。<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**影像 \_ 游標**</dt> </dl>                | 游標。<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**影像 \_ ENHMETAFILE**</dt> </dl> | 增強的中繼檔。<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**影像 \_ 圖示**</dt> </dl>                      | 圖示。<br/>              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是影像的控制碼（如果有的話）。否則，它會是 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**STM \_ SETIMAGE**](stm-setimage.md)
</dt> </dl>

 

 






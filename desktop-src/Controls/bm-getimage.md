---
title: 'BM_GETIMAGE 訊息 (Winuser .h) '
description: 抓取影像的控制碼 (圖示或點陣圖) 與按鈕相關聯。
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- BM_GETIMAGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- BM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b98ede304499aa97d9129957aa69a0991dee98565ff7827cdad4d0c1a82f19b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921258"
---
# <a name="bm_getimage-message"></a>BM \_ GETIMAGE 訊息

抓取影像的控制碼 (圖示或點陣圖) 與按鈕相關聯。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要與按鈕相關聯的影像類型。 此參數可以是下列其中一個值。



| 值                                                                                                                                                      | 意義              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**影像 \_ 點陣圖**</dt> </dl> | 點陣圖。<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**影像 \_ 圖示**</dt> </dl>       | 圖示。<br/>  |



 

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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**BM \_ SETIMAGE**](bm-setimage.md)
</dt> <dt>

**概念**
</dt> <dt>

[按鈕](buttons.md)
</dt> </dl>

 

 






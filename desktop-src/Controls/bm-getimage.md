---
title: 'BM_GETIMAGE 訊息 (Winuser .h) '
description: 抓取影像的控制碼 (圖示或點陣圖) 與按鈕相關聯。
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- BM_GETIMAGE message Windows 控制項
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
ms.openlocfilehash: 9319f5310b40ff76a011e1a06b2be1d41be611f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317364"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



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

 

 






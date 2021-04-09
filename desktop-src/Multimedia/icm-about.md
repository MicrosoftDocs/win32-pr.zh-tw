---
title: 'ICM_ABOUT 訊息 (Vfw .h) '
description: '\_關於訊息的 ICM 會通知視訊壓縮驅動程式顯示其 [關於] 對話方塊，或查詢 video 壓縮驅動程式來判斷它是否有 [關於] 對話方塊。 您可以使用 ICAbout 宏明確地傳送此訊息。'
ms.assetid: 6eca69a3-0463-48e6-befb-5003b7515e7d
keywords:
- ICM_ABOUT message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_ABOUT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e03e88993ba1e345a3ea32a9de7adb2d63abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024567"
---
# <a name="icm_about-message"></a>\_關於訊息的 ICM

**\_ 關於** 訊息的 ICM 會通知視訊壓縮驅動程式顯示其 [關於] 對話方塊，或查詢 video 壓縮驅動程式來判斷它是否有 [關於] 對話方塊。 您可以使用 [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) 宏明確地傳送此訊息。


```C++
ICM_ABOUT 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*hwnd*
</dt> <dd>

顯示之對話方塊的父視窗控制碼。 您也可以在這個參數中指定-1，以判斷驅動程式是否有 [關於] 對話方塊，如同在 [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) 宏中一樣。 如果驅動程式 \_ 有 [關於] 對話方塊或 ICERR 不支援，則會傳回 ICERR OK \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果驅動程式支援此訊息或 ICERR 不支援，則會傳回 ICERR OK \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片壓縮管理員](video-compression-manager.md)
</dt> <dt>

[影片壓縮訊息](video-compression-messages.md)
</dt> </dl>

 

 






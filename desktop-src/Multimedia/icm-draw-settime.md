---
title: 'ICM_DRAW_SETTIME 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ SETTIME 提供同步處理資訊給轉譯驅動程式，以處理繪製框架的時間。
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- ICM_DRAW_SETTIME message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_SETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e37709477ba6080219e5225b3fde02dfed75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843404"
---
# <a name="icm_draw_settime-message"></a>ICM \_ 繪圖 \_ SETTIME 訊息

**ICM \_ DRAW \_ SETTIME** 提供同步處理資訊給轉譯驅動程式，以處理繪製框架的時間。 同步處理資訊是要繪製的框架樣本數。 您可以使用 [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) 宏明確地傳送此訊息。


```C++
ICM_DRAW_SETTIME 
wParam = (DWORD_PTR) lpTime; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*
</dt> <dd>

要轉譯的框架樣本數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

通常，驅動程式會將指定的值與其內部時鐘的時間相關聯的框架編號進行比較，並在差異很大時嘗試同步處理兩者。

當硬體執行它自己的非同步解壓縮、時間和繪圖，且硬體依賴外部同步處理信號 (硬體未用來作為同步處理主機) 時，請使用此訊息。

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

 

 






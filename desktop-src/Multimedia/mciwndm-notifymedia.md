---
title: 'MCIWNDM_NOTIFYMEDIA 訊息 (Vfw .h) '
description: MCIWNDM \_ NOTIFYMEDIA 訊息會通知應用程式的父視窗已變更。
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- MCIWNDM_NOTIFYMEDIA 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa64b17fb3910e518e5b5d4318f8d988cf71f8c314f047a5f2eed1ff80cc843d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783019"
---
# <a name="mciwndm_notifymedia-message"></a>MCIWNDM \_ NOTIFYMEDIA 訊息

**MCIWNDM \_ NOTIFYMEDIA** 訊息會通知應用程式的父視窗已變更。


```C++
MCIWNDM_NOTIFYMEDIA 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*hwnd*
</dt> <dd>

MCIWnd 視窗的控制碼。

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

以 null 結束的字串指標，其中包含新的檔案名。 如果媒體正在關閉，則會指定 null 字串。

</dd> </dl>

## <a name="remarks"></a>備註

您可以藉由指定 [MCIWNDF \_ NOTIFYMEDIA] 視窗樣式，來啟用媒體變更的通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



 

 






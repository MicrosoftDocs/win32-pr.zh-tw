---
title: 'MCIWNDM_NOTIFYMEDIA 訊息 (Vfw .h) '
description: MCIWNDM \_ NOTIFYMEDIA 訊息會通知應用程式的父視窗已變更。
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- MCIWNDM_NOTIFYMEDIA message Windows 多媒體
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
ms.openlocfilehash: 7026bd984e1d79775aac52caad56c87be6e8098e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685820"
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



 

 






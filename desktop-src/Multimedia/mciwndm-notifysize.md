---
title: 'MCIWNDM_NOTIFYSIZE 訊息 (Vfw .h) '
description: MCIWNDM \_ NOTIFYSIZE 訊息會通知應用程式的父視窗，視窗大小已變更。
ms.assetid: 76e1f663-bfc6-4d3c-9486-c8c7f79e4265
keywords:
- MCIWNDM_NOTIFYSIZE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYSIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59db02d69302127937a7203729de9cc8b98a58f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094383"
---
# <a name="mciwndm_notifysize-message"></a>MCIWNDM \_ NOTIFYSIZE 訊息

**MCIWNDM \_ NOTIFYSIZE** 訊息會通知應用程式的父視窗，視窗大小已變更。


```C++
MCIWNDM_NOTIFYSIZE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*hwnd*
</dt> <dd>

MCIWnd 視窗的控制碼。

</dd> </dl>

## <a name="remarks"></a>備註

您可以藉由指定 MCIWNDF NOTIFYSIZE 視窗樣式，來啟用 MCIWnd 視窗大小變更的通知 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



 

 






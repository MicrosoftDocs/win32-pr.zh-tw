---
title: 'MCIWNDM_NOTIFYPOS 訊息 (Vfw .h) '
description: MCIWNDM \_ NOTIFYPOS 訊息會通知應用程式的父視窗，該視窗的位置已變更。
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- MCIWNDM_NOTIFYPOS message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYPOS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bebb3a8facd6478c21888cf0cf5ca81e3735ff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934878"
---
# <a name="mciwndm_notifypos-message"></a>MCIWNDM \_ NOTIFYPOS 訊息

**MCIWNDM \_ NOTIFYPOS** 訊息會通知應用程式的父視窗，該視窗的位置已變更。


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*hwnd*
</dt> <dd>

MCIWnd 視窗的控制碼。

</dd> <dt>

<span id="pos"></span><span id="POS"></span>*Pos*
</dt> <dd>

描述新的位置。

</dd> </dl>

## <a name="remarks"></a>備註

您可以藉由指定 MCIWNDF NOTIFYPOS 視窗樣式，在 MCIWnd 視窗的位置啟用變更的通知 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



 

 






---
title: 'MCIWNDM_NOTIFYERROR 訊息 (Vfw .h) '
description: MCIWNDM \_ NOTIFYERROR 訊息會通知應用程式的父視窗發生 MCI 錯誤。
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- MCIWNDM_NOTIFYERROR message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbef9180c31091f3bd1a85f23a08990c2f7e7ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024967"
---
# <a name="mciwndm_notifyerror-message"></a>MCIWNDM \_ NOTIFYERROR 訊息

**MCIWNDM \_ NOTIFYERROR** 訊息會通知應用程式的父視窗發生 MCI 錯誤。


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*hwnd*
</dt> <dd>

MCIWnd 視窗的控制碼。

</dd> <dt>

<span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*錯誤碼*
</dt> <dd>

MCI 錯誤的數值代碼。

</dd> </dl>

## <a name="remarks"></a>備註

您可以藉由指定 [MCIWNDF \_ NOTIFYERROR] 視窗樣式來啟用 MCI 錯誤通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



 

 






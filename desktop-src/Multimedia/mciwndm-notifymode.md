---
title: 'MCIWNDM_NOTIFYMODE 訊息 (Vfw .h) '
description: MCIWNDM \_ NOTIFYMODE 訊息會通知應用程式的父視窗，該應用程式的 MCI 裝置操作模式已變更。
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- MCIWNDM_NOTIFYMODE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe75048a53023dab67bef4048d6149438ad54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024562"
---
# <a name="mciwndm_notifymode-message"></a>MCIWNDM \_ NOTIFYMODE 訊息

**MCIWNDM \_ NOTIFYMODE** 訊息會通知應用程式的父視窗，該應用程式的 MCI 裝置操作模式已變更。


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*hwnd*
</dt> <dd>

MCIWnd 視窗的控制碼。

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*模式*
</dt> <dd>

對應至 MCI 模式的整數。

</dd> </dl>

## <a name="remarks"></a>備註

您可以藉由指定 [MCIWNDF \_ NOTIFYMODE] 視窗樣式，來啟用 MCI 裝置之模式變更的通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



 

 






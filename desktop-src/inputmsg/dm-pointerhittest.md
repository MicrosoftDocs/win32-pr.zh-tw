---
title: DM_POINTERHITTEST 訊息
description: 傳送至視窗時，在第一次偵測到指標輸入時，為了判斷直接操作最可能的輸入目標。
ms.assetid: E4CE60F0-0C2A-440A-8F64-B070867A1572
keywords:
- DM_POINTERHITTEST 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- DM_POINTERHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 23efab4606f758acfffdd02fa4c53a729f1f4a99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104862"
---
# <a name="dm_pointerhittest-message"></a>DM_POINTERHITTEST 訊息

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

傳送至視窗時，在第一次偵測到指標輸入時，為了判斷 [直接操作](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)最可能的輸入目標。

> \[!重要\]  
> 桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。

 


```C++
#define DM_POINTERHITTEST       0x0250
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用的。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="return-value"></a>傳回值

NULL

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[訊息](messages.md)
</dt> </dl>

 


---
title: WM_POINTERDEVICEINRANGE 訊息
description: 在輸入數位板的範圍內偵測到指標裝置時，傳送至視窗。 此訊息包含裝置及其鄰近性的相關資訊。
ms.assetid: 04244758-E662-4FB2-850E-20B4B3D1294A
keywords:
- WM_POINTERDEVICEINRANGE 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEINRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 854640d63225945eb19dd56bd092d5b2eb66c2a3cf30c735f3dc64d7594e7502
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602323"
---
# <a name="wm_pointerdeviceinrange-message"></a>WM_POINTERDEVICEINRANGE 訊息

在輸入數位板的範圍內偵測到指標裝置時，傳送至視窗。 此訊息包含裝置及其鄰近性的相關資訊。

> \[!重要\]  
> 桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。

 


```C++
#define WM_POINTERDEVICEINRANGE       0X239
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

其他特定訊息資訊。

</dd> <dt>

*lParam* 
</dt> <dd>

其他特定訊息資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

如果應用程式未處理此訊息，則應該呼叫 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[訊息](messages.md)
</dt> </dl>

 


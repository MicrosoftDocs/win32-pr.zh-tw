---
title: 'TBN_INITCUSTOMIZE (Commctrl 的通知碼) '
description: 通知工具列的父視窗，自訂已開始。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: f4b9a1b0-94f7-4b2b-81b3-772da09134d2
keywords:
- TBN_INITCUSTOMIZE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_INITCUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5e855374699a100bf78019f1ca3d89857bc7c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966283"
---
# <a name="tbn_initcustomize-notification-code"></a>TBN \_ INITCUSTOMIZE 通知碼

通知工具列的父視窗，自訂已開始。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_INITCUSTOMIZE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

工具列 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 TBNRF \_ HIDEHELP 來隱藏 [說明] 按鈕。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






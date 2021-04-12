---
title: 'TBN_DUPACCELERATOR (Commctrl 的通知碼) '
description: Ascertains 快速鍵是否可用於兩個或多個作用中的工具列。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 98068d1a-1460-4be3-8575-9294b82ce903
keywords:
- TBN_DUPACCELERATOR 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_DUPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e530fa2101f8145148b7ede7d74f53a1828fa58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025325"
---
# <a name="tbn_dupaccelerator-notification-code"></a>TBN \_ DUPACCELERATOR 通知碼

Ascertains 快速鍵是否可用於兩個或多個作用中的工具列。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_DUPACCELERATOR

    lpnmtb = (NMTBDUPACCELERATOR) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

結構的指標，此結構會提供快速鍵，並接收指定多個工具列是否回應相同字元的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE**。

## <a name="remarks"></a>備註

應用程式必須宣告 **NMTBDUPACCELERATOR** 結構，如下所示：

``` syntax
typedef struct tagNMTBDUPACCELERATOR
{
    NMHDR hdr;
    UINT ch;   // The accelerator.
    BOOL fDup; // TRUE if multiple toolbars respond to the accelerator.
} NMTBDUPACCELERATOR, *LPNMTBDUPACCELERATOR;
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






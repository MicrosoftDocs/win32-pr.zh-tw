---
title: 'NM_TOOLTIPSCREATED (工具列) 通知碼 (Commctrl) '
description: 通知工具列的父視窗，工具列已建立工具提示控制項。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0e9517c1-aa3f-4b14-82b4-195a4ce99757
keywords:
- NM_TOOLTIPSCREATED (工具列) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c13366348da075fab48e7a2f12381f51f7d87bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464872"
---
# <a name="nm_tooltipscreated-toolbar-notification-code"></a>NM \_ TOOLTIPSCREATED (工具列) 通知碼

通知工具列的父視窗，工具列已建立工具提示控制項。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMTOOLTIPSCREATED) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated)結構的指標，其中包含此通知的其他相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

Toolbar 控制項會忽略此通知碼的傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






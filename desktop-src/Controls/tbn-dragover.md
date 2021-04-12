---
title: 'TBN_DRAGOVER (Commctrl 的通知碼) '
description: Ascertains 是否 \_ 應針對要拖曳的按鈕傳送一則 TB MARKBUTTON 訊息。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- TBN_DRAGOVER 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa02aa8fabf89ea27fce628d3d63165255bbd66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464765"
---
# <a name="tbn_dragover-notification-code"></a>TBN \_ system.windows.dragdrop.dragover> 通知碼

Ascertains 是否應針對要拖曳的按鈕傳送一則 [**TB \_ MARKBUTTON**](tb-markbutton.md) 訊息。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem)結構的指標，指定要將哪些專案拖曳至其中。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果工具列應該傳送 TB 的 MARKBUTTON 訊息，則為 **FALSE** ， \_ 否則為 **TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






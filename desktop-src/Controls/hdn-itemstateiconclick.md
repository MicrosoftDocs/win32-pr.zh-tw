---
title: 'HDN_ITEMSTATEICONCLICK 訊息 (Commctrl .h) '
description: 通知標題控制項的父視窗，使用者按一下專案的狀態圖示。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: a1969579-3a69-49ff-b06e-4b7450146a92
keywords:
- HDN_ITEMSTATEICONCLICK message Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ITEMSTATEICONCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e5e162b78c829e60494f6e8ff81af3ca97eee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466937"
---
# <a name="hdn_itemstateiconclick-message"></a>HDN \_ ITEMSTATEICONCLICK 訊息

通知標題控制項的父視窗，使用者按一下專案的狀態圖示。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
HDN_ITEMSTATEICONCLICK

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含有關已按一下之狀態圖示的其他資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






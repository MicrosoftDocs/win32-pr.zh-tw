---
title: 'NM_RDBLCLK (清單視圖) 通知碼 (Commctrl) '
description: 當使用者以滑鼠右鍵按一下專案時，由清單視圖控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ebbb127f-07bd-48e0-bf38-7bbda5802f70
keywords:
- NM_RDBLCLK (清單視圖) 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41832b228fe40b212c0aba809b15022c6f7b39ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935164"
---
# <a name="nm_rdblclk-list-view-notification-code"></a>NM \_ RDBLCLK (清單視圖) 通知碼

當使用者以滑鼠右鍵按一下專案時，由清單視圖控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_RDBLCLK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[版本 4.71](common-control-versions.md)。 [**NMITEMACTI加值稅E**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate)結構的指標，其中包含此通知的其他相關資訊。 此結構的 **iItem**、 **iSubItem** 和 **ptAction** 成員包含專案的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此通知的傳回值。

## <a name="remarks"></a>備註

只有在按一下圖示或第一個資料行的標籤時， *lParam* 的 **iItem** 成員才有效。 若要判斷在某個資料列中的其他地方發生按一下時所要選取的專案，請傳送 [**LVM \_ SUBITEMHITTEST**](lvm-subitemhittest.md) 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






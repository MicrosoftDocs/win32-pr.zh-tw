---
title: 'LVN_MARQUEEBEGIN (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，表示已開始) 選取範圍 (的周框方塊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- LVN_MARQUEEBEGIN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_MARQUEEBEGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d46d399b8355bea0ddb2054340d52db59c3ad27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966158"
---
# <a name="lvn_marqueebegin-notification-code"></a>LVN \_ MARQUEEBEGIN 通知碼

通知清單視圖控制項的父視窗，表示已開始) 選取範圍 (的周框方塊。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

若要接受通知碼，請傳回零。 若要結束周框方塊選取範圍，則傳回非零值。

## <a name="remarks"></a>備註

周 *框方塊選取範圍* 是按一下清單視圖視窗的工作區，並拖曳以同時選取多個專案的流程。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






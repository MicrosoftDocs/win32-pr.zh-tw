---
title: 'LVN_COLUMNCLICK (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗：當清單視圖控制項處於報表模式時，已按下資料行標頭。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- LVN_COLUMNCLICK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_COLUMNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27cfd75d913c62c89c4cfe305333a934fe172fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024658"
---
# <a name="lvn_columnclick-notification-code"></a>LVN \_ COLUMNCLICK 通知碼

通知清單視圖控制項的父視窗：當清單視圖控制項處於報表模式時，已按下資料行標頭。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_COLUMNCLICK

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的指標。 **IItem** 成員為-1，而 **iSubItem** 成員會識別資料行。 所有其他成員都是零。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

使用標題控制項格式（例如 [HDF \_ ] 核取方塊）來修改清單視圖控制項中的資料行標頭格式，會導致控制項在按一下標頭專案時，傳送 [HDN \_ ITEMSTATEICONCLICK](hdn-itemstateiconclick.md) 通知碼，而不是 LVN \_ COLUMNCLICK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






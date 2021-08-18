---
title: 'LVN_LINKCLICK (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗已按一下連結。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: de8f40d6-b79e-4324-af67-9a3c0915609d
keywords:
- LVN_LINKCLICK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e89db641bc17e8c3d9d548bdf502e077c88dfc6c7452f8059b085c3432d23bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019066"
---
# <a name="lvn_linkclick-notification-code"></a>LVN \_ LINKCLICK 通知碼

通知清單視圖控制項的父視窗已按一下連結。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_LINKCLICK
        
    pLinkInfo = (NMLVLINK*) lParam;         
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink)結構的指標。 包含連結的群組識別碼位於 **iSubItem** 成員中。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

下列範例顯示應用程式如何在其 [**WM \_ 通知**](wm-notify.md) 訊息處理常式中回應此通知碼。 此範例會切換群組的折迭狀態，並設定適當的連結文字。

``` syntax
case LVN_LINKCLICK:
{
    NMLVLINK* pLinkInfo = (NMLVLINK*)lParam;
    HWND hList = pLinkInfo->hdr.hwndFrom;
    LVGROUP groupInfo;
    groupInfo.cbSize = sizeof(groupInfo);
    groupInfo.mask = LVGF_TASK;
    int groupIndex = pLinkInfo->iSubItem;
    if (ListView_GetGroupState(hList, groupIndex, LVGS_COLLAPSED))
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, 0);
        groupInfo.pszTask = L"Hide";
    }
    else
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, LVGS_COLLAPSED);
        groupInfo.pszTask = L"Show";
     }
      ListView_SetGroupInfo(hList, groupIndex, &groupInfo);
      break;
}
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






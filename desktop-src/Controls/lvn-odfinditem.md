---
title: 'LVN_ODFINDITEM 訊息 (Commctrl .h) '
description: 當需要擁有者尋找特定回呼專案時，由虛擬清單-view 控制項傳送。
ms.assetid: 5a3f9fed-0c57-46bf-b986-ea8b54290b5e
keywords:
- LVN_ODFINDITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LVN_ODFINDITEM
- LVN_ODFINDITEMA
- LVN_ODFINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a610f3de00e204bcdfbac51545553cebffe4c61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104813"
---
# <a name="lvn_odfinditem-message"></a>LVN \_ ODFINDITEM 訊息

當需要擁有者尋找特定回呼專案時，由 [虛擬清單-view](list-view-controls-overview.md) 控制項傳送。 例如，當此控制項收到快速鍵鍵盤輸入或收到 [**LVM \_ FINDITEM**](lvm-finditem.md) 訊息時，會傳送此通知碼。 LVN \_ ODFINDITEM 通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_ODFINDITEM

    pFindInfo = (PNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema)結構的指標，其中包含要用於搜尋的資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回找到之專案的索引，如果找不到任何專案，則傳回-1。

## <a name="remarks"></a>備註

搜尋資訊會以 [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) 結構的形式傳送，這是 [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) 結構的成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVN \_ODFINDITEMW** (Unicode) 和 **LVN \_ ODFINDITEMA** (ANSI) <br/>             |



 

 






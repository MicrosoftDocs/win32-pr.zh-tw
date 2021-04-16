---
title: 'TBN_WRAPHOTITEM (Commctrl 的通知碼) '
description: 通知應用程式有兩個或多個最忙碌專案即將變更的工具列。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- TBN_WRAPHOTITEM 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_WRAPHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58eb513780da464ead40f8a4fb1264f6268d4370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465029"
---
# <a name="tbn_wraphotitem-notification-code"></a>TBN \_ WRAPHOTITEM 通知碼

通知應用程式有兩個或多個最忙碌專案即將變更的工具列。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

結構的指標，其中包含舊的熱專案 (**iStart**) 以及新的熱專案是否早于 (**iDir** =-1) 或 (**iDir** = 1) 之後，以及熱專案變更的原因。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式正在處理熱專案變更本身，則為 **TRUE** ;否則 **為 FALSE**。

## <a name="remarks"></a>備註

**NMTBWRAPHOTITEM** 結構必須由應用程式定義，如下所示：

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






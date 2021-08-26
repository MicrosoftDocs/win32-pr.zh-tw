---
description: 當事件發生時可能會影響 appbar 的大小和位置時，通知 appbar。
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: 'ABN_POSCHANGED 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92528de38b60c1f4705873427616b1ed7a5be6be5875a21e352d2136313c84df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943598"
---
# <a name="abn_poschanged-message"></a>ABN \_ POSCHANGED 訊息

當事件發生時可能會影響 appbar 的大小和位置時，通知 appbar。 事件包括工作列大小、位置和可見度狀態的變更，以及在螢幕相同側邊的其他 appbar 的新增、移除或調整大小。


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a>參數

此訊息沒有任何參數。

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

Appbar 應該藉由傳送 [**ABM \_ QUERYPOS**](abm-querypos.md) 和 [**ABM \_ SETPOS**](abm-setpos.md) 訊息來回應此通知訊息。 如果它的位置已變更，則 appbar 應該呼叫 [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) 函式，將其本身移至新的位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



 


---
title: 'PGN_SCROLL (Commctrl 的通知碼) '
description: 通知頁面控制項的父視窗，其中包含的視窗即將進行滾動。 此通知會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- PGN_SCROLL 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PGN_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 864903c73eeb611d1c748ec6a4d936192a1a27f22d3f37115af8879916286a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830142"
---
# <a name="pgn_scroll-notification-code"></a>PGN \_ 捲軸通知碼

通知頁面控制項的父視窗，其中包含的視窗即將進行滾動。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
PGN_SCROLL

    lpnms = (LPNMPGSCROLL) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll)結構的指標，其中包含和接收通知程式碼的相關資訊。 此結構的 **iDir** 成員會指出捲軸的方向。 **IXpos** 和 **iYpos** 成員包含滾動之前所包含視窗的水準和垂直位置。 **IScroll** 成員包含預設的滾動差異數量。 如有需要，您可以將此成員修改為不同的捲軸量。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






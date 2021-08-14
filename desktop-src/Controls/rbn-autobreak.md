---
title: 'RBN_AUTOBREAK 訊息 (Commctrl .h) '
description: 通知 Rebar 的父系，將會在橫條中顯示中斷。 父代會決定是否要進行中斷。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: b7a63027-6cfa-4d5a-9ea6-fdd8b4fb6864
keywords:
- RBN_AUTOBREAK 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- RBN_AUTOBREAK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63a6b0279199bc0c1d96f0d31884b85e13b9c42036bf0e0f98404825eb66e5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169230"
---
# <a name="rbn_autobreak-message"></a>RBN \_ AUTOBREAK 訊息

通知 [Rebar 的](rebar-controls.md) 父系，將會在橫條中顯示中斷。 父代會決定是否要進行中斷。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
RBN_AUTOBREAK

    pnmRebarAutoBreak = (LPNMREBARAUTOBREAK) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak)結構的指標，其中包含通知碼的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此通知的傳回值。

## <a name="remarks"></a>備註

[**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak)結構之 **fAutoBreak** 成員中的值會指出是否應該在 Rebar 中出現中斷。

若要使用此通知碼，請在資訊清單中指定 Comctl32.dll 第6版。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






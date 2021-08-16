---
title: 'PGN_HOTITEMCHANGE 訊息 (Commctrl .h) '
description: 通知頁面控制項的父視窗，其中的熱 (反白顯示) 專案已變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0f59677c-0251-49f4-b909-6fac6d93f354
keywords:
- PGN_HOTITEMCHANGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PGN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6510eeb648ad883d04ccc0baf916223bb5209d110c2237ef3bf618d241c2ede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830132"
---
# <a name="pgn_hotitemchange-message"></a>PGN \_ HOTITEMCHANGE 訊息

通知頁面控制項的父視窗，其中的熱 (反白顯示) 專案已變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
PGN_HOTITEMCHANGE

    pnmPGHotItem = (LPNMPGHOTITEM) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem)結構的指標，其中包含此通知碼的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零，以反白顯示專案或非零，以防止反白顯示。

## <a name="remarks"></a>備註

> [!Note]  
> 若要使用此通知碼，您必須提供指定 Comclt32.dll 版本6.0 的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






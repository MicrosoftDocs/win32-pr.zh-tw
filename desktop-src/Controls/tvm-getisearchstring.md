---
title: 'TVM_GETISEARCHSTRING 訊息 (Commctrl .h) '
description: 抓取樹狀檢視控制項的累加式搜尋字串。
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- TVM_GETISEARCHSTRING 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETISEARCHSTRING
- TVM_GETISEARCHSTRINGA
- TVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79838b2b0d2f109216caf970d33d51b4a3c1369da7b1fc47f5a53e45c3ee82fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060238"
---
# <a name="tvm_getisearchstring-message"></a>TVM \_ GETISEARCHSTRING 訊息

抓取樹狀檢視控制項的累加式搜尋字串。 樹狀檢視控制項會使用增量搜尋字串，根據使用者輸入的字元來選取專案。 您可以使用 [**TreeView \_ GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

接收累加式搜尋字串的緩衝區指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回增量搜尋字串中的字元數。

## <a name="remarks"></a>備註

**安全性警告：** 不當使用此訊息可能會危及程式的安全性。 您必須配置夠大的緩衝區來保存字串。 首先，在 *lParam* 中呼叫傳遞 **Null** 的訊息。 這會傳回所需的字元數，但不包括 **Null**。 然後第二次呼叫訊息以抓取字串。 您應複習[安全性考慮： Microsoft Windows 控制項](sec-comctls.md)，再繼續進行。

如果樹狀檢視控制項不在累加式搜尋模式中，則傳回值為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TVM \_GETISEARCHSTRINGW** (Unicode) 和 **TVM \_ GETISEARCHSTRINGA** (ANSI) <br/> |



 

 






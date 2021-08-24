---
title: 'TTM_UPDATETIPTEXT 訊息 (Commctrl .h) '
description: 設定工具的工具提示文字。
ms.assetid: 2a7432dd-76f9-42b4-b639-178dce1d89ef
keywords:
- TTM_UPDATETIPTEXT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TTM_UPDATETIPTEXT
- TTM_UPDATETIPTEXTA
- TTM_UPDATETIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c44b28d4913e4ae502db4d48268de945660610b374b7a1b98c0754fe99bafc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119542847"
---
# <a name="ttm_updatetiptext-message"></a>TTM \_ UPDATETIPTEXT 訊息

設定工具的工具提示文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標。 **Hinst** 和 **lpszText** 成員必須指定實例控制碼和文字的位址。 **Hwnd** 和 **uId** 成員會識別要更新的工具。 傳送此訊息之前，必須先填入此結構的 **cbSize** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TTM \_UPDATETIPTEXTW** (Unicode) 和 **TTM \_ UPDATETIPTEXTA** (ANSI) <br/>       |



 

 






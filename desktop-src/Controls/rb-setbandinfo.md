---
title: 'RB_SETBANDINFO 訊息 (Commctrl .h) '
description: 在 Rebar 控制項中設定現有波段的特性。
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- RB_SETBANDINFO 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETBANDINFO
- RB_SETBANDINFOA
- RB_SETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee89d91bc65556179d14c7e86a69a9e6399223f38bb1bcc44f746d7cd8f8a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798468"
---
# <a name="rb_setbandinfo-message"></a>RB \_ SETBANDINFO 訊息

在 Rebar 控制項中設定現有波段的特性。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的索引，這是用來接收新設定的頻外索引。

</dd> <dt>

*lParam* 
</dt> <dd>

[**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)結構的指標，該結構定義要修改的頻外和新的設定。 傳送此訊息之前，您必須將此結構的 **cbSize** 成員設定為 **sizeof** (REBARBANDINFO) 結構。 此外，當指定 RBBIM 文字時，您必須將 **REBARBANDINFO** 結構的 **cch** 成員設定為 **lpText** 緩衝區的大小 \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **RB \_SETBANDINFOW** (Unicode) 和 **RB \_ SETBANDINFOA** (ANSI) <br/>             |



 

 






---
title: 'RB_GETBANDINFO 訊息 (Commctrl .h) '
description: 抓取 Rebar 控制項中指定之頻外的相關資訊。
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- RB_GETBANDINFO 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b0ae509699c23ad24b9b97451178f4711ab52176a9c15aeef757bab85c861c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409439"
---
# <a name="rb_getbandinfo-message"></a>RB \_ GETBANDINFO 訊息

抓取 Rebar 控制項中指定之頻外的相關資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為起始的寬線索引，將會抓取資訊。

</dd> <dt>

*lParam* 
</dt> <dd>

[**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)結構的指標，此結構會接收要求的頻外資訊。 傳送此訊息之前，您必須將此結構的 **cbSize** 成員設定為 **REBARBANDINFO** 結構的大小，並將 **fMask** 成員設定為您想要取出的專案。 此外，當指定 RBBIM 文字時，您必須將 **REBARBANDINFO** 結構的 **cch** 成員設定為 **lpText** 緩衝區的大小 \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **RB \_GETBANDINFOW** (Unicode) 和 **RB \_ GETBANDINFOA** (ANSI) <br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RB \_ SETBANDINFO**](rb-setbandinfo.md)
</dt> </dl>

 

 






---
title: 'TB_INSERTBUTTON 訊息 (Commctrl .h) '
description: 在工具列中插入按鈕。
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- TB_INSERTBUTTON 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_INSERTBUTTON
- TB_INSERTBUTTONA
- TB_INSERTBUTTONW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 909a4e039450e001757cd054cf27a15d24af392d6a55841c2857e2312252145c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829649"
---
# <a name="tb_insertbutton-message"></a>TB \_ INSERTBUTTON 訊息

在工具列中插入按鈕。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的按鈕索引。 訊息會將新按鈕插入此按鈕的左邊。

</dd> <dt>

*lParam* 
</dt> <dd>

[**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構的指標，其中包含要插入之按鈕的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TB \_INSERTBUTTONW** (Unicode) 和 **TB \_ INSERTBUTTONA** (ANSI) <br/>           |



 

 






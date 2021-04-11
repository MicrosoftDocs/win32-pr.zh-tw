---
title: 'TB_INSERTBUTTON 訊息 (Commctrl .h) '
description: 在工具列中插入按鈕。
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- TB_INSERTBUTTON message Windows 控制項
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
ms.openlocfilehash: 4e08eed328a99d4a8927a7e09084bf122f2e4e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094291"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TB \_INSERTBUTTONW** (Unicode) 和 **TB \_ INSERTBUTTONA** (ANSI) <br/>           |



 

 






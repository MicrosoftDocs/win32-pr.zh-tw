---
title: 'SB_GETTIPTEXT 訊息 (Commctrl .h) '
description: 抓取狀態列中某部分的工具提示文字。 您必須使用 SBT \_ 工具提示樣式來建立狀態列，才能啟用工具提示。
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- SB_GETTIPTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- SB_GETTIPTEXT
- SB_GETTIPTEXTA
- SB_GETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d492bc19f82300f460666b3213c545fe95b8db85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844000"
---
# <a name="sb_gettiptext-message"></a>SB \_ GETTIPTEXT 訊息

抓取狀態列中某部分的工具提示文字。 您必須使用 [**SBT \_ 工具提示**](status-bar-styles.md) 樣式來建立狀態列，才能啟用工具提示。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定接收工具提示文字之部分的以零為起始的索引。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定 *lParam* 的緩衝區大小（以字元為單位）。

</dd> <dt>

*lParam* 
</dt> <dd>

接收工具提示文字之字元緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="remarks"></a>備註

**安全性警告：** 不當使用此訊息可能會導致您的應用程式發生問題。 例如，如果文字對 *lParam* 緩衝區來說太大，可能會造成緩衝區溢位。 您應該先複習 [安全性考慮： Microsoft Windows 控制項](sec-comctls.md) ，再繼續進行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **SB \_GETTIPTEXTW** (Unicode) 和 **SB \_ GETTIPTEXTA** (ANSI) <br/>               |



 


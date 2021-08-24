---
title: 'SB_SETTIPTEXT 訊息 (Commctrl .h) '
description: 設定狀態列中某部分的工具提示文字。 您必須使用 SBT \_ 工具提示樣式來建立狀態列，才能啟用工具提示。
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- SB_SETTIPTEXT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- SB_SETTIPTEXT
- SB_SETTIPTEXTA
- SB_SETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 864ba53066b000f9f7ae65365341238a701b4e70bc4ce8cc70adba923d57a5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637018"
---
# <a name="sb_settiptext-message"></a>SB \_ SETTIPTEXT 訊息

設定狀態列中某部分的工具提示文字。 您必須使用 [**SBT \_ 工具提示**](status-bar-styles.md) 樣式來建立狀態列，才能啟用工具提示。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

將接收工具提示文字之部分的以零為基底的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

字元緩衝區的指標，其中包含新的工具提示文字。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="remarks"></a>備註

在兩種情況下，會顯示此工具提示文字：

-   當狀態列中的對應窗格只包含一個圖示時。
-   當狀態列中的對應窗格包含由於窗格大小而截斷的文字時。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **SB \_SETTIPTEXTW** (Unicode) 和 **SB \_ SETTIPTEXTA** (ANSI) <br/>               |



 

 






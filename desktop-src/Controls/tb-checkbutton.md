---
title: 'TB_CHECKBUTTON 訊息 (Commctrl .h) '
description: 檢查或取消核取工具列中的指定按鈕。
ms.assetid: e67734a9-851c-41ab-8ad7-15d434f58e5a
keywords:
- TB_CHECKBUTTON 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_CHECKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fec35b6a333e0663acc8c94dec22c2b8f4138cb6024b1f7919fd0ec73cdb0eb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919128"
---
# <a name="tb_checkbutton-message"></a>TB \_ CHECKBUTTON 訊息

檢查或取消核取工具列中的指定按鈕。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要檢查之按鈕的命令識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 **布林** 值，指出是否要檢查或取消選取指定的按鈕。 若 **為 TRUE**，則會新增檢查。 如果 **為 FALSE**，則會移除檢查。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

核取按鈕時，會顯示為已按下的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 


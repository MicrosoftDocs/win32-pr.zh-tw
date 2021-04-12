---
title: 'TB_ISBUTTONHIGHLIGHTED 訊息 (Commctrl .h) '
description: 檢查工具列按鈕的醒目提示狀態。
ms.assetid: d5aab670-a989-46f2-b4f8-d8a8968cbe07
keywords:
- TB_ISBUTTONHIGHLIGHTED message Windows 控制項
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIGHLIGHTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53e25058fee8fa5dcac218a641277ac46aed4e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024852"
---
# <a name="tb_isbuttonhighlighted-message"></a>TB \_ ISBUTTONHIGHLIGHTED 訊息

檢查工具列按鈕的醒目提示狀態。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

工具列按鈕的命令識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果按鈕已反白顯示，則會傳回非零，否則會傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






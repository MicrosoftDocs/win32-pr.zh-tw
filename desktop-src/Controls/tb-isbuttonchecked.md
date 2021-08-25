---
title: 'TB_ISBUTTONCHECKED 訊息 (Commctrl .h) '
description: 決定是否核取工具列中指定的按鈕。
ms.assetid: ce576951-8db6-4854-8457-211ece018ce8
keywords:
- TB_ISBUTTONCHECKED 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_ISBUTTONCHECKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26d93340668e926f99271e9acd450eed5d51aa454571e779601744dc4d283b1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876988"
---
# <a name="tb_isbuttonchecked-message"></a>TB \_ ISBUTTONCHECKED 訊息

決定是否核取工具列中指定的按鈕。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

按鈕的命令識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果已核取按鈕，則傳回非零，否則會傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






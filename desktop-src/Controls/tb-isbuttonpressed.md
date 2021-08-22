---
title: 'TB_ISBUTTONPRESSED 訊息 (Commctrl .h) '
description: 決定是否按下工具列中指定的按鈕。
ms.assetid: b8e2434c-24c2-47eb-b243-ffdaf31d5b8f
keywords:
- TB_ISBUTTONPRESSED 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_ISBUTTONPRESSED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187b7dd6c39fb972d53391dcbd67d7b45bb895a2e521fa8db22c2a7a411c05e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503638"
---
# <a name="tb_isbuttonpressed-message"></a>TB \_ ISBUTTONPRESSED 訊息

決定是否按下工具列中指定的按鈕。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

按鈕的命令識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果已按下按鈕，則傳回非零，否則會傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






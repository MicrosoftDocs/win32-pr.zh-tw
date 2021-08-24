---
title: 'TB_SETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 設定工具列控制項的延伸樣式。
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- TB_SETEXTENDEDSTYLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 600e5904637215eeb052c85ec0203c9b86c75ed6b179be643dc9a213156b3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318878"
---
# <a name="tb_setextendedstyle-message"></a>TB \_ SETEXTENDEDSTYLE 訊息

設定工具列控制項的延伸樣式。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

指定新擴充樣式的值。 這個參數可以是 [擴充樣式](toolbar-extended-styles.md)的組合。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回表示先前擴充樣式的 **DWORD** 。 這個值可以是 [擴充樣式](toolbar-extended-styles.md)的組合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TB \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md)
</dt> </dl>

 

 






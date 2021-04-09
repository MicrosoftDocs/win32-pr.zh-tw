---
title: 'TB_SETINSERTMARK 訊息 (Commctrl .h) '
description: 設定工具列的目前插入標記。
ms.assetid: 9a576fca-89cf-4db5-9840-35bfa56af89e
keywords:
- TB_SETINSERTMARK message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f65ba83d13cbb45f54833725a46de61a5f0444c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093816"
---
# <a name="tb_setinsertmark-message"></a>TB \_ SETINSERTMARK 訊息

設定工具列的目前插入標記。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

包含插入標記之 [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TB \_ GETINSERTMARK**](tb-getinsertmark.md)
</dt> </dl>

 

 






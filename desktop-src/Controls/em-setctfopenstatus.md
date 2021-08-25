---
title: 'EM_SETCTFOPENSTATUS 訊息 (Richedit .h) '
description: 開啟或關閉文字服務架構 (TSF) 鍵盤。
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- EM_SETCTFOPENSTATUS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ac27017abbadeb038f5b881aefe1aff394036931529c84c9c5a34a36e556c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048628"
---
# <a name="em_setctfopenstatus-message"></a>EM \_ SETCTFOPENSTATUS 訊息

開啟或關閉文字服務架構 (TSF) 鍵盤。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

若要開啟 TSF 鍵盤，請使用 **TRUE**。 若要關閉 TSF 鍵盤，請使用 **FALSE**。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，此訊息會傳回 **TRUE**。 如果不成功，則此訊息會傳回 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP （含 SP1） \[ 桌面應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETCTFOPENSTATUS**](em-getctfopenstatus.md)
</dt> </dl>

 

 






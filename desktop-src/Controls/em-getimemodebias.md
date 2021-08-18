---
title: 'EM_GETIMEMODEBIAS 訊息 (Richedit .h) '
description: 抓取 Microsoft Rich Edit 控制項的輸入方法編輯器 (IME) 模式偏差。
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- EM_GETIMEMODEBIAS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ad5504ca2e5ac1a332657c4f539c9f983292617b6e74b949598488ceb38dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019536"
---
# <a name="em_getimemodebias-message"></a>EM \_ GETIMEMODEBIAS 訊息

抓取 Microsoft Rich Edit 控制項的輸入方法編輯器 (IME) 模式偏差。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息會傳回目前的 IME 模式偏差設定。

## <a name="remarks"></a>備註

若要取得文字服務架構模式偏差，請使用 [**EM \_ GETCTFMODEBIAS**](em-getctfmodebias.md)。

在呼叫此函式之前，應用程式應該呼叫 [**EM \_ ISIME**](em-isime.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP （含 SP1） \[ 桌面應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ ISIME**](em-isime.md)
</dt> <dt>

[**EM \_ GETCTFMODEBIAS**](em-getctfmodebias.md)
</dt> </dl>

 

 






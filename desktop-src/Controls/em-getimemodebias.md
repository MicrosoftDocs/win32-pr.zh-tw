---
title: 'EM_GETIMEMODEBIAS 訊息 (Richedit .h) '
description: 抓取 Microsoft Rich Edit 控制項的輸入方法編輯器 (IME) 模式偏差。
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- EM_GETIMEMODEBIAS message Windows 控制項
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
ms.openlocfilehash: ea13e151ae9d487340ee440e3b123ae70b437a02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025292"
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
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP1） \[ 桌面應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ ISIME**](em-isime.md)
</dt> <dt>

[**EM \_ GETCTFMODEBIAS**](em-getctfmodebias.md)
</dt> </dl>

 

 






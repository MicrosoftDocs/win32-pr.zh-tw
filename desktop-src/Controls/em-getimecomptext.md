---
title: 'EM_GETIMECOMPTEXT 訊息 (Richedit .h) '
description: 抓取輸入方法編輯器 (IME) 組合文字。
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- EM_GETIMECOMPTEXT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETIMECOMPTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dd915f037275d428df37ca02a206b936a63bfd2f6ac8fbb605d1573b9535789
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049068"
---
# <a name="em_getimecomptext-message"></a>EM \_ GETIMECOMPTEXT 訊息

抓取輸入方法編輯器 (IME) 組合文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext)結構。

</dd> <dt>

*lParam* 
</dt> <dd>

接收組合文字的緩衝區。 這個緩衝區的大小是包含在 *wParam* 結構的 **cb** 成員中。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，傳回值就是複製到緩衝區的 Unicode 字元數。 否則，它是零。

## <a name="remarks"></a>備註

此訊息只會採用 Unicode 字串。

**安全性警告：** 請確定有足夠的緩衝區來滿足輸入的大小。 若未這麼做，可能會導致您的應用程式發生問題。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP （含 SP1） \[ 桌面應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 






---
title: 'TB_GETBUTTONTEXT 訊息 (Commctrl .h) '
description: 抓取工具列上按鈕的顯示文字。
ms.assetid: 16dd7181-a404-4056-b084-05f49f5a4b14
keywords:
- TB_GETBUTTONTEXT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETBUTTONTEXT
- TB_GETBUTTONTEXTA
- TB_GETBUTTONTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ec63815886ecc32f8f0b0759b9f6a8cf847bfe56e6c898fd6e3a3ae8e0f40ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829764"
---
# <a name="tb_getbuttontext-message"></a>TB \_ GETBUTTONTEXT 訊息

抓取工具列上按鈕的顯示文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要取出其文字之按鈕的命令識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

接收按鈕文字之緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 *lParam* 所指向之字串的長度（以字元為單位）。 長度不包含終止的 null 字元。 如果不成功，則傳回值為-1。

## <a name="remarks"></a>備註

**安全性警告：** 不當使用此訊息可能會危及程式的安全性。 此訊息不會提供您知道緩衝區大小的方法。 如果您使用此訊息，請先呼叫在 *lParam* 中傳遞 **null** 的訊息，這會傳回字元數，但不包括需要的 **null** 。 然後第二次呼叫訊息以抓取字串。 您應該先複習[安全性考慮： Microsoft Windows 控制項](sec-comctls.md)，再繼續進行。

傳回的字串會對應至按鈕目前所顯示的文字。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TB \_GETBUTTONTEXTW** (Unicode) 和 **TB \_ GETBUTTONTEXTA** (ANSI) <br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**TB \_ GETBUTTONINFO**](tb-getbuttoninfo.md)
</dt> <dt>

[**TB \_ GETSTRING**](tb-getstring.md)
</dt> <dt>

[**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> </dl>

 

 






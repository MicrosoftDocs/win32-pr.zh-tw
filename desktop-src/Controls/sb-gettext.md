---
title: 'SB_GETTEXT 訊息 (Commctrl .h) '
description: 從狀態視窗的指定部分抓取文字。
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- SB_GETTEXT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- SB_GETTEXT
- SB_GETTEXTA
- SB_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05967d41d86ad039e39259c8179a9e768e8fbbf76e5112b531048ac0ed7b56bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168725"
---
# <a name="sb_gettext-message"></a>SB \_ GETTEXT 訊息

從狀態視窗的指定部分抓取文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的索引，這是要從中取得文字的部分。

</dd> <dt>

*lParam* 
</dt> <dd>

以 null 終止字串的形式接收文字之緩衝區的指標。 使用 [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) 訊息來判斷所需的緩衝區大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回包含 2 16 位值的32位值。 [低] 字組指定文字的長度（以字元為單位）。 High 單字指定用來繪製文字的作業類型。 此類型可以是下列其中一個值。



| 傳回碼                                                                                    | 描述                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | 文字會以框線繪製，並顯示為低於視窗的平面。<br/>  |
| <dl> <dt>**SBT \_ NOBORDERS**</dt> </dl>  | 不以框線繪製文字。<br/>                                             |
| <dl> <dt>**SBT \_ 彈出**</dt> </dl>     | 文字會以框線繪製，並顯示在視窗的平面的上方。<br/> |
| <dl> <dt>**SBT \_ RTLREADING**</dt> </dl> | 文字會在父視窗中以相反的方向顯示文字。<br/>  |



 

## <a name="remarks"></a>備註

**安全性警告：** 不當使用此訊息可能會危及程式的安全性。 此訊息不會提供您知道緩衝區大小的方法。 如果您使用此訊息，請先呼叫 [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) 來取得所需的字元數，然後呼叫訊息以取得字串。 如果您在呼叫 Sb 之前等候 **\_ GETTEXT** ，文字可能會變更，因此會使 **SB \_ GETTEXTLENGTH** 的傳回值失效。 您應該先複習[安全性考慮： Microsoft Windows 控制項](sec-comctls.md)，再繼續進行。

此訊息最多會傳回65535個字元。 如果文字字串的長度超過該字串，則會被截斷。

如果文字具有 SBT \_ OWNERDRAW 繪圖類型，則此訊息會傳回與文字相關聯的32位值，而不是長度和作業類型。

一般視窗會將文字從左至右顯示 (LTR) 。 Windows 可以進行 *鏡像*，以顯示如希伯來文或阿拉伯文等語言，由右至左 (RTL) 。 如果 \_ 設定了 SBT RTLREADING，則 *lParam* 字串會從父視窗中的文字以相反的方向讀取。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **SB \_GETTEXTW** (Unicode) 和 **SB \_ GETTEXTA** (ANSI) <br/>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SB \_ SETTEXT**](sb-settext.md)
</dt> </dl>

 

 






---
title: 'SB_GETTEXTLENGTH 訊息 (Commctrl .h) '
description: 從狀態視窗的指定部分抓取文字長度（以字元為單位）。
ms.assetid: 2cd43106-dd43-499e-b595-760e9ededab5
keywords:
- SB_GETTEXTLENGTH 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- SB_GETTEXTLENGTH
- SB_GETTEXTLENGTHA
- SB_GETTEXTLENGTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2c203862b2a17352924f3df07560034c9f52784c84676d924d78524b05be1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084958"
---
# <a name="sb_gettextlength-message"></a>SB \_ GETTEXTLENGTH 訊息

從狀態視窗的指定部分抓取文字長度（以字元為單位）。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的索引，這是要從中取得文字的部分。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回包含 2 16 位值的32位值。 [低] 字組指定文字的長度（以字元為單位）。 High 單字指定用來繪製文字的作業類型。 此類型可以是下列其中一個值：



| 傳回碼                                                                                    | 描述                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | 文字會以框線繪製，並顯示為低於視窗的平面。<br/>          |
| <dl> <dt>**SBT \_ NOBORDERS**</dt> </dl>  | 不以框線繪製文字。<br/>                                                     |
| <dl> <dt>**SBT \_ OWNERDRAW**</dt> </dl>  | 文字是由父視窗繪製。<br/>                                                |
| <dl> <dt>**SBT \_ 彈出**</dt> </dl>     | 文字會以框線繪製，並顯示在視窗的平面的上方。<br/>         |
| <dl> <dt>**SBT \_ RTLREADING**</dt> </dl> | 文字將會以相反方向顯示在父視窗中的文字。<br/> |



 

## <a name="remarks"></a>備註

一般視窗會將文字從左至右顯示 (LTR) 。 Windows 可以進行 *鏡像*，以顯示如希伯來文或阿拉伯文等語言，由右至左 (RTL) 。 如果 \_ 已設定 [SBT RTLREADING]，則會從父視窗中的文字，以相反的方向讀取指定的狀態視窗文字。

此訊息會傳回65535個字元的字串長度上限。 如果實際文字字串的長度超過該字串，則 [**SB \_ GETTEXT**](sb-gettext.md) 訊息會將它截斷。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **SB \_GETTEXTLENGTHW** (Unicode) 和 **SB \_ GETTEXTLENGTHA** (ANSI) <br/>         |



 

 






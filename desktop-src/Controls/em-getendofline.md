---
title: 'EM_GETENDOFLINE 訊息 (Commctrl .h) '
description: 抓取插入 linebreak 時所使用的行尾字元。 明確地傳送此訊息，或使用 Edit \_ GetEndOfLine 宏。
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETENDOFLINE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETENDOFLINE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 64ddb55ce592b71c7abaa8c35b1bf14a004b324586094f27a3b418a67e5b24e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019686"
---
# <a name="em_getendofline-message"></a>EM \_ GETENDOFLINE 訊息

抓取編輯控制項的行尾字元。 明確地傳送此訊息，或使用 [**Edit \_ GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回編輯控制項使用的行尾字元。 這可以是下列其中一個值。

| 值                                                                                                                                                   | 意義                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**EC \_ ENDOFLINE \_ CRLF**</dt> </dl> | 用於新分行符號的行尾字元是換行字元，後面接著換行字元 (CRLF) 。<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ ENDOFLINE \_ CR**</dt> </dl>       | 用於新分行符號的行尾字元是 (CR) 的回車。<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ ENDOFLINE \_ LF**</dt> </dl>       | 用於新分行符號的行尾字元是換行字元 (LF) 。<br/>                               |

## <a name="remarks"></a>備註

使用 [[**編輯 \_ SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline)] 將使用的行尾字元設定為 [ **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** ] 時，此訊息會傳回偵測到的行尾字元。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 \[僅限桌面應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2019 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETENDOFLINE*](em-setendofline.md)
</dt> </dl>
 

 






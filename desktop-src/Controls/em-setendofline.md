---
title: 'EM_SETENDOFLINE 訊息 (CommCtrl .h) '
description: 設定插入 linebreak 時所使用的行尾字元。
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETENDOFLINE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETENDOFLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 5ee7c500ba3818cad0f5ee74e9994ed8af049ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466544"
---
# <a name="em_setendofline-message"></a>EM \_ SETENDOFLINE 訊息

設定插入 linebreak 時所使用的行尾字元。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定插入 linebreak 時所使用的行尾字元。 這可以是下列其中一個值。


| 值                                                                                                                                                   | 意義                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_DETECTFROMCONTENT"></span><span id="ec_endofline_detectfromcontent"></span><dl> <dt>**EC \_ ENDOFLINE \_ DETECTFROMCONTENT**</dt> </dl> | 將用於新分行符號的行尾字元設定為目前檔所使用的字元。<br/>  |
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**EC \_ ENDOFLINE \_ CRLF**</dt> </dl>                                        | 將新分行符號的行尾字元設定為分行符號，後面接著換行字元 (CRLF) 。<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ ENDOFLINE \_ CR**</dt> </dl>                                              | 將新分行符號的行尾字元設定為換行字元， (CR) 。<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ ENDOFLINE \_ LF**</dt> </dl>                                              | 將用於新分行符號的行尾字元設定為換行 (LF) 。<br/>                               |

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業成功，則傳回值為非零。

如果作業失敗，則傳回值為零。

## <a name="remarks"></a>備註

當行尾字元集為 **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** 時，編輯控制項只會偵測根據其擴充視窗樣式所支援的行尾字元，請參閱 [編輯控制項延伸樣式](edit-control-window-extended-styles.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限 1809 desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2019 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>CommCtrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETENDOFLINE*](em-getendofline.md)
</dt> </dl>

 

 






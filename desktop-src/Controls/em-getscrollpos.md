---
title: 'EM_GETSCROLLPOS 訊息 (Richedit .h) '
description: 取得編輯控制項的目前滾動位置。
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- EM_GETSCROLLPOS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70458abca94e483f8e202f13ecaed3df04a68366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465153"
---
# <a name="em_getscrollpos-message"></a>EM \_ GETSCROLLPOS 訊息

取得編輯控制項的目前滾動位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**點**](/previous-versions//dd162805(v=vs.85))結構的指標。 在呼叫 **EM \_ GETSCROLLPOS** 之後，此參數會在檔的虛擬文字空間中包含點（以圖元表示）。 這一點將會是目前位於 [編輯] 控制項視窗左上角的點。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息一律會傳回1。

## <a name="remarks"></a>備註

[**點**](/previous-versions//dd162805(v=vs.85))結構中所傳回的值為16位值， (偶數) 的32位寬欄位中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Rich Edit 3。0<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETSCROLLPOS**](em-setscrollpos.md)
</dt> </dl>

 


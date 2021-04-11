---
title: 'TTM_SETMAXTIPWIDTH 訊息 (Commctrl .h) '
description: 設定工具提示視窗的最大寬度。
ms.assetid: 3cfb6011-d0c3-4a57-aead-d4ec09a057cc
keywords:
- TTM_SETMAXTIPWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_SETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ce930b289205b5fb0d2768068b8cb28cd11aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187284"
---
# <a name="ttm_setmaxtipwidth-message"></a>TTM \_ SETMAXTIPWIDTH 訊息

設定工具提示視窗的最大寬度。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

最大工具提示視窗寬度，或-1 可允許任何寬度。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前的工具提示最大寬度。

## <a name="remarks"></a>備註

最大寬度值不會指出工具提示視窗的實際寬度。 相反地，如果工具提示字串超過最大寬度，控制項會將文字分成多行，使用空格來決定分行符號。 如果無法將文字分割成多行，它就會顯示在一行中，可能會超過工具提示寬度上限。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TTM \_ GETMAXTIPWIDTH**](ttm-getmaxtipwidth.md)
</dt> </dl>

 

 






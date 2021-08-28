---
title: 'TTM_GETMAXTIPWIDTH 訊息 (Commctrl .h) '
description: 抓取工具提示視窗的最大寬度。
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- TTM_GETMAXTIPWIDTH 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TTM_GETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bce561b254645932b214b48879aa0be04deb31b32e8dc591fc3183ec39871273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751048"
---
# <a name="ttm_getmaxtipwidth-message"></a>TTM \_ GETMAXTIPWIDTH 訊息

抓取工具提示視窗的最大寬度。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **INT** 值，表示最大工具提示寬度（以圖元為單位）。 如果先前未設定最大寬度，則訊息會傳回-1。

## <a name="remarks"></a>備註

工具提示寬度值的最大值不會指出工具提示視窗的實際寬度。 相反地，如果工具提示字串超過最大寬度，控制項會將文字分成多行，使用空格來決定分行符號。 如果無法將文字分割成多行，它就會顯示在同一行上。 此行的長度可能會超過工具提示寬度上限。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 






---
title: 'TTM_GETMAXTIPWIDTH 訊息 (Commctrl .h) '
description: 抓取工具提示視窗的最大寬度。
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- TTM_GETMAXTIPWIDTH message Windows 控制項
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
ms.openlocfilehash: f89c56692db9d451eb18db61af262cc0f3a715f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934395"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 






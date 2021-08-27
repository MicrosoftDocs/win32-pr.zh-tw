---
title: 'SB_SIMPLE 訊息 (Commctrl .h) '
description: 指定狀態視窗是否顯示簡單文字，或顯示先前 SB SETPARTS 訊息所設定的所有視窗元件 \_ 。
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- SB_SIMPLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f0a896c9adcab6886151753761c62aefb8f4dc6ee21b7e85bb7507bda11f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132208"
---
# <a name="sb_simple-message"></a>SB \_ 簡單訊息

指定狀態視窗是否顯示簡單文字，或顯示先前 [**SB \_ SETPARTS**](sb-setparts.md) 訊息所設定的所有視窗元件。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

顯示類型旗標。 如果此參數為 **TRUE**，視窗會顯示簡單文字。 如果為 **FALSE**，則會顯示多個部分。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="remarks"></a>備註

如果狀態視窗是從簡單變更為 simple，或反之亦然，則會立即重新繪製視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






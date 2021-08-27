---
title: 'TDM_SET_MARQUEE_PROGRESS_BAR 訊息 (Commctrl .h) '
description: 指出工作對話方塊的裝載進度列是否應顯示在捲軸模式中。
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- TDM_SET_MARQUEE_PROGRESS_BAR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TDM_SET_MARQUEE_PROGRESS_BAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13262339f7d87ea68755a38a49cc8c327706939d6b18025f350334dfdbe3dd4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104608"
---
# <a name="tdm_set_marquee_progress_bar-message"></a>TDM \_ SET \_ 天棚 \_ 進度列 \_ 訊息

指出工作對話方塊的裝載進度列是否應顯示在捲軸模式中。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

**布林** 值，指出進度列是否應顯示在捲軸模式中。 值為 **TRUE** 會開啟字幕模式，而值為 **FALSE** 則會關閉字幕模式。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

如需捲軸模式的詳細資訊，請參閱 [進度列控制項](progress-bar-control.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






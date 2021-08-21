---
title: 'TBM_SETTIC 訊息 (Commctrl .h) '
description: 在指定的邏輯位置的 [查看] 中設定刻度。
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- TBM_SETTIC 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74f286a2f03e318629a10651d066da5aa6cfe70aa293f242ad7508d0ef4739a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540018"
---
# <a name="tbm_settic-message"></a>TBM \_ SETTIC 訊息

在指定的邏輯位置的 [查看] 中設定刻度。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

刻度的位置。 此參數可以是最小至最大滑杆位置的最小值範圍中的任何整數值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果已設定刻度，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

然後，會建立自己的第一個和最後一個刻度標記。 請勿使用此訊息來設定第一個和最後一個刻度標記。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**TBM \_ GETPTICS**](tbm-getptics.md)
</dt> <dt>

[**TBM \_ GETTIC**](tbm-gettic.md)
</dt> </dl>

 

 






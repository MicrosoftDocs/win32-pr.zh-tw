---
title: 'TBM_SETTIC 訊息 (Commctrl .h) '
description: 在指定的邏輯位置的 [查看] 中設定刻度。
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- TBM_SETTIC message Windows 控制項
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
ms.openlocfilehash: a42839157125c8def28a19dd9c2ccce21d3b96c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094171"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**TBM \_ GETPTICS**](tbm-getptics.md)
</dt> <dt>

[**TBM \_ GETTIC**](tbm-gettic.md)
</dt> </dl>

 

 






---
title: 'RB_MAXIMIZEBAND 訊息 (Commctrl .h) '
description: 將 Rebar 控制項中的寬線大小調整為理想或最大的大小。
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- RB_MAXIMIZEBAND message Windows 控制項
topic_type:
- apiref
api_name:
- RB_MAXIMIZEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708a8fae7c0dd8e72eea8e5acefe43ab50054592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843924"
---
# <a name="rb_maximizeband-message"></a>RB \_ MAXIMIZEBAND 訊息

將 Rebar 控制項中的寬線大小調整為理想或最大的大小。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的寬線索引，要最大化。

</dd> <dt>

*lParam* 
</dt> <dd>

指出當寬線最大化時，是否應使用寬線的理想寬度。 如果此值為非零值，則會使用理想的寬度。 如果此值為零，則會盡可能將此寬線設為最大。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

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

[**RB \_ SETBANDINFO**](rb-setbandinfo.md)
</dt> </dl>

 

 






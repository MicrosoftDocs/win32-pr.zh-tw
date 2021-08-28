---
title: 'RB_MAXIMIZEBAND 訊息 (Commctrl .h) '
description: 將 Rebar 控制項中的寬線大小調整為理想或最大的大小。
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- RB_MAXIMIZEBAND 訊息 Windows 控制項
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
ms.openlocfilehash: 13ef02fbe9611c09d1932907c8218ffd169d3e18d10e0b07faa2b63d50058af1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770088"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**RB \_ SETBANDINFO**](rb-setbandinfo.md)
</dt> </dl>

 

 






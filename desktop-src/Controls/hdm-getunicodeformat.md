---
title: 'HDM_GETUNICODEFORMAT 訊息 (Commctrl .h) '
description: 取得控制項的 Unicode 字元格式旗標。 您可以明確地傳送此訊息，或使用標頭 \_ GetUnicodeFormat 宏。
ms.assetid: 2b36265a-023c-4083-a755-769461f3804b
keywords:
- HDM_GETUNICODEFORMAT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 804d27d74c0702dd2e2d26ab90b494992aa95924b39a75c65466a8733214c710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118171164"
---
# <a name="hdm_getunicodeformat-message"></a>HDM \_ GETUNICODEFORMAT 訊息

取得控制項的 Unicode 字元格式旗標。 您可以明確地傳送此訊息，或使用 [**標頭 \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回控制項的 Unicode 格式旗標。 如果這個值為非零值，則控制項會使用 Unicode 字元。 如果這個值為零，則控制項會使用 ANSI 字元。

## <a name="remarks"></a>備註

如需此訊息的討論，請參閱 [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) 的備註。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**HDM \_ SETUNICODEFORMAT**](hdm-setunicodeformat.md)
</dt> </dl>

 

 






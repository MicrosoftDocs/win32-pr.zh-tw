---
title: 'LVM_GETUNICODEFORMAT 訊息 (Commctrl .h) '
description: 抓取控制項的 UNICODE 字元格式旗標。 您可以明確地傳送此訊息，或使用 ListView \_ GetUnicodeFormat 宏。
ms.assetid: b0598b60-4d0e-4c68-b63a-e614c6268129
keywords:
- LVM_GETUNICODEFORMAT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3166d7349bf138fa853523c019a4c1db86e3f1a2d81a6da86c4ef25b5ed405
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019256"
---
# <a name="lvm_getunicodeformat-message"></a>LVM \_ GETUNICODEFORMAT 訊息

抓取控制項的 UNICODE 字元格式旗標。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat) 宏。

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

[**LVM \_ SETUNICODEFORMAT**](lvm-setunicodeformat.md)
</dt> </dl>

 

 






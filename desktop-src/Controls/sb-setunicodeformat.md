---
title: 'SB_SETUNICODEFORMAT 訊息 (Commctrl .h) '
description: SB_SETUNICODEFORMAT 訊息：設定控制項的 Unicode 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。
ms.assetid: 022e7138-c12f-4c59-82da-2ac6d276fa77
keywords:
- SB_SETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- SB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 278a5645928a51732b87c12447bb2524bfadfbcd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085886"
---
# <a name="sb_setunicodeformat-message"></a>SB \_ SETUNICODEFORMAT 訊息

設定控制項的 Unicode 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

決定控制項所使用的字元集。 如果這個值為 **TRUE**，控制項將會使用 Unicode 字元。 如果這個值為 **FALSE**，控制項將會使用 ANSI 字元。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回控制項的先前 Unicode 格式旗標。

## <a name="remarks"></a>備註

如需此訊息的討論，請參閱 [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) 的備註。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SB \_ GETUNICODEFORMAT**](sb-getunicodeformat.md)
</dt> </dl>

 

 






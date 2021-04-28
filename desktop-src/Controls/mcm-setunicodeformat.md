---
title: 'MCM_SETUNICODEFORMAT 訊息 (Commctrl .h) '
description: MCM_SETUNICODEFORMAT 訊息：設定控制項的 Unicode 字元格式旗標。
ms.assetid: 250789b5-694b-4502-9cc0-3bc260ea06e7
keywords:
- MCM_SETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa922b0dde8702f447690f9626938364174cbff6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112367"
---
# <a name="mcm_setunicodeformat-message"></a>MCM \_ SETUNICODEFORMAT 訊息

設定控制項的 Unicode 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。 您可以明確地傳送此訊息，或使用 [**MonthCal \_ SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

決定控制項所使用的字元集。 如果這個值為非零值，控制項將會使用 Unicode 字元。 如果這個值為零，控制項將會使用 ANSI 字元。

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

[**MCM \_ GETUNICODEFORMAT**](mcm-getunicodeformat.md)
</dt> </dl>

 

 






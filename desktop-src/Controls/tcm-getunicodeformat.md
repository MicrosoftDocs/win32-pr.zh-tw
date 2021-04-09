---
title: 'TCM_GETUNICODEFORMAT 訊息 (Commctrl .h) '
description: 抓取控制項的 Unicode 字元格式旗標。 您可以明確地傳送此訊息，或使用 TabCtrl \_ GetUnicodeFormat 宏。
ms.assetid: 720e0325-500b-436c-8713-38ed780735bf
keywords:
- TCM_GETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b497f1b2c2b5ac55ee949b498602b50b267fef3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844175"
---
# <a name="tcm_getunicodeformat-message"></a>TCM \_ GETUNICODEFORMAT 訊息

抓取控制項的 Unicode 字元格式旗標。 您可以明確地傳送此訊息，或使用 [**TabCtrl \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) 宏。

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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TCM \_ SETUNICODEFORMAT**](tcm-setunicodeformat.md)
</dt> </dl>

 

 






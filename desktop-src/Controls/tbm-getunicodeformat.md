---
title: 'TBM_GETUNICODEFORMAT 訊息 (Commctrl .h) '
description: 抓取控制項的 Unicode 字元格式旗標。
ms.assetid: cecd7e55-f482-4381-bde8-a60b8c5173eb
keywords:
- TBM_GETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a9fafad2504e51a65b879e58298c5cd06f1f345
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843603"
---
# <a name="tbm_getunicodeformat-message"></a>TBM \_ GETUNICODEFORMAT 訊息

抓取控制項的 Unicode 字元格式旗標。

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

[**TBM \_ SETUNICODEFORMAT**](tbm-setunicodeformat.md)
</dt> </dl>

 

 






---
title: 'CBEM_GETUNICODEFORMAT 訊息 (Commctrl .h) '
description: 取得控制項的 UNICODE 字元格式旗標。
ms.assetid: 854ff8d5-6e2f-4918-a6c5-91356a4454af
keywords:
- CBEM_GETUNICODEFORMAT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4665877c3a9cae9fc559c55040d1972128dbb7404f59e5c61a5739829aca629
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699268"
---
# <a name="cbem_getunicodeformat-message"></a>CBEM \_ GETUNICODEFORMAT 訊息

取得控制項的 UNICODE 字元格式旗標。

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

[**CBEM \_ SETUNICODEFORMAT**](cbem-setunicodeformat.md)
</dt> </dl>

 

 






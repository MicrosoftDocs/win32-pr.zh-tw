---
title: 'CBEM_SETUNICODEFORMAT 訊息 (Commctrl .h) '
description: 設定控制項的 UNICODE 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。
ms.assetid: 4811709b-1639-4468-8598-97d9dc8d9057
keywords:
- CBEM_SETUNICODEFORMAT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d59730922c1d72da90e1c7ba47a287e42ce4ad40375d8216be114e7c280b5a38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699300"
---
# <a name="cbem_setunicodeformat-message"></a>CBEM \_ SETUNICODEFORMAT 訊息

設定控制項的 UNICODE 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。

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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBEM \_ GETUNICODEFORMAT**](cbem-getunicodeformat.md)
</dt> </dl>

 

 






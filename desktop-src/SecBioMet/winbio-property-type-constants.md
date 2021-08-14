---
title: 'WINBIO_PROPERTY_TYPE 常數 (Winbio) '
description: 在 WinBioGetProperty 函數中指定屬性資訊的來源。
ms.assetid: 82C54092-032B-4F32-820E-A1D4BB81ECCE
topic_type:
- apiref
api_name:
- WINBIO_PROPERTY_TYPE_SESSION
- WINBIO_PROPERTY_TYPE_TEMPLATE
- WINBIO_PROPERTY_TYPE_UNIT
- WINBIO_PROPERTY_TYPE_ACCOUNT
api_location:
- Winbio.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7b7c17da736e117f099ec66dafc4ef2cfbba037f90a35f2522d7710cb3cef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909356"
---
# <a name="winbio_property_type-constants"></a>WINBIO \_ 屬性 \_ 類型常數

下列 **WINBIO \_ 屬性 \_ 類型** 常數可以用來指定 [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) 函數中的屬性資訊來源。

<dl> <dt>

<span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**WINBIO \_ 屬性 \_ 類型 \_ 會話**
</dt> <dd> <dl> <dt>



屬性會套用至特定的生物識別會話。


</dt> </dl> </dd> <dt>

<span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**WINBIO \_ 屬性 \_ 類型 \_ 範本**
</dt> <dd> <dl> <dt>



屬性會套用至特定的生物識別範本。


</dt> </dl> </dd> <dt>

<span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**WINBIO \_ 屬性 \_ 類型 \_ 單位**
</dt> <dd> <dl> <dt>



屬性會套用至特定的生物特徵辨識單位。


</dt> </dl> </dd> <dt>

<span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**WINBIO \_ 屬性 \_ 類型 \_ 帳戶**
</dt> <dd> <dl> <dt>



屬性會套用至具有生物特徵辨識註冊的特定使用者帳戶。 從 Windows 10 開始支援此值。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>Winbio (包含 Winbio) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式常數](client-application-constants.md)
</dt> <dt>

[**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> </dl>

 

 






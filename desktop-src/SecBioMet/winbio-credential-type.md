---
title: 'WINBIO_CREDENTIAL_TYPE 列舉 (Winbio \_ 類型 .h) '
description: 定義可以用來篩選認證類型的旗標。
ms.assetid: 7ef2d4b3-e1f9-46a0-8fc2-0e8660805ac3
keywords:
- WINBIO_CREDENTIAL_TYPE 列舉 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_TYPE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d559d97022f6c240e8a310adef829d47799683ad214fd0bfb0b54c6ec66cf5c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867968"
---
# <a name="winbio_credential_type-enumeration"></a>WINBIO \_ 認證 \_ 類型列舉

定義可以用來篩選認證類型的旗標。 [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)、 [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)和 [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)函式會使用這個列舉。

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_CREDENTIAL_TYPE { 
  WINBIO_CREDENTIAL_PASSWORD  = 0x00000001,
  WINBIO_CREDENTIAL_ALL       = 0xffffffff
} WINBIO_CREDENTIAL_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WINBIO_CREDENTIAL_PASSWORD"></span><span id="winbio_credential_password"></span>**WINBIO \_ 認證 \_ 密碼**
</dt> <dd>

篩選密碼認證。

</dd> <dt>

<span id="WINBIO_CREDENTIAL_ALL"></span><span id="winbio_credential_all"></span>**WINBIO \_ 認證 \_ 全部**
</dt> <dd>

篩選所有認證。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式列舉](client-application-enumerations.md)
</dt> <dt>

[**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> <dt>

[**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
</dt> <dt>

[**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

 






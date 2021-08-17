---
title: 'WINBIO_CREDENTIAL_FORMAT 列舉 (Winbio \_ 類型 .h) '
description: 定義可以用來指定使用者認證格式的旗標。
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- WINBIO_CREDENTIAL_FORMAT 列舉 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82185bdb9d8170abbdba04e758010443dc8be6a37e198edb27a137024dacf9af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910821"
---
# <a name="winbio_credential_format-enumeration"></a>WINBIO \_ 認證 \_ 格式列舉

定義可以用來指定使用者認證格式的旗標。 [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)函數會使用這個列舉。

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_CREDENTIAL_FORMAT { 
  WINBIO_PASSWORD_GENERIC    = 0x00000001,
  WINBIO_PASSWORD_PACKED     = 0x00000002,
  WINBIO_PASSWORD_PROTECTED  = 0x00000003
} WINBIO_CREDENTIAL_FORMAT;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**WINBIO \_ 密碼 \_ 泛型**
</dt> <dd>

密碼採用一般格式。

</dd> <dt>

<span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**WINBIO 的 \_ 密碼已 \_ 壓縮**
</dt> <dd>

密碼是壓縮格式。

</dd> <dt>

<span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO \_ 密碼 \_ 受保護**
</dt> <dd>

密碼認證已使用 [**CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta)包裝。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式列舉](client-application-enumerations.md)
</dt> <dt>

[**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 


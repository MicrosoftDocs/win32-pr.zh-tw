---
title: 'WINBIO_BSP_SCHEMA 結構 (Winbio \_ 類型 .h) '
description: 描述生物特徵辨識服務提供者的功能。
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- WINBIO_BSP_SCHEMA 結構 Windows 生物特徵辨識架構 API
- PWINBIO_BSP_SCHEMA 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_BSP_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ae63aefb64eb22f454559b76e9922242ca9530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465413"
---
# <a name="winbio_bsp_schema-structure"></a>WINBIO \_ BSP \_ 架構結構

**WINBIO \_ BSP \_ 架構** 結構描述生物特徵辨識服務提供者的功能。 [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)函數會使用這個結構。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_BSP_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           BspId;
  WINBIO_STRING         Description;
  WINBIO_STRING         Vendor;
  WINBIO_VERSION        Version;
} WINBIO_BSP_SCHEMA, *PWINBIO_BSP_SCHEMA;
```



## <a name="members"></a>成員

<dl> <dt>

**BiometricFactor**
</dt> <dd>

此裝置使用的生物特徵辨識測量型別。 目前，這必須是 **WINBIO \_ 類型 \_ 指紋**。

</dd> <dt>

**BspId**
</dt> <dd>

可唯一識別此生物特徵辨識服務提供者元件的值。

</dd> <dt>

**說明**
</dt> <dd>

以 **Null** 終止的 Unicode 字串，其中包含生物識別服務提供者的描述。

</dd> <dt>

**廠商**
</dt> <dd>

以 **Null** 終止的 Unicode 字串，其中包含提供生物特徵辨識服務提供者的供應商名稱。

</dd> <dt>

**版本**
</dt> <dd>

[**WINBIO \_ 版本**](winbio-version.md)結構包含生物特徵辨識服務提供者元件的軟體版本。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式結構](client-application-structures.md)
</dt> <dt>

[**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 






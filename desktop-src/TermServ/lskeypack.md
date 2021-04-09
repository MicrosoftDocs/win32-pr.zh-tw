---
title: LSKeyPack 結構
description: 包含特定遠端桌面服務授權金鑰套件的相關資訊。
ms.assetid: c26d27ee-7dd3-49f0-a79c-752d23693a2a
ms.tgt_platform: multiple
keywords:
- LSKeyPack 結構遠端桌面服務
- LPLSKeyPack 結構指標遠端桌面服務
topic_type:
- apiref
api_name:
- LSKeyPack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b1ac1f51e66a0a3c15c33f2535bc02f1fd3528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934967"
---
# <a name="lskeypack-structure"></a>LSKeyPack 結構

包含特定遠端桌面服務授權金鑰套件的相關資訊。

> [!Note]  
> 此結構未定義于任何標頭檔中。 若要使用這個結構，您必須自行定義，如本主題所示。

 

## <a name="syntax"></a>語法


```C++
typedef struct _LSKeyPack {
  DWORD dwVersion;
  UCHAR ucKeyPackType;
  TCHAR szCompanyName[256];
  TCHAR szKeyPackId[256];
  TCHAR szProductName[256];
  TCHAR szProductId[256];
  TCHAR szProductDesc[256];
  WORD  wMajorVersion;
  WORD  wMinorVersion;
  DWORD dwPlatformType;
  UCHAR ucLicenseType;
  DWORD dwLanguageId;
  UCHAR ucChannelOfPurchase;
  TCHAR szBeginSerialNumber[256];
  DWORD dwTotalLicenseInKeyPack;
  DWORD dwProductFlags;
  DWORD dwKeyPackId;
  UCHAR ucKeyPackStatus;
  DWORD dwActivateDate;
  DWORD dwExpirationDate;
  DWORD dwNumberOfLicenses;
} LSKeyPack, *LPLSKeyPack;
```



## <a name="members"></a>成員

<dl> <dt>

**dwVersion**
</dt> <dd>

金鑰套件的版本。

</dd> <dt>

**ucKeyPackType**
</dt> <dd>

金鑰套件的類型。

</dd> <dt>

**szCompanyName**
</dt> <dd>

簽發金鑰套件的公司名稱。

</dd> <dt>

**szKeyPackId**
</dt> <dd>

金鑰套件的識別碼。

</dd> <dt>

**szProductName**
</dt> <dd>

此金鑰套件所屬的產品名稱。

</dd> <dt>

**szProductId**
</dt> <dd>

此金鑰套件所屬產品的識別碼。

</dd> <dt>

**szProductDesc**
</dt> <dd>

此金鑰套件所屬產品的描述。

</dd> <dt>

**wMajorVersion**
</dt> <dd>

此金鑰套件所屬產品的主要版本。

</dd> <dt>

**wMinorVersion**
</dt> <dd>

此金鑰套件所屬產品的次要版本。

</dd> <dt>

**dwPlatformType**
</dt> <dd>

平臺類型。

</dd> <dt>

**ucLicenseType**
</dt> <dd>

金鑰套件中的授權類型。

</dd> <dt>

**dwLanguageId**
</dt> <dd>

語言識別碼。

</dd> <dt>

**ucChannelOfPurchase**
</dt> <dd>

購買通道。

</dd> <dt>

**szBeginSerialNumber**
</dt> <dd>

第一個授權的序號。

</dd> <dt>

**dwTotalLicenseInKeyPack**
</dt> <dd>

金鑰套件中的授權總數。

</dd> <dt>

**dwProductFlags**
</dt> <dd>

標誌。

</dd> <dt>

**dwKeyPackId**
</dt> <dd>

金鑰套件的識別碼。

</dd> <dt>

**ucKeyPackStatus**
</dt> <dd>

金鑰套件的狀態。

</dd> <dt>

**dwActivateDate**
</dt> <dd>

金鑰套件的啟用日期。

</dd> <dt>

**dwExpirationDate**
</dt> <dd>

金鑰套件的到期日。

</dd> <dt>

**dwNumberOfLicenses**
</dt> <dd>

授權數目。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> </dl>

 

 






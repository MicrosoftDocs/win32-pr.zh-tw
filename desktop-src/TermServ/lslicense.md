---
title: LSLicense 結構
description: 包含特定遠端桌面服務授權的相關資訊。
ms.assetid: 2c7f7b7a-e3b5-4f84-b49f-5f1d6960652d
ms.tgt_platform: multiple
keywords:
- LSLicense 結構遠端桌面服務
- LPLSLicense 結構指標遠端桌面服務
topic_type:
- apiref
api_name:
- LSLicense
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ea276b1b1217505a7bb44e1d70dd58d53eb57933d755ed9f79100abc177c3a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605411"
---
# <a name="lslicense-structure"></a>LSLicense 結構

包含特定遠端桌面服務授權的相關資訊。

> [!Note]  
> 此結構未定義于任何標頭檔中。 若要使用這個結構，您必須自行定義，如本主題所示。

 

## <a name="syntax"></a>語法


```C++
typedef struct _LSLicense {
  DWORD dwVersion;
  DWORD dwLicenseId;
  DWORD dwKeyPackId;
  TCHAR szHWID[GUID_MAX_SIZE];
  TCHAR szMachineName[MAXCOMPUTERNAMELENGTH];
  TCHAR szUserName[MAXUSERNAMELENGTH];
  DWORD dwCertSerialLicense;
  DWORD dwLicenseSerialNumber;
  DWORD ftIssueDate;
  DWORD ftExpireDate;
  UCHAR ucLicenseStatus;
} LSLicense, *LPLSLicense;
```



## <a name="members"></a>成員

<dl> <dt>

**dwVersion**
</dt> <dd>

授權版本。

</dd> <dt>

**dwLicenseId**
</dt> <dd>

授權的識別碼。

</dd> <dt>

**dwKeyPackId**
</dt> <dd>

包含授權的 [**LSKEYPACK**](lskeypack.md) 識別碼。

</dd> <dt>

**szHWID**
</dt> <dd>

發出授權的遠端桌面連線 (RDC) 用戶端的硬體識別碼。

</dd> <dt>

**szMachineName**
</dt> <dd>

已發出授權之遠端桌面連線 (RDC) 用戶端的名稱。

</dd> <dt>

**szUserName**
</dt> <dd>

已發出授權之使用者的名稱。

</dd> <dt>

**dwCertSerialLicense**
</dt> <dd>

保留供未來使用。

</dd> <dt>

**dwLicenseSerialNumber**
</dt> <dd>

授權的序號。

</dd> <dt>

**ftIssueDate**
</dt> <dd>

授權的發出日期。

</dd> <dt>

**ftExpireDate**
</dt> <dd>

授權將到期的日期。

</dd> <dt>

**ucLicenseStatus**
</dt> <dd>

授權的目前狀態。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> </dl>

 

 






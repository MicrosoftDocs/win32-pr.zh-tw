---
description: 包含 (GRL) 標頭的全域撤銷清單。
ms.assetid: 806ae550-5106-47ec-8466-f967598d3e61
title: GRL_HEADER 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GRL_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: c20c9323ac627f9f1d6c63ae893d1633fb3cd96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973403"
---
# <a name="grl_header-structure"></a>GRL \_ 標頭結構

包含 (GRL) 標頭的全域撤銷清單。

## <a name="syntax"></a>語法


```C++
typedef struct _GRL_HEADER {
  WCHAR    wszIdentifier[6];
  WORD     wFormatMajor;
  WORD     wFormatMinor;
  FILETIME CreationTime;
  DWORD    dwSequenceNumber;
  DWORD    dwForceRebootVersion;
  DWORD    dwForceProcessRestartVersion;
  DWORD    cbRevocationSectionOffset;
  DWORD    cRevokedKernelBinaries;
  DWORD    cRevokedUserBinaries;
  DWORD    cRevokedCertificates;
  DWORD    cTrustedRoots;
  DWORD    cbExtensibleSectionOffset;
  DWORD    cExtensibleEntries;
  DWORD    cbRenewalSectionOffset;
  DWORD    cRevokedKernelBinaryRenewals;
  DWORD    cRevokedUserBinaryRenewals;
  DWORD    cRevokedCertificateRenewals;
  DWORD    cbSignatureCoreOffset;
  DWORD    cbSignatureExtOffset;
} GRL_HEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**wszIdentifier**
</dt> <dd>

GRL 識別碼。 此值一律為 L "MSGRL"。

</dd> <dt>

**wFormatMajor**
</dt> <dd>

主要版本號碼。 此值目前必須為1。

</dd> <dt>

**wFormatMinor**
</dt> <dd>

次要版本號碼。 此值目前必須為零。

</dd> <dt>

**CreationTime**
</dt> <dd>

指定檔案建立時間的 **FILETIME** 值。

</dd> <dt>

**dwSequenceNumber**
</dt> <dd>

GRL 版本號碼。 值目前必須至少為3

</dd> <dt>

**dwForceRebootVersion**
</dt> <dd>

保留的。

</dd> <dt>

**dwForceProcessRestartVersion**
</dt> <dd>

保留的。

</dd> <dt>

**cbRevocationSectionOffset**
</dt> <dd>

從 GRL 開頭到核心區段的位移（以位元組為單位）。

</dd> <dt>

**cRevokedKernelBinaries**
</dt> <dd>

在 GRL 中列出的已撤銷核心二進位檔數目。

</dd> <dt>

**cRevokedUserBinaries**
</dt> <dd>

在 GRL 中列出的已撤銷使用者模式二進位檔的數目。

</dd> <dt>

**cRevokedCertificates**
</dt> <dd>

在 GRL 中列出的已撤銷憑證數目。

</dd> <dt>

**cTrustedRoots**
</dt> <dd>

在 GRL 中列出的受根信任目錄數目。

</dd> <dt>

**cbExtensibleSectionOffset**
</dt> <dd>

從 GRL 開頭到可擴充區段的位移（以位元組為單位）。

</dd> <dt>

**cExtensibleEntries**
</dt> <dd>

可擴充區段中的專案數。

</dd> <dt>

**cbRenewalSectionOffset**
</dt> <dd>

從 GRL 開頭到續約區段的位移（以位元組為單位）。

</dd> <dt>

**cRevokedKernelBinaryRenewals**
</dt> <dd>

在 GRL 中列出的核心二進位檔續約數目。

</dd> <dt>

**cRevokedUserBinaryRenewals**
</dt> <dd>

在 GRL 中列出的使用者模式二進位續約數目。

</dd> <dt>

**cRevokedCertificateRenewals**
</dt> <dd>

在 GRL 中列出的憑證續約數目。

</dd> <dt>

**cbSignatureCoreOffset**
</dt> <dd>

從 GRL 開頭到核心區段簽章的位移（以位元組為單位）。

</dd> <dt>

**cbSignatureExtOffset**
</dt> <dd>

從 GRL 開頭到可延伸區段簽章的位移（以位元組為單位）。

</dd> </dl>

## <a name="remarks"></a>備註

GRL 中的所有整數都有位元組由小到小的位元組順序。 所有結構都對齊1位元組的界限。

SDK 標頭中未宣告此結構。 若要使用此結構，請將此處顯示的宣告新增至您的原始程式碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[OPM 憑證撤銷](opm-certificate-revocation.md)
</dt> <dt>

[OPM 結構](opm-structures.md)
</dt> </dl>

 

 





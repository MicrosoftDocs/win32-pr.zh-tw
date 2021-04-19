---
description: 傳回用來建立鏈物件的 EKU 物件。
ms.assetid: d02f1614-6a4f-4c60-b406-ce174a99e9a5
title: CertificateStatus EKU 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d386251c6d7f674d3850de275559bcb87ea6d61e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988662"
---
# <a name="certificatestatuseku-method"></a>CertificateStatus EKU 方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ChainStatus 結構**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1)。\]

**Eku** 方法會傳回用來建立 [**鏈**](chain.md)物件的 [**eku**](eku.md)物件。

## <a name="syntax"></a>語法


```VB
CertificateStatus.EKU()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法會傳回 [**EKU**](eku.md) 物件，指出 [*憑證*](../secgloss/c-gly.md)的擴充金鑰使用方式設定。 EKU 設定會建立憑證的有效使用。 只能為每個憑證設定單一 **EKU** 物件。

## <a name="remarks"></a>備註

[**CertificateStatus. ApplicationPolicies**](certificatestatus-applicationpolicies.md)方法提供的功能與這個方法相同，但允許指定許多設定，而不是只有一個。 如果 **ApplicationPolicies** 方法所傳回的 [**oid**](oids.md)集合包含一個或多個 [**OID**](oid.md)物件，則會忽略這個方法所傳回的 [**EKU**](eku.md)物件。 使用 **ApplicationPolicies** 方法，而不是此方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CertificateStatus**](certificatestatus.md)
</dt> <dt>

[**加密物件**](cryptography-objects.md)
</dt> <dt>

[**EKU**](eku.md)
</dt> </dl>

 

 

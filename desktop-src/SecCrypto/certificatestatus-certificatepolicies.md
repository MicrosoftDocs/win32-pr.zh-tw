---
description: 傳回 Oid 集合，表示用來建立鏈物件的憑證原則。
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: CertificateStatus. CertificatePolicies 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e4d6507446bf15d00d8e388699ee0c0892c8755b94913d18657634311db57ec1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126708"
---
# <a name="certificatestatuscertificatepolicies-method"></a>CertificateStatus. CertificatePolicies 方法

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ChainStatus 結構**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1)。\]

**CertificatePolicies** 方法會傳回 [**oid**](oids.md)集合，表示用來建立 [**Chain**](chain.md)物件的憑證原則。

## <a name="syntax"></a>語法


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

[**Oid**](oids.md)集合。 集合中的每個 [**OID**](oid.md) 物件都代表一個憑證原則 OID。

## <a name="remarks"></a>備註

將憑證原則 Oid 新增至集合，以指定應該用來建立憑證信任鏈的憑證原則。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

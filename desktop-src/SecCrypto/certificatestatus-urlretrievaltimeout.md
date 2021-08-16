---
description: 設定或抓取 URL 判定為無法存取之前的時間長度。
ms.assetid: f39dafc4-6017-463c-aeee-948b6173862a
title: CertificateStatus. UrlRetrievalTimeout 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.UrlRetrievalTimeout
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b56e9bca2cc7c666f980df8905ac79fc885050d37359e524a83e287dcd5415e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770088"
---
# <a name="certificatestatusurlretrievaltimeout-property"></a>CertificateStatus. UrlRetrievalTimeout 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ChainStatus 結構**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1)。\]

**UrlRetrievalTimeout** 屬性會設定或抓取 URL 判定為無法存取之前的時間長度。

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.UrlRetrievalTimeout As Long
```



## <a name="property-value"></a>屬性值

將 URL 判定為無法存取之前的秒數。

## <a name="remarks"></a>備註

如果未設定此屬性，預設的超時時間為15秒。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

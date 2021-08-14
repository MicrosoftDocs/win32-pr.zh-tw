---
description: 判斷憑證是否有與其相關聯的私密金鑰。 方法會藉由檢查是否 \_ 有 CERT KEY \_ >prov \_ INFO \_ \_ 屬性識別碼屬性來決定這一點。
ms.assetid: 80478956-1ed7-4c25-9ae3-d7176649e6d7
title: ICertificate2：： HasPrivateKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.HasPrivateKey
- ICertificate2.HasPrivateKey
- ICertificate.HasPrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ac38a62e11d75e21de5fd61dffd821cb4384e4e9b59d2bf11f6e217589ab578b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771529"
---
# <a name="icertificate2hasprivatekey-method"></a>ICertificate2：： HasPrivateKey 方法

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]

**HasPrivateKey** 方法會判斷 [*憑證*](../secgloss/c-gly.md)是否有與其相關聯的 [*私密金鑰*](../secgloss/p-gly.md)。 方法會藉由檢查是否 \_ 有 CERT KEY \_ >prov \_ INFO \_ \_ 屬性識別碼屬性來決定這一點。

## <a name="syntax"></a>語法


```VB
Certificate.HasPrivateKey()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PrivateKey。開啟**](privatekey-open.md)
</dt> <dt>

[加密物件](cryptography-objects.md)
</dt> <dt>

[**憑證**](certificate.md)
</dt> </dl>

 

 

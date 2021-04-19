---
description: 抓取包含存放區中所有憑證的集合。
ms.assetid: 06cfc0e9-8a77-4e10-b559-4d42ac93c01b
title: 存放區憑證屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 979cf31c98286ca5bdd2df709176a27a5abb2321
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984048"
---
# <a name="storecertificates-property"></a>存放區憑證屬性

\[[ **憑證** ] 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/previous-versions/windows/embedded/hh424027(v=msdn.10))。\]

[ **憑證** ] 屬性會抓取包含存放區中所有憑證的集合。 這是預設屬性。

## <a name="syntax"></a>Syntax


```VB
Store.Certificates As Certificates
```



## <a name="property-value"></a>屬性值

存放區中的憑證集合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**市集**](store.md)
</dt> </dl>

 

 

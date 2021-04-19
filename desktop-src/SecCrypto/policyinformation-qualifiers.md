---
description: 捕獲原則限定詞的集合。
ms.assetid: aa5e2225-0a39-40bc-868c-d96f5953edaa
title: 'PolicyInformation 的限定詞屬性 (Iads. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 89f24e21acd24cbcaa021f7c668fc8c208102c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977408"
---
# <a name="policyinformationqualifiers-property"></a>PolicyInformation 的限定詞屬性

\[[ **限定詞** ] 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 oid 來處理憑證原則延伸中的原則資訊。\]

**限定詞** 屬性會抓取原則的限定詞集合。

## <a name="syntax"></a>Syntax


```VB
PolicyInformation.Qualifiers As Qualifiers
```



## <a name="property-value"></a>屬性值

原則的認證實務聲明 (CPS) 指標或使用者聲明辨識符號，作為 [**限定詞**](qualifiers.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| 標頭<br/>          | <dl> <dt>Iads。h</dt> </dl>      |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PolicyInformation**](policyinformation.md)
</dt> </dl>

 

 

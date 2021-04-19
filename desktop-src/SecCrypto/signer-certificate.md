---
description: 設定或抓取代表資料簽署者之憑證的憑證物件。
ms.assetid: 92ac209e-59b5-4a75-922d-d61629ca41b1
title: 簽署者憑證屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 96652f85e6058682dedd3370965ea7ff2408b3b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992384"
---
# <a name="signercertificate-property"></a>簽署者憑證屬性

\[[ **憑證** ] 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**CmsSigner 類別**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**Certificate** 屬性會設定或抓取代表資料簽署者之憑證的 [**憑證**](certificate.md)物件。 這是預設屬性。

## <a name="syntax"></a>Syntax


```VB
Signer.Certificate As Certificate
```



## <a name="property-value"></a>屬性值

代表資料簽署者之憑證的 [**憑證**](certificate.md) 物件。

## <a name="remarks"></a>備註

當這個屬性的值是直接或間接重設時，會重設物件的整個 [*狀態*](../secgloss/s-gly.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**簽署者**](signer.md)
</dt> </dl>

 

 

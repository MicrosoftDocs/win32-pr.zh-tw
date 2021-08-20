---
description: 抓取指向憑證實務聲明的 URI， (CPS) 由憑證授權單位單位 (CA) 發佈。
ms.assetid: fd030c1c-137c-4036-bf13-ae989a9703cc
title: CPSPointer 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.CPSPointer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b7e24cd47c26c2ec365fc8c52be7319b325199fdfca8af2a0f9967a9713a9c81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975842"
---
# <a name="qualifiercpspointer-property"></a>CPSPointer 屬性

\[**CPSPointer** 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 Oid 來處理憑證原則延伸中屬於原則資訊的限定詞。\]

**CPSPointer** 屬性會抓取指向憑證實務聲明的 URI， (CPS) 由憑證授權單位單位 (CA) 發佈。

## <a name="syntax"></a>Syntax


```VB
Qualifier.CPSPointer As String
```



## <a name="property-value"></a>屬性值

指向 CA 所發佈之 CPS 的 URI。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Qualifier**](qualifier.md)
</dt> </dl>

 

 

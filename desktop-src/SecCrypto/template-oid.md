---
description: 抓取識別範本物件的 OID 物件。
ms.assetid: bdd9d401-e9c4-4307-9817-7dcb55c539f8
title: Template 的 OID 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ecfc56210d5fa81f6e7623b2c471cf0df1b5f091f7dab6c797b56f6af8d2496e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897383"
---
# <a name="templateoid-property"></a>Template 的 OID 屬性

\[**OID** 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫接受 OID 作為參數的函式，然後使用憑證範本的 oid 來取得憑證延伸範本。\]

**Oid** 屬性會抓取可識別 [**範本**](template.md)物件的 [**oid**](oid.md)物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Template.OID As OID
```



## <a name="property-value"></a>屬性值

識別 [**範本**](template.md)物件的 [**OID**](oid.md)物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**範本**](template.md)
</dt> </dl>

 

 

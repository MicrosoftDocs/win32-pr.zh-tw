---
description: 抓取布林值，指出範本延伸是否存在。
ms.assetid: cc7f9853-8212-470d-b372-43a4bbd517f7
title: IsPresent 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23dcd8cc5ee92a689300078d439998e43933af93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986799"
---
# <a name="templateispresent-property"></a>IsPresent 屬性

\[**IsPresent** 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫接受 OID 作為參數的函式，然後使用憑證範本的 oid 來取得憑證延伸範本。\]

**IsPresent** 屬性會抓取布林值，指出範本延伸是否存在。

## <a name="syntax"></a>Syntax


```VB
Template.IsPresent As Boolean
```



## <a name="property-value"></a>屬性值

若 **為 true**，表示範本延伸模組存在。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**範本**](template.md)
</dt> </dl>

 

 

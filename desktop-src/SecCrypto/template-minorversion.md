---
description: 捕獲範本的次要版本號碼。
ms.assetid: 3fc51d43-9113-4b4b-88ab-27cf6e5c4fa0
title: MinorVersion 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MinorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 695bde72274f9fe1e6df6e77eed1f956052a46201ae4be10e0848e8285cfa3b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897403"
---
# <a name="templateminorversion-property"></a>MinorVersion 屬性

\[**MinorVersion** 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫接受 OID 作為參數的函式，然後使用憑證範本的 oid 來取得憑證延伸範本。\]

**MinorVersion** 屬性會捕獲範本的次要版本號碼。

## <a name="syntax"></a>Syntax


```VB
Template.MinorVersion As Long
```



## <a name="property-value"></a>屬性值

範本的次要版本號碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**範本**](template.md)
</dt> </dl>

 

 

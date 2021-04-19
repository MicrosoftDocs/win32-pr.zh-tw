---
description: 捕獲範本的主要版本號碼。
ms.assetid: efde3a7c-48e0-4bfe-9118-3098c7ef8771
title: MajorVersion 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MajorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a193a36ed7e914d1ed45d26c21008a7e59a5b8a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998655"
---
# <a name="templatemajorversion-property"></a>MajorVersion 屬性

\[**MajorVersion** 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫接受 OID 作為參數的函式，然後使用憑證範本的 oid 來取得憑證延伸範本。\]

**MajorVersion** 屬性會捕獲範本的主要版本號碼。

## <a name="syntax"></a>Syntax


```VB
Template.MajorVersion As Long
```



## <a name="property-value"></a>屬性值

範本的主要版本號碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**範本**](template.md)
</dt> </dl>

 

 

---
description: 抓取已驗證之屬性的集合。
ms.assetid: d4b3efab-d71e-4fef-9691-0c0bbcb27281
title: AuthenticatedAttributes 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.AuthenticatedAttributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3963ec60d699300c4cde368d4d78c39c0873edd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977618"
---
# <a name="signerauthenticatedattributes-property"></a>AuthenticatedAttributes 屬性

\[**AuthenticatedAttributes** 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**CmsSigner 類別**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**AuthenticatedAttributes** 屬性會抓取已驗證之屬性的集合。

## <a name="syntax"></a>Syntax


```VB
Signer.AuthenticatedAttributes As Attributes
```



## <a name="property-value"></a>屬性值

代表簽署者之已驗證屬性的 [**屬性**](attributes.md) 集合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**簽署者**](signer.md)
</dt> </dl>

 

 

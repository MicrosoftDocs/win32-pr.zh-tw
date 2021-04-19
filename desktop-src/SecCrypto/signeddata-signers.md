---
description: 抓取資料的簽名建立者。
ms.assetid: 3e28f08a-c4d8-4dd7-953a-e1500eb5bee0
title: SignedData。簽署者屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5f4c58c2a69c483fc38412a6aa8377742d52d39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985746"
---
# <a name="signeddatasigners-property"></a>SignedData。簽署者屬性

\[[ **簽署** 者] 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**SignedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**簽署** 者屬性會抓取資料的簽章建立者。

## <a name="syntax"></a>Syntax


```VB
SignedData.Signers As Signers
```



## <a name="property-value"></a>屬性值

代表資料簽章建立者的 [**簽署**](signers.md) 者集合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 

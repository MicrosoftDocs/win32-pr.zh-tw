---
description: 抓取代表索引簽署者的簽署者物件。
ms.assetid: a95f4e33-ab92-44e1-91ab-2c5335a04f05
title: 簽署者. 專案屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 33630586282b745da94a442c13a0e85574c5f2e06fc04ab909e4ebf59fc2707b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898405"
---
# <a name="signersitem-property"></a>簽署者. 專案屬性

\[**專案** 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用 CmsSigner 物件的集合。 For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]

**Item** 屬性會抓取代表索引簽署者的 [**簽署者**](signer.md)物件。 這是預設屬性。

## <a name="syntax"></a>Syntax


```VB
Signers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>屬性值

代表索引簽署者的 [**簽署者**](signer.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**簽名**](signers.md)
</dt> </dl>

 

 

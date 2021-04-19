---
description: 抓取集合中的簽署者物件數目。
ms.assetid: 990e273a-8f3d-4a77-b0a4-243eeb32e6f3
title: 簽署者. 計數屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fd8296acfaf5e0d25f7d8a80c1c96e53cfa35578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984751"
---
# <a name="signerscount-property"></a>簽署者. 計數屬性

\[[ **計數** ] 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用 CmsSigner 物件的集合。 For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]

**Count** 屬性會抓取集合中的 [**簽署者**](signer.md)物件數目。

## <a name="syntax"></a>Syntax


```VB
Signers.Count As Long
```



## <a name="property-value"></a>屬性值

集合中的 [**簽署者**](signer.md) 物件數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**簽名**](signers.md)
</dt> </dl>

 

 

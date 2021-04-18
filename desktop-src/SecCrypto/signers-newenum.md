---
description: 簽署者的 \_ NewEnum 屬性會抓取可用於列舉集合之物件上的 IEnumVARIANT 介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。
ms.assetid: 99d7ddd3-a552-4125-b220-d1b28f20d1ed
title: Signers._NewEnum 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 91007e7ce282cb44267927f54ab26f8f930028f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976202"
---
# <a name="signers_newenum-property"></a>簽署者。 \_NewEnum 屬性

\[**\_ NewEnum** 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用 CmsSigner 物件的集合。 For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]

**\_ NewEnum** 屬性會抓取可用於列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。

## <a name="syntax"></a>Syntax


```VB
Signers._NewEnum As IUnknown
```



## <a name="property-value"></a>屬性值

可以用來列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。

## <a name="remarks"></a>備註

當您使用 Visual Basic Scripting Edition 中的結構時，會自動在內部使用此屬性 `For Each In` (VBScript) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**簽名**](signers.md)
</dt> </dl>

 

 

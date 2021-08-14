---
description: 收件者的 \_ NewEnum 屬性會抓取可用於列舉集合之物件上的 IEnumVARIANT 介面。 這個屬性會在 Visual Basic 腳本版本 (VBScript) 中隱藏。
ms.assetid: affdc695-b78c-48b5-b66d-5f94e1a86ff2
title: Recipients._NewEnum 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b71b015ccec741070d6c0261b0da094be98a716f1596ffab2d66575249ba9baf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900748"
---
# <a name="recipients_newenum-property"></a>收件者。 \_NewEnum 屬性

\[**\_ NewEnum** 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**CmsRecipientCollection 類別**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**\_ NewEnum** 屬性會抓取可用於列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)介面。 這個屬性會在 Visual Basic 腳本版本 (VBScript) 中隱藏。

## <a name="syntax"></a>Syntax


```VB
Recipients._NewEnum As IUnknown
```



## <a name="property-value"></a>屬性值

可以用來列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。

## <a name="remarks"></a>備註

當您使用 `For Each In` Visual Basic 腳本版本 (VBScript) 中的結構時，會自動在內部使用此屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**收件者**](recipients.md)
</dt> </dl>

 

 

---
description: 屬性（attribute）的 \_ NewEnum 屬性（attribute）會在可以用來列舉集合的物件上，抓取 IEnumVARIANT 介面。 這個屬性會在 Visual Basic 腳本版本 (VBScript) 中隱藏。
ms.assetid: a90ef28b-3926-4542-bcd2-27f0eda4e339
title: Attributes._NewEnum 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e52428afa3a31c588417979b28d9c29ca23fcb446542cedc45c57127326507e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879818"
---
# <a name="attributes_newenum-property"></a>屬性。 \_NewEnum 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista Windows XP。 請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**CryptographicAttributeObjectCollection 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true)。\]

**\_ NewEnum** 屬性會抓取可用於列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)介面。 這個屬性會在 Visual Basic 腳本版本 (VBScript) 中隱藏。

## <a name="syntax"></a>Syntax


```VB
Attributes._NewEnum As IUnknown
```



## <a name="property-value"></a>屬性值

可以用來列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。

## <a name="remarks"></a>備註

當您使用 `For Each In` Visual Basic 腳本版本 (VBScript) 中的結構時，會自動在內部使用此屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性**](attributes.md)
</dt> </dl>

 

 

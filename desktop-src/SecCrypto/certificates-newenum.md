---
description: '\_憑證的 NewEnum 屬性會在可用來列舉集合的物件上，捕獲 IEnumVARIANT 介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。'
ms.assetid: bbe6c82c-1949-4d81-bb87-3f05613efa6d
title: Certificates._NewEnum 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 71760f23bbb19d32c3caf8011eb87b8d03941eac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984440"
---
# <a name="certificates_newenum-property"></a>憑證。 \_NewEnum 屬性

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1)。\]

**\_ NewEnum** 屬性會抓取可用於列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。

## <a name="syntax"></a>Syntax


```VB
Certificates._NewEnum As IUnknown
```



## <a name="property-value"></a>屬性值

可以用來列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。

## <a name="remarks"></a>備註

當您使用 Visual Basic Scripting Edition 中的結構時，會自動在內部使用此屬性 `For Each In` (VBScript) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**憑證**](certificates.md)
</dt> </dl>

 

 

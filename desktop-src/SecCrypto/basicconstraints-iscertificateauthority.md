---
description: 取得布林值，指出憑證是否為憑證授權單位單位 (CA) 。
ms.assetid: 3ca43475-fe97-4eb4-875d-dbc15a0b953c
title: BasicConstraints. IsCertificateAuthority 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCertificateAuthority
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 90d616f4a7a0fe8522118848826bee88523ad45c34cb8a3fff23c722e68f2495
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879758"
---
# <a name="basicconstraintsiscertificateauthority-property"></a>BasicConstraints. IsCertificateAuthority 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/previous-versions/windows/)命名空間中的 [**X509BasicConstraintsExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1)。\]

**IsCertificateAuthority** 屬性會取得布林值，指出憑證是否為證書 [*頒發機構*](../secgloss/c-gly.md)單位 (CA) 。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
BasicConstraints.IsCertificateAuthority As Boolean
```



## <a name="property-value"></a>屬性值

若 **為 True**，則憑證只能由 CA 使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

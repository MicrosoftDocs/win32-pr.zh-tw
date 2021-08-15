---
description: 抓取包含憑證簽發者名稱的字串。
ms.assetid: 6cf528e3-061a-44dc-b320-0e4b48a6c6ab
title: Certificate. IssuerName 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IssuerName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f4404a105748a79ef942f37c088a5436fc3eeea0784bb6ff814dd0782262dcf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771576"
---
# <a name="certificateissuername-property"></a>Certificate. IssuerName 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]

**IssuerName** 屬性會捕獲包含憑證簽發者名稱的字串。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Certificate.IssuerName As String
```



## <a name="property-value"></a>屬性值

包含憑證簽發者名稱的字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

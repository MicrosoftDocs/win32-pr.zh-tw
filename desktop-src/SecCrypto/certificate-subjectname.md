---
description: 抓取包含憑證主體名稱的字串。
ms.assetid: 95dc7e8b-6670-4dfc-9fe1-d37635fb92d6
title: Certificate. SubjectName 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.SubjectName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: de38f1bbaf9af03eba8c026615eeb285c5a578002341a7c5023bf35a40e36f83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878168"
---
# <a name="certificatesubjectname-property"></a>Certificate. SubjectName 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]

**SubjectName** 屬性會抓取包含憑證主體名稱的字串。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Certificate.SubjectName As String
```



## <a name="property-value"></a>屬性值

包含憑證主體名稱的字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**憑證**](certificate.md)
</dt> </dl>

 

 

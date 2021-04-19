---
description: 抓取包含憑證序號的字串。
ms.assetid: d08be744-4ae8-49f9-8b00-48e76c296f2b
title: Certificate. SerialNumber 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.SerialNumber
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6dbd9485891cc89e686cef118e12dd43ec400f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994041"
---
# <a name="certificateserialnumber-property"></a>Certificate. SerialNumber 屬性

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]

**SerialNumber** 屬性會捕獲包含憑證序號的字串。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Certificate.SerialNumber As String
```



## <a name="property-value"></a>屬性值

包含憑證序號的字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

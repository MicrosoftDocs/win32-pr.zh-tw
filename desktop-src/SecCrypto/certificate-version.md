---
description: Version 屬性會捕獲憑證的版本號碼。
ms.assetid: 7f135a1a-ca77-4ff1-9437-532e468c6b41
title: Certificate. Version 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Version
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 10abf278d1b9c0d761b8819b461b785b2b4b025f71904ae50b09b7c66161f2ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771037"
---
# <a name="certificateversion-property"></a>Certificate. Version 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]

**Version** 屬性會捕獲憑證的版本號碼。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Certificate.Version As Long
```



## <a name="property-value"></a>屬性值

憑證的版本號碼。

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

 

 

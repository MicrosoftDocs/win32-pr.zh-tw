---
description: Result 屬性會抓取指出憑證是否有效的值。 這是預設屬性。
ms.assetid: b1edfbde-9d54-4e9c-ba9b-33e4c354c23f
title: CertificateStatus 結果屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Result
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df13e9a9fb0454d30ce855b3d272fa521e96e0f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000370"
---
# <a name="certificatestatusresult-property"></a>CertificateStatus 結果屬性

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ChainStatus 結構**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1)。\]

**Result** 屬性會抓取指出憑證是否有效的值。 這是預設屬性。

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.Result As Boolean
```



## <a name="property-value"></a>屬性值

若 **為 true**，則表示憑證有效。 使用 [**CheckFlag**](certificatestatus-checkflag.md) 屬性的目前設定和各種原則設定，檢查憑證的有效性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

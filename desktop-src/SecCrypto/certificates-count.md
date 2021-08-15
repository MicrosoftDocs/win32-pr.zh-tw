---
description: 抓取集合中的憑證物件數目。
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Certificate. Count 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 703b929ee4b9cbe69a0f2ff37ad7e1d0c2c0005c0aa461fc38a14baa8a8ab443
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770547"
---
# <a name="certificatescount-property"></a>Certificate. Count 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1)。\]

**Count** 屬性會抓取集合中的 [**憑證**](certificate.md)物件數目。

## <a name="syntax"></a>Syntax


```VB
Certificates.Count As Long
```



## <a name="property-value"></a>屬性值

集合中的 [**憑證**](certificate.md) 物件數目。 每個 **憑證** 物件都代表集合中的單一憑證。

## <a name="remarks"></a>備註

CAPICOM 只支援 [*智慧卡*](../secgloss/s-gly.md) 存放區的單一憑證。 即使智慧卡存放區包含一個以上的憑證，此屬性也會包含1。 如需智慧卡存放區的詳細資訊，請參閱 [**capicom \_ 存放區 \_ 位置**](capicom-store-location.md)列舉的 **capicom \_ 智慧 \_ 卡 \_ 使用者 \_ 存放區** 成員。

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

 

 

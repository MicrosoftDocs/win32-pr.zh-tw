---
description: 抓取集合中的 PolicyInformation 物件數目。
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: CertificatePolicies Count 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0ee51e37b3fd4ac66c4e615eaf068edc98a64807
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994884"
---
# <a name="certificatepoliciescount-property"></a>CertificatePolicies Count 屬性

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 oid 來取得憑證原則。\]

**Count** 屬性會抓取集合中的 [**PolicyInformation**](policyinformation.md)物件數目。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a>屬性值

集合中的 [**PolicyInformation**](policyinformation.md) 物件數目。 每個 **PolicyInformation** 物件都代表集合中的單一憑證原則。

## <a name="remarks"></a>備註

當您使用 [**CertificatePolicies. Item**](certificatepolicies-item.md)屬性來抓取特定 **PolicyInformation** 物件時，可以使用 **Count** 屬性來指定集合中的最後一個 [**PolicyInformation**](policyinformation.md)物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

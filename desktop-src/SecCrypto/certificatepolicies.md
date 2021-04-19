---
description: PolicyInformation 物件的集合。
ms.assetid: 2abdd070-82ae-47fd-afbc-6d4361e5a3f1
title: CertificatePolicies 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8ec217276b5d038f85f33887b771b0afa0c6e40a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995299"
---
# <a name="certificatepolicies-object"></a>CertificatePolicies 物件

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 oid 來取得憑證原則。\]

**CertificatePolicies** 物件代表 [**PolicyInformation**](policyinformation.md)物件的集合。 每個 [**PolicyInformation**](policyinformation.md) 物件都代表一個憑證原則。

## <a name="when-to-use"></a>使用時機

**CertificatePolicies** 物件是用來執行下列工作：

-   取得集合中的憑證原則數目。
-   從集合中取出特定的 [**PolicyInformation**](policyinformation.md) 物件。
-   逐一查看集合。

## <a name="members"></a>成員

**CertificatePolicies** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CertificatePolicies** 物件具有這些屬性。



| 屬性                                                    | 存取類型          | Description                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificatepolicies-newenum.md)<br/> | 唯讀<br/> | 在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。<br/> |
| [**計數**](certificatepolicies-count.md)<br/>       | 唯讀<br/> | 抓取集合中的 [**PolicyInformation**](policyinformation.md) 物件數目。<br/>                                                                                                                    |
| [**項目**](certificatepolicies-item.md)<br/>         | 唯讀<br/> | 抓取 [**PolicyInformation**](policyinformation.md) 物件，該物件代表集合的索引憑證原則。 這是預設屬性。<br/>                                                    |



 

## <a name="remarks"></a>備註

無法建立 **CertificatePolicies** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

---
description: 抓取集合中的 EKU 物件數目。
ms.assetid: a38ac480-4f9b-4d69-a7e6-fae4993fe2cf
title: Eku. Count 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41e77f3803fa65db1573c6619ebf1265b7418924
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979501"
---
# <a name="ekuscount-property"></a>Eku. Count 屬性

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ExtensionCollection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1)。\]

**Count** 屬性會抓取集合中的 [**EKU**](eku.md)物件數目。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
EKUs.Count As Long
```



## <a name="property-value"></a>屬性值

集合中的 [**EKU**](eku.md) 物件數目。 每個 **EKU** 物件都代表憑證 (EKU) 屬性的單一擴充金鑰使用方式。

## <a name="remarks"></a>備註

您可以使用 [**計數**] 屬性，在使用 [**eku. Item**](ekus-item.md)屬性抓取特定的 **eku** 物件時，指定集合中的最後一個 [**eku**](eku.md)物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

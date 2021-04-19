---
description: 表示 EKU 物件的集合。
ms.assetid: 04b9f0bf-e1d4-4a2c-be5d-bae7c1090bdb
title: Eku 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 56fd6eaeb5a00549cbb4ee659b99ece391e0ebed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997729"
---
# <a name="ekus-object"></a>Eku 物件

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ExtensionCollection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1)。\]

Eku **物件代表** [**EKU**](eku.md) 物件的集合。 每個 [**EKU**](eku.md) 物件都代表憑證 (EKU) 屬性的單一擴充金鑰使用方式。

## <a name="when-to-use"></a>使用時機

**Eku** 集合是用來執行下列工作：

-   取得集合中的 EKU 屬性數目。
-   從集合中取出特定的 [**EKU**](eku.md) 物件。
-   逐一查看集合。

## <a name="members"></a>成員

**Eku** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Eku** 物件具有這些屬性。



| 屬性                                     | 存取類型          | Description                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ekus-newenum.md)<br/> | 唯讀<br/> | 在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。<br/> |
| [**計數**](ekus-count.md)<br/>       | 唯讀<br/> | 抓取集合中的 [**EKU**](eku.md) 物件數目。<br/>                                                                                                                                                |
| [**項目**](ekus-item.md)<br/>         | 唯讀<br/> | 抓取表示已編制索引之 EKU 屬性的 [**eku**](eku.md) 物件。 這是預設屬性。<br/>                                                                                                      |



 

## <a name="remarks"></a>備註

這個集合是由 [**ExtendedKeyUsage**](extendedkeyusage-ekus.md) 屬性所抓取。

無法建立 **eku** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

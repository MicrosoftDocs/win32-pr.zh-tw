---
description: 表示擴充物件的集合。
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Extension 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3af518d6f1918c82d5819b04a086195c06b79740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976110"
---
# <a name="extensions-object"></a>Extension 物件

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ExtensionCollection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1)。\]

**Extensions** 物件代表 [**擴充**](extension.md)物件的集合。 每個 [**擴充**](extension.md) 物件都代表一個憑證延伸。

## <a name="when-to-use"></a>使用時機

**擴充** 物件是用來執行下列工作：

-   取得集合中的憑證擴充功能數目。
-   從集合中取出特定的 [**擴充**](extension.md) 物件。
-   逐一查看集合。

## <a name="members"></a>成員

**擴充** 物件有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Extensions** 物件具有這些屬性。



| 屬性                                           | 存取類型          | Description                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extensions-newenum.md)<br/> | 唯讀<br/> | 在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。<br/> |
| [**計數**](extensions-count.md)<br/>       | 唯讀<br/> | 抓取集合中的 [**擴充**](extension.md) 物件數目。<br/>                                                                                                                                    |
| [**項目**](extensions-item.md)<br/>         | 唯讀<br/> | 抓取代表集合之索引憑證延伸的 [**擴充**](extension.md) 物件。 這是預設屬性。<br/>                                                               |



 

## <a name="remarks"></a>備註

**Extension** 物件是由 [**Certificate. extension**](certificate-extensions.md)方法傳回。

無法建立 **擴充** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

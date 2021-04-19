---
description: 代表單一憑證延伸。
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: '擴充物件 (Mmcobj .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a048cd5f29825c2d96a9d924473159e93d3e0be1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990579"
---
# <a name="extension-object"></a>Extension 物件

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)。\]

**擴充** 物件代表單一憑證延伸。

## <a name="when-to-use"></a>使用時機

**擴充** 物件是用來執行下列工作：

-   取出憑證延伸的 OID。
-   取出 [**EncodedData**](encodeddata.md) 物件所代表的憑證擴充資料。
-   判斷憑證延伸是否標記為「重大」。

## <a name="members"></a>成員

**擴充** 物件有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**擴充** 物件具有這些屬性。



| 屬性                                                | 存取類型          | Description                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**EncodedData**](extension-encodeddata.md)<br/> | 唯讀<br/> | 抓取延伸模組的編碼資料。<br/>                                      |
| [**IsCritical**](extension-iscritical.md)<br/>   | 唯讀<br/> | 抓取布林值，指出是否將延伸標記為重大。<br/> |
| [**老**](extension-oid.md)<br/>                 | 唯讀<br/> | 抓取延伸模組的物件識別碼。 這是預設屬性。<br/>   |



 

## <a name="remarks"></a>備註

無法建立 **擴充** 物件。

[**擴充**](extensions.md)功能集合物件會使用 **擴充** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| 標頭<br/>                | <dl> <dt>Mmcobj。h</dt> </dl>    |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

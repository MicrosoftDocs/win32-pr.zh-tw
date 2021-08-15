---
description: 代表憑證的憑證延伸範本。
ms.assetid: 1ae9220a-f6b3-47c5-bd08-a36ffd84e1f9
title: 範本物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 53c7b06fa4194d0adb4124f3978787f5d1fce0ba88e78ef99dcd6ac162eca2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897319"
---
# <a name="template-object"></a>範本物件

\[**範本** 物件可在 [需求] 區段中指定的作業系統中使用。 相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫接受 OID 作為參數的函式，然後使用憑證範本的 oid 來取得憑證延伸範本。\]

**範本** 物件代表憑證的憑證延伸範本。

## <a name="when-to-use"></a>使用時機

**範本** 物件是用來執行下列工作：

-   判斷範本是否標記為重大或存在。
-   取得 (OID) 或範本名稱的 [*物件識別碼*](../secgloss/o-gly.md) 。
-   取出範本的次要或主要版本。

## <a name="members"></a>成員

**範本** 物件有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**範本** 物件具有這些屬性。



| 屬性                                                 | 存取類型          | Description                                                                                            |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| [**IsCritical**](template-iscritical.md)<br/>     | 唯讀<br/> | 抓取布林值，指出範本延伸是否標記為重大。<br/> |
| [**IsPresent**](template-ispresent.md)<br/>       | 唯讀<br/> | 抓取布林值，指出範本延伸是否存在。<br/>         |
| [**MajorVersion**](template-majorversion.md)<br/> | 唯讀<br/> | 捕獲範本的主要版本號碼。<br/>                                         |
| [**MinorVersion**](template-minorversion.md)<br/> | 唯讀<br/> | 捕獲範本的次要版本號碼。<br/>                                         |
| [**Name**](template-name.md)<br/>                 | 唯讀<br/> | 抓取包含範本名稱的字串。<br/>                                  |
| [**老**](template-oid.md)<br/>                   | 唯讀<br/> | 抓取識別 **範本** 物件的 [**OID**](oid.md)物件。<br/>             |



 

## <a name="remarks"></a>備註

無法建立 **範本** 物件。

[**Certificate. template**](certificate-template.md)方法會傳回 **範本** 物件。

CAPICOM 會使用兩種不同版本的憑證範本。 下表顯示每個憑證範本版本的名稱和 OID。



| 版本 | Name                               | OID                    |
|---------|------------------------------------|------------------------|
| V1      | szOID \_ 註冊 \_ CERTTYPE \_ 延伸模組 | 元1.3.6.1.4.1.311.20.2 參考 |
| V2      | szOID \_ 證書 \_ 範本       | "1.3.6.1.4.1.311.21.7" |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

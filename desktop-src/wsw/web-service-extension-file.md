---
title: Web 服務延伸模組檔案
description: 本節將概述 Web 服務延伸模組檔案。
ms.assetid: 856d4ff5-2292-4d87-ae7c-19b100fd1cb3
keywords:
- 適用于 Windows 的 web 服務延伸模組檔案 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0802e31895aa5dd5051c94746e774033a1ebe677
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316813"
---
# <a name="web-service-extension-file"></a>Web 服務延伸模組檔案

本節將概述 Web 服務延伸模組檔案。


.WSX 檔案 (WCF 服務延伸模組) 是我們的擴充檔，可讓應用程式操作不影響網路資料表示的本機行為。 它應該是可擴充的，我們可以在未來加入新功能，而不會中斷互通性。

.WSX 的整體結構會模仿 XSD 或 WSDL 檔案的結構，這是一個 XML 檔案，它會維護與主要輸入檔相同的結構。 在主要檔案中，相同命名權杖上的額外屬性會指定應用程式想要控制預設行為的屬性。

我們可能不會在 M3 中進行任何動作。 在 V1 中，我可以看到支援下列屬性：

指定 count 引數/parameter 欄位的使用方式。

這是元素屬性，但僅適用于陣列類型。 IsCountOf 屬性會指定陣列元素。 [計數] 欄位/參數未出現在網路上。

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="FooInParam">
  <complexType> 
   <!-- MyArray field is presented in WSDL file as an element -->
    <element name="MyArrayCount" IsCountOf="MyArray"></element>
   </complexType>
  </element>
 </xs:schema>
```

指定自訂類型的讀取/寫入回呼

這些屬性會強制 wsutil.exe，以產生指定類型的 [**WS \_ 自訂 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_type) 。 自訂 \_ readcallback 屬性會指定 [**讀取回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) 常式，而自訂 \_ writecallback 會指定 [**寫入回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) 常式。

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="mytype" custom_readcallback="myreadcallback" custom_writecallback="mywritecallback"> 
 </element>
</xs:schema>
```

我們可以有相符的 .WSX 檔案來描述其本機行為：

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">

 <element name="FooInParam" DataValidationRoutine="MyArrayValidation">
  <complexType> 
   <element name="MyLocalArrayCount" IsCountOf="MyArray"></element> 
  </complexType>
 </element>
</xs:schema>
```

WsUtil.exe 會產生下列結構的原型：

``` syntax
typedef struct FooInParam
{
  ULONG MyLocalArrayCount;
  int * MyArray;
};
```

 

 





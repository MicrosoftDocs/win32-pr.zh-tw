---
description: 定義要在主機建立器函式中裝載的服務。
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: hostedService 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08479e88214e5fe6d1fbbb6ff5a3fffb7bb2047e8b7ca08cde92d64dd7dd6b2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130790"
---
# <a name="hostedservice-element"></a>hostedService 元素

定義要在主機建立器函式中裝載的服務。

## <a name="usage"></a>使用方式

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                     | 描述                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**代號**](codename.md)<br/>     | 指定要在產生的程式碼中用於埠類型的名稱。 根據預設，會從埠類型的限定名稱產生程式碼名稱。<br/> <br/> |
| [**portType**](porttype.md)<br/>     | 要產生程式碼的埠類型。<br/> <br/>                                                                                                       |
| [**proxyClass**](proxyclass.md)<br/> | 要從 builder 函式產生的類別名稱。<br/> <br/>                                                                                                      |
| [**ServiceID**](serviceid.md)<br/>   | 表示服務識別碼的 URI。<br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [**檔**](file.md)<br/> | 程式碼產生器的輸出檔規格。<br/> <br/> |



## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 否            |



 

 





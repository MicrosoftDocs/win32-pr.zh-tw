---
description: 產生函數以建立具類型的 proxy。
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: proxyBuilderImplementations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2cb64a6ea87b1083871931359a4f7c01ece9b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000160"
---
# <a name="proxybuilderimplementations-element"></a>proxyBuilderImplementations 元素

產生函數以建立具類型的 proxy。

## <a name="usage"></a>使用方式

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                     | 描述                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**代號**](codename.md)<br/>     | 要在產生的程式碼中用於埠類型的名稱。 根據預設，會從埠類型的限定名稱產生程式碼名稱。<br/> <br/> |
| [**portType**](porttype.md)<br/>     | 要產生程式碼的埠類型。<br/> <br/>                                                                                             |
| [**proxyClass**](proxyclass.md)<br/> | 要從 proxy 產生器函數產生的類別名稱。<br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**檔**](file.md)<br/> | 從程式碼產生器輸出檔案。<br/> <br/> |



## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 否            |



 

 





---
description: 產生可建立具型別主機的函式。
ms.assetid: 2b4a4016-cc5d-4912-8e08-ce3a11ab0a06
title: hostBuilderImplementation 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9cfabb9ab4193162044420fc3980f0bbeeb55a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969304"
---
# <a name="hostbuilderimplementation-element"></a>hostBuilderImplementation 元素

產生可建立具型別主機的函式。

## <a name="usage"></a>使用方式

``` syntax
<hostBuilderImplementation>
  child elements
</hostBuilderImplementation>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                           | 描述                                                      |
|---------------------------------------------------|------------------------------------------------------------------|
| [**hostedService**](hostedservice.md)<br/> | 要包含給主機的服務。 <br/> <br/> |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
hostedService+
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



 

 





---
description: 指定存根函式所要使用的釋放器類型。
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: 釋放器元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3604f0efb366c3f88e2e0828c02344ee75606079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192178"
---
# <a name="deallocator-element"></a>釋放器元素

指定存根函式所要使用的釋放器類型。

## <a name="usage"></a>使用方式

``` syntax
<deallocator/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                               | 描述                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | 針對埠類型作業產生存根函式的實作為。<br/> <br/> |



## <a name="remarks"></a>備註

釋放器類型應該包含在一對 <deallocator></deallocator> 標記中。 下列字串是有效的釋放器值：

-   無
-   WSDFreeLinkedMemory
-   CoTaskMemFree
-   free
-   delete
-   deleteArray
-   版本

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 





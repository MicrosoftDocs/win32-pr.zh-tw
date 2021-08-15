---
description: 指定存根函式所要使用的釋放器類型。
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: 釋放器元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e9a27f768d0c9d854d13bd58c0c797234a0526c4abb95a0c5f4fb553466a6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991748"
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



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 





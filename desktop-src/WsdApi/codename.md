---
description: 定義用來在產生的程式碼中識別命名空間的名稱。
ms.assetid: 4e476be2-fa73-4b3e-b0cc-799c8d16b5de
title: codeName 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44c10b937f503c2d3994543db8852b5d7ee923b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985300"
---
# <a name="codename-element"></a>codeName 元素

定義用來在產生的程式碼中識別命名空間的名稱。

## <a name="usage"></a>使用方式

``` syntax
<codeName/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                         | 描述                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| [**命名 空間**](namespace.md)<br/>                       | 要用於產生程式碼的命名空間。<br/> <br/>       |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/> | 產生埠類型的 C 常數宣告。<br/> <br/> |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>   | 產生埠類型的 C 常數。<br/> <br/>             |



## <a name="remarks"></a>備註

這個元素會覆寫用於產生之程式碼的預設程式碼名稱。 根據預設，產生的程式碼會從 URI 或限定名稱建立程式碼名稱。

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 





---
description: 產生函式的宣告，這個函式會建立具類型的主控制項。
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: hostBuilderDeclaration 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16576050efc76264f42dff6a19549f69933185b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001744"
---
# <a name="hostbuilderdeclaration-element"></a>hostBuilderDeclaration 元素

產生函式的宣告，這個函式會建立具類型的主控制項。

## <a name="usage"></a>使用方式

``` syntax
<hostBuilderDeclaration>
  child elements
</hostBuilderDeclaration>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                   | 描述                                                                                                                                                                                                                  |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**介面**](interface.md)<br/> | 要為主機包含的服務介面名稱。 此元素的值必須符合 [**hostedService**](hostedservice.md)的 [**介面**](interface.md)子項目值。 <br/> <br/> |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
interface+
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



 

 





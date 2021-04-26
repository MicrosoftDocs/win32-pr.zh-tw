---
description: 描述命名空間。
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: nameSpace 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c3e2735efbb99fbe404f2531336c2e2bd0f89d7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994275"
---
# <a name="namespace-element"></a>nameSpace 元素

描述命名空間。 這個命名空間可用於產生程式碼或處理指示詞 \<wsdl:import> 。

## <a name="usage"></a>使用方式

``` syntax
<nameSpace
  uri = "character_string">
  child elements
</nameSpace>
```

## <a name="attributes"></a>屬性



| 屬性          | 類型                         | 必要       | 描述                                             |
|--------------------|------------------------------|----------------|---------------------------------------------------------|
| **uri**<br/> | 字元 \_ 字串<br/> | Yes<br/> | 命名空間的唯一 URI。<br/> <br/> |



## <a name="child-elements"></a>子元素



| 元素                                               | 描述                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**代號**](codename.md)<br/>               | 用來在產生的程式碼中識別命名空間的名稱。<br/> <br/>                  |
| [**macroPrefix**](macroprefix.md)<br/>         | 在命名空間中宏名稱所產生的程式碼中，所要使用的前置詞。<br/> <br/> |
| [**名字**](name.md)<br/>                       | 命名空間中的限定名稱。<br/> <br/>                                                |
| [**preferredPrefix**](preferredprefix.md)<br/> | 應對應命名空間的前置詞，讓 XML 更容易讀取。<br/> <br/> |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  preferredPrefix?, 
  macroPrefix?, 
  codeName?, 
  name*
)
```

## <a name="parent-elements"></a>父元素



| 元素                                     | 描述                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | WSDAPI 程式碼產生器 XML 腳本檔的根項目。<br/> <br/> |



## <a name="remarks"></a>備註

這個元素可用來提供程式碼產生器，其中包含在 WSDL 和 XSD 檔案中遇到之命名空間的其他相關資訊，或引進新的命名空間。

由程式碼產生器會自動剖析型別反映所隱含或在 WSDL 和 XSD 檔案中指定的命名空間，而不需要在腳本中明確定義。 在某些情況下，這個專案可以用來將其他屬性或名稱加入至類型反映或 WSDL/XSD 所參考的命名空間。 程式碼產生器不會將此視為衝突。

下列 XML 會顯示命名空間元素 (已省略子系，以求簡潔) 。

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 





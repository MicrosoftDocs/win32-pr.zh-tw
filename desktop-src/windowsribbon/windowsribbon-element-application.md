---
title: Application 項目
description: 表示 Windows 功能區架構標記規格中的最上層元素。
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- 應用程式元素 Windows 功能區
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4055e271ecf3313596b73aa36a5cbea37250416d9b517fb4512b89fbc203293a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810808"
---
# <a name="application-element"></a>Application 項目

表示 Windows 功能區架構標記規格中的最上層元素。

## <a name="usage"></a>使用方式

``` syntax
<Application
  xmlns = "xs:string">
  child elements
</Application>
```

## <a name="attributes"></a>屬性



| 屬性            | 類型                 | 必要       | 描述                                                                                                                                                                                                       |
|----------------------|----------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **xmlns**<br/> | xs:string<br/> | Yes<br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> 功能區標記命名空間系結的 URI。 <br/> </dd> </dl> |



## <a name="child-elements"></a>子元素



| 元素                                                                               | 描述                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [**應用程式。命令**](windowsribbon-element-application-commands.md)<br/> | 最多可能發生一次<br/> <br/>  |
| [**應用程式。 Views**](windowsribbon-element-application-views.md)<br/>       | 必須剛好發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素

沒有父元素。

## <a name="remarks"></a>備註

必要。

必須剛好一次就能作為所有功能區標記的容器。

**應用程式** 元素的子項目必須以指定的順序發生：

1.  [**應用程式。命令**](windowsribbon-element-application-commands.md)
2.  [**應用程式。 Views**](windowsribbon-element-application-views.md)

## <a name="examples"></a>範例

下列範例顯示 **應用程式** 元素宣告。


```XML
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
...
</Application>
```



## <a name="element-information"></a>項目資訊



|                                     |           |
|-------------------------------------|-----------|
| 最低支援系統<br/> | Windows 7 |
| 可以是空的                        | 否        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用功能區標記宣告命令和控制項](windowsribbon-schema.md)
</dt> </dl>

 

 






---
description: 定義 include 元素要重複使用的 text 或 CDATA。
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: 宏元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8759d4afb61883b8bf41472f276882643cfa552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193054"
---
# <a name="macro-element"></a>宏元素

定義 [**include**](include.md) 元素要重複使用的 TEXT 或 CDATA。

## <a name="usage"></a>使用方式

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a>屬性



| 屬性           | 類型                         | 必要       | 描述                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| **name**<br/> | 字元 \_ 字串<br/> | Yes<br/> | 宏的名稱。<br/> <br/> |



## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                     | 描述                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | WSDAPI 程式碼產生器 XML 腳本檔的根項目。<br/> <br/> |



## <a name="remarks"></a>備註

WsdCodeGen 會定義名為 **DoNotModify** 的宏。 包含此宏時，產生的程式碼會包含高可見度的批註區塊，指示開發人員不修改產生的程式碼。

下列 XML 說明如何包含 **DoNotModify** 宏。 您可以將此 XML 新增至 XML 設定檔以進行 WsdCodeGen。

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 





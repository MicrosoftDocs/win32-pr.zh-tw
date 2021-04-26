---
description: 定義 include 元素要重複使用的 text 或 CDATA。
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: 宏元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f794566b0fd789c463d404289644976c8301a2e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994325"
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



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 





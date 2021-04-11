---
description: 在產生的輸出中包含宏或檔案的內容。
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: 包含元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f22cfde339ca218d4cd10525bbca3e57b8d836f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027167"
---
# <a name="include-element"></a>包含元素

在產生的輸出中包含宏或檔案的內容。

## <a name="usage"></a>使用方式

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a>屬性



| 屬性            | 類型                         | 必要      | 描述                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| **file**<br/>  | 字元 \_ 字串<br/> | No<br/> | 要包含之檔案的路徑。<br/> <br/>  |
| **宏觀**<br/> | 字元 \_ 字串<br/> | No<br/> | 要包含的宏名稱。<br/> <br/> |



## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [**檔**](file.md)<br/> | 指示程式碼產生器產生檔案並指定輸出檔名稱。<br/> <br/> |



## <a name="remarks"></a>備註

必須指定 **宏** 屬性或 **檔** 屬性。 請勿同時指定這兩個屬性。

WsdCodeGen 會定義名為 **DoNotModify** 的宏。 包含此宏時，產生的程式碼會包含高可見度的批註區塊，指示開發人員不修改產生的程式碼。

## <a name="examples"></a>範例

下列 XML 說明如何包含 **DoNotModify** 宏。 您可以將此 XML 新增至 XML 設定檔以進行 WsdCodeGen。

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 





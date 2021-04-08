---
description: 針對訊息類型產生 XML 架構資料表的 C 常數宣告。
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: messageTypeDeclarations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 700511d3c0a83badcb15b0e07491a14ade53f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944929"
---
# <a name="messagetypedeclarations-element"></a>messageTypeDeclarations 元素

針對訊息類型產生 XML 架構資料表的 C 常數宣告。

## <a name="usage"></a>使用方式

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                   | 描述                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [**操作**](operation.md)<br/> | 指定要產生程式碼的作業。<br/> <br/>  |
| [**portType**](porttype.md)<br/>   | 指定要產生程式碼的埠類型。<br/> <br/> |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**檔**](file.md)<br/> | 從程式碼產生器輸出檔案。<br/> <br/> |



## <a name="remarks"></a>備註

架構資料表是由埠類型定義所參考。 因此，這個元素通常會在 [**portTypeDefinitions**](porttypedefinitions.md) 元素之前使用。

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 





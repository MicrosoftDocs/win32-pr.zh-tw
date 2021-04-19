---
description: 產生訊息類型的 C 結構定義。
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: messageStructureDefinitions 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8840e4493cb97d33cb0dac8ce1ace97cc1789e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986858"
---
# <a name="messagestructuredefinitions-element"></a>messageStructureDefinitions 元素

產生訊息類型的 C 結構定義。

## <a name="usage"></a>使用方式

``` syntax
<messageStructureDefinitions>
  child elements
</messageStructureDefinitions>
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

訊息結構會由產生的 proxy 和存根程式碼所參考。 此元素用來產生 include 檔案。

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 





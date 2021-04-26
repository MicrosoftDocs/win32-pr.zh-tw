---
description: 產生 QueryInterface、AddRef 和 Release 函數的實作為。
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: IUnknownDefinitions 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb3a4f76145e585411e64c10ea7af922db931846
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995145"
---
# <a name="iunknowndefinitions-element"></a>IUnknownDefinitions 元素

產生 QueryInterface、AddRef 和 Release 函數的實作為。

## <a name="usage"></a>使用方式

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a>屬性



| 屬性                  | 類型                         | 必要       | 描述                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| **proxyClass**<br/>  | 字元 \_ 字串<br/> | Yes<br/> | 執行類別的名稱。<br/> <br/> |
| **refCountVar**<br/> | 字元 \_ 字串<br/> | Yes<br/> | 參考計數變數名稱。<br/> <br/>  |



## <a name="child-elements"></a>子元素



| 元素                                   | 描述                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [**介面**](interface.md)<br/> | QueryInterface 要傳回的介面名稱。<br/> <br/> |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
interface
```

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**檔**](file.md)<br/> | 從程式碼產生器輸出檔案。<br/> <br/> |



## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 否            |



 

 





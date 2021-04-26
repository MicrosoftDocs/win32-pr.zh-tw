---
description: 產生已知類型的 C 結構定義。
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: structDefinitions 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f680db18b06253362f932cc7d34d5b85f7c1b5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996455"
---
# <a name="structdefinitions-element"></a>structDefinitions 元素

產生已知類型的 C 結構定義。

## <a name="usage"></a>使用方式

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**檔**](file.md)<br/> | 從程式碼產生器輸出檔案。<br/> <br/> |



## <a name="remarks"></a>備註

已知類型的結構會由許多產生的程式碼和應用程式程式碼所參考。 此元素用來產生 include 檔案。 這個元素應該會在 [**structDeclarations**](structdeclarations.md) 元素之後發生，以便妥善處理結構之間的參考。

## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 





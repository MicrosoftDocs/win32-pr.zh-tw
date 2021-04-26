---
description: 指定 WSDL 檔案的位置和檔案名。 路徑可以是檔案的絕對路徑或相對路徑，但不能是 URL。
ms.assetid: 0664dcc6-1e71-46cf-9084-1adc84861b52
title: '裝置上 (Web 服務的路徑元素) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48df5a156149f00b8b153ccc0d46d6d2d34a1ce
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994305"
---
# <a name="path-element"></a>path 元素

指定 WSDL 檔案的位置和檔案名。 路徑可以是檔案的絕對路徑或相對路徑，但不能是 URL。

## <a name="usage"></a>使用方式

``` syntax
<path/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                             |
|---------------------------------|-------------------------------------------------------------------------|
| [**Wsdl**](wsdl.md)<br/> | 要針對合約資訊處理的 WSDL 檔案。<br/> <br/> |



## <a name="examples"></a>範例

下列 XML 會顯示有效的 **路徑** 元素。

``` syntax
<path>"..\wsdls\example.wsdl"</path>
```

## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 





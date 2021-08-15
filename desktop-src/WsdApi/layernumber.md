---
description: 定義要產生的程式碼層數目。
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: layerNumber 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 603815fc178cb02df0eeb33e6ad856076b99b8ea582574703078323b36ba1cbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130770"
---
# <a name="layernumber-element"></a>layerNumber 元素

定義要產生的程式碼層數目。

## <a name="usage"></a>使用方式

``` syntax
<layerNumber/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                     | 描述                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | WSDAPI 程式碼產生器 XML 腳本檔的根項目。<br/> <br/> |



## <a name="remarks"></a>備註

在執行時間資料表中，會使用圖層編號來區分另一層程式碼。 WSDAPI 本身會使用產生的程式碼，其層號為0。

通常，這個值會是1，表示產生的程式碼會分層在 WSDAPI 的上方，而不是其他圖層。 在某些情況下，可能會使用較高的數位。 例如，如果有一家公司產生裝置類別的程式碼， (編號層 1) ，則特定硬體廠商可能會想要新增額外的圖層編號第2層。

合法值（除了 WSDAPI 本身的情況以外）會大於0且小於16。

## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 





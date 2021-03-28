---
title: outputtopology
description: 定義鑲嵌的輸出基本類型。
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 917a927ff80d4abe1b6509fd41281992a998c945
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103932819"
---
# <a name="outputtopology"></a>outputtopology

定義鑲嵌的輸出基本類型。


```
outputtopology(X)      
```



## <a name="remarks"></a>備註

X 必須是 [**點**](dx-graphics-hlsl-geometry-shader.md)、 **線條**、 **三角形的 \_ cw** 或 **三角形 \_ ccw** ，而且必須在引號內。 以下是此屬性的有效選項：


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



下列著色器類型支援此屬性：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5屬性](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





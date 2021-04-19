---
description: 定義一組兩個布林值，用於 MeshFaceWraps 範本以定義個別臉部的材質拓撲。 當材質座標 (u，v) 範圍介於0到2（而不是0到1）時，請使用而不是 Boolean2d。
ms.assetid: 0d1755fc-66cb-4372-b9d0-fb320c55d6a7
title: MaterialWrap
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6797719919a4f52421751a5cad008aa8a581089a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972737"
---
# <a name="materialwrap"></a>MaterialWrap

定義一組兩個布林值，用於 [**MeshFaceWraps**](meshfacewraps.md) 範本以定義個別臉部的材質拓撲。 當材質座標 (u，v) 範圍介於0到2（而不是0到1）時，請使用而不是 [**Boolean2d**](boolean2d.md) 。

``` syntax
template MaterialWrap
{
    < 4885ae60-78e8-11cf-8f52-0040333594a3 >
    Boolean u;
    Boolean v;
} 
```

其中：

-   u-布林值。 請參閱 [**布林值**](boolean.md)。
-   v 布林值。 請參閱 [**布林值**](boolean.md)。

> [!Note]  
> 不再使用 [**MeshFaceWraps**](meshfacewraps.md) 範本。

 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 




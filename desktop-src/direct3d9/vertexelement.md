---
description: 描述頂點宣告中的個別頂點元素。
ms.assetid: efe3e98b-938d-4d4c-b790-2b8c8aab0ded
title: VertexElement
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 049511c89b335c0da31a9f41344082c3b818fa0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109329"
---
# <a name="vertexelement"></a>VertexElement

描述頂點宣告中的個別頂點元素。

``` syntax
template VertexElement 
{ 
    < F752461C-1E23-48f6-B9F8-8350850F336F > 
    DWORD Type; 
    DWORD Method; 
    DWORD Usage; 
    DWORD UsageIndex; 
} 
```

其中：

-   類型-頂點資料類型。 請參閱 [**D3DDECLTYPE**](./d3ddecltype.md)。
-   方法鑲嵌處理方法。 請參閱 [**D3DDECLMETHOD**](./d3ddeclmethod.md)。
-   使用方式-端點資料的用途。 請參閱 [**D3DDECLUSAGE**](./d3ddeclusage.md)。
-   UsageIndex-修改使用方式資料。 請參閱 [**D3DDECLUSAGE**](./d3ddeclusage.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)
</dt> </dl>

 

 

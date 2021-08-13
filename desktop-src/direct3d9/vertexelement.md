---
description: 描述頂點宣告中的個別頂點元素。
ms.assetid: efe3e98b-938d-4d4c-b790-2b8c8aab0ded
title: VertexElement
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c2ecef6cfa8c522532599acef1b83343c64edd2b5eca93fe461d8bf8419ada8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518850"
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

 

 

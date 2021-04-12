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
# <a name="vertexelement"></a><span data-ttu-id="5f954-103">VertexElement</span><span class="sxs-lookup"><span data-stu-id="5f954-103">VertexElement</span></span>

<span data-ttu-id="5f954-104">描述頂點宣告中的個別頂點元素。</span><span class="sxs-lookup"><span data-stu-id="5f954-104">Describes an individual vertex element in a vertex declaration.</span></span>

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

<span data-ttu-id="5f954-105">其中：</span><span class="sxs-lookup"><span data-stu-id="5f954-105">Where:</span></span>

-   <span data-ttu-id="5f954-106">類型-頂點資料類型。</span><span class="sxs-lookup"><span data-stu-id="5f954-106">Type - Vertex data type.</span></span> <span data-ttu-id="5f954-107">請參閱 [**D3DDECLTYPE**](./d3ddecltype.md)。</span><span class="sxs-lookup"><span data-stu-id="5f954-107">See [**D3DDECLTYPE**](./d3ddecltype.md).</span></span>
-   <span data-ttu-id="5f954-108">方法鑲嵌處理方法。</span><span class="sxs-lookup"><span data-stu-id="5f954-108">Method - Tessellator processing method.</span></span> <span data-ttu-id="5f954-109">請參閱 [**D3DDECLMETHOD**](./d3ddeclmethod.md)。</span><span class="sxs-lookup"><span data-stu-id="5f954-109">See [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span></span>
-   <span data-ttu-id="5f954-110">使用方式-端點資料的用途。</span><span class="sxs-lookup"><span data-stu-id="5f954-110">Usage - Intended use of the vertex data.</span></span> <span data-ttu-id="5f954-111">請參閱 [**D3DDECLUSAGE**](./d3ddeclusage.md)。</span><span class="sxs-lookup"><span data-stu-id="5f954-111">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>
-   <span data-ttu-id="5f954-112">UsageIndex-修改使用方式資料。</span><span class="sxs-lookup"><span data-stu-id="5f954-112">UsageIndex - Modifies the usage data.</span></span> <span data-ttu-id="5f954-113">請參閱 [**D3DDECLUSAGE**](./d3ddeclusage.md)。</span><span class="sxs-lookup"><span data-stu-id="5f954-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5f954-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f954-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f954-115">範本</span><span class="sxs-lookup"><span data-stu-id="5f954-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[<span data-ttu-id="5f954-116">**D3DVERTEXELEMENT9**</span><span class="sxs-lookup"><span data-stu-id="5f954-116">**D3DVERTEXELEMENT9**</span></span>](d3dvertexelement9.md)
</dt> </dl>

 

 

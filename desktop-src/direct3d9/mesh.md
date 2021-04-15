---
description: 定義簡單的網格。 第一個陣列是頂點的清單，而第二個數組會透過索引至頂點陣列來定義網格的臉部。
ms.assetid: vs|directx_sdk|~\mesh.htm
title: 網狀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced60785a5f013db7fc26e4d203119a160953b65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467436"
---
# <a name="mesh"></a><span data-ttu-id="11cf2-104">網狀</span><span class="sxs-lookup"><span data-stu-id="11cf2-104">Mesh</span></span>

<span data-ttu-id="11cf2-105">定義簡單的網格。</span><span class="sxs-lookup"><span data-stu-id="11cf2-105">Defines a simple mesh.</span></span> <span data-ttu-id="11cf2-106">第一個陣列是頂點的清單，而第二個數組會透過索引至頂點陣列來定義網格的臉部。</span><span class="sxs-lookup"><span data-stu-id="11cf2-106">The first array is a list of vertices, and the second array defines the faces of the mesh by indexing into the vertex array.</span></span>

``` syntax
template Mesh
{
    <3D82AB44-62DA-11CF-AB39-0020AF71E433>
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nFaces;
    array MeshFace faces[nFaces];
    [...]
}
```

<span data-ttu-id="11cf2-107">其中：</span><span class="sxs-lookup"><span data-stu-id="11cf2-107">Where:</span></span>

-   <span data-ttu-id="11cf2-108">nVertices-頂點數目。</span><span class="sxs-lookup"><span data-stu-id="11cf2-108">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="11cf2-109">陣列向量頂點 \[ nVertices \] -頂點的陣列，每個型別向量。</span><span class="sxs-lookup"><span data-stu-id="11cf2-109">array Vector vertices\[nVertices\] - Array of vertices, each of type Vector.</span></span> <span data-ttu-id="11cf2-110">請參閱 [**Vector**](vector.md)。</span><span class="sxs-lookup"><span data-stu-id="11cf2-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="11cf2-111">nFaces-臉部數目。</span><span class="sxs-lookup"><span data-stu-id="11cf2-111">nFaces - Number of faces.</span></span>
-   <span data-ttu-id="11cf2-112">陣列 MeshFace 臉部 \[ nFaces \] -臉部的陣列，每個類型都 MeshFace。</span><span class="sxs-lookup"><span data-stu-id="11cf2-112">array MeshFace faces\[nFaces\] - Array of faces, each of type MeshFace.</span></span> <span data-ttu-id="11cf2-113">請參閱 [**MeshFace**](meshface.md)。</span><span class="sxs-lookup"><span data-stu-id="11cf2-113">See [**MeshFace**](meshface.md).</span></span>
-   <span data-ttu-id="11cf2-114">\[ ... \] -您可以在這裡使用任何的. x 檔案範本。</span><span class="sxs-lookup"><span data-stu-id="11cf2-114">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="11cf2-115">這可讓架構成為可擴充的。</span><span class="sxs-lookup"><span data-stu-id="11cf2-115">This makes the architecture extensible.</span></span> <span data-ttu-id="11cf2-116">通常會使用 [**材質**](material.md)和 [**TextureFilename**](texturefilename.md)範本。</span><span class="sxs-lookup"><span data-stu-id="11cf2-116">[**Material**](material.md) and [**TextureFilename**](texturefilename.md) templates are typically used.</span></span>

## <a name="see-also"></a><span data-ttu-id="11cf2-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11cf2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11cf2-118">範本</span><span class="sxs-lookup"><span data-stu-id="11cf2-118">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 




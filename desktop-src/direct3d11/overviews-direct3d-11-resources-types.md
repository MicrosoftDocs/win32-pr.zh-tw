---
title: 資源類型
description: 本主題說明 Direct3D 10 中的資源類型，以及 Direct3D 11 中的新類型，包括結構化緩衝區和可寫入的材質和緩衝區。
ms.assetid: 9329f260-e806-4d6d-b6d1-3d001fad411a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3df57c5a4f6010df0494b6533a200d70be892e4
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104374315"
---
# <a name="types-of-resources"></a><span data-ttu-id="b53d3-103">資源類型</span><span class="sxs-lookup"><span data-stu-id="b53d3-103">Types of Resources</span></span>

<span data-ttu-id="b53d3-104">資源是在記憶體中的區域，可由 Direct3D 管線存取，它們是您場景的構成要素。</span><span class="sxs-lookup"><span data-stu-id="b53d3-104">Resources are areas in memory that can be accessed by the Direct3D pipeline, they are the building blocks of your scene.</span></span> <span data-ttu-id="b53d3-105">資源包含許多類型的資料，例如 Direct3D 用來填入和轉譯場景的幾何、紋理或著色器資料。</span><span class="sxs-lookup"><span data-stu-id="b53d3-105">Resources contain many types of data such as geometry, textures or shader data that Direct3D uses to populate and render your scene.</span></span> <span data-ttu-id="b53d3-106">本主題說明 Direct3D 10 中的資源類型，以及 Direct3D 11 中的新類型，包括結構化緩衝區和可寫入的材質和緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b53d3-106">This topic describes the types of resources from Direct3D 10, as well as new types in Direct3D 11 including structured buffers and writable textures and buffers.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b53d3-107">Direct3D 11 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="b53d3-107">Differences between Direct3D 11 and Direct3D 10:</span></span><br/> <span data-ttu-id="b53d3-108">Direct3D 11 支援數種新的資源類型，包括：</span><span class="sxs-lookup"><span data-stu-id="b53d3-108">Direct3D 11 supports several new resource types including:</span></span><br/>
<ul>
<li><span data-ttu-id="b53d3-109"><a href="direct3d-11-advanced-stages-cs-resources.md">讀寫緩衝區和紋理</a></span><span class="sxs-lookup"><span data-stu-id="b53d3-109"><a href="direct3d-11-advanced-stages-cs-resources.md">read-write buffers and textures</a></span></span></li>
<li><span data-ttu-id="b53d3-110"><a href="direct3d-11-advanced-stages-cs-resources.md">結構化緩衝區</a></span><span class="sxs-lookup"><span data-stu-id="b53d3-110"><a href="direct3d-11-advanced-stages-cs-resources.md">structured buffers</a></span></span></li>
<li><span data-ttu-id="b53d3-111"><a href="direct3d-11-advanced-stages-cs-resources.md">位元組位址緩衝區</a></span><span class="sxs-lookup"><span data-stu-id="b53d3-111"><a href="direct3d-11-advanced-stages-cs-resources.md">byte-address buffers</a></span></span></li>
<li><span data-ttu-id="b53d3-112"><a href="direct3d-11-advanced-stages-cs-resources.md">附加和使用緩衝區</a></span><span class="sxs-lookup"><span data-stu-id="b53d3-112"><a href="direct3d-11-advanced-stages-cs-resources.md">append and consume buffers</a></span></span></li>
<li><span data-ttu-id="b53d3-113"><a href="direct3d-11-advanced-stages-cs-resources.md">未排序的存取緩衝區或紋理</a></span><span class="sxs-lookup"><span data-stu-id="b53d3-113"><a href="direct3d-11-advanced-stages-cs-resources.md">unordered access buffer or texture</a></span></span></li>
</ul>
<span data-ttu-id="b53d3-114">Direct3D 11.2 支援已 <a href="tiled-resources.md">平平的資源</a>。</span><span class="sxs-lookup"><span data-stu-id="b53d3-114">Direct3D 11.2 supports <a href="tiled-resources.md">tiled resources</a>.</span></span><br/> <span data-ttu-id="b53d3-115">Direct3D 10 和 Direct3D 11 都支援 Direct3D 10 中引進的 <a href="overviews-direct3d-11-resources-buffers-intro.md">緩衝區</a> 和 <a href="overviews-direct3d-11-resources-textures-intro.md">材質</a> 類型。</span><span class="sxs-lookup"><span data-stu-id="b53d3-115">Both Direct3D 10 and Direct3D 11 support the <a href="overviews-direct3d-11-resources-buffers-intro.md">buffer</a> and <a href="overviews-direct3d-11-resources-textures-intro.md">texture</a> types that were introduced in Direct3D 10.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="b53d3-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="b53d3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b53d3-117">資源</span><span class="sxs-lookup"><span data-stu-id="b53d3-117">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 






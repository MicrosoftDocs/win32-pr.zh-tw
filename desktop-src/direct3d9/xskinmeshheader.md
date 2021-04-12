---
description: 此範本只會在包含匯出外觀資訊的網格中，以每個網狀架構為基礎來具現化。 此範本的目的是要提供已匯出之外觀資訊性質的相關資訊。
ms.assetid: 95a4fa45-63d1-4931-9c91-b26807d2b043
title: XSkinMeshHeader
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306f8c183086846fca020040af00b9ccef2665cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385787"
---
# <a name="xskinmeshheader"></a><span data-ttu-id="5e3f6-104">XSkinMeshHeader</span><span class="sxs-lookup"><span data-stu-id="5e3f6-104">XSkinMeshHeader</span></span>

<span data-ttu-id="5e3f6-105">此範本只會在包含匯出外觀資訊的網格中，以每個網狀架構為基礎來具現化。</span><span class="sxs-lookup"><span data-stu-id="5e3f6-105">This template is instantiated on a per-mesh basis only in meshes that contain exported skinning information.</span></span> <span data-ttu-id="5e3f6-106">此範本的目的是要提供已匯出之外觀資訊性質的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5e3f6-106">The purpose of this template is to provide information about the nature of the skinning information that was exported.</span></span>

``` syntax
template XSkinMeshHeader 
{ 
    < 3CF169CE-FF7C-44ab-93C0-F78F62D172E2 >  
    WORD nMaxSkinWeightsPerVertex; 
    WORD nMaxSkinWeightsPerFace; 
    WORD nBones; 
}
```

<span data-ttu-id="5e3f6-107">其中：</span><span class="sxs-lookup"><span data-stu-id="5e3f6-107">Where:</span></span>

-   <span data-ttu-id="5e3f6-108">nMaxSkinWeightsPerVertex-影響網格中頂點的最大轉換數目。</span><span class="sxs-lookup"><span data-stu-id="5e3f6-108">nMaxSkinWeightsPerVertex - Maximum number of transforms that affect a vertex in the mesh.</span></span>
-   <span data-ttu-id="5e3f6-109">nMaxSkinWeightsPerFace-影響任何臉部之三個頂點的唯一轉換數目上限。</span><span class="sxs-lookup"><span data-stu-id="5e3f6-109">nMaxSkinWeightsPerFace - Maximum number of unique transforms that affect the three vertices of any face.</span></span>
-   <span data-ttu-id="5e3f6-110">nBones-影響此網格中頂點的骨骼數目。</span><span class="sxs-lookup"><span data-stu-id="5e3f6-110">nBones - Number of bones that affect vertices in this mesh.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e3f6-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e3f6-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e3f6-112">範本</span><span class="sxs-lookup"><span data-stu-id="5e3f6-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 




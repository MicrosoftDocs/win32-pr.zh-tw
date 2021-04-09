---
description: 您也可以在材質中提供 Alpha。 若要啟用材質 Alpha，請設定擴散材質轉譯狀態，讓執行時間使用材質擴散色彩元件，而不是頂點擴散色彩元件。
ms.assetid: fd477d8f-d838-4a08-a8c6-38678798e0b0
title: " (Direct3D 9 的材質 Alpha) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07ac2c28b497167f7bd742ecd8176b82b61e8f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108393"
---
# <a name="material-alpha-direct3d-9"></a><span data-ttu-id="a6219-104"> (Direct3D 9 的材質 Alpha) </span><span class="sxs-lookup"><span data-stu-id="a6219-104">Material Alpha (Direct3D 9)</span></span>

<span data-ttu-id="a6219-105">您也可以在材質中提供 Alpha。</span><span class="sxs-lookup"><span data-stu-id="a6219-105">Alpha can also be supplied in a material.</span></span> <span data-ttu-id="a6219-106">若要啟用材質 Alpha，請設定擴散材質轉譯狀態，讓執行時間使用材質擴散色彩元件，而不是頂點擴散色彩元件。</span><span class="sxs-lookup"><span data-stu-id="a6219-106">To enable material alpha, set the diffuse material render state so that the runtime will use the material diffuse color components rather than the vertex diffuse color components.</span></span>


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL );
```



<span data-ttu-id="a6219-107">使用 Alpha 值初始化材質，並在繪製前設定材質。</span><span class="sxs-lookup"><span data-stu-id="a6219-107">Initialize the material with an alpha value, and set the material before drawing.</span></span>


```
D3DMATERIAL9 mtrl;
mtrl.Diffuse = mtrl.Ambient = mtrl.Specular = mtrl.Emissive = 
    D3DCOLORVALUE(255,0,0,0.5f)

m_pd3dDevice->SetMaterial(&mtrl);     
```



## <a name="related-topics"></a><span data-ttu-id="a6219-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="a6219-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6219-109">Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="a6219-109">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 




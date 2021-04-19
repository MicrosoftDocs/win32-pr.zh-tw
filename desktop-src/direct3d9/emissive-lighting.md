---
description: 放射光源是以單一字詞描述。
ms.assetid: b6ccf274-a6c5-4b26-8c43-c857c2c24e0f
title: 放射 (Direct3D 9) 的照明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19cb0566d2409fb68e5fbbdca1cc609c31120e95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106966998"
---
# <a name="emissive-lighting-direct3d-9"></a><span data-ttu-id="99475-103">放射 (Direct3D 9) 的照明</span><span class="sxs-lookup"><span data-stu-id="99475-103">Emissive Lighting (Direct3D 9)</span></span>

<span data-ttu-id="99475-104">放射光源是以單一字詞描述。</span><span class="sxs-lookup"><span data-stu-id="99475-104">Emissive lighting is described by a single term.</span></span>

<span data-ttu-id="99475-105">放射光源 = Cₑ</span><span class="sxs-lookup"><span data-stu-id="99475-105">Emissive Lighting = Cₑ</span></span>

<span data-ttu-id="99475-106">其中：</span><span class="sxs-lookup"><span data-stu-id="99475-106">Where:</span></span>



| <span data-ttu-id="99475-107">參數</span><span class="sxs-lookup"><span data-stu-id="99475-107">Parameter</span></span> | <span data-ttu-id="99475-108">預設值</span><span class="sxs-lookup"><span data-stu-id="99475-108">Default value</span></span> | <span data-ttu-id="99475-109">類型</span><span class="sxs-lookup"><span data-stu-id="99475-109">Type</span></span>          | <span data-ttu-id="99475-110">Description</span><span class="sxs-lookup"><span data-stu-id="99475-110">Description</span></span>     |
|-----------|---------------|---------------|-----------------|
| <span data-ttu-id="99475-111">Cₑ</span><span class="sxs-lookup"><span data-stu-id="99475-111">Cₑ</span></span>        | <span data-ttu-id="99475-112">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="99475-112">(0,0,0,0)</span></span>     | <span data-ttu-id="99475-113">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="99475-113">D3DCOLORVALUE</span></span> | <span data-ttu-id="99475-114">放射色彩。</span><span class="sxs-lookup"><span data-stu-id="99475-114">Emissive color.</span></span> |



 

<span data-ttu-id="99475-115">C ₑ的值為：</span><span class="sxs-lookup"><span data-stu-id="99475-115">The value for Cₑ is either:</span></span>

-   <span data-ttu-id="99475-116">頂點 color1 （如果 EMISSIVEMATERIALSOURCE = D3DMCS \_ color1）和第一個頂點色彩是在頂點宣告中提供。</span><span class="sxs-lookup"><span data-stu-id="99475-116">vertex color1, if EMISSIVEMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="99475-117">頂點 color2 （如果 EMISSIVEMATERIALSOURCE = D3DMCS \_ color2），而第二個頂點色彩則是在頂點宣告中提供。</span><span class="sxs-lookup"><span data-stu-id="99475-117">vertex color2, if EMISSIVEMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="99475-118">材質放射色彩</span><span class="sxs-lookup"><span data-stu-id="99475-118">material emissive color</span></span>

> [!Note]  
> <span data-ttu-id="99475-119">如果使用任一個 EMISSIVEMATERIALSOURCE 選項，而且未提供頂點色彩，則會使用材質放射色彩。</span><span class="sxs-lookup"><span data-stu-id="99475-119">If either EMISSIVEMATERIALSOURCE option is used, and the vertex color is not provided, the material emissive color is used.</span></span>

 

## <a name="example"></a><span data-ttu-id="99475-120">範例</span><span class="sxs-lookup"><span data-stu-id="99475-120">Example</span></span>

<span data-ttu-id="99475-121">在此範例中，物件使用場景環境光線和材料環境色彩上色。</span><span class="sxs-lookup"><span data-stu-id="99475-121">In this example, the object is colored using the scene ambient light and a material ambient color.</span></span> <span data-ttu-id="99475-122">程式碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="99475-122">The code is shown below.</span></span>


```
// create material
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );
mtrl.Emissive.r = 0.0f;
mtrl.Emissive.g = 0.75f;
mtrl.Emissive.b = 0.0f;
mtrl.Emissive.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_EMISSIVEMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="99475-123">根據公式，產生的物件頂點色彩為材質色彩。</span><span class="sxs-lookup"><span data-stu-id="99475-123">According to the equation, the resulting color for the object vertices is the material color.</span></span>

<span data-ttu-id="99475-124">下圖顯示材質色彩，也就是綠色。</span><span class="sxs-lookup"><span data-stu-id="99475-124">The following illustration shows the material color, which is green.</span></span> <span data-ttu-id="99475-125">放射光線使用相同色彩照亮所有物件端點。</span><span class="sxs-lookup"><span data-stu-id="99475-125">Emissive light lights all object vertices with the same color.</span></span> <span data-ttu-id="99475-126">其不取決於頂點標準或光線方向。</span><span class="sxs-lookup"><span data-stu-id="99475-126">It is not dependent on the vertex normal or the light direction.</span></span> <span data-ttu-id="99475-127">如此一來，球體看起來像是 2D 圓形，因為物件表面周圍的陰影並無差別。</span><span class="sxs-lookup"><span data-stu-id="99475-127">As a result, the sphere looks like a 2D circle because there is no difference in shading around the surface of the object.</span></span>

![綠色球體圖例](images/lighte.jpg)

<span data-ttu-id="99475-129">下圖顯示在上述範例中，放射光源如何與其他三種類型的燈光混合。</span><span class="sxs-lookup"><span data-stu-id="99475-129">The following illustration shows how the emissive light blends with the other three types of lights, from the previous examples.</span></span> <span data-ttu-id="99475-130">在球體右側，有綠色放射光線和紅色環境光線的混合。</span><span class="sxs-lookup"><span data-stu-id="99475-130">On the right side of the sphere, there is a blend of the green emissive and the red ambient light.</span></span> <span data-ttu-id="99475-131">在球體左側，綠色放射光線與紅色環境和擴散光線混合，產生紅色漸層。</span><span class="sxs-lookup"><span data-stu-id="99475-131">On the left side of the sphere, the green emissive light blends with red ambient and diffuse light producing a red gradient.</span></span> <span data-ttu-id="99475-132">反射強光中心為白色，在反射光線值驟然消失時會產生黃色光環，使得環境、擴散和放射光線值彼此混合而產生黃色。</span><span class="sxs-lookup"><span data-stu-id="99475-132">The specular highlight is white in the center and creates a yellow ring as the specular light value falls off sharply leaving the ambient, diffuse and emissive light values which blend together to make yellow.</span></span>

![有放射光線的綠色球體圖](images/lightadse.jpg)

## <a name="related-topics"></a><span data-ttu-id="99475-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="99475-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99475-135">燈光數學</span><span class="sxs-lookup"><span data-stu-id="99475-135">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 




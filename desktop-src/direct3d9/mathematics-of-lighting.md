---
description: Direct3D 燈光模型涵蓋環境、擴散、反射及發光。
ms.assetid: cf870c89-4be0-4b95-92aa-ec7bcdc6d9dd
title: " (Direct3D 9) 的照明數學"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683e320788d720883702ebfa56941b1a3a5cf090
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467535"
---
# <a name="mathematics-of-lighting-direct3d-9"></a><span data-ttu-id="4a5dd-103"> (Direct3D 9) 的照明數學</span><span class="sxs-lookup"><span data-stu-id="4a5dd-103">Mathematics of Lighting (Direct3D 9)</span></span>

<span data-ttu-id="4a5dd-104">Direct3D 燈光模型涵蓋環境、擴散、反射及發光。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-104">The Direct3D Light Model covers ambient, diffuse, specular, and emissive lighting.</span></span> <span data-ttu-id="4a5dd-105">這個範圍足以因應大範圍的照明情況。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-105">This is enough flexibility to solve a wide range of lighting situations.</span></span> <span data-ttu-id="4a5dd-106">您可以參考場景中的光線總數量作為全球照明，然後使用下列方程式來計算。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-106">You refer to the total amount of light in a scene as the global illumination and compute it using the following equation.</span></span>


```
Global Illumination = Ambient Light + Diffuse Light + Specular Light + Emissive Light 
```



<span data-ttu-id="4a5dd-107">[環境光源 (Direct3D 9) ](ambient-lighting.md) 是固定光源。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-107">[Ambient Lighting (Direct3D 9)](ambient-lighting.md) is constant lighting.</span></span> <span data-ttu-id="4a5dd-108">它在所有方向都是固定的，而且會以相同的方式將物件的所有圖元色彩。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-108">It is constant in all directions and it colors all pixels of an object the same.</span></span> <span data-ttu-id="4a5dd-109">加以計算很快速，但是會讓物件看起來很平板且不真實。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-109">It is fast to calculate but leaves objects looking flat and unrealistic.</span></span> <span data-ttu-id="4a5dd-110">若要瞭解 Direct3D 如何計算環境光源，請參閱 (Direct3D 9) 的環境光源。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-110">To see how ambient lighting is calculated by Direct3D, see Ambient Lighting (Direct3D 9).</span></span>

<span data-ttu-id="4a5dd-111">[擴散光源 (Direct3D 9) ](diffuse-lighting.md) 取決於光線方向和物件介面正常。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-111">[Diffuse Lighting (Direct3D 9)](diffuse-lighting.md) depends on both the light direction and the object surface normal.</span></span> <span data-ttu-id="4a5dd-112">它會因變化光線方向和變化的 surface 數位向量而在物件的表面上有所不同。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-112">It varies across the surface of an object as a result of the changing light direction and the changing surface numeral vector.</span></span> <span data-ttu-id="4a5dd-113">計算擴散光源需要較長時間，因為它改變每個物件頂點，不過使用它的優點是它會遮蔽物件，並提供物件三維 (3D) 深度。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-113">It takes longer to calculate diffuse lighting because it changes for each object vertex, however the benefit of using it is that it shades objects and gives them three-dimensional (3D) depth.</span></span> <span data-ttu-id="4a5dd-114">若要查看如何在 Direct3D 中計算擴散光源，請參閱 (Direct3D 9) 的擴散光源。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-114">To see how diffuse lighting is calculated in Direct3D, see Diffuse Lighting (Direct3D 9).</span></span>

<span data-ttu-id="4a5dd-115">[ (Direct3D 9 的反射光源) ](specular-lighting.md) 識別光碰到物件介面並反映到相機上時所發生的明亮高光。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-115">[Specular Lighting (Direct3D 9)](specular-lighting.md) identifies the bright specular highlights that occur when light hits an object surface and reflects back toward the camera.</span></span> <span data-ttu-id="4a5dd-116">它比擴散燈更密集，並且在物件介面上更快速地下降。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-116">It is more intense than diffuse light and falls off more rapidly across the object surface.</span></span> <span data-ttu-id="4a5dd-117">反射光源比擴散光源需要較長的時間計算，但是使用它的優點是它在物件表面上新增重要細節。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-117">It takes longer to calculate specular lighting than diffuse lighting, however the benefit of using it is that it adds significant detail to a surface.</span></span> <span data-ttu-id="4a5dd-118">若要瞭解如何在 Direct3D 中計算反射光源，請參閱 (Direct3D 9) 的反射光源。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-118">To see how specular lighting is calculated in Direct3D, see Specular Lighting (Direct3D 9).</span></span>

<span data-ttu-id="4a5dd-119">[放射光源 (Direct3D 9) ](emissive-lighting.md) 是由物件發出的淺色;例如，發光。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-119">[Emissive Lighting (Direct3D 9)](emissive-lighting.md) is light that is emitted by an object; for example, a glow.</span></span> <span data-ttu-id="4a5dd-120">若要查看如何在 Direct3D 中計算放射光源，請參閱放射光源 (Direct3D 9) 。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-120">To see how emissive lighting is calculated in Direct3D, see Emissive Lighting (Direct3D 9).</span></span>

<span data-ttu-id="4a5dd-121">可藉由運用每一種類型的光源至 3D 場景來成就實際光源。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-121">Realistic lighting can be accomplished by applying each of these types of lighting to a 3D scene.</span></span> <span data-ttu-id="4a5dd-122">計算環境、放射，擴散元件的值會輸出為擴散頂點色彩，而反射光源元件的值則輸出為反射頂點色彩。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-122">The values calculated for ambient, emissive, and diffuse components are output as the diffuse vertex color; the value for the specular lighting component is output as the specular vertex color.</span></span> <span data-ttu-id="4a5dd-123">環境、擴散及反射光線值可能受到指定光線衰減和聚光燈係數的影響。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-123">Ambient, diffuse, and specular light values can be affected by a given light's attenuation and spotlight factor.</span></span> <span data-ttu-id="4a5dd-124">如需衰減運作方式的詳細資訊，請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-124">For more information about how attenuation works, see [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>

<span data-ttu-id="4a5dd-125">若要完成更多實際照明效果，您可以新增更多光線，不過場景會花較長的時間來呈現。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-125">To achieve a more realistic lighting effect, you add more lights; however, the scene takes longer to render.</span></span> <span data-ttu-id="4a5dd-126">若要取得所有效果設計師的想法，某些遊戲使用比一般常用者更多的 CPU 功率。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-126">To achieve all the effects a designer wants, some games use more CPU power than is commonly available.</span></span> <span data-ttu-id="4a5dd-127">若是如此，通常會將照明計算數目減到最小值，方法是在使用材質貼圖的同時，使用光照貼圖和環境貼圖將光源引入場景。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-127">In this case, it is typical to reduce the number of lighting calculations to a minimum by using lighting maps and environment maps to add lighting to a scene while using texture maps.</span></span>

<span data-ttu-id="4a5dd-128">在相機空間計算光源。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-128">Lighting is computed in the camera space.</span></span> <span data-ttu-id="4a5dd-129">若要查看如何計算光源轉換，請參閱 [ (Direct3D 9) 的相機空間轉換 ](camera-space-transformations.md)。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-129">To see how lighting transformations are calculated, see [Camera Space Transformations (Direct3D 9)](camera-space-transformations.md).</span></span> <span data-ttu-id="4a5dd-130">當特殊條件存在時，可在模型空間中計算優化光源：已正規化標準向量 (D3DRS \_ NORMALIZENORMALS 為 True) 、不需要頂點混色、轉換矩陣為正向等。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-130">Optimized lighting can be computed in model space, when special conditions exist: normal vectors are already normalized (D3DRS\_NORMALIZENORMALS is True), vertex blending is not needed, transformation matrices are orthogonal, and so forth.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a5dd-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="4a5dd-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a5dd-132">燈光和材質</span><span class="sxs-lookup"><span data-stu-id="4a5dd-132">Lights and Materials</span></span>](lights-and-materials.md)
</dt> </dl>

 

 




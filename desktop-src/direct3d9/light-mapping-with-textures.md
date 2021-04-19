---
description: 應用程式要逼真呈現 3D 場景，必須考慮光源效果對場景外觀的影響。
ms.assetid: ff2037e4-2cf6-4247-b93f-13f0078f3b58
title: 使用 (Direct3D 9) 的材質進行淺色對應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5652446562e4c66390d67e11fa624a4a5659b85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972526"
---
# <a name="light-mapping-with-textures-direct3d-9"></a><span data-ttu-id="cc445-103">使用 (Direct3D 9) 的材質進行淺色對應</span><span class="sxs-lookup"><span data-stu-id="cc445-103">Light Mapping with Textures (Direct3D 9)</span></span>

<span data-ttu-id="cc445-104">應用程式要逼真呈現 3D 場景，必須考慮光源效果對場景外觀的影響。</span><span class="sxs-lookup"><span data-stu-id="cc445-104">For an application to realistically render a 3D scene, it must take into account the effect that light sources have on the appearance of the scene.</span></span> <span data-ttu-id="cc445-105">雖然平面和 Gouraud shading 這方面的技術都是難能可貴的工具，但可能無法滿足您的需求。</span><span class="sxs-lookup"><span data-stu-id="cc445-105">Although techniques such as flat and Gouraud shading are valuable tools in this respect, they can be insufficient for your needs.</span></span> <span data-ttu-id="cc445-106">Direct3D 支援物件多重紋理混合。</span><span class="sxs-lookup"><span data-stu-id="cc445-106">Direct3D supports multipass and multiple texture blending.</span></span> <span data-ttu-id="cc445-107">這些功能可讓應用程式的轉譯具有比單獨使用陰影技術呈現的場景更逼真的外觀場景。</span><span class="sxs-lookup"><span data-stu-id="cc445-107">These capabilities enable your application to render scenes with a more realistic appearance than scenes rendered with shading techniques alone.</span></span> <span data-ttu-id="cc445-108">藉由套用一或多個光線對應，您的應用程式可將光線和陰影區域對應到其基本類型。</span><span class="sxs-lookup"><span data-stu-id="cc445-108">By applying one or more light maps, your application can map areas of light and shadow onto its primitives.</span></span>

<span data-ttu-id="cc445-109">光線對應為紋理或紋理群組，其包含 3D 場景中的照明相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cc445-109">A light map is a texture or group of textures that contains information about lighting in a 3D scene.</span></span> <span data-ttu-id="cc445-110">您可以在光線對應 alpha 值或色彩值或兩者中，儲存光源資訊。</span><span class="sxs-lookup"><span data-stu-id="cc445-110">You can store the lighting information in the alpha values of the light map, in the color values, or in both.</span></span>

<span data-ttu-id="cc445-111">如果您使用物件多重紋理混合執行光線對應，您的應用程式應將光線對應轉譯到第一輪基本類型。</span><span class="sxs-lookup"><span data-stu-id="cc445-111">If you implement light mapping using multipass texture blending, your application should render the light map onto its primitives on the first pass.</span></span> <span data-ttu-id="cc445-112">它應該使用第二輪來呈現基底紋理。</span><span class="sxs-lookup"><span data-stu-id="cc445-112">It should use a second pass to render the base texture.</span></span> <span data-ttu-id="cc445-113">例外是反射光線對應。</span><span class="sxs-lookup"><span data-stu-id="cc445-113">The exception to this is specular light mapping.</span></span> <span data-ttu-id="cc445-114">若是如此，第一次呈現基本紋理，接著新增光線對應。</span><span class="sxs-lookup"><span data-stu-id="cc445-114">In that case, render the base texture first; then add the light map.</span></span>

<span data-ttu-id="cc445-115">多個紋理混合可讓應用程式一次呈現光線對應與基本紋理。</span><span class="sxs-lookup"><span data-stu-id="cc445-115">Multiple texture blending enables your application to render the light map and the base texture in one pass.</span></span> <span data-ttu-id="cc445-116">如果使用者的硬體提供多個紋理混合，您的應用程式應該利用它執行光線對應。</span><span class="sxs-lookup"><span data-stu-id="cc445-116">If the user's hardware provides for multiple texture blending, your application should take advantage of it when performing light mapping.</span></span> <span data-ttu-id="cc445-117">這會大幅改善應用程式效能。</span><span class="sxs-lookup"><span data-stu-id="cc445-117">This significantly improves your application's performance.</span></span>

<span data-ttu-id="cc445-118">使用光線對應，當在轉譯基本類型時，Direct3D 應用程式可以獲得各種照明效果。</span><span class="sxs-lookup"><span data-stu-id="cc445-118">Using light maps, a Direct3D application can achieve a variety of lighting effects when it renders primitives.</span></span> <span data-ttu-id="cc445-119">它不僅可以在場景中對應單色及彩色光線，也可以新增細節，例如反射強光，並擴散光源。</span><span class="sxs-lookup"><span data-stu-id="cc445-119">It can map not only monochrome and colored lights in a scene, but it can also add details such as specular highlights and diffuse lighting.</span></span>

<span data-ttu-id="cc445-120">有關使用 Direct3D 紋理混合執行光線對應的資訊，顯示於下列主題中。</span><span class="sxs-lookup"><span data-stu-id="cc445-120">Information on using Direct3D texture blending to perform light mapping is presented in the following topics.</span></span>

-   [<span data-ttu-id="cc445-121"> (Direct3D 9) 的單色燈光地圖 </span><span class="sxs-lookup"><span data-stu-id="cc445-121">Monochrome Light Maps (Direct3D 9)</span></span>](monochrome-light-maps.md)
-   [<span data-ttu-id="cc445-122"> (Direct3D 9) 的色彩淺色地圖 </span><span class="sxs-lookup"><span data-stu-id="cc445-122">Color Light Maps (Direct3D 9)</span></span>](color-light-maps.md)
-   [<span data-ttu-id="cc445-123"> (Direct3D 9) 的鏡面燈光地圖 </span><span class="sxs-lookup"><span data-stu-id="cc445-123">Specular Light Maps (Direct3D 9)</span></span>](specular-light-maps.md)
-   [<span data-ttu-id="cc445-124"> (Direct3D 9) 的擴散燈光地圖 </span><span class="sxs-lookup"><span data-stu-id="cc445-124">Diffuse Light Maps (Direct3D 9)</span></span>](diffuse-light-maps.md)

## <a name="related-topics"></a><span data-ttu-id="cc445-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="cc445-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc445-126">材質混色</span><span class="sxs-lookup"><span data-stu-id="cc445-126">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 




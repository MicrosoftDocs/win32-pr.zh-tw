---
description: 您可以使用 Microsoft Direct3D 來模擬涉及能源的自然現象。
ms.assetid: a16af13d-3a38-42b5-900b-ff58a0c917b2
title: )  (Direct3D 9 的火災、光暈和爆炸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708730bd8e5f198664bb20c11fa98243ac98f0d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687460"
---
# <a name="fire-flares-and-explosions-direct3d-9"></a><span data-ttu-id="a9024-103">)  (Direct3D 9 的火災、光暈和爆炸</span><span class="sxs-lookup"><span data-stu-id="a9024-103">Fire, Flares, and Explosions (Direct3D 9)</span></span>

<span data-ttu-id="a9024-104">您可以使用 Microsoft Direct3D 來模擬涉及能源的自然現象。</span><span class="sxs-lookup"><span data-stu-id="a9024-104">You can use Microsoft Direct3D to simulate natural phenomena involving energy releases.</span></span> <span data-ttu-id="a9024-105">例如，應用程式可以將類似火焰的材質套用至一組公告欄，以產生火災的外觀。</span><span class="sxs-lookup"><span data-stu-id="a9024-105">For instance, an application can generate the appearance of fire by applying flame-like textures to a set of billboards.</span></span> <span data-ttu-id="a9024-106">如果應用程式使用一連串的火材質，以在火災中的每個佈告欄上建立點火的動畫效果，這就特別有效。</span><span class="sxs-lookup"><span data-stu-id="a9024-106">This is especially effective if the application uses a sequence of fire textures to animate the flames on each billboard in the fire.</span></span> <span data-ttu-id="a9024-107">將動畫播放的速度從佈告欄切換至佈告欄會增加實際點火的外觀。</span><span class="sxs-lookup"><span data-stu-id="a9024-107">Varying the speed of the animation playback from billboard to billboard increases the appearance of real flames.</span></span> <span data-ttu-id="a9024-108">混合3D 點火的類似可透過將公告欄上的公告欄和材質分層來達成。</span><span class="sxs-lookup"><span data-stu-id="a9024-108">The semblance of intermingled 3D flames can be achieved by layering the billboards and the textures on the billboards.</span></span>

<span data-ttu-id="a9024-109">您可以藉由將連續亮亮的燈光對應套用至場景中的所有基本型別，來模擬光暈和閃爍。</span><span class="sxs-lookup"><span data-stu-id="a9024-109">You can simulate flares and flashes by applying successively brighter light maps to all primitives in a scene.</span></span> <span data-ttu-id="a9024-110">雖然這是一種計算高度負荷的技術，但它可讓您的應用程式模擬當地語系化的光暈或 flash。</span><span class="sxs-lookup"><span data-stu-id="a9024-110">Although this is a computationally high-overhead technique, it allows your application to simulate a localized flare or flash.</span></span> <span data-ttu-id="a9024-111">也就是說，flare 或 flash 源自的場景部分，會先使其變亮。</span><span class="sxs-lookup"><span data-stu-id="a9024-111">That is, the portion of the scene where the flare or flash originates can brighten first.</span></span>

<span data-ttu-id="a9024-112">另一種方法是在場景前方放置佈告欄，以涵蓋整個轉譯目的地區域。</span><span class="sxs-lookup"><span data-stu-id="a9024-112">Another technique is to position a billboard in front of the scene so that the entire render-target area is covered.</span></span> <span data-ttu-id="a9024-113">應用程式會將連續的 whiter 紋理套用至佈告欄，並隨著時間減少透明度。</span><span class="sxs-lookup"><span data-stu-id="a9024-113">The application applies successively whiter textures to the billboard and decreases the transparency over time.</span></span> <span data-ttu-id="a9024-114">整個場景會隨著時間的推移淡化為白色。</span><span class="sxs-lookup"><span data-stu-id="a9024-114">The entire scene fades to white as time passes.</span></span> <span data-ttu-id="a9024-115">這是建立光暈的低負擔方法。</span><span class="sxs-lookup"><span data-stu-id="a9024-115">This is a low overhead method of creating a flare.</span></span> <span data-ttu-id="a9024-116">不過，使用這項技術時，可能很難從單一點光源來源產生亮閃 flash 的外觀。</span><span class="sxs-lookup"><span data-stu-id="a9024-116">However, using this technique, it can be difficult to generate the appearance of a bright flash from a single point light source.</span></span>

<span data-ttu-id="a9024-117">爆炸可以顯示在類似于引發、閃爍和光暈的3D 場景程式中。</span><span class="sxs-lookup"><span data-stu-id="a9024-117">Explosions can be displayed in a 3D scene procedure similar to those used for fire, flashes, and flares.</span></span> <span data-ttu-id="a9024-118">比方說，您的應用程式可能會使用佈告欄來顯示震動波，並在發生爆炸時增加 plume。</span><span class="sxs-lookup"><span data-stu-id="a9024-118">For instance, your application might use a billboard to display a shock wave and rising plume of smoke when the explosion occurs.</span></span> <span data-ttu-id="a9024-119">同時，您的應用程式可以使用一組公告欄來模擬點火。</span><span class="sxs-lookup"><span data-stu-id="a9024-119">At the same time, your application can use a set of billboards to simulate flames.</span></span> <span data-ttu-id="a9024-120">此外，它也可以將單一佈告欄放置在場景前方，以將燈光的光暈新增至整個場景。</span><span class="sxs-lookup"><span data-stu-id="a9024-120">In addition, it can position a single billboard in front of the scene to add a flare of light to the entire scene.</span></span>

<span data-ttu-id="a9024-121">您可以使用公告欄來模擬能源字形狀。</span><span class="sxs-lookup"><span data-stu-id="a9024-121">Energy beams can be simulated using billboards.</span></span> <span data-ttu-id="a9024-122">您的應用程式也可以使用定義為行清單或換行的基本專案來顯示它們。</span><span class="sxs-lookup"><span data-stu-id="a9024-122">Your application can also display them using primitives that are defined as line lists or line strips.</span></span> <span data-ttu-id="a9024-123">如需詳細資訊，請參閱 [行清單](line-lists.md) 和 [行條紋](line-strips.md)。</span><span class="sxs-lookup"><span data-stu-id="a9024-123">For details, see [Line Lists](line-lists.md) and [Line Strips](line-strips.md).</span></span>

<span data-ttu-id="a9024-124">您的應用程式可以使用定義為三角形清單的公告欄或基本專案來建立強制欄位。</span><span class="sxs-lookup"><span data-stu-id="a9024-124">Your application can create force fields using billboards or primitives defined as triangle lists.</span></span> <span data-ttu-id="a9024-125">若要從三角形清單建立強制欄位，請在三角形清單中定義一組連續的三角形，而這些三角形會在 [強制] 欄位所涵蓋的區域上平均分佈。</span><span class="sxs-lookup"><span data-stu-id="a9024-125">To create a force field from triangle lists, define a set of disjoint triangles in a triangle list equally spaced over the region covered by the force field.</span></span> <span data-ttu-id="a9024-126">三角形之間的間隙可讓使用者查看三角形背後的場景，如您在查看 [force] 欄位時所預期的情況。</span><span class="sxs-lookup"><span data-stu-id="a9024-126">The gaps between the triangles allow the user to see the scene behind the triangles, as you might expect when looking at a force field.</span></span> <span data-ttu-id="a9024-127">將材質套用至三角形清單，讓三角形成為具有能源發光的外觀。</span><span class="sxs-lookup"><span data-stu-id="a9024-127">Apply a texture to the triangle list that gives the triangles the appearance of glowing with energy.</span></span> <span data-ttu-id="a9024-128">如需詳細資訊，請參閱 [三角形清單](triangle-lists.md)。</span><span class="sxs-lookup"><span data-stu-id="a9024-128">For further information, see [Triangle Lists](triangle-lists.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9024-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9024-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9024-130">Alpha 範例</span><span class="sxs-lookup"><span data-stu-id="a9024-130">Alpha Examples</span></span>](alpha-examples.md)
</dt> </dl>

 

 




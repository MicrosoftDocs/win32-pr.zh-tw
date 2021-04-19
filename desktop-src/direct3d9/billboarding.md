---
description: 在建立3D 場景時，應用程式有時會以使其成為3D 物件的方式轉譯2D 物件，以獲得效能優勢。 這是 billboarding 技術背後的基本概念。
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: 'Billboarding (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e287624ef8800f0b66941e826e211d044b7bf27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970740"
---
# <a name="billboarding-direct3d-9"></a><span data-ttu-id="a7d48-104">Billboarding (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="a7d48-104">Billboarding (Direct3D 9)</span></span>

<span data-ttu-id="a7d48-105">在建立3D 場景時，應用程式有時會以使其成為3D 物件的方式轉譯2D 物件，以獲得效能優勢。</span><span class="sxs-lookup"><span data-stu-id="a7d48-105">When creating 3D scenes, an application can sometimes gain performance advantages by rendering 2D objects in a way that makes them appear to be 3D objects.</span></span> <span data-ttu-id="a7d48-106">這是 billboarding 技術背後的基本概念。</span><span class="sxs-lookup"><span data-stu-id="a7d48-106">This is the basic idea behind the technique of billboarding.</span></span>

<span data-ttu-id="a7d48-107">單字正常意義的佈告欄是一種 roadway 的正負號。</span><span class="sxs-lookup"><span data-stu-id="a7d48-107">A billboard in the normal sense of the word is a sign along a roadway.</span></span> <span data-ttu-id="a7d48-108">Microsoft Direct3D 應用程式可以藉由定義矩形實線並對其套用材質，來建立和轉譯這種類型的佈告欄。</span><span class="sxs-lookup"><span data-stu-id="a7d48-108">Microsoft Direct3D applications can create and render this type of billboard by defining a rectangular solid and applying a texture to it.</span></span> <span data-ttu-id="a7d48-109">以更特製化的3D 圖形方式 Billboarding 是此的延伸。</span><span class="sxs-lookup"><span data-stu-id="a7d48-109">Billboarding in the more specialized sense of 3D graphics is an extension of this.</span></span> <span data-ttu-id="a7d48-110">目標是讓2D 物件顯示為3D。</span><span class="sxs-lookup"><span data-stu-id="a7d48-110">The goal is to make 2D objects appear to be 3D.</span></span> <span data-ttu-id="a7d48-111">技術是將包含物件影像的材質套用至矩形基本。</span><span class="sxs-lookup"><span data-stu-id="a7d48-111">The technique is to apply a texture that contains the object's image to a rectangular primitive.</span></span> <span data-ttu-id="a7d48-112">原始物件會旋轉，讓它一律會臉部給使用者。</span><span class="sxs-lookup"><span data-stu-id="a7d48-112">The primitive is rotated so that it always faces the user.</span></span> <span data-ttu-id="a7d48-113">如果物件的影像不是矩形，就不會有任何影響。</span><span class="sxs-lookup"><span data-stu-id="a7d48-113">It doesn't matter if the object's image is not rectangular.</span></span> <span data-ttu-id="a7d48-114">您可以將佈告欄的部分設為透明，所以看不到您不想要看到的佈告欄影像部分。</span><span class="sxs-lookup"><span data-stu-id="a7d48-114">Portions of the billboard can be made transparent, so the parts of the billboard image that you don't want seen are not visible.</span></span>

<span data-ttu-id="a7d48-115">許多遊戲都採用 billboarding 來進行動畫 sprite。</span><span class="sxs-lookup"><span data-stu-id="a7d48-115">Many games employ billboarding for animated sprites.</span></span> <span data-ttu-id="a7d48-116">例如，當使用者透過3D 迷宮移動時，可能會看到可挑選的武器或獎勵。</span><span class="sxs-lookup"><span data-stu-id="a7d48-116">For instance, when the user is moving through a 3D maze, he or she may see weapons or rewards that can be picked up.</span></span> <span data-ttu-id="a7d48-117">這些通常是以矩形為基本的2D 影像。</span><span class="sxs-lookup"><span data-stu-id="a7d48-117">These are typically 2D images textured on a rectangular primitive.</span></span> <span data-ttu-id="a7d48-118">Billboarding 通常會在遊戲中用來呈現樹狀結構、bushes 和雲端的影像。</span><span class="sxs-lookup"><span data-stu-id="a7d48-118">Billboarding is often used in games to render images of trees, bushes, and clouds.</span></span>

<span data-ttu-id="a7d48-119">將影像套用至佈告欄時，必須先旋轉矩形基本型別，使產生的影像臉部給使用者。</span><span class="sxs-lookup"><span data-stu-id="a7d48-119">When an image is applied to a billboard, the rectangular primitive must first be rotated so that the resulting image faces the user.</span></span> <span data-ttu-id="a7d48-120">然後，您的應用程式必須將它轉譯成位置。</span><span class="sxs-lookup"><span data-stu-id="a7d48-120">Your application must then translate it into position.</span></span> <span data-ttu-id="a7d48-121">然後，應用程式可以將材質套用至基本。</span><span class="sxs-lookup"><span data-stu-id="a7d48-121">The application can then apply a texture to the primitive.</span></span>

<span data-ttu-id="a7d48-122">Billboarding 最適用于對稱物件，尤其是沿著垂直軸對稱的物件。</span><span class="sxs-lookup"><span data-stu-id="a7d48-122">Billboarding works best for symmetrical objects, especially objects that are symmetrical along the vertical axis.</span></span> <span data-ttu-id="a7d48-123">這也需要觀點的高度不會增加太多。</span><span class="sxs-lookup"><span data-stu-id="a7d48-123">It also requires that the altitude of the viewpoint doesn't increase too much.</span></span> <span data-ttu-id="a7d48-124">如果允許使用者查看上述的 billboarded，就會很容易看出物件是2D 而非3D。</span><span class="sxs-lookup"><span data-stu-id="a7d48-124">If the user is allowed to view the billboarded from above, it becomes readily apparent that the object is 2D rather than 3D.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7d48-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7d48-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7d48-126">Alpha 範例</span><span class="sxs-lookup"><span data-stu-id="a7d48-126">Alpha Examples</span></span>](alpha-examples.md)
</dt> </dl>

 

 




---
description: 您可以藉由模糊處理物件，並在物件後面留下模糊的物件影像軌跡，以增強3D 場景中物件的感覺速度。 Direct3D 應用程式會針對每個畫面格多次轉譯物件來完成這項工作。
ms.assetid: 8b1a1f0d-5857-4ab4-828c-8ca7c17a4890
title: " (Direct3D 9) 的動作模糊"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fccb5c00d1208041afc31d4afe1cf0c7a5425037
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510141"
---
# <a name="motion-blur-direct3d-9"></a><span data-ttu-id="816ff-104"> (Direct3D 9) 的動作模糊</span><span class="sxs-lookup"><span data-stu-id="816ff-104">Motion Blur (Direct3D 9)</span></span>

<span data-ttu-id="816ff-105">您可以藉由模糊處理物件，並在物件後面留下模糊的物件影像軌跡，以增強3D 場景中物件的感覺速度。</span><span class="sxs-lookup"><span data-stu-id="816ff-105">You can enhance the perceived speed of an object in a 3D scene by blurring the object and leaving a blurred trail of object images behind the object.</span></span> <span data-ttu-id="816ff-106">Direct3D 應用程式會針對每個畫面格多次轉譯物件來完成這項工作。</span><span class="sxs-lookup"><span data-stu-id="816ff-106">Direct3D applications accomplish this by rendering the object multiple times per frame.</span></span>

<span data-ttu-id="816ff-107">回想一下，Direct3D 應用程式通常會將幕後轉譯成螢幕緩衝。</span><span class="sxs-lookup"><span data-stu-id="816ff-107">Recall that Direct3D applications typically render scenes into an off-screen buffer.</span></span> <span data-ttu-id="816ff-108">當應用程式呼叫 IDirect3DDevice9 時，緩衝區的內容會顯示在螢幕上 [**：:P 重發**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) 的方法。</span><span class="sxs-lookup"><span data-stu-id="816ff-108">The contents of the buffer are displayed on the screen when the application calls the [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method.</span></span> <span data-ttu-id="816ff-109">在螢幕上顯示框架之前，您的 Direct3D 應用程式可以將物件多次轉譯成場景。</span><span class="sxs-lookup"><span data-stu-id="816ff-109">Your Direct3D application can render the object multiple times into a scene before it displays the frame on the screen.</span></span>

<span data-ttu-id="816ff-110">以程式設計的方式，您的應用程式會對 DrawPrimitive 方法進行多次呼叫，重複傳遞相同的3D 物件。</span><span class="sxs-lookup"><span data-stu-id="816ff-110">Programmatically, your application makes multiple calls to a DrawPrimitive method, repeatedly passing the same 3D object.</span></span> <span data-ttu-id="816ff-111">在每次呼叫之前，物件的位置會稍微更新，在目標呈現介面上產生一連串模糊的物件影像。</span><span class="sxs-lookup"><span data-stu-id="816ff-111">Before each call, the position of the object is updated slightly, producing a series of blurred object images on the target rendering surface.</span></span> <span data-ttu-id="816ff-112">如果物件有一或多個紋理，您的應用程式可以藉由轉譯物件的第一個影像，使其所有紋理幾乎透明，以增強動畫模糊效果。</span><span class="sxs-lookup"><span data-stu-id="816ff-112">If the object has one or more textures, your application can enhance the motion blur effect by rendering the first image of the object with all its textures nearly transparent.</span></span> <span data-ttu-id="816ff-113">每次物件轉譯時，物件材質的透明度都會減少。</span><span class="sxs-lookup"><span data-stu-id="816ff-113">Each time the object renders, the transparency of the object's texture decreases.</span></span> <span data-ttu-id="816ff-114">當您的應用程式將物件呈現在其最終位置時，它應該會轉譯物件的材質而不會有透明度。</span><span class="sxs-lookup"><span data-stu-id="816ff-114">When your application renders the object in its final position, it should render the object's textures without transparency.</span></span> <span data-ttu-id="816ff-115">例外狀況是，如果您要將動作模糊新增至其他需要材質透明度的效果。</span><span class="sxs-lookup"><span data-stu-id="816ff-115">The exception is if you're adding motion blur to another effect that requires texture transparency.</span></span> <span data-ttu-id="816ff-116">在任何情況下，框架中物件的初始影像都應該是最透明的。</span><span class="sxs-lookup"><span data-stu-id="816ff-116">In any case, the initial image of the object in the frame should be the most transparent.</span></span> <span data-ttu-id="816ff-117">最後的影像應該是最不透明的。</span><span class="sxs-lookup"><span data-stu-id="816ff-117">The final image should be the least transparent.</span></span>

<span data-ttu-id="816ff-118">當您的應用程式將一系列的物件影像轉譯到目標呈現介面上，並呈現場景的其餘部分之後，它應該呼叫 [**IDirect3DDevice9：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) 重新傳送的方法，在螢幕上顯示畫面格。</span><span class="sxs-lookup"><span data-stu-id="816ff-118">After your application renders the series of object images onto the target rendering surface and renders the rest of the scene, it should call the [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method to display the frame on the screen.</span></span>

<span data-ttu-id="816ff-119">如果您的應用程式正在模擬使用者以高速方式在場景中移動的效果，則可以將動態模糊新增至整個場景。</span><span class="sxs-lookup"><span data-stu-id="816ff-119">If your application is simulating the effect of the user moving through a scene at high speed, it can add motion blur to the entire scene.</span></span> <span data-ttu-id="816ff-120">在此情況下，您的應用程式會針對每個畫面格多次呈現整個場景。</span><span class="sxs-lookup"><span data-stu-id="816ff-120">In this case, your application renders the entire scene multiple times per frame.</span></span> <span data-ttu-id="816ff-121">每次呈現場景時，您的應用程式都必須稍微移動觀點。</span><span class="sxs-lookup"><span data-stu-id="816ff-121">Each time the scene renders, your application must move the viewpoint slightly.</span></span> <span data-ttu-id="816ff-122">如果場景高度複雜，使用者可能會看到效能降低，因為加速增加的原因是每個畫面格的場景轉譯數目增加。</span><span class="sxs-lookup"><span data-stu-id="816ff-122">If the scene is highly complex, the user may see a visible performance degradation as acceleration is increased because of the increasing number of scene renderings per frame.</span></span>

## <a name="related-topics"></a><span data-ttu-id="816ff-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="816ff-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="816ff-124">消除鋸齒</span><span class="sxs-lookup"><span data-stu-id="816ff-124">Antialiasing</span></span>](antialiasing.md)
</dt> </dl>

 

 

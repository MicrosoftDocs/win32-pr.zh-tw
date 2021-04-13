---
description: 雖然詞彙寬度和音調通常是非正式使用的，但它們具有非常重要且意義截然不同的意義。 因此，您應該瞭解每個專案的意義，以及如何解讀 Direct3D 用來描述這些值的值。
ms.assetid: 2f99881b-f95d-470f-b14d-8300ad930e2a
title: '寬度與音調 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50d0c8fc49b3bce984e56f7b1a727ed40fee67b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104552079"
---
# <a name="width-vs-pitch-direct3d-9"></a><span data-ttu-id="9aa84-104">寬度與音調 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="9aa84-104">Width vs. Pitch (Direct3D 9)</span></span>

<span data-ttu-id="9aa84-105">雖然詞彙寬度和音調通常是非正式使用的，但它們具有非常重要且意義截然不同的意義。</span><span class="sxs-lookup"><span data-stu-id="9aa84-105">Although the terms width and pitch are often used informally, they have very important, and distinctly different, meanings.</span></span> <span data-ttu-id="9aa84-106">因此，您應該瞭解每個專案的意義，以及如何解讀 Direct3D 用來描述這些值的值。</span><span class="sxs-lookup"><span data-stu-id="9aa84-106">As a result, you should understand the meanings for each, and how to interpret the values that Direct3D uses to describe them.</span></span>

<span data-ttu-id="9aa84-107">Direct3D 使用 [**D3DSURFACE \_ DESC**](d3dsurface-desc.md) 結構來傳送描述介面的資訊。</span><span class="sxs-lookup"><span data-stu-id="9aa84-107">Direct3D uses the [**D3DSURFACE\_DESC**](d3dsurface-desc.md) structure to carry information describing a surface.</span></span> <span data-ttu-id="9aa84-108">除此之外，此結構的定義是要包含表面維度的相關資訊，以及這些維度在記憶體中的表示方式。</span><span class="sxs-lookup"><span data-stu-id="9aa84-108">Among other things, this structure is defined to contain information about a surface's dimensions, as well as how those dimensions are represented in memory.</span></span> <span data-ttu-id="9aa84-109">結構會使用高度和寬度成員來描述介面的邏輯維度。</span><span class="sxs-lookup"><span data-stu-id="9aa84-109">The structure uses the Height and Width members to describe the logical dimensions of the surface.</span></span> <span data-ttu-id="9aa84-110">這兩個成員都是以圖元為單位。</span><span class="sxs-lookup"><span data-stu-id="9aa84-110">Both members are measured in pixels.</span></span> <span data-ttu-id="9aa84-111">因此，640 x 480 表面的高度和寬度值都相同，無論是8位介面或24位 RGB 表面。</span><span class="sxs-lookup"><span data-stu-id="9aa84-111">Therefore, the Height and Width values for a 640 x 480 surface are the same whether it is an 8-bit surface or a 24-bit RGB surface.</span></span>

<span data-ttu-id="9aa84-112">當您使用 [**IDirect3DSurface9：： LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) 方法鎖定介面時，此方法會填入 [**D3DLOCKED \_ RECT**](d3dlocked-rect.md) 結構，其中包含介面的音調和鎖定位的指標。</span><span class="sxs-lookup"><span data-stu-id="9aa84-112">When you lock a surface using the [**IDirect3DSurface9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) method, the method fills in a [**D3DLOCKED\_RECT**](d3dlocked-rect.md) structure that contains the pitch of the surface and a pointer to the locked bits.</span></span> <span data-ttu-id="9aa84-113">螺距成員中的值會描述表面的記憶體音調，也稱為 stride。</span><span class="sxs-lookup"><span data-stu-id="9aa84-113">The value in the Pitch member describes the surface's memory pitch, also called stride.</span></span> <span data-ttu-id="9aa84-114">「音調」是兩個記憶體位址之間的距離（以位元組為單位），代表一個點陣圖線的開頭和下一個點陣圖行的開頭。</span><span class="sxs-lookup"><span data-stu-id="9aa84-114">Pitch is the distance, in bytes, between two memory addresses that represent the beginning of one bitmap line and the beginning of the next bitmap line.</span></span> <span data-ttu-id="9aa84-115">由於音調以位元組為單位來測量，而不是以圖元為單位，因此640x480x8 介面的音調值會與具有相同維度但不同像素格式的介面非常不同。</span><span class="sxs-lookup"><span data-stu-id="9aa84-115">Because pitch is measured in bytes rather than pixels, a 640x480x8 surface has a very different pitch value than a surface with the same dimensions but a different pixel format.</span></span> <span data-ttu-id="9aa84-116">此外，量值有時會反映 Direct3D 已保留為快取的位元組，因此不安全的方式是將該音調的寬度乘以每個圖元的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="9aa84-116">Additionally, the pitch value sometimes reflects bytes that Direct3D has reserved as a cache, so it is not safe to assume that pitch is just the width multiplied by the number of bytes per pixel.</span></span> <span data-ttu-id="9aa84-117">相反地，將寬度和音調的差異視覺化，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="9aa84-117">Rather, visualize the difference between width and pitch as shown in the following diagram.</span></span>

![相同前端緩衝區、背景緩衝區和快取的音調和寬度圖表](images/pitch.png)

<span data-ttu-id="9aa84-119">在此圖中，前端緩衝區和背景緩衝區都是640x480x8，而且快取為384x480x8。</span><span class="sxs-lookup"><span data-stu-id="9aa84-119">In this diagram, the front buffer and back buffer are both 640x480x8, and the cache is 384x480x8.</span></span>

<span data-ttu-id="9aa84-120">直接存取介面時，請小心保持在配置給表面維度的記憶體內，並將任何保留給快取的記憶體保持不變。</span><span class="sxs-lookup"><span data-stu-id="9aa84-120">When accessing surfaces directly, take care to stay within the memory allocated for the dimensions of the surface and stay out of any memory reserved for cache.</span></span> <span data-ttu-id="9aa84-121">此外，當您只鎖定部分的介面時，您必須保持在鎖定介面時所指定的矩形內。</span><span class="sxs-lookup"><span data-stu-id="9aa84-121">Additionally, when you lock only a portion of a surface, you must stay within the rectangle you specify when locking the surface.</span></span> <span data-ttu-id="9aa84-122">若無法遵循這些指導方針，將會產生無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="9aa84-122">Failing to follow these guidelines will have unpredictable results.</span></span> <span data-ttu-id="9aa84-123">直接轉譯成 surface memory 時，請一律使用 [**IDirect3DSurface9：： LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) 方法所傳回的音調。</span><span class="sxs-lookup"><span data-stu-id="9aa84-123">When rendering directly into surface memory, always use the pitch returned by the [**IDirect3DSurface9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) method.</span></span> <span data-ttu-id="9aa84-124">請勿假設只以顯示模式為基礎的音調。</span><span class="sxs-lookup"><span data-stu-id="9aa84-124">Do not assume a pitch based solely on the display mode.</span></span> <span data-ttu-id="9aa84-125">如果您的應用程式適用于某些顯示器介面卡，但在其他情況下看起來很模糊，這可能是問題的原因。</span><span class="sxs-lookup"><span data-stu-id="9aa84-125">If your application works on some display adapters but looks garbled on others, this may be the cause of the problem.</span></span>

<span data-ttu-id="9aa84-126">如需詳細資訊，請參閱 [直接存取 (Direct3D 9) 的介面記憶體 ](accessing-surface-memory-directly.md)。</span><span class="sxs-lookup"><span data-stu-id="9aa84-126">For more information, see [Accessing Surface Memory Directly (Direct3D 9)](accessing-surface-memory-directly.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9aa84-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="9aa84-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9aa84-128">Direct3D 表面</span><span class="sxs-lookup"><span data-stu-id="9aa84-128">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> </dl>

 

 

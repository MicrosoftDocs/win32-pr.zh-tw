---
description: 沒有紋理的基本專案會以其材質所指定的色彩，或以頂點指定的色彩（如果有的話）來呈現。
ms.assetid: 8a7ed4b1-25a1-4984-baea-6e176f0545ea
title: " (Direct3D 9) 的大綱和填滿狀態"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65092fb2e4bfe29ac5e9f9291250a0c78b80626d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973941"
---
# <a name="outline-and-fill-state-direct3d-9"></a><span data-ttu-id="c87f7-103"> (Direct3D 9) 的大綱和填滿狀態</span><span class="sxs-lookup"><span data-stu-id="c87f7-103">Outline and Fill State (Direct3D 9)</span></span>

<span data-ttu-id="c87f7-104">沒有紋理的基本專案會以其材質所指定的色彩，或以頂點指定的色彩（如果有的話）來呈現。</span><span class="sxs-lookup"><span data-stu-id="c87f7-104">Primitives that have no textures are rendered with the color specified by their material, or with the colors specified for the vertices, if any.</span></span> <span data-ttu-id="c87f7-105">您可以藉由指定 D3DRS FILLMODE 轉譯狀態的 [**D3DFILLMODE**](./d3dfillmode.md) 列舉類型所定義的值，來選取要填入的方法 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c87f7-105">You can select the method to fill them by specifying a value defined by the [**D3DFILLMODE**](./d3dfillmode.md) enumerated type for the D3DRS\_FILLMODE render state.</span></span>

<span data-ttu-id="c87f7-106">若要啟用遞色，您的應用程式必須傳遞 D3DRS \_ DITHERENABLE 列舉值做為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)的第一個參數。</span><span class="sxs-lookup"><span data-stu-id="c87f7-106">To enable dithering, your application must pass the D3DRS\_DITHERENABLE enumerated value as the first parameter to [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span> <span data-ttu-id="c87f7-107">它必須將第二個參數設定為 **TRUE** 以啟用遞色，而 **FALSE** 則會停用。</span><span class="sxs-lookup"><span data-stu-id="c87f7-107">It must set the second parameter to **TRUE** to enable dithering, and **FALSE** to disable it.</span></span>

<span data-ttu-id="c87f7-108">有時候，繪製線條的最後一個圖元可能會使周圍的基本專案發生不美觀的重迭。</span><span class="sxs-lookup"><span data-stu-id="c87f7-108">At times, drawing the last pixel in a line can cause unsightly overlap with surrounding primitives.</span></span> <span data-ttu-id="c87f7-109">您可以使用 D3DRS LASTPIXEL 列舉值來控制這一點 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c87f7-109">You can control this using the D3DRS\_LASTPIXEL enumerated value.</span></span> <span data-ttu-id="c87f7-110">不過，請勿變更此設定，而不需要一些深謀遠慮。</span><span class="sxs-lookup"><span data-stu-id="c87f7-110">However, do not alter this setting without some forethought.</span></span> <span data-ttu-id="c87f7-111">在某些情況下，隱藏最後圖元的轉譯可能會導致基本專案之間的間距不美觀。</span><span class="sxs-lookup"><span data-stu-id="c87f7-111">Under some conditions, suppressing the rendering of the last pixel can cause unsightly gaps between primitives.</span></span>

<span data-ttu-id="c87f7-112">您可以藉由設定適當的線條繪圖模式來繪製物件大綱。</span><span class="sxs-lookup"><span data-stu-id="c87f7-112">Object outlines can be drawn by setting the appropriate line drawing pattern.</span></span> <span data-ttu-id="c87f7-113">預設的線條繪製狀態是繪製實線。</span><span class="sxs-lookup"><span data-stu-id="c87f7-113">The default line drawing state is to draw solid lines.</span></span> <span data-ttu-id="c87f7-114">如需詳細資訊，請參閱 [D3DX 中的線條繪圖支援 (Direct3D 9) ](line-drawing-support-in-d3dx.md) 轉譯狀態。</span><span class="sxs-lookup"><span data-stu-id="c87f7-114">For more information, see [Line Drawing Support in D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) render state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c87f7-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="c87f7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c87f7-116">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="c87f7-116">Render States</span></span>](render-states.md)
</dt> </dl>

 

 

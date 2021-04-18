---
description: 深度緩衝是移除隱藏行和表面的方法。 根據預設，Direct3D 不會使用深度緩衝。
ms.assetid: 03795e4e-1daa-48e3-8724-8dd4b5187edc
title: ) 的深度緩衝狀態 (Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e632d3dfe6eebd54970c59ef6a666cfcb0950fcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467650"
---
# <a name="depth-buffering-state-direct3d-9"></a><span data-ttu-id="c3009-104">) 的深度緩衝狀態 (Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="c3009-104">Depth Buffering State (Direct3D 9)</span></span>

<span data-ttu-id="c3009-105">深度緩衝是移除隱藏行和表面的方法。</span><span class="sxs-lookup"><span data-stu-id="c3009-105">Depth buffering is a method of removing hidden lines and surfaces.</span></span> <span data-ttu-id="c3009-106">根據預設，Direct3D 不會使用深度緩衝。</span><span class="sxs-lookup"><span data-stu-id="c3009-106">By default, Direct3D does not use depth buffering.</span></span>

<span data-ttu-id="c3009-107">如需深度緩衝區的概念總覽，請參閱 [ (Direct3D 9) 的深度緩衝區 ](depth-buffers.md)。</span><span class="sxs-lookup"><span data-stu-id="c3009-107">For a conceptual overview of depth buffers, see [Depth Buffers (Direct3D 9)](depth-buffers.md).</span></span>

<span data-ttu-id="c3009-108">C + + 應用程式會 \_ 使用 [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) 列舉的成員指定新的狀態值，以 D3DRS ZENABLE 轉譯狀態來更新深度緩衝狀態。</span><span class="sxs-lookup"><span data-stu-id="c3009-108">C++ applications update the depth-buffering state with the D3DRS\_ZENABLE render state, using a member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumeration to specify the new state value.</span></span>

<span data-ttu-id="c3009-109">如果您的應用程式需要防止 Direct3D 寫入深度緩衝區，它可以使用 D3DRS \_ ZWRITEENABLE 列舉值，指定 D3DZB \_ FALSE 做為呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)的第二個參數。</span><span class="sxs-lookup"><span data-stu-id="c3009-109">If your application needs to prevent Direct3D from writing to the depth buffer, it can use the D3DRS\_ZWRITEENABLE enumerated value, specifying D3DZB\_FALSE as the second parameter for the call to [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span>

<span data-ttu-id="c3009-110">下列程式碼範例示範如何將深度緩衝區狀態設定為啟用 z 緩衝。</span><span class="sxs-lookup"><span data-stu-id="c3009-110">The following code example shows how the depth-buffer state is set to enable z-buffering.</span></span>


```
// This code example assumes that d3dDevice is a 
// valid pointer to an IDirect3DDevice9 interface.
// Enable z-buffering.
d3dDevice->SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
```



<span data-ttu-id="c3009-111">您的應用程式也可以使用 D3DRS \_ ZFUNC 轉譯狀態，來控制 Direct3D 在執行深度緩衝時所使用的比較函數。</span><span class="sxs-lookup"><span data-stu-id="c3009-111">Your application can also use the D3DRS\_ZFUNC render state to control the comparison function that Direct3D uses when performing depth buffering.</span></span>

<span data-ttu-id="c3009-112">Z-偏差是在另一個表面上顯示一個表面的方法，即使它們的深度值相同也一樣。</span><span class="sxs-lookup"><span data-stu-id="c3009-112">Z-biasing is a method of displaying one surface in front of another, even if their depth values are the same.</span></span> <span data-ttu-id="c3009-113">您可以將這項技術用於各種效果。</span><span class="sxs-lookup"><span data-stu-id="c3009-113">You can use this technique for a variety of effects.</span></span> <span data-ttu-id="c3009-114">常見的範例是在牆上呈現陰影。</span><span class="sxs-lookup"><span data-stu-id="c3009-114">A common example is rendering shadows on walls.</span></span> <span data-ttu-id="c3009-115">陰影和牆都有相同的深度值。</span><span class="sxs-lookup"><span data-stu-id="c3009-115">Both the shadow and the wall have the same depth value.</span></span> <span data-ttu-id="c3009-116">不過，您想要讓應用程式顯示牆上的陰影。</span><span class="sxs-lookup"><span data-stu-id="c3009-116">However, you want your application to show the shadow on the wall.</span></span> <span data-ttu-id="c3009-117">對陰影提供 z 偏差，讓 Direct3D 適當地顯示 (請參閱 D3DRS \_ DEPTHBIAS) 。</span><span class="sxs-lookup"><span data-stu-id="c3009-117">Giving a z-bias to the shadow makes Direct3D display them properly (see D3DRS\_DEPTHBIAS).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3009-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="c3009-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3009-119">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="c3009-119">Render States</span></span>](render-states.md)
</dt> </dl>

 

 

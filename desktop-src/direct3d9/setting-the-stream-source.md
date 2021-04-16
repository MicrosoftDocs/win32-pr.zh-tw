---
description: IDirect3DDevice9：： SetStreamSource 方法會將頂點緩衝區系結至裝置資料流程，建立頂點資料與饋送基本處理函式的數個數據流埠之一之間的關聯。
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: '設定串流來源 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d0c296b79d258be6eee2d683979081673d5d04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510139"
---
# <a name="setting-the-stream-source-direct3d-9"></a><span data-ttu-id="118d1-103">設定串流來源 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="118d1-103">Setting the Stream Source (Direct3D 9)</span></span>

<span data-ttu-id="118d1-104">[**IDirect3DDevice9：： SetStreamSource**](/windows/desktop/api)方法會將頂點緩衝區系結至裝置資料流程，建立頂點資料與饋送基本處理函式的數個數據流埠之一之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="118d1-104">The [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) method binds a vertex buffer to a device data stream, creating an association between the vertex data and one of several data stream ports that feed the primitive processing functions.</span></span> <span data-ttu-id="118d1-105">在呼叫 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)之類的繪圖方法之前，不會發生資料流程資料的實際參考。</span><span class="sxs-lookup"><span data-stu-id="118d1-105">The actual references to the stream data do not occur until a drawing method, such as [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), is called.</span></span>

<span data-ttu-id="118d1-106">資料流程定義為元件資料的統一陣列，其中每個元件都包含一個或多個代表單一實體的元素，例如位置、正常、色彩等等。</span><span class="sxs-lookup"><span data-stu-id="118d1-106">A stream is defined as a uniform array of component data, where each component consists of one or more elements representing a single entity such as position, normal, color, and so on.</span></span> <span data-ttu-id="118d1-107">Stride 參數指定元件的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="118d1-107">The Stride parameter specifies the size of the component, in bytes.</span></span>

<span data-ttu-id="118d1-108">下列程式碼示範如何設定資料流程來源和繪製其內容。</span><span class="sxs-lookup"><span data-stu-id="118d1-108">The following code demonstrates setting the stream source and drawing its contents.</span></span> <span data-ttu-id="118d1-109">G \_ pVB 變數是包含頂點資料的 LPDIRECT3DVERTEXBUFFER9。</span><span class="sxs-lookup"><span data-stu-id="118d1-109">The g\_pVB variable is a LPDIRECT3DVERTEXBUFFER9 that contains vertex data.</span></span>


```
if( SUCCEEDED( g_pd3dDevice->BeginScene() ) )
{
    // Setup the world, view, and projection matrices
    SetupMatrices();

    // Render the vertex buffer contents
    g_pd3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
    g_pd3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
    g_pd3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 1 );

    // End the scene
    g_pd3dDevice->EndScene();
}
```



<span data-ttu-id="118d1-110">如需此程式碼的詳細資訊，請參閱下列教學課程： [教學課程3：使用矩陣](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="118d1-110">For more information about this code see the following tutorial: [Tutorial 3: Using Matrices](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)</span></span>

## <a name="related-topics"></a><span data-ttu-id="118d1-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="118d1-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="118d1-112">呈現基本專案</span><span class="sxs-lookup"><span data-stu-id="118d1-112">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 

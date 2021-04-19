---
description: 除了透過 Direct3DDevice 物件所擁有和操作的交換鏈之外，應用程式也可以使用 IDirect3DDevice9：： CreateAdditionalSwapChain 方法來建立額外的交換鏈，以顯示來自相同裝置的多個視圖。
ms.assetid: f0d01dfb-d1de-4d16-8c64-4ae56d7fed06
title: '視窗模式中的多個視圖 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed750472d1816c0365298630cfb426982743b11a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970284"
---
# <a name="multiple-views-in-windowed-mode-direct3d-9"></a><span data-ttu-id="3d147-103">視窗模式中的多個視圖 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="3d147-103">Multiple Views in Windowed Mode (Direct3D 9)</span></span>

<span data-ttu-id="3d147-104">除了透過 Direct3DDevice 物件所擁有和操作的交換鏈之外，應用程式也可以使用 [**IDirect3DDevice9：： CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) 方法來建立額外的交換鏈，以顯示來自相同裝置的多個視圖。</span><span class="sxs-lookup"><span data-stu-id="3d147-104">In addition to the swap chain that is owned and manipulated through the Direct3DDevice object, an application can use the [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) method to create additional swap chains to present multiple views from the same device.</span></span>

<span data-ttu-id="3d147-105">一般而言，應用程式會為每個視圖建立一個交換鏈，並將每個交換鏈與特定的視圖產生關聯。</span><span class="sxs-lookup"><span data-stu-id="3d147-105">Typically, the application creates one swap chain per view, and it associates each swap chain with a particular view.</span></span> <span data-ttu-id="3d147-106">應用程式會在每個交換鏈的後置緩衝區中轉譯影像，然後使用 [**IDirect3DDevice9：:P 重發**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) 的方法來個別呈現這些影像。</span><span class="sxs-lookup"><span data-stu-id="3d147-106">The application renders images in the back buffers of each swap chain, and then uses the [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method to present them individually.</span></span> <span data-ttu-id="3d147-107">請注意，每個介面卡上一次只能有一個可全螢幕的交換鏈。</span><span class="sxs-lookup"><span data-stu-id="3d147-107">Note that only one swap chain at a time can be full-screen on each adapter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d147-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="3d147-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d147-109">呈現場景</span><span class="sxs-lookup"><span data-stu-id="3d147-109">Presenting a Scene</span></span>](presenting-a-scene.md)
</dt> </dl>

 

 

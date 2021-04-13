---
description: 除了透過 IDirect3DDevice9 介面所擁有和操作的交換鏈之外，應用程式也可以建立額外的交換鏈，以顯示來自相同裝置的多個視圖。
ms.assetid: 4fc09b9c-7adb-4f5d-80e0-2d39bc10420e
title: '以視窗模式呈現多個視圖 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 039b02c487e06c7464dc8163c719371dc2b23706
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510353"
---
# <a name="presenting-multiple-views-in-windowed-mode-direct3d-9"></a><span data-ttu-id="3fc53-103">以視窗模式呈現多個視圖 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="3fc53-103">Presenting Multiple Views in Windowed Mode (Direct3D 9)</span></span>

<span data-ttu-id="3fc53-104">除了透過 [**IDirect3DDevice9**](/windows/desktop/api) 介面所擁有和操作的交換鏈之外，應用程式也可以建立額外的交換鏈，以顯示來自相同裝置的多個視圖。</span><span class="sxs-lookup"><span data-stu-id="3fc53-104">In addition to the swap chain that is owned and manipulated through the [**IDirect3DDevice9**](/windows/desktop/api) interface, an application can create additional swap chains in order to present multiple views from the same device.</span></span> <span data-ttu-id="3fc53-105">應用程式通常會使用 [**IDirect3DDevice9：： CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) 方法為每個視圖建立一個交換鏈，並將每個交換鏈與特定的視窗產生關聯。</span><span class="sxs-lookup"><span data-stu-id="3fc53-105">The application typically creates one swap chain per view by using the [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) method, and associates each swap chain with a particular window.</span></span> <span data-ttu-id="3fc53-106">應用程式會將影像轉譯為每個交換鏈的後置緩衝區，然後個別呈現。</span><span class="sxs-lookup"><span data-stu-id="3fc53-106">The application renders images into the back buffers of each swap chain, and then presents them individually.</span></span>

<span data-ttu-id="3fc53-107">每個介面卡一次只能有一個全螢幕的交換鏈。</span><span class="sxs-lookup"><span data-stu-id="3fc53-107">Only one swap chain at a time can be full-screen on each adapter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fc53-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="3fc53-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fc53-109">程式設計秘訣</span><span class="sxs-lookup"><span data-stu-id="3fc53-109">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 

---
description: Direct3D 提供下列功能來判斷硬體支援。
ms.assetid: 63afa799-2c2c-432c-993e-dca8f7433d59
title: 判斷 (Direct3D 9) 的硬體支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4fbc04343ede671d009054ac3782bbf2563109
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971927"
---
# <a name="determining-hardware-support-direct3d-9"></a><span data-ttu-id="3d011-103">判斷 (Direct3D 9) 的硬體支援</span><span class="sxs-lookup"><span data-stu-id="3d011-103">Determining Hardware Support (Direct3D 9)</span></span>

<span data-ttu-id="3d011-104">Direct3D 提供下列功能來判斷硬體支援。</span><span class="sxs-lookup"><span data-stu-id="3d011-104">Direct3D provides the following functions to determine hardware support.</span></span>

-   [<span data-ttu-id="3d011-105">**IDirect3D9::CheckDeviceFormat**</span><span class="sxs-lookup"><span data-stu-id="3d011-105">**IDirect3D9::CheckDeviceFormat**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

    <span data-ttu-id="3d011-106">用來驗證介面格式是否可作為材質、表面格式是否可作為材質和轉譯目標，或是介面格式是否可做為深度樣板緩衝區來使用。</span><span class="sxs-lookup"><span data-stu-id="3d011-106">Used to verify whether a surface format can be used as a texture, whether a surface format can be used as a texture and a render target, or whether a surface format can be used as a depth-stencil buffer.</span></span> <span data-ttu-id="3d011-107">此外，這個方法是用來驗證深度緩衝區格式支援和深度樣板緩衝區格式支援。</span><span class="sxs-lookup"><span data-stu-id="3d011-107">In addition, this method is used to verify depth buffer format support and depth-stencil buffer format support.</span></span>

-   [<span data-ttu-id="3d011-108">**IDirect3D9::CheckDeviceType**</span><span class="sxs-lookup"><span data-stu-id="3d011-108">**IDirect3D9::CheckDeviceType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)

    <span data-ttu-id="3d011-109">用來確認裝置是否能夠執行硬體加速、裝置是否能夠建立簡報的交換鏈，或可轉譯為目前顯示格式的裝置功能。</span><span class="sxs-lookup"><span data-stu-id="3d011-109">Used to verify a device's ability to perform hardware acceleration, a device's ability to build a swap chain for presentation, or a device's ability to render to the current display format.</span></span>

-   [<span data-ttu-id="3d011-110">**IDirect3D9::CheckDepthStencilMatch**</span><span class="sxs-lookup"><span data-stu-id="3d011-110">**IDirect3D9::CheckDepthStencilMatch**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch)

    <span data-ttu-id="3d011-111">用來驗證深度樣板緩衝區格式是否與轉譯目標格式相容。</span><span class="sxs-lookup"><span data-stu-id="3d011-111">Used to verify whether a depth-stencil buffer format is compatible with a render-target format.</span></span> <span data-ttu-id="3d011-112">請注意，在呼叫這個方法之前，應用程式應該在深度樣板和轉譯目標格式上呼叫 [**IDirect3D9：： CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) 。</span><span class="sxs-lookup"><span data-stu-id="3d011-112">Note that before calling this method, the application should call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) on both the depth-stencil and render-target formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d011-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="3d011-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d011-114">Direct3D 裝置</span><span class="sxs-lookup"><span data-stu-id="3d011-114">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 

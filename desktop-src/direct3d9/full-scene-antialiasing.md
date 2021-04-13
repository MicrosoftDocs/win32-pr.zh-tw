---
description: 全場景消除鋸齒指的是將場景中每個多邊形的邊緣模糊，因為它在單一階段中會進行柵格化;不需要第二次傳遞。
ms.assetid: b57974ab-5654-412d-ae59-58f67a88c121
title: 'Full-Scene 的消除鋸齒 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73d559c4b4fec060efbff7468ee29e6c83b64c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509889"
---
# <a name="full-scene-antialiasing-direct3d-9"></a><span data-ttu-id="8b7bf-103">Full-Scene 的消除鋸齒 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="8b7bf-103">Full-Scene Antialiasing (Direct3D 9)</span></span>

<span data-ttu-id="8b7bf-104">全場景消除鋸齒指的是將場景中每個多邊形的邊緣模糊，因為它在單一階段中會進行柵格化;不需要第二次傳遞。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-104">Full-scene antialiasing refers to blurring the edges of each polygon in the scene as it is rasterized in a single pass; no second pass is required.</span></span> <span data-ttu-id="8b7bf-105">全場景消除鋸齒在支援時，只會影響三角形和三角形的群組。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-105">Full-scene antialiasing, when supported, affects only triangles and groups of triangles.</span></span> <span data-ttu-id="8b7bf-106">使用 Direct3D 服務無法消除鋸齒的程式碼。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-106">Lines cannot be antialiased by using Direct3D services.</span></span> <span data-ttu-id="8b7bf-107">全場景消除鋸齒是在 Direct3D 中使用每個圖元上的交叉取樣來完成。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-107">Full-scene antialiasing is done in Direct3D by using multisampling on each pixel.</span></span> <span data-ttu-id="8b7bf-108">啟用取樣時，圖元的所有 subsamples 會在一個階段中更新，但用於牽涉到多個轉譯行程的其他效果時，應用程式可以指定只有某些 subsamples 會受到給定轉譯傳遞的影響。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-108">When multisampling is enabled, all subsamples of a pixel are updated in one pass but when used for other effects that involve multiple rendering passes, the application can specify that only some subsamples are to be affected by a given rendering pass.</span></span> <span data-ttu-id="8b7bf-109">第二種方法可模擬動作模糊、欄位深度焦點效果、反映模糊等等。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-109">This latter approach enables simulation of motion blur, depth-of-field focus effects, reflection blur, and so on.</span></span>

<span data-ttu-id="8b7bf-110">在這兩種情況下，為每個圖元記錄的各種樣本會混合在一起，並輸出到畫面。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-110">In both cases, the various samples recorded for each pixel are blended together and output to the screen.</span></span> <span data-ttu-id="8b7bf-111">這可改善消除鋸齒或其他效果的影像品質。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-111">This enables the improved image quality of antialiasing or other effects.</span></span>

<span data-ttu-id="8b7bf-112">使用 [**IDirect3D9：： CreateDevice**](/windows/desktop/api) 方法建立裝置之前，您必須先判斷是否支援全場景消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-112">Before creating a device with the [**IDirect3D9::CreateDevice**](/windows/desktop/api) method, you need to determine if full-scene antialiasing is supported.</span></span> <span data-ttu-id="8b7bf-113">若要這麼做，請呼叫 [**IDirect3D9：： CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) 方法，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-113">Do this by calling the [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) method as shown in the code example below.</span></span>


```
/*
* The code below assumes that pD3D is a valid pointer 
*   to a IDirect3D9 interface.
*/

if( SUCCEEDED(pD3D->CheckDeviceMultiSampleType( D3DADAPTER_DEFAULT, 
                    D3DDEVTYPE_HAL , D3DFMT_R8G8B8, FALSE, 
                    D3DMULTISAMPLE_2_SAMPLES, NULL ) ) )
// Full-scene antialiasing is supported. Enable it here.
```



<span data-ttu-id="8b7bf-114">[**IDirect3D9：： CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)所接受的第一個參數是表示要查詢之顯示配接器的序號。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-114">The first parameter that [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) accepts is an ordinal number that denotes the display adapter to query.</span></span> <span data-ttu-id="8b7bf-115">此範例使用 D3DADAPTER \_ 預設值來指定主顯示器介面卡。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-115">This sample uses D3DADAPTER\_DEFAULT to specify the primary display adapter.</span></span> <span data-ttu-id="8b7bf-116">第二個參數是 [**D3DDEVTYPE**](./d3ddevtype.md) 列舉型別中的值，指定裝置類型。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-116">The second parameter is a value from the [**D3DDEVTYPE**](./d3ddevtype.md) enumerated type, specifying the device type.</span></span> <span data-ttu-id="8b7bf-117">第三個參數指定介面的格式。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-117">The third parameter specifies the format of the surface.</span></span> <span data-ttu-id="8b7bf-118">第四個參數會告訴 Direct3D 是否 (**TRUE**) 或全場景消除鋸齒 (**FALSE**) 。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-118">The fourth parameter tells Direct3D whether to inquire about full-windowed multisampling (**TRUE**) or full-scene antialiasing (**FALSE**).</span></span> <span data-ttu-id="8b7bf-119">此範例會使用 **FALSE** 來告訴 Direct3D，它會詢問如何進行全場景消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-119">This sample uses **FALSE** to tell Direct3D that it is inquiring about full-scene antialiasing.</span></span> <span data-ttu-id="8b7bf-120">最後一個參數指定您想要測試的取樣技巧。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-120">The last parameter specifies the multisampling technique that you want to test.</span></span> <span data-ttu-id="8b7bf-121">使用 [**D3DMULTISAMPLE \_ 型**](./d3dmultisample-type.md) 別列舉型別中的值。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-121">Use a value from the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="8b7bf-122">此範例會測試是否支援兩種層級的取樣。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-122">This sample tests to see if two levels of multisampling are supported.</span></span>

<span data-ttu-id="8b7bf-123">如果裝置支援您要使用的取樣層級，則下一個步驟是藉由填入 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md) 結構的適當成員來設定呈現參數，以建立多重程式呈現介面。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-123">If the device supports the level of multisampling that you want to use, the next step is to set the presentation parameters by filling in the appropriate members of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure to create a multisample rendering surface.</span></span> <span data-ttu-id="8b7bf-124">之後，您就可以建立裝置。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-124">After that, you can create the device.</span></span> <span data-ttu-id="8b7bf-125">下列範例程式碼顯示如何使用多取樣轉譯介面來設定裝置。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-125">The sample code below shows how to set up a device with a multisampling render surface.</span></span>


```
/*
* The example below assumes that pD3D is a valid pointer 
* to a IDirect3D9 interface, d3dDevice is a pointer to a 
* IDirect3DDevice9 interface, and hWnd is a valid handle
* to a window.
*/

D3DPRESENT_PARAMETER d3dPP
ZeroMemory( &d3dPP, sizeof( d3dPP ) );
d3dPP.Windowed        = FALSE
d3dPP.SwapEffect      = D3DSWAPEFFECT_DISCARD;
d3dPP.MultiSampleType = D3DMULTISAMPLE_2_SAMPLES;
pD3D->CreateDevice(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                    &d3dpp, &d3dDevice)
```



<span data-ttu-id="8b7bf-126">若要使用取樣，必須將 D3DPRESENT 參數的 SwapEffect 成員 \_ 設定為 D3DSWAPEFFECT \_ 捨棄。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-126">To use multisampling, the SwapEffect member of D3DPRESENT\_PARAMETER must be set to D3DSWAPEFFECT\_DISCARD.</span></span>

<span data-ttu-id="8b7bf-127">最後一個步驟是藉由呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法，並將 D3DRS \_ MULTISAMPLEANTIALIAS 設定為 **TRUE**，啟用取樣消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-127">The last step is to enable multisampling antialiasing by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method and setting the D3DRS\_MULTISAMPLEANTIALIAS to **TRUE**.</span></span> <span data-ttu-id="8b7bf-128">將此值設定為 **TRUE** 之後，您所做的任何轉譯都會套用至它。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-128">After setting this value to **TRUE**, any rendering that you do will have multisampling applied to it.</span></span> <span data-ttu-id="8b7bf-129">您可能會想要根據所呈現的內容來啟用和停用取樣。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-129">You might want to enable and disable multisampling, depending on what you are rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b7bf-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="8b7bf-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b7bf-131">消除鋸齒</span><span class="sxs-lookup"><span data-stu-id="8b7bf-131">Antialiasing</span></span>](antialiasing.md)
</dt> </dl>

 

 

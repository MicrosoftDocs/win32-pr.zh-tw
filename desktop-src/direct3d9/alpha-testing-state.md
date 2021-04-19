---
description: C + + 應用程式可以使用 Alpha 測試來控制何時將圖元寫入呈現目標介面。
ms.assetid: 368c3d12-2c8b-43e3-94c3-bccfe6c73e66
title: " (Direct3D 9) 的 Alpha 測試狀態"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020322ee31bc08352dbb2796ea5e7141d03c77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970537"
---
# <a name="alpha-testing-state-direct3d-9"></a><span data-ttu-id="500bb-103"> (Direct3D 9) 的 Alpha 測試狀態</span><span class="sxs-lookup"><span data-stu-id="500bb-103">Alpha Testing State (Direct3D 9)</span></span>

<span data-ttu-id="500bb-104">C + + 應用程式可以使用 Alpha 測試來控制何時將圖元寫入呈現目標介面。</span><span class="sxs-lookup"><span data-stu-id="500bb-104">C++ applications can use alpha testing to control when pixels are written to the render-target surface.</span></span> <span data-ttu-id="500bb-105">藉由使用 [**D3DRS \_ ALPHATESTENABLE**](./d3drenderstatetype.md) 轉譯狀態，您的應用程式會設定目前的 Direct3D 裝置，讓它根據 Alpha 測試函式來測試每個圖元。</span><span class="sxs-lookup"><span data-stu-id="500bb-105">By using the [**D3DRS\_ALPHATESTENABLE**](./d3drenderstatetype.md) render state, your application sets the current Direct3D device so that it tests each pixel according to an alpha test function.</span></span> <span data-ttu-id="500bb-106">如果測試成功，則會將圖元寫入介面。</span><span class="sxs-lookup"><span data-stu-id="500bb-106">If the test succeeds, the pixel is written to the surface.</span></span> <span data-ttu-id="500bb-107">如果不是，Direct3D 會忽略圖元。</span><span class="sxs-lookup"><span data-stu-id="500bb-107">If it does not, Direct3D ignores the pixel.</span></span> <span data-ttu-id="500bb-108">選取 **D3DRS \_ ALPHAFUNC** 轉譯狀態的 Alpha 測試函數。</span><span class="sxs-lookup"><span data-stu-id="500bb-108">Select the alpha test function with the **D3DRS\_ALPHAFUNC** render state.</span></span> <span data-ttu-id="500bb-109">您的應用程式可以使用 **D3DRS \_ ALPHAREF** 轉譯狀態來設定要比較的所有圖元的參考 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="500bb-109">Your application can set a reference alpha value for all pixels to compare against by using the **D3DRS\_ALPHAREF** render state.</span></span>

<span data-ttu-id="500bb-110">Alpha 測試最常見的用法是在將幾乎透明的物件進行點陣化時，改善效能。</span><span class="sxs-lookup"><span data-stu-id="500bb-110">The most common use for alpha testing is to improve performance when rasterizing objects that are nearly transparent.</span></span> <span data-ttu-id="500bb-111">如果要進行柵格化的色彩資料比指定圖元 (D3DPCMPCAPS GREATEREQUAL) 的色彩更不透明 \_ ，則會寫入圖元。</span><span class="sxs-lookup"><span data-stu-id="500bb-111">If the color data being rasterized is more opaque than the color at a given pixel (D3DPCMPCAPS\_GREATEREQUAL), then the pixel is written.</span></span> <span data-ttu-id="500bb-112">否則，轉譯器會完全忽略圖元，儲存混合兩種色彩所需的處理。</span><span class="sxs-lookup"><span data-stu-id="500bb-112">Otherwise, the rasterizer ignores the pixel altogether, saving the processing required to blend the two colors.</span></span> <span data-ttu-id="500bb-113">下列程式碼範例會檢查是否支援給定的比較函式，如果是的話，它會設定在轉譯期間改善效能所需的比較函數參數。</span><span class="sxs-lookup"><span data-stu-id="500bb-113">The following code example checks if a given comparison function is supported and, if so, it sets the comparison function parameters required to improve performance during rendering.</span></span>


```
// This code example assumes that pCaps is a
// D3DCAPS9 structure that was filled with a 
// previous call to IDirect3D9::GetDeviceCaps.

if (pCaps.AlphaCmpCaps & D3DPCMPCAPS_GREATEREQUAL)
{
    dev->SetRenderState(D3DRS_ALPHAREF, (DWORD)0x00000001);
    dev->SetRenderState(D3DRS_ALPHATESTENABLE, TRUE); 
    dev->SetRenderState(D3DRS_ALPHAFUNC, D3DCMP_GREATEREQUAL);
}

// If the comparison is not supported, render anyway. 
// The only drawback is no performance gain.
```



<span data-ttu-id="500bb-114">並非所有硬體都支援所有的 Alpha 測試功能。</span><span class="sxs-lookup"><span data-stu-id="500bb-114">Not all hardware supports all alpha-testing features.</span></span> <span data-ttu-id="500bb-115">您可以藉由呼叫 [**IDirect3D9：： GetDeviceCaps**](/windows/desktop/api) 方法來檢查裝置功能。</span><span class="sxs-lookup"><span data-stu-id="500bb-115">You can check the device capabilities by calling the [**IDirect3D9::GetDeviceCaps**](/windows/desktop/api) method.</span></span> <span data-ttu-id="500bb-116">在抓取裝置功能之後，請檢查相關聯的 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 AlphaCmpCaps 成員，以尋找所需的比較函數。</span><span class="sxs-lookup"><span data-stu-id="500bb-116">After retrieving the device capabilities, check the associated [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's AlphaCmpCaps member for the desired comparison function.</span></span> <span data-ttu-id="500bb-117">如果 AlphaCmpCaps 成員只包含 D3DPCMPCAPS \_ ALWAYS 功能，或只包含 D3DPCMPCAPS \_ 永遠沒有的功能，則驅動程式不支援 Alpha 測試。</span><span class="sxs-lookup"><span data-stu-id="500bb-117">If the AlphaCmpCaps member contains only the D3DPCMPCAPS\_ALWAYS capability or only the D3DPCMPCAPS\_NEVER capability, the driver does not support alpha tests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="500bb-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="500bb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="500bb-119">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="500bb-119">Render States</span></span>](render-states.md)
</dt> </dl>

 

 

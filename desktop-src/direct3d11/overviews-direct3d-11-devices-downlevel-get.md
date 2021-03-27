---
title: 如何取得裝置功能等級
description: 本主題說明如何取得裝置支援的最高功能層級。
ms.assetid: 5eb7dd5b-3be3-4b7f-bcc7-20027fdfe6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e587ad488a84641a92f0058d201014030e3467e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840584"
---
# <a name="how-to-get-the-device-feature-level"></a><span data-ttu-id="d9e0d-103">如何：取得裝置功能等級</span><span class="sxs-lookup"><span data-stu-id="d9e0d-103">How To: Get the Device Feature Level</span></span>

<span data-ttu-id="d9e0d-104">本主題說明如何取得[裝置](overviews-direct3d-11-devices-intro.md)支援的最高[功能層級](overviews-direct3d-11-devices-downlevel-intro.md)。</span><span class="sxs-lookup"><span data-stu-id="d9e0d-104">This topics shows how to get the highest [feature level](overviews-direct3d-11-devices-downlevel-intro.md) supported by a [device](overviews-direct3d-11-devices-intro.md).</span></span> <span data-ttu-id="d9e0d-105">Direct3D 11 裝置可支援在 [**D3D \_ 功能 \_ 層級**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) 列舉中定義的一組固定功能等級。</span><span class="sxs-lookup"><span data-stu-id="d9e0d-105">Direct3D 11 devices support a fixed set of feature levels that are defined in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span> <span data-ttu-id="d9e0d-106">當您知道裝置支援的最高 [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 時，您可以執行適用于該裝置的程式碼路徑。</span><span class="sxs-lookup"><span data-stu-id="d9e0d-106">When you know the highest [feature level](overviews-direct3d-11-devices-downlevel-intro.md) supported by a device, you can run code paths that are appropriate for that device.</span></span>

<span data-ttu-id="d9e0d-107">**取得裝置功能等級**</span><span class="sxs-lookup"><span data-stu-id="d9e0d-107">**To get the device feature level**</span></span>

1.  <span data-ttu-id="d9e0d-108">針對 *ppDevice* 參數指定 **Null** 時，請呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice)函數或 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)函數。</span><span class="sxs-lookup"><span data-stu-id="d9e0d-108">Call either the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function or the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) functions while specifying **NULL** for the *ppDevice* parameter.</span></span> <span data-ttu-id="d9e0d-109">您可以在裝置建立之前完成此動作。</span><span class="sxs-lookup"><span data-stu-id="d9e0d-109">You can do this before device creation.</span></span>

    <span data-ttu-id="d9e0d-110">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="d9e0d-110">\- or -</span></span>

    <span data-ttu-id="d9e0d-111">建立裝置之後，請呼叫 [**ID3D11Device：： GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) 。</span><span class="sxs-lookup"><span data-stu-id="d9e0d-111">Call [**ID3D11Device::GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) after device creation.</span></span>

2.  <span data-ttu-id="d9e0d-112">檢查從上一個步驟傳回的 [**D3D \_ 功能 \_ 層級**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) 列舉值，以判斷支援的功能層級。</span><span class="sxs-lookup"><span data-stu-id="d9e0d-112">Examine the value of the returned [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration from the last step to determine the supported feature level.</span></span>

<span data-ttu-id="d9e0d-113">下列程式碼範例示範如何藉由呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) 函數來判斷最高支援的功能層級。</span><span class="sxs-lookup"><span data-stu-id="d9e0d-113">The following code example demonstrates how to determine the highest supported feature level by calling the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function.</span></span> <span data-ttu-id="d9e0d-114">**D3D11CreateDevice** 會將最高支援的功能層級儲存在 FeatureLevel 變數中。</span><span class="sxs-lookup"><span data-stu-id="d9e0d-114">**D3D11CreateDevice** stores the highest supported feature level in the FeatureLevel variable.</span></span> <span data-ttu-id="d9e0d-115">您可以使用此程式碼來檢查 **D3D11CreateDevice** 傳回的 [**D3D \_ 功能 \_ 層級**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)列舉型別值。</span><span class="sxs-lookup"><span data-stu-id="d9e0d-115">You can use this code to examine the value of the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumerated type that **D3D11CreateDevice** returns.</span></span> <span data-ttu-id="d9e0d-116">請注意，此程式碼會針對 Direct3D 11.1 和 Direct3D 11.2) 明確 (列出所有功能層級。</span><span class="sxs-lookup"><span data-stu-id="d9e0d-116">Note that this code lists all feature levels explicitly (for Direct3D 11.1 and Direct3D 11.2).</span></span>

> [!Note]  
> <span data-ttu-id="d9e0d-117">如果電腦上有 Direct3D 11.1 執行時間，且 *pFeatureLevels* 設定為 **Null**，則此函式不會建立 [**D3D \_ 功能 \_ 等級 \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) 的裝置。</span><span class="sxs-lookup"><span data-stu-id="d9e0d-117">If the Direct3D 11.1 runtime is present on the computer and *pFeatureLevels* is set to **NULL**, this function won't create a [**D3D\_FEATURE\_LEVEL\_11\_1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) device.</span></span> <span data-ttu-id="d9e0d-118">若要建立 **d3d \_ 功能 \_ 等級 \_ 11 \_ 1** 的裝置，您必須明確提供包含 **d3d \_ 功能等級 \_ \_ 11 \_ 1** 的 **d3d \_ 功能 \_ 等級** 陣列。</span><span class="sxs-lookup"><span data-stu-id="d9e0d-118">To create a **D3D\_FEATURE\_LEVEL\_11\_1** device, you must explicitly provide a **D3D\_FEATURE\_LEVEL** array that includes **D3D\_FEATURE\_LEVEL\_11\_1**.</span></span> <span data-ttu-id="d9e0d-119">如果您在未安裝 Direct3D 11.1 執行時間的電腦上提供包含 **d3d \_ 功能 \_ 等級 \_ 11 \_ 1** 的 **d3d \_ 功能 \_ 層級** 陣列，此函式會立即失敗，並出現 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="d9e0d-119">If you provide a **D3D\_FEATURE\_LEVEL** array that contains **D3D\_FEATURE\_LEVEL\_11\_1** on a computer that doesn't have the Direct3D 11.1 runtime installed, this function immediately fails with E\_INVALIDARG.</span></span>

 


```C++
HRESULT hr = E_FAIL;
D3D_FEATURE_LEVEL MaxSupportedFeatureLevel = D3D_FEATURE_LEVEL_9_1;
D3D_FEATURE_LEVEL FeatureLevels[] = {
    D3D_FEATURE_LEVEL_11_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1
    };

hr = D3D11CreateDevice(
    NULL,
    D3D_DRIVER_TYPE_HARDWARE,
    NULL, 
    0, 
    &FeatureLevels, 
    ARRAYSIZE(FeatureLevels), 
    D3D11_SDK_VERSION, 
    NULL, 
    &MaxSupportedFeatureLevel, 
    NULL 
    );

if(FAILED(hr))
{
    return hr;
}
```



<span data-ttu-id="d9e0d-120">[ [10Level9 參考](d3d11-graphics-reference-10level9.md) ] 區段會列出各種 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 和 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 方法在各種10Level9 功能層級的行為方式之間的差異。</span><span class="sxs-lookup"><span data-stu-id="d9e0d-120">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9e0d-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="d9e0d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9e0d-122">舊版硬體上的 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d9e0d-122">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[<span data-ttu-id="d9e0d-123">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d9e0d-123">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 





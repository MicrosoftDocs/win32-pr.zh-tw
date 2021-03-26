---
title: 舊版硬體上的 Direct3D 11
description: 本節討論如何設計 Direct3D 11，以支援新的和現有的硬體，從 DirectX 9 到 DirectX 11。
ms.assetid: 9a1ca4ff-df3d-46e5-8895-37199523343e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f730a43db803e1e5198794167d0078a5b2896f6c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104564407"
---
# <a name="direct3d-11-on-downlevel-hardware"></a><span data-ttu-id="81ed7-103">舊版硬體上的 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="81ed7-103">Direct3D 11 on Downlevel Hardware</span></span>

<span data-ttu-id="81ed7-104">本節討論如何設計 Direct3D 11，以支援新的和現有的硬體，從 DirectX 9 到 DirectX 11。</span><span class="sxs-lookup"><span data-stu-id="81ed7-104">This section discusses how Direct3D 11 is designed to support both new and existing hardware, from DirectX 9 to DirectX 11.</span></span>

<span data-ttu-id="81ed7-105">下圖顯示 Direct3D 11 如何支援新的和現有的硬體。</span><span class="sxs-lookup"><span data-stu-id="81ed7-105">This diagram shows how Direct3D 11 supports new and existing hardware.</span></span>

![direct3d 11 支援的硬體圖表](images/d3d11-on-downlevel-hardware.png)

<span data-ttu-id="81ed7-107">使用 Direct3D 11 時，引進了新的典範，稱為功能層級。</span><span class="sxs-lookup"><span data-stu-id="81ed7-107">With Direct3D 11, a new paradigm is introduced called feature levels.</span></span> <span data-ttu-id="81ed7-108">功能層級是一組定義完善的 GPU 功能。</span><span class="sxs-lookup"><span data-stu-id="81ed7-108">A feature level is a well defined set of GPU functionality.</span></span> <span data-ttu-id="81ed7-109">使用功能層級，您可以將 Direct3D 應用程式的目標設為在舊版 Direct3D 硬體上執行。</span><span class="sxs-lookup"><span data-stu-id="81ed7-109">Using a feature level, you can target a Direct3D application to run on a downlevel version of Direct3D hardware.</span></span>

<span data-ttu-id="81ed7-110">[ [10Level9 參考](d3d11-graphics-reference-10level9.md) ] 區段會列出各種 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 和 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 方法在各種10Level9 功能層級的行為方式之間的差異。</span><span class="sxs-lookup"><span data-stu-id="81ed7-110">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="81ed7-111">本節內容</span><span class="sxs-lookup"><span data-stu-id="81ed7-111">In this section</span></span>



| <span data-ttu-id="81ed7-112">主題</span><span class="sxs-lookup"><span data-stu-id="81ed7-112">Topic</span></span>                                                                                                                  | <span data-ttu-id="81ed7-113">描述</span><span class="sxs-lookup"><span data-stu-id="81ed7-113">Description</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81ed7-114">Direct3D 功能層級</span><span class="sxs-lookup"><span data-stu-id="81ed7-114">Direct3D feature levels</span></span>](overviews-direct3d-11-devices-downlevel-intro.md)<br/>                                | <span data-ttu-id="81ed7-115">本主題討論 Direct3D 功能等級。</span><span class="sxs-lookup"><span data-stu-id="81ed7-115">This topic discusses Direct3D feature levels.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="81ed7-116">例外狀況</span><span class="sxs-lookup"><span data-stu-id="81ed7-116">Exceptions</span></span>](overviews-direct3d-11-devices-downlevel-exceptions.md)<br/>                                        | <span data-ttu-id="81ed7-117">本主題說明在舊版硬體上使用 Direct3D 11 時的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="81ed7-117">This topic describes exceptions when using Direct3D 11 on downlevel hardware.</span></span> <br/>                                                                                      |
| [<span data-ttu-id="81ed7-118">下層硬體上的計算著色器</span><span class="sxs-lookup"><span data-stu-id="81ed7-118">Compute Shaders on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel-compute-shaders.md)<br/>        | <span data-ttu-id="81ed7-119">本主題將討論如何在 Direct3D 10 硬體上的 Direct3D 11 應用程式中使用 [計算著色](direct3d-11-advanced-stages-compute-shader.md) 器。</span><span class="sxs-lookup"><span data-stu-id="81ed7-119">This topic discusses how to make use of [compute shaders](direct3d-11-advanced-stages-compute-shader.md) in a Direct3D 11 app on Direct3D 10 hardware.</span></span><br/>             |
| [<span data-ttu-id="81ed7-120">防止不必要的 Null 圖元著色器 SRVs</span><span class="sxs-lookup"><span data-stu-id="81ed7-120">Preventing Unwanted NULL Pixel Shader SRVs</span></span>](overviews-direct3d-11-devices-downlevel-prevent-null-srvs.md)<br/> | <span data-ttu-id="81ed7-121">本主題討論如何解決接收 **null** 著色器資源檢視 (SRVs) 的驅動程式，即使非 **Null** SRVs 系結至圖元著色器階段也是如此。</span><span class="sxs-lookup"><span data-stu-id="81ed7-121">This topic discusses how to work around the driver receiving **NULL** shader-resource views (SRVs) even when non-**NULL** SRVs are bound to the pixel shader stage.</span></span><br/> |



 

## <a name="how-to-topics-about-feature-levels"></a><span data-ttu-id="81ed7-122">功能層級的相關主題</span><span class="sxs-lookup"><span data-stu-id="81ed7-122">How to topics about feature levels</span></span>



| <span data-ttu-id="81ed7-123">主題</span><span class="sxs-lookup"><span data-stu-id="81ed7-123">Topic</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="81ed7-124">描述</span><span class="sxs-lookup"><span data-stu-id="81ed7-124">Description</span></span>                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="81ed7-125"><span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[如何：取得裝置功能等級](overviews-direct3d-11-devices-downlevel-get.md)</span><span class="sxs-lookup"><span data-stu-id="81ed7-125"><span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[How To: Get the Device Feature Level](overviews-direct3d-11-devices-downlevel-get.md)</span></span><br/> | <span data-ttu-id="81ed7-126">如何取得功能等級。</span><span class="sxs-lookup"><span data-stu-id="81ed7-126">How to get a feature level.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="81ed7-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="81ed7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81ed7-128">裝置</span><span class="sxs-lookup"><span data-stu-id="81ed7-128">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 






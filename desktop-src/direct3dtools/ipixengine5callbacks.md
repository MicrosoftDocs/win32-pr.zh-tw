---
description: 用來查看材質的回呼。
MS-HAID: vspixengine.IPixEngine5Callbacks
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5Callbacks 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F87F00ED-C816-49A3-926B-28E3C8330EA2
api_name:
- IPixEngine5Callbacks
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 80f00a0d7e2e3478114d94480e01e31add63ef90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109316"
---
# <a name="span-idvspixengineipixengine5callbacksspanipixengine5callbacks-interface"></a><span data-ttu-id="2743c-103"><span id="vspixengine.ipixengine5callbacks"></span>IPixEngine5Callbacks 介面</span><span class="sxs-lookup"><span data-stu-id="2743c-103"><span id="vspixengine.ipixengine5callbacks"></span>IPixEngine5Callbacks interface</span></span>

<span data-ttu-id="2743c-104">用來查看材質的回呼。</span><span class="sxs-lookup"><span data-stu-id="2743c-104">Callbacks used for viewing textures.</span></span>

## <a name="members"></a><span data-ttu-id="2743c-105">成員</span><span class="sxs-lookup"><span data-stu-id="2743c-105">Members</span></span>

<span data-ttu-id="2743c-106">**IPixEngine5Callbacks** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="2743c-106">The **IPixEngine5Callbacks** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2743c-107">**IPixEngine5Callbacks** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2743c-107">**IPixEngine5Callbacks** also has these types of members:</span></span>

-   [<span data-ttu-id="2743c-108">方法</span><span class="sxs-lookup"><span data-stu-id="2743c-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="2743c-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="2743c-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="2743c-110">**IPixEngine5Callbacks** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2743c-110">The **IPixEngine5Callbacks** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="2743c-111">方法</span><span class="sxs-lookup"><span data-stu-id="2743c-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="2743c-112">描述</span><span class="sxs-lookup"><span data-stu-id="2743c-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="2743c-113"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>FreeTextureComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="2743c-113"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>FreeTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="2743c-114">釋放材質時，用來通知主機的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="2743c-114">A callback function used to notify the host when a texture has been freed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="2743c-115"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>LoadHistogramComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="2743c-115"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>LoadHistogramComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="2743c-116">當長條圖載入已完成時，用來通知主機的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="2743c-116">A callback function used to notify the host when a histogram load has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="2743c-117"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>LoadTextureFromFileComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="2743c-117"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>LoadTextureFromFileComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="2743c-118">當材質載入已完成時，用來通知主機的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="2743c-118">A callback function used to notify the host when a texture load has been completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="2743c-119"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>LoadTextureSliceComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="2743c-119"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>LoadTextureSliceComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="2743c-120">當材質配量載入已完成時，用來通知主機的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="2743c-120">A callback function used to notify the host when a texture slice load has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="2743c-121"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>ReadTexelValueComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="2743c-121"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>ReadTexelValueComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="2743c-122">當材質值讀取完成時，用來通知主機的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="2743c-122">A callback function used to notify the host when a texel value read has been completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="2743c-123"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>RenderTextureComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="2743c-123"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>RenderTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="2743c-124">在紋理轉譯完成時，用來通知主機的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="2743c-124">A callback function used to notify the host when a texture render has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="2743c-125"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>SaveTextureComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="2743c-125"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>SaveTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="2743c-126">在儲存材質時，用來通知主控制項的回呼函式已完成。</span><span class="sxs-lookup"><span data-stu-id="2743c-126">A callback function used to notify the host when saving a texture has been completed.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="2743c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="2743c-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2743c-128">標頭</span><span class="sxs-lookup"><span data-stu-id="2743c-128">Header</span></span></p></td><td><span data-ttu-id="2743c-129">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="2743c-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 

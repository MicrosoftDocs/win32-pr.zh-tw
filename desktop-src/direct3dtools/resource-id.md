---
description: 定義共用字串資源的資源識別碼。
MS-HAID: vspixengine.Resource\_Id
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Resource_Id 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC04FDC4-CD35-4A87-8EE8-48FFA07B8FC0
api_name:
- Resource_Id
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e7d93111defb01000e32e4f5ade0c9eb09c827e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510134"
---
# <a name="span-idvspixengineresource_idspanresource_id-enumeration"></a><span data-ttu-id="6e054-103"><span id="vspixengine.resource_id"></span>資源 \_ 識別碼列舉</span><span class="sxs-lookup"><span data-stu-id="6e054-103"><span id="vspixengine.resource_id"></span>Resource\_Id enumeration</span></span>

<span data-ttu-id="6e054-104">定義共用字串資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e054-104">Defines resource IDs for shared string resources.</span></span> <span data-ttu-id="6e054-105">這些會從主機傳遞至 capture engine。</span><span class="sxs-lookup"><span data-stu-id="6e054-105">These are passed to the capture engine from the host.</span></span> <span data-ttu-id="6e054-106">它們可用來顯示所要抬頭顯示器之應用程式的重迭字串，或是將登錄值從 Visual Studio 選項傳遞至 capture engi</span><span class="sxs-lookup"><span data-stu-id="6e054-106">They are used to display strings to the HUD overlay of the app being captured or to pass registry values from Visual Studio options to the capture engi</span></span>

## <a name="syntax"></a><span data-ttu-id="6e054-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e054-107">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="6e054-108">常數</span><span class="sxs-lookup"><span data-stu-id="6e054-108">Constants</span></span>

<span data-ttu-id="6e054-109"><span id="IDS_ENGINEDISCONNECTED"></span><span id="ids_enginedisconnected"></span>**識別碼 \_ ENGINEDISCONNECTED**</span><span class="sxs-lookup"><span data-stu-id="6e054-109"><span id="IDS_ENGINEDISCONNECTED"></span><span id="ids_enginedisconnected"></span>**IDS\_ENGINEDISCONNECTED**</span></span>  
<span data-ttu-id="6e054-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-110">Not used.</span></span> <span data-ttu-id="6e054-111">先前用來表示在完成 capture 會話之後，已達到 printscreen 的字串資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e054-111">Resource id for string formerly used to indicate that printscreen was hit after the capture session was complete.</span></span>

<span data-ttu-id="6e054-112"><span id="IDR_RCDATA1"></span><span id="idr_rcdata1"></span>**IDR \_ RCDATA1**</span><span class="sxs-lookup"><span data-stu-id="6e054-112"><span id="IDR_RCDATA1"></span><span id="idr_rcdata1"></span>**IDR\_RCDATA1**</span></span>  
<span data-ttu-id="6e054-113">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-113">Not used.</span></span>

<span data-ttu-id="6e054-114"><span id="IDS_DEFAULTEXPFILE_CONTENT"></span><span id="ids_defaultexpfile_content"></span>**識別碼 \_ DEFAULTEXPFILE \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="6e054-114"><span id="IDS_DEFAULTEXPFILE_CONTENT"></span><span id="ids_defaultexpfile_content"></span>**IDS\_DEFAULTEXPFILE\_CONTENT**</span></span>  
<span data-ttu-id="6e054-115">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-115">Not used.</span></span> <span data-ttu-id="6e054-116">先前用於舊版捕獲案例中 XML 資料的字串資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e054-116">Resource id for string formerly used for XML data in legacy capture scenarios.</span></span>

<span data-ttu-id="6e054-117"><span id="IDS_CAPTURE_MESSAGE"></span><span id="ids_capture_message"></span>**識別碼 \_ 捕獲 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="6e054-117"><span id="IDS_CAPTURE_MESSAGE"></span><span id="ids_capture_message"></span>**IDS\_CAPTURE\_MESSAGE**</span></span>  
<span data-ttu-id="6e054-118">字串「已捕獲框架」的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e054-118">Resource ID for string "Captured frame."</span></span>

<span data-ttu-id="6e054-119"><span id="IDS_CAPTURE_NOT_SUPPORTED"></span><span id="ids_capture_not_supported"></span>**\_ \_ 不支援識別碼 \_ 捕獲**</span><span class="sxs-lookup"><span data-stu-id="6e054-119"><span id="IDS_CAPTURE_NOT_SUPPORTED"></span><span id="ids_capture_not_supported"></span>**IDS\_CAPTURE\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="6e054-120">字串的資源識別碼「此程式指出它無法搭配圖形診斷工具使用」。</span><span class="sxs-lookup"><span data-stu-id="6e054-120">Resource ID for string "This program has indicated that it cannot be used with Graphics Diagnostics tools."</span></span>

<span data-ttu-id="6e054-121"><span id="IDS_CAPTURE_NOT_SUPPORTED_TITLE"></span><span id="ids_capture_not_supported_title"></span>**\_不支援識別碼捕捉的 \_ \_ \_ 標題**</span><span class="sxs-lookup"><span data-stu-id="6e054-121"><span id="IDS_CAPTURE_NOT_SUPPORTED_TITLE"></span><span id="ids_capture_not_supported_title"></span>**IDS\_CAPTURE\_NOT\_SUPPORTED\_TITLE**</span></span>  
<span data-ttu-id="6e054-122">字串「不支援的功能」的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6e054-122">Resource ID for string "Unsupported functionality"</span></span>

<span data-ttu-id="6e054-123"><span id="IDS_FEATURE_NOT_SUPPORTED"></span><span id="ids_feature_not_supported"></span>**\_ \_ 不 \_ 支援的識別碼功能**</span><span class="sxs-lookup"><span data-stu-id="6e054-123"><span id="IDS_FEATURE_NOT_SUPPORTED"></span><span id="ids_feature_not_supported"></span>**IDS\_FEATURE\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="6e054-124">字串「裝置功能層級不受支援」的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6e054-124">Resource ID for string "Device feature level not supported"</span></span>

<span data-ttu-id="6e054-125"><span id="IDS_DXVERSION_NOT_SUPPORTED"></span><span id="ids_dxversion_not_supported"></span>**\_ \_ 不 \_ 支援的識別碼 DXVERSION**</span><span class="sxs-lookup"><span data-stu-id="6e054-125"><span id="IDS_DXVERSION_NOT_SUPPORTED"></span><span id="ids_dxversion_not_supported"></span>**IDS\_DXVERSION\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="6e054-126">字串 "DirectX version not capturable" 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6e054-126">Resource ID for string "DirectX version not capturable"</span></span>

<span data-ttu-id="6e054-127"><span id="IDS_DCOMP_NOT_SUPPORTED"></span><span id="ids_dcomp_not_supported"></span>**\_ \_ 不 \_ 支援的識別碼 DCOMP**</span><span class="sxs-lookup"><span data-stu-id="6e054-127"><span id="IDS_DCOMP_NOT_SUPPORTED"></span><span id="ids_dcomp_not_supported"></span>**IDS\_DCOMP\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="6e054-128">字串「在應用程式中使用，但此 OS 不支援 DCOMP」的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6e054-128">Resource ID for string "DCOMP in use by app but not supported on this OS"</span></span>

<span data-ttu-id="6e054-129"><span id="IDS_DWRITE_NOT_SUPPORTED"></span><span id="ids_dwrite_not_supported"></span>**\_ \_ 不 \_ 支援的識別碼 DWRITE**</span><span class="sxs-lookup"><span data-stu-id="6e054-129"><span id="IDS_DWRITE_NOT_SUPPORTED"></span><span id="ids_dwrite_not_supported"></span>**IDS\_DWRITE\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="6e054-130">字串「在應用程式中使用，但此 OS 不支援 DWRITE」的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6e054-130">Resource ID for string "DWRITE in use by app but not supported on this OS"</span></span>

<span data-ttu-id="6e054-131"><span id="IDS_EXPECTED_FAILURE_FORMAT"></span><span id="ids_expected_failure_format"></span>**識別碼 \_ 預期 \_ 失敗 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="6e054-131"><span id="IDS_EXPECTED_FAILURE_FORMAT"></span><span id="ids_expected_failure_format"></span>**IDS\_EXPECTED\_FAILURE\_FORMAT**</span></span>  
<span data-ttu-id="6e054-132">字串 "% s" 的資源識別碼在播放期間傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6e054-132">Resource ID for string "%s returned an error during playback.</span></span> <span data-ttu-id="6e054-133"> (HRESULT =% s) \\ r \\ n」。</span><span class="sxs-lookup"><span data-stu-id="6e054-133">(HRESULT=%s)\\r\\n".</span></span>

<span data-ttu-id="6e054-134"><span id="IDS_CAPTURETOOLTIP_MESSAGE"></span><span id="ids_capturetooltip_message"></span>**識別碼 \_ CAPTURETOOLTIP \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="6e054-134"><span id="IDS_CAPTURETOOLTIP_MESSAGE"></span><span id="ids_capturetooltip_message"></span>**IDS\_CAPTURETOOLTIP\_MESSAGE**</span></span>  
<span data-ttu-id="6e054-135">字串「使用 ' Print Screen ' 鍵來捕捉框架」的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e054-135">Resource ID for string "Use 'Print Screen' key to capture a frame."</span></span>

<span data-ttu-id="6e054-136"><span id="IDS_D2D_AND_D10_NOT_SUPPORTED"></span><span id="ids_d2d_and_d10_not_supported"></span>**\_不支援的識別碼 D2D \_ 和 \_ D10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6e054-136"><span id="IDS_D2D_AND_D10_NOT_SUPPORTED"></span><span id="ids_d2d_and_d10_not_supported"></span>**IDS\_D2D\_AND\_D10\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="6e054-137">在此 OS 上，不支援字串 "D2D 和 D10 的資源識別碼"</span><span class="sxs-lookup"><span data-stu-id="6e054-137">Resource ID for string "D2D and D10 not supported together on this OS"</span></span>

<span data-ttu-id="6e054-138"><span id="IDS_HUD_STATISTICS"></span><span id="ids_hud_statistics"></span>**識別碼 \_ 抬頭顯示器 \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="6e054-138"><span id="IDS_HUD_STATISTICS"></span><span id="ids_hud_statistics"></span>**IDS\_HUD\_STATISTICS**</span></span>  
<span data-ttu-id="6e054-139">字串的資源識別碼已被捕獲的框架% d。</span><span class="sxs-lookup"><span data-stu-id="6e054-139">Resource ID for string "Frames captured %d.</span></span> <span data-ttu-id="6e054-140">畫面格時間 (ms) % 0.00 f "</span><span class="sxs-lookup"><span data-stu-id="6e054-140">Frame time (ms) %0.00f"</span></span>

<span data-ttu-id="6e054-141"><span id="IDS_INTERNAL_METHOD"></span><span id="ids_internal_method"></span>**IDS \_ 內部 \_ 方法**</span><span class="sxs-lookup"><span data-stu-id="6e054-141"><span id="IDS_INTERNAL_METHOD"></span><span id="ids_internal_method"></span>**IDS\_INTERNAL\_METHOD**</span></span>  
<span data-ttu-id="6e054-142">字串 "Directx Internal Method" 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6e054-142">Resource ID for string "Directx Internal Method"</span></span>

<span data-ttu-id="6e054-143"><span id="IDS_CAPTURE_FRAME_MARK"></span><span id="ids_capture_frame_mark"></span>**識別碼 \_ 捕獲 \_ 框架 \_ 標記**</span><span class="sxs-lookup"><span data-stu-id="6e054-143"><span id="IDS_CAPTURE_FRAME_MARK"></span><span id="ids_capture_frame_mark"></span>**IDS\_CAPTURE\_FRAME\_MARK**</span></span>  
<span data-ttu-id="6e054-144">字串「捕獲的框架% ld」的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6e054-144">Resource ID for string "Captured Frame %ld"</span></span>

<span data-ttu-id="6e054-145"><span id="PIPELINESTAGE_INPUTASSEMBLER"></span><span id="pipelinestage_inputassembler"></span>**PIPELINESTAGE \_ INPUTASSEMBLER**</span><span class="sxs-lookup"><span data-stu-id="6e054-145"><span id="PIPELINESTAGE_INPUTASSEMBLER"></span><span id="pipelinestage_inputassembler"></span>**PIPELINESTAGE\_INPUTASSEMBLER**</span></span>  
<span data-ttu-id="6e054-146">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-146">Not used.</span></span>

<span data-ttu-id="6e054-147"><span id="PIPELINESTAGE_VERTEXSHADER"></span><span id="pipelinestage_vertexshader"></span>**PIPELINESTAGE \_ VERTEXSHADER**</span><span class="sxs-lookup"><span data-stu-id="6e054-147"><span id="PIPELINESTAGE_VERTEXSHADER"></span><span id="pipelinestage_vertexshader"></span>**PIPELINESTAGE\_VERTEXSHADER**</span></span>  
<span data-ttu-id="6e054-148">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-148">Not used.</span></span>

<span data-ttu-id="6e054-149"><span id="PIPELINESTAGE_HULLSHADER"></span><span id="pipelinestage_hullshader"></span>**PIPELINESTAGE \_ HULLSHADER**</span><span class="sxs-lookup"><span data-stu-id="6e054-149"><span id="PIPELINESTAGE_HULLSHADER"></span><span id="pipelinestage_hullshader"></span>**PIPELINESTAGE\_HULLSHADER**</span></span>  
<span data-ttu-id="6e054-150">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-150">Not used.</span></span>

<span data-ttu-id="6e054-151"><span id="PIPELINESTAGE_TESSELATOR"></span><span id="pipelinestage_tesselator"></span>**PIPELINESTAGE \_ TESSELATOR**</span><span class="sxs-lookup"><span data-stu-id="6e054-151"><span id="PIPELINESTAGE_TESSELATOR"></span><span id="pipelinestage_tesselator"></span>**PIPELINESTAGE\_TESSELATOR**</span></span>  
<span data-ttu-id="6e054-152">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-152">Not used.</span></span>

<span data-ttu-id="6e054-153"><span id="PIPELINESTAGE_DOMAINSHADER"></span><span id="pipelinestage_domainshader"></span>**PIPELINESTAGE \_ DOMAINSHADER**</span><span class="sxs-lookup"><span data-stu-id="6e054-153"><span id="PIPELINESTAGE_DOMAINSHADER"></span><span id="pipelinestage_domainshader"></span>**PIPELINESTAGE\_DOMAINSHADER**</span></span>  
<span data-ttu-id="6e054-154">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-154">Not used.</span></span>

<span data-ttu-id="6e054-155"><span id="PIPELINESTAGE_GEOMETRYSHADER"></span><span id="pipelinestage_geometryshader"></span>**PIPELINESTAGE \_ GEOMETRYSHADER**</span><span class="sxs-lookup"><span data-stu-id="6e054-155"><span id="PIPELINESTAGE_GEOMETRYSHADER"></span><span id="pipelinestage_geometryshader"></span>**PIPELINESTAGE\_GEOMETRYSHADER**</span></span>  
<span data-ttu-id="6e054-156">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-156">Not used.</span></span>

<span data-ttu-id="6e054-157"><span id="PIPELINESTAGE_STREAMOUTPUT"></span><span id="pipelinestage_streamoutput"></span>**PIPELINESTAGE \_ >STREAMOUTPUT**</span><span class="sxs-lookup"><span data-stu-id="6e054-157"><span id="PIPELINESTAGE_STREAMOUTPUT"></span><span id="pipelinestage_streamoutput"></span>**PIPELINESTAGE\_STREAMOUTPUT**</span></span>  
<span data-ttu-id="6e054-158">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-158">Not used.</span></span>

<span data-ttu-id="6e054-159"><span id="PIPELINESTAGE_RASTERIZER"></span><span id="pipelinestage_rasterizer"></span>**PIPELINESTAGE \_ 轉譯器**</span><span class="sxs-lookup"><span data-stu-id="6e054-159"><span id="PIPELINESTAGE_RASTERIZER"></span><span id="pipelinestage_rasterizer"></span>**PIPELINESTAGE\_RASTERIZER**</span></span>  
<span data-ttu-id="6e054-160">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-160">Not used.</span></span>

<span data-ttu-id="6e054-161"><span id="PIPELINESTAGE_PIXELSHADER"></span><span id="pipelinestage_pixelshader"></span>**PIPELINESTAGE \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="6e054-161"><span id="PIPELINESTAGE_PIXELSHADER"></span><span id="pipelinestage_pixelshader"></span>**PIPELINESTAGE\_PIXELSHADER**</span></span>  
<span data-ttu-id="6e054-162">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-162">Not used.</span></span>

<span data-ttu-id="6e054-163"><span id="PIPELINESTAGE_OUTPUTMERGER"></span><span id="pipelinestage_outputmerger"></span>**PIPELINESTAGE \_ OUTPUTMERGER**</span><span class="sxs-lookup"><span data-stu-id="6e054-163"><span id="PIPELINESTAGE_OUTPUTMERGER"></span><span id="pipelinestage_outputmerger"></span>**PIPELINESTAGE\_OUTPUTMERGER**</span></span>  
<span data-ttu-id="6e054-164">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-164">Not used.</span></span>

<span data-ttu-id="6e054-165"><span id="PIPELINESTAGE_COMPUTESHADER"></span><span id="pipelinestage_computeshader"></span>**PIPELINESTAGE \_ COMPUTESHADER**</span><span class="sxs-lookup"><span data-stu-id="6e054-165"><span id="PIPELINESTAGE_COMPUTESHADER"></span><span id="pipelinestage_computeshader"></span>**PIPELINESTAGE\_COMPUTESHADER**</span></span>  
<span data-ttu-id="6e054-166">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-166">Not used.</span></span>

<span data-ttu-id="6e054-167"><span id="BUFFEROBJECT_SUPPORTEDFORMAT"></span><span id="bufferobject_supportedformat"></span>**BUFFEROBJECT \_ SUPPORTEDFORMAT**</span><span class="sxs-lookup"><span data-stu-id="6e054-167"><span id="BUFFEROBJECT_SUPPORTEDFORMAT"></span><span id="bufferobject_supportedformat"></span>**BUFFEROBJECT\_SUPPORTEDFORMAT**</span></span>  
<span data-ttu-id="6e054-168">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-168">Not used.</span></span>

<span data-ttu-id="6e054-169"><span id="BUFFEROBJECT_CURRENTFORMAT"></span><span id="bufferobject_currentformat"></span>**BUFFEROBJECT \_ CURRENTFORMAT**</span><span class="sxs-lookup"><span data-stu-id="6e054-169"><span id="BUFFEROBJECT_CURRENTFORMAT"></span><span id="bufferobject_currentformat"></span>**BUFFEROBJECT\_CURRENTFORMAT**</span></span>  
<span data-ttu-id="6e054-170">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-170">Not used.</span></span>

<span data-ttu-id="6e054-171"><span id="BUFFEROBJECT_HEADER"></span><span id="bufferobject_header"></span>**BUFFEROBJECT \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="6e054-171"><span id="BUFFEROBJECT_HEADER"></span><span id="bufferobject_header"></span>**BUFFEROBJECT\_HEADER**</span></span>  
<span data-ttu-id="6e054-172">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-172">Not used.</span></span>

<span data-ttu-id="6e054-173"><span id="BUFFEROBJECT_LINE"></span><span id="bufferobject_line"></span>**BUFFEROBJECT \_ 行**</span><span class="sxs-lookup"><span data-stu-id="6e054-173"><span id="BUFFEROBJECT_LINE"></span><span id="bufferobject_line"></span>**BUFFEROBJECT\_LINE**</span></span>  
<span data-ttu-id="6e054-174">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-174">Not used.</span></span>

<span data-ttu-id="6e054-175"><span id="BUFFEROBJECT_INVALIDFORMAT"></span><span id="bufferobject_invalidformat"></span>**BUFFEROBJECT \_ INVALIDFORMAT**</span><span class="sxs-lookup"><span data-stu-id="6e054-175"><span id="BUFFEROBJECT_INVALIDFORMAT"></span><span id="bufferobject_invalidformat"></span>**BUFFEROBJECT\_INVALIDFORMAT**</span></span>  
<span data-ttu-id="6e054-176">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-176">Not used.</span></span>

<span data-ttu-id="6e054-177"><span id="BUFFEROBJECT_INVALIDEMPTYFORMAT"></span><span id="bufferobject_invalidemptyformat"></span>**BUFFEROBJECT \_ INVALIDEMPTYFORMAT**</span><span class="sxs-lookup"><span data-stu-id="6e054-177"><span id="BUFFEROBJECT_INVALIDEMPTYFORMAT"></span><span id="bufferobject_invalidemptyformat"></span>**BUFFEROBJECT\_INVALIDEMPTYFORMAT**</span></span>  
<span data-ttu-id="6e054-178">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-178">Not used.</span></span>

<span data-ttu-id="6e054-179"><span id="BUFFEROBJECT_INVALIDFORMATSIZE"></span><span id="bufferobject_invalidformatsize"></span>**BUFFEROBJECT \_ INVALIDFORMATSIZE**</span><span class="sxs-lookup"><span data-stu-id="6e054-179"><span id="BUFFEROBJECT_INVALIDFORMATSIZE"></span><span id="bufferobject_invalidformatsize"></span>**BUFFEROBJECT\_INVALIDFORMATSIZE**</span></span>  
<span data-ttu-id="6e054-180">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-180">Not used.</span></span>

<span data-ttu-id="6e054-181"><span id="SUMMARYINFO_TARGETAPPLICATION"></span><span id="summaryinfo_targetapplication"></span>**SUMMARYINFO \_ TARGETAPPLICATION**</span><span class="sxs-lookup"><span data-stu-id="6e054-181"><span id="SUMMARYINFO_TARGETAPPLICATION"></span><span id="summaryinfo_targetapplication"></span>**SUMMARYINFO\_TARGETAPPLICATION**</span></span>  
<span data-ttu-id="6e054-182">顯示在 [vsglog 屬性] 視窗中的文字-目標應用程式</span><span class="sxs-lookup"><span data-stu-id="6e054-182">Text shown in the vsglog properties window - Target Application</span></span>

<span data-ttu-id="6e054-183"><span id="SUMMARYINFO_PATH"></span><span id="summaryinfo_path"></span>**SUMMARYINFO \_ 路徑**</span><span class="sxs-lookup"><span data-stu-id="6e054-183"><span id="SUMMARYINFO_PATH"></span><span id="summaryinfo_path"></span>**SUMMARYINFO\_PATH**</span></span>  
<span data-ttu-id="6e054-184">Vsglog 屬性視窗-Path 中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-184">Text shown in the vsglog Properties window - Path</span></span>

<span data-ttu-id="6e054-185"><span id="SUMMARYINFO_TARGETVERSION"></span><span id="summaryinfo_targetversion"></span>**SUMMARYINFO \_ TARGETVERSION**</span><span class="sxs-lookup"><span data-stu-id="6e054-185"><span id="SUMMARYINFO_TARGETVERSION"></span><span id="summaryinfo_targetversion"></span>**SUMMARYINFO\_TARGETVERSION**</span></span>  
<span data-ttu-id="6e054-186">Vsglog 屬性視窗-目標版本中所顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-186">Text shown in the vsglog Properties window - Target Version</span></span>

<span data-ttu-id="6e054-187"><span id="SUMMARYINFO_LASTMODIFIEDDATE"></span><span id="summaryinfo_lastmodifieddate"></span>**SUMMARYINFO \_ LASTMODIFIEDDATE**</span><span class="sxs-lookup"><span data-stu-id="6e054-187"><span id="SUMMARYINFO_LASTMODIFIEDDATE"></span><span id="summaryinfo_lastmodifieddate"></span>**SUMMARYINFO\_LASTMODIFIEDDATE**</span></span>  
<span data-ttu-id="6e054-188">Vsglog 屬性視窗所顯示的文字-上次修改日期</span><span class="sxs-lookup"><span data-stu-id="6e054-188">Text shown in the vsglog Properties window - Last Modified Date</span></span>

<span data-ttu-id="6e054-189"><span id="SUMMARYINFO_PROCESSID"></span><span id="summaryinfo_processid"></span>**SUMMARYINFO \_ PROCESSID**</span><span class="sxs-lookup"><span data-stu-id="6e054-189"><span id="SUMMARYINFO_PROCESSID"></span><span id="summaryinfo_processid"></span>**SUMMARYINFO\_PROCESSID**</span></span>  
<span data-ttu-id="6e054-190">Vsglog 屬性視窗-進程識別碼中所顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-190">Text shown in the vsglog Properties window - Process ID</span></span>

<span data-ttu-id="6e054-191"><span id="SUMMARYINFO_EXPERIMENTFILE"></span><span id="summaryinfo_experimentfile"></span>**SUMMARYINFO \_ EXPERIMENTFILE**</span><span class="sxs-lookup"><span data-stu-id="6e054-191"><span id="SUMMARYINFO_EXPERIMENTFILE"></span><span id="summaryinfo_experimentfile"></span>**SUMMARYINFO\_EXPERIMENTFILE**</span></span>  
<span data-ttu-id="6e054-192">Vsglog 屬性視窗實驗檔案中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-192">Text shown in the vsglog Properties window - Experiment File</span></span>

<span data-ttu-id="6e054-193"><span id="SUMMARYINFO_RUNFILE"></span><span id="summaryinfo_runfile"></span>**SUMMARYINFO \_ RUNFILE**</span><span class="sxs-lookup"><span data-stu-id="6e054-193"><span id="SUMMARYINFO_RUNFILE"></span><span id="summaryinfo_runfile"></span>**SUMMARYINFO\_RUNFILE**</span></span>  
<span data-ttu-id="6e054-194">Vsglog 屬性視窗-Run 檔案中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-194">Text shown in the vsglog Properties window - Run File</span></span>

<span data-ttu-id="6e054-195"><span id="SUMMARYINFO_SIZE"></span><span id="summaryinfo_size"></span>**SUMMARYINFO \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="6e054-195"><span id="SUMMARYINFO_SIZE"></span><span id="summaryinfo_size"></span>**SUMMARYINFO\_SIZE**</span></span>  
<span data-ttu-id="6e054-196">Vsglog 中顯示的文字屬性視窗大小</span><span class="sxs-lookup"><span data-stu-id="6e054-196">Text shown in the vsglog Properties window - Size</span></span>

<span data-ttu-id="6e054-197"><span id="SUMMARYINFO_CREATEDBYPIXVERSION"></span><span id="summaryinfo_createdbypixversion"></span>**SUMMARYINFO \_ CREATEDBYPIXVERSION**</span><span class="sxs-lookup"><span data-stu-id="6e054-197"><span id="SUMMARYINFO_CREATEDBYPIXVERSION"></span><span id="summaryinfo_createdbypixversion"></span>**SUMMARYINFO\_CREATEDBYPIXVERSION**</span></span>  
<span data-ttu-id="6e054-198">Vsglog 屬性視窗所顯示的文字（依版本而建立）</span><span class="sxs-lookup"><span data-stu-id="6e054-198">Text shown in the vsglog Properties window - Created By Version</span></span>

<span data-ttu-id="6e054-199"><span id="SUMMARYINFO_SESSIONSTARTTIME"></span><span id="summaryinfo_sessionstarttime"></span>**SUMMARYINFO \_ SESSIONSTARTTIME**</span><span class="sxs-lookup"><span data-stu-id="6e054-199"><span id="SUMMARYINFO_SESSIONSTARTTIME"></span><span id="summaryinfo_sessionstarttime"></span>**SUMMARYINFO\_SESSIONSTARTTIME**</span></span>  
<span data-ttu-id="6e054-200">Vsglog 屬性視窗中顯示的文字-會話開始時間</span><span class="sxs-lookup"><span data-stu-id="6e054-200">Text shown in the vsglog Properties window - Session Start time</span></span>

<span data-ttu-id="6e054-201"><span id="SUMMARYINFO_SYSTEMINFORMATION"></span><span id="summaryinfo_systeminformation"></span>**SUMMARYINFO \_ SYSTEMINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="6e054-201"><span id="SUMMARYINFO_SYSTEMINFORMATION"></span><span id="summaryinfo_systeminformation"></span>**SUMMARYINFO\_SYSTEMINFORMATION**</span></span>  
<span data-ttu-id="6e054-202">Vsglog 屬性視窗系統資訊中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-202">Text shown in the vsglog Properties window - System Information</span></span>

<span data-ttu-id="6e054-203"><span id="SUMMARYINFO_PROCESSOR"></span><span id="summaryinfo_processor"></span>**SUMMARYINFO \_ 處理器**</span><span class="sxs-lookup"><span data-stu-id="6e054-203"><span id="SUMMARYINFO_PROCESSOR"></span><span id="summaryinfo_processor"></span>**SUMMARYINFO\_PROCESSOR**</span></span>  
<span data-ttu-id="6e054-204">Vsglog 屬性視窗-處理器中所顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-204">Text shown in the vsglog Properties window - Processor</span></span>

<span data-ttu-id="6e054-205"><span id="SUMMARYINFO_MEMORY"></span><span id="summaryinfo_memory"></span>**SUMMARYINFO \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="6e054-205"><span id="SUMMARYINFO_MEMORY"></span><span id="summaryinfo_memory"></span>**SUMMARYINFO\_MEMORY**</span></span>  
<span data-ttu-id="6e054-206">Vsglog 屬性視窗記憶體中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-206">Text shown in the vsglog Properties window - Memory</span></span>

<span data-ttu-id="6e054-207"><span id="SUMMARYINFO_OSVERSION"></span><span id="summaryinfo_osversion"></span>**SUMMARYINFO \_ OSVERSION**</span><span class="sxs-lookup"><span data-stu-id="6e054-207"><span id="SUMMARYINFO_OSVERSION"></span><span id="summaryinfo_osversion"></span>**SUMMARYINFO\_OSVERSION**</span></span>  
<span data-ttu-id="6e054-208">Vsglog 屬性視窗-OS 版本中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-208">Text shown in the vsglog Properties window - OS Version</span></span>

<span data-ttu-id="6e054-209"><span id="SUMMARYINFO_OSARCHITECTURE"></span><span id="summaryinfo_osarchitecture"></span>**SUMMARYINFO \_ OSARCHITECTURE**</span><span class="sxs-lookup"><span data-stu-id="6e054-209"><span id="SUMMARYINFO_OSARCHITECTURE"></span><span id="summaryinfo_osarchitecture"></span>**SUMMARYINFO\_OSARCHITECTURE**</span></span>  
<span data-ttu-id="6e054-210">Vsglog 屬性視窗-OS 架構中所顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-210">Text shown in the vsglog Properties window - OS Architecture</span></span>

<span data-ttu-id="6e054-211"><span id="SUMMARYINFO_TARGETAPPARCHITECTURE"></span><span id="summaryinfo_targetapparchitecture"></span>**SUMMARYINFO \_ TARGETAPPARCHITECTURE**</span><span class="sxs-lookup"><span data-stu-id="6e054-211"><span id="SUMMARYINFO_TARGETAPPARCHITECTURE"></span><span id="summaryinfo_targetapparchitecture"></span>**SUMMARYINFO\_TARGETAPPARCHITECTURE**</span></span>  
<span data-ttu-id="6e054-212">Vsglog 屬性視窗-目標應用程式架構中所顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-212">Text shown in the vsglog Properties window - Target App Architecture</span></span>

<span data-ttu-id="6e054-213"><span id="SUMMARYINFO_MAXHWFEATURELEVEL"></span><span id="summaryinfo_maxhwfeaturelevel"></span>**SUMMARYINFO \_ MAXHWFEATURELEVEL**</span><span class="sxs-lookup"><span data-stu-id="6e054-213"><span id="SUMMARYINFO_MAXHWFEATURELEVEL"></span><span id="summaryinfo_maxhwfeaturelevel"></span>**SUMMARYINFO\_MAXHWFEATURELEVEL**</span></span>  
<span data-ttu-id="6e054-214">Vsglog 屬性視窗中顯示的文字-最大硬體功能等級</span><span class="sxs-lookup"><span data-stu-id="6e054-214">Text shown in the vsglog Properties window - Max Hardware Feature Level</span></span>

<span data-ttu-id="6e054-215"><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES"></span><span id="summaryinfo_driverconcurrentcreates"></span>**SUMMARYINFO \_ DRIVERCONCURRENTCREATES**</span><span class="sxs-lookup"><span data-stu-id="6e054-215"><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES"></span><span id="summaryinfo_driverconcurrentcreates"></span>**SUMMARYINFO\_DRIVERCONCURRENTCREATES**</span></span>  
<span data-ttu-id="6e054-216">Vsglog 屬性視窗-驅動程式並行建立中所顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-216">Text shown in the vsglog Properties window - Driver Concurrent Creates</span></span>

<span data-ttu-id="6e054-217"><span id="SUMMARYINFO_DRIVERCOMMANDLISTS"></span><span id="summaryinfo_drivercommandlists"></span>**SUMMARYINFO \_ DRIVERCOMMANDLISTS**</span><span class="sxs-lookup"><span data-stu-id="6e054-217"><span id="SUMMARYINFO_DRIVERCOMMANDLISTS"></span><span id="summaryinfo_drivercommandlists"></span>**SUMMARYINFO\_DRIVERCOMMANDLISTS**</span></span>  
<span data-ttu-id="6e054-218">Vsglog 屬性視窗驅動程式命令清單中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-218">Text shown in the vsglog Properties window - Driver Command Lists</span></span>

<span data-ttu-id="6e054-219"><span id="SUMMARYINFO_DOUBLEPRECISIONSHADERS"></span><span id="summaryinfo_doubleprecisionshaders"></span>**SUMMARYINFO \_ DOUBLEPRECISIONSHADERS**</span><span class="sxs-lookup"><span data-stu-id="6e054-219"><span id="SUMMARYINFO_DOUBLEPRECISIONSHADERS"></span><span id="summaryinfo_doubleprecisionshaders"></span>**SUMMARYINFO\_DOUBLEPRECISIONSHADERS**</span></span>  
<span data-ttu-id="6e054-220">Vsglog 屬性視窗-雙精確度著色器中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-220">Text shown in the vsglog Properties window - Double Precision Shaders</span></span>

<span data-ttu-id="6e054-221"><span id="SUMMARYINFO_DIRECTCOMPUTECS4X"></span><span id="summaryinfo_directcomputecs4x"></span>**SUMMARYINFO \_ DIRECTCOMPUTECS4X**</span><span class="sxs-lookup"><span data-stu-id="6e054-221"><span id="SUMMARYINFO_DIRECTCOMPUTECS4X"></span><span id="summaryinfo_directcomputecs4x"></span>**SUMMARYINFO\_DIRECTCOMPUTECS4X**</span></span>  
<span data-ttu-id="6e054-222">Vsglog 屬性視窗-Direct Compute CS 4.x 中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-222">Text shown in the vsglog Properties window - Direct Compute CS 4.x</span></span>

<span data-ttu-id="6e054-223"><span id="SUMMARYINFO_10BITXRHIGHCOLORFORMAT"></span><span id="summaryinfo_10bitxrhighcolorformat"></span>**SUMMARYINFO \_ 10BITXRHIGHCOLORFORMAT**</span><span class="sxs-lookup"><span data-stu-id="6e054-223"><span id="SUMMARYINFO_10BITXRHIGHCOLORFORMAT"></span><span id="summaryinfo_10bitxrhighcolorformat"></span>**SUMMARYINFO\_10BITXRHIGHCOLORFORMAT**</span></span>  
<span data-ttu-id="6e054-224">Vsglog 屬性視窗-10BITXRHIGHCOLORFORMAT 中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-224">Text shown in the vsglog Properties window - 10BITXRHIGHCOLORFORMAT</span></span>

<span data-ttu-id="6e054-225"><span id="SUMMARYINFO_EXTENDEDCOLORFORMATSUPPORT"></span><span id="summaryinfo_extendedcolorformatsupport"></span>**SUMMARYINFO \_ EXTENDEDCOLORFORMATSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="6e054-225"><span id="SUMMARYINFO_EXTENDEDCOLORFORMATSUPPORT"></span><span id="summaryinfo_extendedcolorformatsupport"></span>**SUMMARYINFO\_EXTENDEDCOLORFORMATSUPPORT**</span></span>  
<span data-ttu-id="6e054-226">Vsglog 中顯示的文字屬性視窗-擴充的色彩格式支援</span><span class="sxs-lookup"><span data-stu-id="6e054-226">Text shown in the vsglog Properties window - Extended Color Format Support</span></span>

<span data-ttu-id="6e054-227"><span id="SUMMARYINFO_DISPLAYINFORMATION"></span><span id="summaryinfo_displayinformation"></span>**SUMMARYINFO \_ DISPLAYINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="6e054-227"><span id="SUMMARYINFO_DISPLAYINFORMATION"></span><span id="summaryinfo_displayinformation"></span>**SUMMARYINFO\_DISPLAYINFORMATION**</span></span>  
<span data-ttu-id="6e054-228">Vsglog 屬性視窗顯示資訊中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-228">Text shown in the vsglog Properties window - Display Information</span></span>

<span data-ttu-id="6e054-229"><span id="SUMMARYINFO_DISPLAYNINFORMATION"></span><span id="summaryinfo_displayninformation"></span>**SUMMARYINFO \_ DISPLAYNINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="6e054-229"><span id="SUMMARYINFO_DISPLAYNINFORMATION"></span><span id="summaryinfo_displayninformation"></span>**SUMMARYINFO\_DISPLAYNINFORMATION**</span></span>  
<span data-ttu-id="6e054-230">Vsglog 中顯示的文字屬性視窗-顯示 N 資訊</span><span class="sxs-lookup"><span data-stu-id="6e054-230">Text shown in the vsglog Properties window - Display N Information</span></span>

<span data-ttu-id="6e054-231"><span id="SUMMARYINFO_NAME"></span><span id="summaryinfo_name"></span>**SUMMARYINFO \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="6e054-231"><span id="SUMMARYINFO_NAME"></span><span id="summaryinfo_name"></span>**SUMMARYINFO\_NAME**</span></span>  
<span data-ttu-id="6e054-232">Vsglog 屬性視窗名稱中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-232">Text shown in the vsglog Properties window - Name</span></span>

<span data-ttu-id="6e054-233"><span id="SUMMARYINFO_DESCRIPTION"></span><span id="summaryinfo_description"></span>**SUMMARYINFO \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="6e054-233"><span id="SUMMARYINFO_DESCRIPTION"></span><span id="summaryinfo_description"></span>**SUMMARYINFO\_DESCRIPTION**</span></span>  
<span data-ttu-id="6e054-234">Vsglog 中顯示的文字屬性視窗-Description</span><span class="sxs-lookup"><span data-stu-id="6e054-234">Text shown in the vsglog Properties window - Description</span></span>

<span data-ttu-id="6e054-235"><span id="SUMMARYINFO_DISPLAYMEMORY"></span><span id="summaryinfo_displaymemory"></span>**SUMMARYINFO \_ DISPLAYMEMORY**</span><span class="sxs-lookup"><span data-stu-id="6e054-235"><span id="SUMMARYINFO_DISPLAYMEMORY"></span><span id="summaryinfo_displaymemory"></span>**SUMMARYINFO\_DISPLAYMEMORY**</span></span>  
<span data-ttu-id="6e054-236">Vsglog 屬性視窗顯示的文字顯示記憶體</span><span class="sxs-lookup"><span data-stu-id="6e054-236">Text shown in the vsglog Properties window - Display Memory</span></span>

<span data-ttu-id="6e054-237"><span id="SUMMARYINFO_DRIVERNAME"></span><span id="summaryinfo_drivername"></span>**SUMMARYINFO \_ DRIVERNAME**</span><span class="sxs-lookup"><span data-stu-id="6e054-237"><span id="SUMMARYINFO_DRIVERNAME"></span><span id="summaryinfo_drivername"></span>**SUMMARYINFO\_DRIVERNAME**</span></span>  
<span data-ttu-id="6e054-238">Vsglog 屬性視窗-驅動程式名稱中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-238">Text shown in the vsglog Properties window - Driver Name</span></span>

<span data-ttu-id="6e054-239"><span id="SUMMARYINFO_DRIVERVERSION"></span><span id="summaryinfo_driverversion"></span>**SUMMARYINFO \_ DRIVERVERSION**</span><span class="sxs-lookup"><span data-stu-id="6e054-239"><span id="SUMMARYINFO_DRIVERVERSION"></span><span id="summaryinfo_driverversion"></span>**SUMMARYINFO\_DRIVERVERSION**</span></span>  
<span data-ttu-id="6e054-240">Vsglog 屬性視窗-驅動程式版本中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-240">Text shown in the vsglog Properties window - Driver Version</span></span>

<span data-ttu-id="6e054-241"><span id="SUMMARYINFO_MODULEINFORMATION"></span><span id="summaryinfo_moduleinformation"></span>**SUMMARYINFO \_ MODULEINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="6e054-241"><span id="SUMMARYINFO_MODULEINFORMATION"></span><span id="summaryinfo_moduleinformation"></span>**SUMMARYINFO\_MODULEINFORMATION**</span></span>  
<span data-ttu-id="6e054-242">Vsglog 屬性視窗模組資訊中所顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-242">Text shown in the vsglog Properties window - Module Information</span></span>

<span data-ttu-id="6e054-243"><span id="SUMMARYINFO_DIRECT3DINFORMATION"></span><span id="summaryinfo_direct3dinformation"></span>**SUMMARYINFO \_ DIRECT3DINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="6e054-243"><span id="SUMMARYINFO_DIRECT3DINFORMATION"></span><span id="summaryinfo_direct3dinformation"></span>**SUMMARYINFO\_DIRECT3DINFORMATION**</span></span>  
<span data-ttu-id="6e054-244">Vsglog 屬性視窗-Direct3D 資訊中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-244">Text shown in the vsglog Properties window - Direct3D Information</span></span>

<span data-ttu-id="6e054-245"><span id="SUMMARYINFO_VSGVERSION"></span><span id="summaryinfo_vsgversion"></span>**SUMMARYINFO \_ VSGVERSION**</span><span class="sxs-lookup"><span data-stu-id="6e054-245"><span id="SUMMARYINFO_VSGVERSION"></span><span id="summaryinfo_vsgversion"></span>**SUMMARYINFO\_VSGVERSION**</span></span>  
<span data-ttu-id="6e054-246">Vsglog 屬性視窗-VSG 版本中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-246">Text shown in the vsglog Properties window - VSG Version</span></span>

<span data-ttu-id="6e054-247"><span id="SUMMARYINFO_CAPTUREMACHINE"></span><span id="summaryinfo_capturemachine"></span>**SUMMARYINFO \_ CAPTUREMACHINE**</span><span class="sxs-lookup"><span data-stu-id="6e054-247"><span id="SUMMARYINFO_CAPTUREMACHINE"></span><span id="summaryinfo_capturemachine"></span>**SUMMARYINFO\_CAPTUREMACHINE**</span></span>  
<span data-ttu-id="6e054-248">Vsglog 屬性視窗-Capture 電腦中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-248">Text shown in the vsglog Properties window - Capture Machine</span></span>

<span data-ttu-id="6e054-249"><span id="SUMMARYINFO_PLAYBACKMACHINE"></span><span id="summaryinfo_playbackmachine"></span>**SUMMARYINFO \_ PLAYBACKMACHINE**</span><span class="sxs-lookup"><span data-stu-id="6e054-249"><span id="SUMMARYINFO_PLAYBACKMACHINE"></span><span id="summaryinfo_playbackmachine"></span>**SUMMARYINFO\_PLAYBACKMACHINE**</span></span>  
<span data-ttu-id="6e054-250">Vsglog 屬性視窗播放電腦所顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-250">Text shown in the vsglog Properties window - Playback Machine</span></span>

<span data-ttu-id="6e054-251"><span id="SUMMARYINFO_REMOTEDATA"></span><span id="summaryinfo_remotedata"></span>**SUMMARYINFO \_ REMOTEDATA**</span><span class="sxs-lookup"><span data-stu-id="6e054-251"><span id="SUMMARYINFO_REMOTEDATA"></span><span id="summaryinfo_remotedata"></span>**SUMMARYINFO\_REMOTEDATA**</span></span>  
<span data-ttu-id="6e054-252">Vsglog 屬性視窗-遠端資料中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-252">Text shown in the vsglog Properties window - Remote Data</span></span>

<span data-ttu-id="6e054-253"><span id="SUMMARYINFO_OtherDirect3DInformation"></span><span id="summaryinfo_otherdirect3dinformation"></span><span id="SUMMARYINFO_OTHERDIRECT3DINFORMATION"></span>**SUMMARYINFO \_ OtherDirect3DInformation**</span><span class="sxs-lookup"><span data-stu-id="6e054-253"><span id="SUMMARYINFO_OtherDirect3DInformation"></span><span id="summaryinfo_otherdirect3dinformation"></span><span id="SUMMARYINFO_OTHERDIRECT3DINFORMATION"></span>**SUMMARYINFO\_OtherDirect3DInformation**</span></span>  
<span data-ttu-id="6e054-254">Vsglog 屬性視窗中顯示的文字-其他 Direct3D 資訊</span><span class="sxs-lookup"><span data-stu-id="6e054-254">Text shown in the vsglog Properties window - Other Direct3D Information</span></span>

<span data-ttu-id="6e054-255"><span id="SUMMARYINFO_SIZEGB"></span><span id="summaryinfo_sizegb"></span>**SUMMARYINFO \_ SIZEGB**</span><span class="sxs-lookup"><span data-stu-id="6e054-255"><span id="SUMMARYINFO_SIZEGB"></span><span id="summaryinfo_sizegb"></span>**SUMMARYINFO\_SIZEGB**</span></span>  
<span data-ttu-id="6e054-256">Vsglog 中顯示的文字屬性視窗大小 GB</span><span class="sxs-lookup"><span data-stu-id="6e054-256">Text shown in the vsglog Properties window - Size GB</span></span>

<span data-ttu-id="6e054-257"><span id="SUMMARYINFO_SIZEMB"></span><span id="summaryinfo_sizemb"></span>**SUMMARYINFO \_ SIZEMB**</span><span class="sxs-lookup"><span data-stu-id="6e054-257"><span id="SUMMARYINFO_SIZEMB"></span><span id="summaryinfo_sizemb"></span>**SUMMARYINFO\_SIZEMB**</span></span>  
<span data-ttu-id="6e054-258">Vsglog 中顯示的文字屬性視窗大小 MB</span><span class="sxs-lookup"><span data-stu-id="6e054-258">Text shown in the vsglog Properties window - Size MB</span></span>

<span data-ttu-id="6e054-259"><span id="SUMMARYINFO_SIZEBYTES"></span><span id="summaryinfo_sizebytes"></span>**SUMMARYINFO \_ SIZEBYTES**</span><span class="sxs-lookup"><span data-stu-id="6e054-259"><span id="SUMMARYINFO_SIZEBYTES"></span><span id="summaryinfo_sizebytes"></span>**SUMMARYINFO\_SIZEBYTES**</span></span>  
<span data-ttu-id="6e054-260">Vsglog 中顯示的文字屬性視窗大小位元組</span><span class="sxs-lookup"><span data-stu-id="6e054-260">Text shown in the vsglog Properties window - Size Bytes</span></span>

<span data-ttu-id="6e054-261"><span id="SUMMARYINFO_MEMORYMB"></span><span id="summaryinfo_memorymb"></span>**SUMMARYINFO \_ MEMORYMB**</span><span class="sxs-lookup"><span data-stu-id="6e054-261"><span id="SUMMARYINFO_MEMORYMB"></span><span id="summaryinfo_memorymb"></span>**SUMMARYINFO\_MEMORYMB**</span></span>  
<span data-ttu-id="6e054-262">Vsglog 中顯示的文字屬性視窗記憶體 MB</span><span class="sxs-lookup"><span data-stu-id="6e054-262">Text shown in the vsglog Properties window - Memory MB</span></span>

<span data-ttu-id="6e054-263"><span id="SUMMARYINFO_X86"></span><span id="summaryinfo_x86"></span>**SUMMARYINFO \_ X86**</span><span class="sxs-lookup"><span data-stu-id="6e054-263"><span id="SUMMARYINFO_X86"></span><span id="summaryinfo_x86"></span>**SUMMARYINFO\_X86**</span></span>  
<span data-ttu-id="6e054-264">Vsglog 屬性視窗中顯示的文字-X86</span><span class="sxs-lookup"><span data-stu-id="6e054-264">Text shown in the vsglog Properties window - X86</span></span>

<span data-ttu-id="6e054-265"><span id="SUMMARYINFO_X64"></span><span id="summaryinfo_x64"></span>**SUMMARYINFO \_ X64**</span><span class="sxs-lookup"><span data-stu-id="6e054-265"><span id="SUMMARYINFO_X64"></span><span id="summaryinfo_x64"></span>**SUMMARYINFO\_X64**</span></span>  
<span data-ttu-id="6e054-266">Vsglog 屬性視窗-X64 中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-266">Text shown in the vsglog Properties window - X64</span></span>

<span data-ttu-id="6e054-267"><span id="SUMMARYINFO_TRUE"></span><span id="summaryinfo_true"></span>**SUMMARYINFO \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="6e054-267"><span id="SUMMARYINFO_TRUE"></span><span id="summaryinfo_true"></span>**SUMMARYINFO\_TRUE**</span></span>  
<span data-ttu-id="6e054-268">Vsglog 屬性視窗-True 中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-268">Text shown in the vsglog Properties window - True</span></span>

<span data-ttu-id="6e054-269"><span id="SUMMARYINFO_FALSE"></span><span id="summaryinfo_false"></span>**SUMMARYINFO \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="6e054-269"><span id="SUMMARYINFO_FALSE"></span><span id="summaryinfo_false"></span>**SUMMARYINFO\_FALSE**</span></span>  
<span data-ttu-id="6e054-270">Vsglog 中顯示的文字屬性視窗-False</span><span class="sxs-lookup"><span data-stu-id="6e054-270">Text shown in the vsglog Properties window - False</span></span>

<span data-ttu-id="6e054-271"><span id="SUMMARYINFO_ARM32"></span><span id="summaryinfo_arm32"></span>**SUMMARYINFO \_ ARM32**</span><span class="sxs-lookup"><span data-stu-id="6e054-271"><span id="SUMMARYINFO_ARM32"></span><span id="summaryinfo_arm32"></span>**SUMMARYINFO\_ARM32**</span></span>  
<span data-ttu-id="6e054-272">Vsglog 屬性視窗-ARM 32 中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-272">Text shown in the vsglog Properties window - ARM 32</span></span>

<span data-ttu-id="6e054-273"><span id="SUMMARYINFO_UNKNOWNCPUARCHITECTURE"></span><span id="summaryinfo_unknowncpuarchitecture"></span>**SUMMARYINFO \_ UNKNOWNCPUARCHITECTURE**</span><span class="sxs-lookup"><span data-stu-id="6e054-273"><span id="SUMMARYINFO_UNKNOWNCPUARCHITECTURE"></span><span id="summaryinfo_unknowncpuarchitecture"></span>**SUMMARYINFO\_UNKNOWNCPUARCHITECTURE**</span></span>  
<span data-ttu-id="6e054-274">Vsglog 屬性視窗中顯示的文字-未知的 CPU 架構</span><span class="sxs-lookup"><span data-stu-id="6e054-274">Text shown in the vsglog Properties window - Unknown CPU Architecture</span></span>

<span data-ttu-id="6e054-275"><span id="SUMMARYINFO_AllDXGIFormatValues"></span><span id="summaryinfo_alldxgiformatvalues"></span><span id="SUMMARYINFO_ALLDXGIFORMATVALUES"></span>**SUMMARYINFO \_ AllDXGIFormatValues**</span><span class="sxs-lookup"><span data-stu-id="6e054-275"><span id="SUMMARYINFO_AllDXGIFormatValues"></span><span id="summaryinfo_alldxgiformatvalues"></span><span id="SUMMARYINFO_ALLDXGIFORMATVALUES"></span>**SUMMARYINFO\_AllDXGIFormatValues**</span></span>  
<span data-ttu-id="6e054-276">Vsglog 屬性視窗中顯示的文字-所有 DXGI 格式值</span><span class="sxs-lookup"><span data-stu-id="6e054-276">Text shown in the vsglog Properties window - All DXGI Format Values</span></span>

<span data-ttu-id="6e054-277"><span id="SUMMARYINFO_AllD3D11FormatSupportValues"></span><span id="summaryinfo_alld3d11formatsupportvalues"></span><span id="SUMMARYINFO_ALLD3D11FORMATSUPPORTVALUES"></span>**SUMMARYINFO \_ AllD3D11FormatSupportValues**</span><span class="sxs-lookup"><span data-stu-id="6e054-277"><span id="SUMMARYINFO_AllD3D11FormatSupportValues"></span><span id="summaryinfo_alld3d11formatsupportvalues"></span><span id="SUMMARYINFO_ALLD3D11FORMATSUPPORTVALUES"></span>**SUMMARYINFO\_AllD3D11FormatSupportValues**</span></span>  
<span data-ttu-id="6e054-278">Vsglog 屬性視窗中顯示的文字-所有 D3D11 格式支援值</span><span class="sxs-lookup"><span data-stu-id="6e054-278">Text shown in the vsglog Properties window - All D3D11 Format Support Values</span></span>

<span data-ttu-id="6e054-279"><span id="SUMMARYINFO_D3D11_FEATURE_THREADING"></span><span id="summaryinfo_d3d11_feature_threading"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ 執行緒**</span><span class="sxs-lookup"><span data-stu-id="6e054-279"><span id="SUMMARYINFO_D3D11_FEATURE_THREADING"></span><span id="summaryinfo_d3d11_feature_threading"></span>**SUMMARYINFO\_D3D11\_FEATURE\_THREADING**</span></span>  
<span data-ttu-id="6e054-280">Vsglog 屬性視窗-D3D11 \_ 功能執行緒中顯示的 \_ 文字</span><span class="sxs-lookup"><span data-stu-id="6e054-280">Text shown in the vsglog Properties window - D3D11\_FEATURE\_THREADING</span></span>

<span data-ttu-id="6e054-281"><span id="SUMMARYINFO_DriverConcurrentCreates1"></span><span id="summaryinfo_driverconcurrentcreates1"></span><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES1"></span>**SUMMARYINFO \_ DriverConcurrentCreates1**</span><span class="sxs-lookup"><span data-stu-id="6e054-281"><span id="SUMMARYINFO_DriverConcurrentCreates1"></span><span id="summaryinfo_driverconcurrentcreates1"></span><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES1"></span>**SUMMARYINFO\_DriverConcurrentCreates1**</span></span>  
<span data-ttu-id="6e054-282">Vsglog 屬性視窗-驅動程式中顯示的文字會並行建立1</span><span class="sxs-lookup"><span data-stu-id="6e054-282">Text shown in the vsglog Properties window - Driver Concurrent Creates 1</span></span>

<span data-ttu-id="6e054-283"><span id="SUMMARYINFO_DriverCommandLists1"></span><span id="summaryinfo_drivercommandlists1"></span><span id="SUMMARYINFO_DRIVERCOMMANDLISTS1"></span>**SUMMARYINFO \_ DriverCommandLists1**</span><span class="sxs-lookup"><span data-stu-id="6e054-283"><span id="SUMMARYINFO_DriverCommandLists1"></span><span id="summaryinfo_drivercommandlists1"></span><span id="SUMMARYINFO_DRIVERCOMMANDLISTS1"></span>**SUMMARYINFO\_DriverCommandLists1**</span></span>  
<span data-ttu-id="6e054-284">Vsglog 屬性視窗驅動程式命令中顯示的文字清單1</span><span class="sxs-lookup"><span data-stu-id="6e054-284">Text shown in the vsglog Properties window - Driver Command Lists 1</span></span>

<span data-ttu-id="6e054-285"><span id="SUMMARYINFO_D3D11_FEATURE_DOUBLES"></span><span id="summaryinfo_d3d11_feature_doubles"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ 雙精度浮點數**</span><span class="sxs-lookup"><span data-stu-id="6e054-285"><span id="SUMMARYINFO_D3D11_FEATURE_DOUBLES"></span><span id="summaryinfo_d3d11_feature_doubles"></span>**SUMMARYINFO\_D3D11\_FEATURE\_DOUBLES**</span></span>  
<span data-ttu-id="6e054-286">Vsglog 屬性視窗-D3D11 功能中所顯示的文字 \_ \_ 雙精度浮點數</span><span class="sxs-lookup"><span data-stu-id="6e054-286">Text shown in the vsglog Properties window - D3D11\_FEATURE\_DOUBLES</span></span>

<span data-ttu-id="6e054-287"><span id="SUMMARYINFO_DoublePrecisionFloatShaderOps"></span><span id="summaryinfo_doubleprecisionfloatshaderops"></span><span id="SUMMARYINFO_DOUBLEPRECISIONFLOATSHADEROPS"></span>**SUMMARYINFO \_ DoublePrecisionFloatShaderOps**</span><span class="sxs-lookup"><span data-stu-id="6e054-287"><span id="SUMMARYINFO_DoublePrecisionFloatShaderOps"></span><span id="summaryinfo_doubleprecisionfloatshaderops"></span><span id="SUMMARYINFO_DOUBLEPRECISIONFLOATSHADEROPS"></span>**SUMMARYINFO\_DoublePrecisionFloatShaderOps**</span></span>  
<span data-ttu-id="6e054-288">Vsglog 屬性視窗-雙精確度浮點數著色器 Ops 中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-288">Text shown in the vsglog Properties window - Double Precision Float Shader Ops</span></span>

<span data-ttu-id="6e054-289"><span id="SUMMARYINFO_D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d10_x_hardware_options"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D10 \_ X \_ 硬體 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="6e054-289"><span id="SUMMARYINFO_D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d10_x_hardware_options"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D10\_X\_HARDWARE\_OPTIONS**</span></span>  
<span data-ttu-id="6e054-290">Vsglog 屬性視窗-D3D11 \_ FEATURE \_ D3D10 \_ X \_ 硬體 \_ 選項中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-290">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D10\_X\_HARDWARE\_OPTIONS</span></span>

<span data-ttu-id="6e054-291"><span id="SUMMARYINFO_ComputeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x"></span><span id="summaryinfo_computeshaders_plus_rawandstructuredbuffers_via_shader_4_x"></span><span id="SUMMARYINFO_COMPUTESHADERS_PLUS_RAWANDSTRUCTUREDBUFFERS_VIA_SHADER_4_X"></span>**SUMMARYINFO \_ ComputeShaders \_ Plus \_ RawAndStructuredBuffers \_ Via \_ 著色器 \_ 4 \_ x**</span><span class="sxs-lookup"><span data-stu-id="6e054-291"><span id="SUMMARYINFO_ComputeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x"></span><span id="summaryinfo_computeshaders_plus_rawandstructuredbuffers_via_shader_4_x"></span><span id="SUMMARYINFO_COMPUTESHADERS_PLUS_RAWANDSTRUCTUREDBUFFERS_VIA_SHADER_4_X"></span>**SUMMARYINFO\_ComputeShaders\_Plus\_RawAndStructuredBuffers\_Via\_Shader\_4\_x**</span></span>  
<span data-ttu-id="6e054-292">Vsglog 中所顯示的文字屬性視窗-ComputeShaders + Raw 和 Structure dBuffers via 著色器4。x</span><span class="sxs-lookup"><span data-stu-id="6e054-292">Text shown in the vsglog Properties window - ComputeShaders + Raw and Structure dBuffers via Shader 4.x</span></span>

<span data-ttu-id="6e054-293"><span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d11_options"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ D3D11 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="6e054-293"><span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d11_options"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D11\_OPTIONS**</span></span>  
<span data-ttu-id="6e054-294">Vsglog 屬性視窗-D3D11 \_ 功能 \_ D3D11 \_ 選項中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-294">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D11\_OPTIONS</span></span>

<span data-ttu-id="6e054-295"><span id="SUMMARYINFO_OutputMergerLogicOp"></span><span id="summaryinfo_outputmergerlogicop"></span><span id="SUMMARYINFO_OUTPUTMERGERLOGICOP"></span>**SUMMARYINFO \_ OutputMergerLogicOp**</span><span class="sxs-lookup"><span data-stu-id="6e054-295"><span id="SUMMARYINFO_OutputMergerLogicOp"></span><span id="summaryinfo_outputmergerlogicop"></span><span id="SUMMARYINFO_OUTPUTMERGERLOGICOP"></span>**SUMMARYINFO\_OutputMergerLogicOp**</span></span>  
<span data-ttu-id="6e054-296">Vsglog 屬性視窗輸出合併邏輯 Op 中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-296">Text shown in the vsglog Properties window - Output Merger Logic Op</span></span>

<span data-ttu-id="6e054-297"><span id="SUMMARYINFO_UAVOnlyRenderingForcedSampleCount"></span><span id="summaryinfo_uavonlyrenderingforcedsamplecount"></span><span id="SUMMARYINFO_UAVONLYRENDERINGFORCEDSAMPLECOUNT"></span>**SUMMARYINFO \_ UAVOnlyRenderingForcedSampleCount**</span><span class="sxs-lookup"><span data-stu-id="6e054-297"><span id="SUMMARYINFO_UAVOnlyRenderingForcedSampleCount"></span><span id="summaryinfo_uavonlyrenderingforcedsamplecount"></span><span id="SUMMARYINFO_UAVONLYRENDERINGFORCEDSAMPLECOUNT"></span>**SUMMARYINFO\_UAVOnlyRenderingForcedSampleCount**</span></span>  
<span data-ttu-id="6e054-298">Vsglog 中所顯示的文字屬性視窗-UAV 只轉譯強制取樣計數</span><span class="sxs-lookup"><span data-stu-id="6e054-298">Text shown in the vsglog Properties window - UAV Only Rendering Forced Sample Count</span></span>

<span data-ttu-id="6e054-299"><span id="SUMMARYINFO_DiscardAPIsSeenByDriver"></span><span id="summaryinfo_discardapisseenbydriver"></span><span id="SUMMARYINFO_DISCARDAPISSEENBYDRIVER"></span>**SUMMARYINFO \_ DiscardAPIsSeenByDriver**</span><span class="sxs-lookup"><span data-stu-id="6e054-299"><span id="SUMMARYINFO_DiscardAPIsSeenByDriver"></span><span id="summaryinfo_discardapisseenbydriver"></span><span id="SUMMARYINFO_DISCARDAPISSEENBYDRIVER"></span>**SUMMARYINFO\_DiscardAPIsSeenByDriver**</span></span>  
<span data-ttu-id="6e054-300">Vsglog 中顯示的文字屬性視窗-捨棄驅動程式所見的 Api</span><span class="sxs-lookup"><span data-stu-id="6e054-300">Text shown in the vsglog Properties window - Discard APIs Seen By Driver</span></span>

<span data-ttu-id="6e054-301"><span id="SUMMARYINFO_FlagsForUpdateAndCopySeenByDriver"></span><span id="summaryinfo_flagsforupdateandcopyseenbydriver"></span><span id="SUMMARYINFO_FLAGSFORUPDATEANDCOPYSEENBYDRIVER"></span>**SUMMARYINFO \_ FlagsForUpdateAndCopySeenByDriver**</span><span class="sxs-lookup"><span data-stu-id="6e054-301"><span id="SUMMARYINFO_FlagsForUpdateAndCopySeenByDriver"></span><span id="summaryinfo_flagsforupdateandcopyseenbydriver"></span><span id="SUMMARYINFO_FLAGSFORUPDATEANDCOPYSEENBYDRIVER"></span>**SUMMARYINFO\_FlagsForUpdateAndCopySeenByDriver**</span></span>  
<span data-ttu-id="6e054-302">Vsglog 中顯示的文字屬性視窗-驅動程式所見的更新和複製的旗標</span><span class="sxs-lookup"><span data-stu-id="6e054-302">Text shown in the vsglog Properties window - Flags For Update And Copy Seen By Driver</span></span>

<span data-ttu-id="6e054-303"><span id="SUMMARYINFO_ClearView"></span><span id="summaryinfo_clearview"></span><span id="SUMMARYINFO_CLEARVIEW"></span>**SUMMARYINFO \_ ClearView**</span><span class="sxs-lookup"><span data-stu-id="6e054-303"><span id="SUMMARYINFO_ClearView"></span><span id="summaryinfo_clearview"></span><span id="SUMMARYINFO_CLEARVIEW"></span>**SUMMARYINFO\_ClearView**</span></span>  
<span data-ttu-id="6e054-304">Vsglog 屬性視窗清除視圖中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-304">Text shown in the vsglog Properties window - Clear View</span></span>

<span data-ttu-id="6e054-305"><span id="SUMMARYINFO_CopyWithOverlap"></span><span id="summaryinfo_copywithoverlap"></span><span id="SUMMARYINFO_COPYWITHOVERLAP"></span>**SUMMARYINFO \_ CopyWithOverlap**</span><span class="sxs-lookup"><span data-stu-id="6e054-305"><span id="SUMMARYINFO_CopyWithOverlap"></span><span id="summaryinfo_copywithoverlap"></span><span id="SUMMARYINFO_COPYWITHOVERLAP"></span>**SUMMARYINFO\_CopyWithOverlap**</span></span>  
<span data-ttu-id="6e054-306">Vsglog 中顯示的文字屬性視窗-與重迭的複製</span><span class="sxs-lookup"><span data-stu-id="6e054-306">Text shown in the vsglog Properties window - Copy With Overlap</span></span>

<span data-ttu-id="6e054-307"><span id="SUMMARYINFO_ConstantBufferPartialUpdate"></span><span id="summaryinfo_constantbufferpartialupdate"></span><span id="SUMMARYINFO_CONSTANTBUFFERPARTIALUPDATE"></span>**SUMMARYINFO \_ ConstantBufferPartialUpdate**</span><span class="sxs-lookup"><span data-stu-id="6e054-307"><span id="SUMMARYINFO_ConstantBufferPartialUpdate"></span><span id="summaryinfo_constantbufferpartialupdate"></span><span id="SUMMARYINFO_CONSTANTBUFFERPARTIALUPDATE"></span>**SUMMARYINFO\_ConstantBufferPartialUpdate**</span></span>  
<span data-ttu-id="6e054-308">Vsglog 屬性視窗常數緩衝區部分更新中所顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-308">Text shown in the vsglog Properties window - Constant Buffer Partial Update</span></span>

<span data-ttu-id="6e054-309"><span id="SUMMARYINFO_ConstantBufferOffsetting"></span><span id="summaryinfo_constantbufferoffsetting"></span><span id="SUMMARYINFO_CONSTANTBUFFEROFFSETTING"></span>**SUMMARYINFO \_ ConstantBufferOffsetting**</span><span class="sxs-lookup"><span data-stu-id="6e054-309"><span id="SUMMARYINFO_ConstantBufferOffsetting"></span><span id="summaryinfo_constantbufferoffsetting"></span><span id="SUMMARYINFO_CONSTANTBUFFEROFFSETTING"></span>**SUMMARYINFO\_ConstantBufferOffsetting**</span></span>  
<span data-ttu-id="6e054-310">Vsglog 中所顯示的文字屬性視窗常數緩衝區偏移</span><span class="sxs-lookup"><span data-stu-id="6e054-310">Text shown in the vsglog Properties window - Constant Buffer Offsetting</span></span>

<span data-ttu-id="6e054-311"><span id="SUMMARYINFO_MapNoOverwriteOnDynamicConstantBuffer"></span><span id="summaryinfo_mapnooverwriteondynamicconstantbuffer"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICCONSTANTBUFFER"></span>**SUMMARYINFO \_ MapNoOverwriteOnDynamicConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="6e054-311"><span id="SUMMARYINFO_MapNoOverwriteOnDynamicConstantBuffer"></span><span id="summaryinfo_mapnooverwriteondynamicconstantbuffer"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICCONSTANTBUFFER"></span>**SUMMARYINFO\_MapNoOverwriteOnDynamicConstantBuffer**</span></span>  
<span data-ttu-id="6e054-312">Vsglog 中所顯示的文字屬性視窗-不會在動態常數緩衝區上進行覆寫</span><span class="sxs-lookup"><span data-stu-id="6e054-312">Text shown in the vsglog Properties window - Map No Overwrite On Dynamic Constant Buffer</span></span>

<span data-ttu-id="6e054-313"><span id="SUMMARYINFO_MapNoOverwriteOnDynamicBufferSRV"></span><span id="summaryinfo_mapnooverwriteondynamicbuffersrv"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICBUFFERSRV"></span>**SUMMARYINFO \_ MapNoOverwriteOnDynamicBufferSRV**</span><span class="sxs-lookup"><span data-stu-id="6e054-313"><span id="SUMMARYINFO_MapNoOverwriteOnDynamicBufferSRV"></span><span id="summaryinfo_mapnooverwriteondynamicbuffersrv"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICBUFFERSRV"></span>**SUMMARYINFO\_MapNoOverwriteOnDynamicBufferSRV**</span></span>  
<span data-ttu-id="6e054-314">Vsglog 中顯示的文字屬性視窗對應動態緩衝區 SRV 沒有覆寫</span><span class="sxs-lookup"><span data-stu-id="6e054-314">Text shown in the vsglog Properties window - Map No Overwrite On Dynamic Buffer SRV</span></span>

<span data-ttu-id="6e054-315"><span id="SUMMARYINFO_MultisampleRTVWithForcedSampleCountOne"></span><span id="summaryinfo_multisamplertvwithforcedsamplecountone"></span><span id="SUMMARYINFO_MULTISAMPLERTVWITHFORCEDSAMPLECOUNTONE"></span>**SUMMARYINFO \_ MultisampleRTVWithForcedSampleCountOne**</span><span class="sxs-lookup"><span data-stu-id="6e054-315"><span id="SUMMARYINFO_MultisampleRTVWithForcedSampleCountOne"></span><span id="summaryinfo_multisamplertvwithforcedsamplecountone"></span><span id="SUMMARYINFO_MULTISAMPLERTVWITHFORCEDSAMPLECOUNTONE"></span>**SUMMARYINFO\_MultisampleRTVWithForcedSampleCountOne**</span></span>  
<span data-ttu-id="6e054-316">Vsglog 中所顯示的文字屬性視窗-具有強制取樣計數1的多層式 RTV</span><span class="sxs-lookup"><span data-stu-id="6e054-316">Text shown in the vsglog Properties window - Multisample RTV With Forced Sample Count One</span></span>

<span data-ttu-id="6e054-317"><span id="SUMMARYINFO_SAD4ShaderInstructions"></span><span id="summaryinfo_sad4shaderinstructions"></span><span id="SUMMARYINFO_SAD4SHADERINSTRUCTIONS"></span>**SUMMARYINFO \_ SAD4ShaderInstructions**</span><span class="sxs-lookup"><span data-stu-id="6e054-317"><span id="SUMMARYINFO_SAD4ShaderInstructions"></span><span id="summaryinfo_sad4shaderinstructions"></span><span id="SUMMARYINFO_SAD4SHADERINSTRUCTIONS"></span>**SUMMARYINFO\_SAD4ShaderInstructions**</span></span>  
<span data-ttu-id="6e054-318">Vsglog 屬性視窗-SAD4 著色器指示中所顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-318">Text shown in the vsglog Properties window - SAD4 Shader Instructions</span></span>

<span data-ttu-id="6e054-319"><span id="SUMMARYINFO_ExtendedDoublesShaderInstructions"></span><span id="summaryinfo_extendeddoublesshaderinstructions"></span><span id="SUMMARYINFO_EXTENDEDDOUBLESSHADERINSTRUCTIONS"></span>**SUMMARYINFO \_ ExtendedDoublesShaderInstructions**</span><span class="sxs-lookup"><span data-stu-id="6e054-319"><span id="SUMMARYINFO_ExtendedDoublesShaderInstructions"></span><span id="summaryinfo_extendeddoublesshaderinstructions"></span><span id="SUMMARYINFO_EXTENDEDDOUBLESSHADERINSTRUCTIONS"></span>**SUMMARYINFO\_ExtendedDoublesShaderInstructions**</span></span>  
<span data-ttu-id="6e054-320">Vsglog 屬性視窗-擴充的雙精確度著色器指示中所顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-320">Text shown in the vsglog Properties window - Extended Doubles Shader Instructions</span></span>

<span data-ttu-id="6e054-321"><span id="SUMMARYINFO_ExtendedResourceSharing"></span><span id="summaryinfo_extendedresourcesharing"></span><span id="SUMMARYINFO_EXTENDEDRESOURCESHARING"></span>**SUMMARYINFO \_ ExtendedResourceSharing**</span><span class="sxs-lookup"><span data-stu-id="6e054-321"><span id="SUMMARYINFO_ExtendedResourceSharing"></span><span id="summaryinfo_extendedresourcesharing"></span><span id="SUMMARYINFO_EXTENDEDRESOURCESHARING"></span>**SUMMARYINFO\_ExtendedResourceSharing**</span></span>  
<span data-ttu-id="6e054-322">Vsglog 中顯示的文字屬性視窗-擴充的資源分享</span><span class="sxs-lookup"><span data-stu-id="6e054-322">Text shown in the vsglog Properties window - Extended Resource Sharing</span></span>

<span data-ttu-id="6e054-323"><span id="SUMMARYINFO_D3D11_FEATURE_ARCHITECTURE_INFO"></span><span id="summaryinfo_d3d11_feature_architecture_info"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ 架構 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="6e054-323"><span id="SUMMARYINFO_D3D11_FEATURE_ARCHITECTURE_INFO"></span><span id="summaryinfo_d3d11_feature_architecture_info"></span>**SUMMARYINFO\_D3D11\_FEATURE\_ARCHITECTURE\_INFO**</span></span>  
<span data-ttu-id="6e054-324">Vsglog 屬性視窗-D3D11 \_ 功能 \_ 架構 \_ 資訊中所顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-324">Text shown in the vsglog Properties window - D3D11\_FEATURE\_ARCHITECTURE\_INFO</span></span>

<span data-ttu-id="6e054-325"><span id="SUMMARYINFO_TileBasedDeferredRenderer"></span><span id="summaryinfo_tilebaseddeferredrenderer"></span><span id="SUMMARYINFO_TILEBASEDDEFERREDRENDERER"></span>**SUMMARYINFO \_ TileBasedDeferredRenderer**</span><span class="sxs-lookup"><span data-stu-id="6e054-325"><span id="SUMMARYINFO_TileBasedDeferredRenderer"></span><span id="summaryinfo_tilebaseddeferredrenderer"></span><span id="SUMMARYINFO_TILEBASEDDEFERREDRENDERER"></span>**SUMMARYINFO\_TileBasedDeferredRenderer**</span></span>  
<span data-ttu-id="6e054-326">Vsglog 屬性視窗中顯示的文字（以磚為基礎的延遲轉譯器）</span><span class="sxs-lookup"><span data-stu-id="6e054-326">Text shown in the vsglog Properties window - Tile Based Deferred Renderer</span></span>

<span data-ttu-id="6e054-327"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d9_options"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ D3D9 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="6e054-327"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d9_options"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D9\_OPTIONS**</span></span>  
<span data-ttu-id="6e054-328">Vsglog 屬性視窗-D3D11 \_ 功能 \_ D3D9 \_ 選項中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-328">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D9\_OPTIONS</span></span>

<span data-ttu-id="6e054-329"><span id="SUMMARYINFO_FullNonPow2TextureSupport"></span><span id="summaryinfo_fullnonpow2texturesupport"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORT"></span>**SUMMARYINFO \_ FullNonPow2TextureSupport**</span><span class="sxs-lookup"><span data-stu-id="6e054-329"><span id="SUMMARYINFO_FullNonPow2TextureSupport"></span><span id="summaryinfo_fullnonpow2texturesupport"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORT"></span>**SUMMARYINFO\_FullNonPow2TextureSupport**</span></span>  
<span data-ttu-id="6e054-330">Vsglog 屬性視窗-完整的非 Pow2 材質支援中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-330">Text shown in the vsglog Properties window - Full Non-Pow2 Texture Support</span></span>

<span data-ttu-id="6e054-331"><span id="SUMMARYINFO_D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT"></span><span id="summaryinfo_d3d11_feature_shader_min_precision_support"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ 著色器 \_ 最小 \_ 精確度 \_ 支援**</span><span class="sxs-lookup"><span data-stu-id="6e054-331"><span id="SUMMARYINFO_D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT"></span><span id="summaryinfo_d3d11_feature_shader_min_precision_support"></span>**SUMMARYINFO\_D3D11\_FEATURE\_SHADER\_MIN\_PRECISION\_SUPPORT**</span></span>  
<span data-ttu-id="6e054-332">Vsglog 屬性視窗-D3D11 功能著色器中顯示的文字 \_ \_ \_ 最小 \_ 精確度 \_ 支援</span><span class="sxs-lookup"><span data-stu-id="6e054-332">Text shown in the vsglog Properties window - D3D11\_FEATURE\_SHADER\_MIN\_PRECISION\_SUPPORT</span></span>

<span data-ttu-id="6e054-333"><span id="SUMMARYINFO_PixelShaderMinPrecision"></span><span id="summaryinfo_pixelshaderminprecision"></span><span id="SUMMARYINFO_PIXELSHADERMINPRECISION"></span>**SUMMARYINFO \_ PixelShaderMinPrecision**</span><span class="sxs-lookup"><span data-stu-id="6e054-333"><span id="SUMMARYINFO_PixelShaderMinPrecision"></span><span id="summaryinfo_pixelshaderminprecision"></span><span id="SUMMARYINFO_PIXELSHADERMINPRECISION"></span>**SUMMARYINFO\_PixelShaderMinPrecision**</span></span>  
<span data-ttu-id="6e054-334">Vsglog 中所顯示的文字屬性視窗圖元著色器的最小精確度</span><span class="sxs-lookup"><span data-stu-id="6e054-334">Text shown in the vsglog Properties window - Pixel Shader Min Precision</span></span>

<span data-ttu-id="6e054-335"><span id="SUMMARYINFO_AllOtherShaderStagesMinPrecision"></span><span id="summaryinfo_allothershaderstagesminprecision"></span><span id="SUMMARYINFO_ALLOTHERSHADERSTAGESMINPRECISION"></span>**SUMMARYINFO \_ AllOtherShaderStagesMinPrecision**</span><span class="sxs-lookup"><span data-stu-id="6e054-335"><span id="SUMMARYINFO_AllOtherShaderStagesMinPrecision"></span><span id="summaryinfo_allothershaderstagesminprecision"></span><span id="SUMMARYINFO_ALLOTHERSHADERSTAGESMINPRECISION"></span>**SUMMARYINFO\_AllOtherShaderStagesMinPrecision**</span></span>  
<span data-ttu-id="6e054-336">Vsglog 屬性視窗中顯示的文字-所有其他著色器階段的最小精確度</span><span class="sxs-lookup"><span data-stu-id="6e054-336">Text shown in the vsglog Properties window - All Other Shader Stages Min Precision</span></span>

<span data-ttu-id="6e054-337"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SHADOW_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_shadow_support"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ D3D9 \_ 陰影 \_ 支援**</span><span class="sxs-lookup"><span data-stu-id="6e054-337"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SHADOW_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_shadow_support"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D9\_SHADOW\_SUPPORT**</span></span>  
<span data-ttu-id="6e054-338">Vsglog 屬性視窗-D3D11 \_ 功能 \_ D3D9 \_ 陰影 \_ 支援中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-338">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D9\_SHADOW\_SUPPORT</span></span>

<span data-ttu-id="6e054-339"><span id="SUMMARYINFO_SupportsDepthAsTextureWithLessEqualComparisonFilter"></span><span id="summaryinfo_supportsdepthastexturewithlessequalcomparisonfilter"></span><span id="SUMMARYINFO_SUPPORTSDEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTER"></span>**SUMMARYINFO \_ SupportsDepthAsTextureWithLessEqualComparisonFilter**</span><span class="sxs-lookup"><span data-stu-id="6e054-339"><span id="SUMMARYINFO_SupportsDepthAsTextureWithLessEqualComparisonFilter"></span><span id="summaryinfo_supportsdepthastexturewithlessequalcomparisonfilter"></span><span id="SUMMARYINFO_SUPPORTSDEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTER"></span>**SUMMARYINFO\_SupportsDepthAsTextureWithLessEqualComparisonFilter**</span></span>  
<span data-ttu-id="6e054-340">Vsglog 屬性視窗中顯示的文字-以較不相等的比較篩選支援深度為材質</span><span class="sxs-lookup"><span data-stu-id="6e054-340">Text shown in the vsglog Properties window - Supports Depth As Texture With Less Equal Comparison Filter</span></span>

<span data-ttu-id="6e054-341"><span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d11_options1"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ D3D11 \_ OPTIONS1**</span><span class="sxs-lookup"><span data-stu-id="6e054-341"><span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d11_options1"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D11\_OPTIONS1**</span></span>  
<span data-ttu-id="6e054-342">Vsglog 屬性視窗-D3D11 \_ 功能 \_ D3D11 \_ OPTIONS1 中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-342">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D11\_OPTIONS1</span></span>

<span data-ttu-id="6e054-343"><span id="SUMMARYINFO_TiledResourcesTier"></span><span id="summaryinfo_tiledresourcestier"></span><span id="SUMMARYINFO_TILEDRESOURCESTIER"></span>**SUMMARYINFO \_ TiledResourcesTier**</span><span class="sxs-lookup"><span data-stu-id="6e054-343"><span id="SUMMARYINFO_TiledResourcesTier"></span><span id="summaryinfo_tiledresourcestier"></span><span id="SUMMARYINFO_TILEDRESOURCESTIER"></span>**SUMMARYINFO\_TiledResourcesTier**</span></span>  
<span data-ttu-id="6e054-344">Vsglog 屬性視窗並排顯示的資源層級中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-344">Text shown in the vsglog Properties window - Tiled Resources Tier</span></span>

<span data-ttu-id="6e054-345"><span id="SUMMARYINFO_MinMaxFiltering"></span><span id="summaryinfo_minmaxfiltering"></span><span id="SUMMARYINFO_MINMAXFILTERING"></span>**SUMMARYINFO \_ MinMaxFiltering**</span><span class="sxs-lookup"><span data-stu-id="6e054-345"><span id="SUMMARYINFO_MinMaxFiltering"></span><span id="summaryinfo_minmaxfiltering"></span><span id="SUMMARYINFO_MINMAXFILTERING"></span>**SUMMARYINFO\_MinMaxFiltering**</span></span>  
<span data-ttu-id="6e054-346">Vsglog 屬性視窗中顯示的文字最小值篩選</span><span class="sxs-lookup"><span data-stu-id="6e054-346">Text shown in the vsglog Properties window - Min Max Filtering</span></span>

<span data-ttu-id="6e054-347"><span id="SUMMARYINFO_ClearViewAlsoSupportsDepthOnlyFormats"></span><span id="summaryinfo_clearviewalsosupportsdepthonlyformats"></span><span id="SUMMARYINFO_CLEARVIEWALSOSUPPORTSDEPTHONLYFORMATS"></span>**SUMMARYINFO \_ ClearViewAlsoSupportsDepthOnlyFormats**</span><span class="sxs-lookup"><span data-stu-id="6e054-347"><span id="SUMMARYINFO_ClearViewAlsoSupportsDepthOnlyFormats"></span><span id="summaryinfo_clearviewalsosupportsdepthonlyformats"></span><span id="SUMMARYINFO_CLEARVIEWALSOSUPPORTSDEPTHONLYFORMATS"></span>**SUMMARYINFO\_ClearViewAlsoSupportsDepthOnlyFormats**</span></span>  
<span data-ttu-id="6e054-348">Vsglog 中顯示的文字屬性視窗清除視圖也支援深度專用格式</span><span class="sxs-lookup"><span data-stu-id="6e054-348">Text shown in the vsglog Properties window - Clear View Also Supports Depth Only Formats</span></span>

<span data-ttu-id="6e054-349"><span id="SUMMARYINFO_MapOnDefaultBuffers"></span><span id="summaryinfo_mapondefaultbuffers"></span><span id="SUMMARYINFO_MAPONDEFAULTBUFFERS"></span>**SUMMARYINFO \_ MapOnDefaultBuffers**</span><span class="sxs-lookup"><span data-stu-id="6e054-349"><span id="SUMMARYINFO_MapOnDefaultBuffers"></span><span id="summaryinfo_mapondefaultbuffers"></span><span id="SUMMARYINFO_MAPONDEFAULTBUFFERS"></span>**SUMMARYINFO\_MapOnDefaultBuffers**</span></span>  
<span data-ttu-id="6e054-350">預設緩衝區上的 vsglog 屬性視窗對應中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-350">Text shown in the vsglog Properties window - Map On Default Buffers</span></span>

<span data-ttu-id="6e054-351"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_simple_instancing_support"></span>**\_ \_ \_ D3D9 \_ 簡單 \_ 實例 \_ 支援的 SUMMARYINFO D3D11 功能**</span><span class="sxs-lookup"><span data-stu-id="6e054-351"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_simple_instancing_support"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D9\_SIMPLE\_INSTANCING\_SUPPORT**</span></span>  
<span data-ttu-id="6e054-352">Vsglog 屬性視窗-D3D11 功能中所顯示的文字 \_ \_ D3D9 \_ 簡單 \_ 實例 \_ 支援</span><span class="sxs-lookup"><span data-stu-id="6e054-352">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D9\_SIMPLE\_INSTANCING\_SUPPORT</span></span>

<span data-ttu-id="6e054-353"><span id="SUMMARYINFO_SimpleInstancingSupported0"></span><span id="summaryinfo_simpleinstancingsupported0"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED0"></span>**SUMMARYINFO \_ SimpleInstancingSupported0**</span><span class="sxs-lookup"><span data-stu-id="6e054-353"><span id="SUMMARYINFO_SimpleInstancingSupported0"></span><span id="summaryinfo_simpleinstancingsupported0"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED0"></span>**SUMMARYINFO\_SimpleInstancingSupported0**</span></span>  
<span data-ttu-id="6e054-354">Vsglog 屬性視窗所顯示的文字-簡單實例支援0</span><span class="sxs-lookup"><span data-stu-id="6e054-354">Text shown in the vsglog Properties window - Simple Instancing Supported 0</span></span>

<span data-ttu-id="6e054-355"><span id="SUMMARYINFO_D3D11_FEATURE_MARKER_SUPPORT"></span><span id="summaryinfo_d3d11_feature_marker_support"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ 標記 \_ 支援**</span><span class="sxs-lookup"><span data-stu-id="6e054-355"><span id="SUMMARYINFO_D3D11_FEATURE_MARKER_SUPPORT"></span><span id="summaryinfo_d3d11_feature_marker_support"></span>**SUMMARYINFO\_D3D11\_FEATURE\_MARKER\_SUPPORT**</span></span>  
<span data-ttu-id="6e054-356">Vsglog 屬性視窗-D3D11 \_ 功能 \_ 標記 \_ 支援中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-356">Text shown in the vsglog Properties window - D3D11\_FEATURE\_MARKER\_SUPPORT</span></span>

<span data-ttu-id="6e054-357"><span id="SUMMARYINFO_Profile"></span><span id="summaryinfo_profile"></span><span id="SUMMARYINFO_PROFILE"></span>**SUMMARYINFO \_ 設定檔**</span><span class="sxs-lookup"><span data-stu-id="6e054-357"><span id="SUMMARYINFO_Profile"></span><span id="summaryinfo_profile"></span><span id="SUMMARYINFO_PROFILE"></span>**SUMMARYINFO\_Profile**</span></span>  
<span data-ttu-id="6e054-358">Vsglog 屬性視窗-設定檔中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-358">Text shown in the vsglog Properties window - Profile</span></span>

<span data-ttu-id="6e054-359"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d9_options1"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ D3D9 \_ OPTIONS1**</span><span class="sxs-lookup"><span data-stu-id="6e054-359"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d9_options1"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D9\_OPTIONS1**</span></span>  
<span data-ttu-id="6e054-360">Vsglog 屬性視窗-D3D11 \_ 功能 \_ D3D9 \_ OPTIONS1 中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-360">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D9\_OPTIONS1</span></span>

<span data-ttu-id="6e054-361"><span id="SUMMARYINFO_FullNonPow2TextureSupported"></span><span id="summaryinfo_fullnonpow2texturesupported"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORTED"></span>**SUMMARYINFO \_ FullNonPow2TextureSupported**</span><span class="sxs-lookup"><span data-stu-id="6e054-361"><span id="SUMMARYINFO_FullNonPow2TextureSupported"></span><span id="summaryinfo_fullnonpow2texturesupported"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORTED"></span>**SUMMARYINFO\_FullNonPow2TextureSupported**</span></span>  
<span data-ttu-id="6e054-362">Vsglog 屬性視窗中所顯示的文字-支援完整的非 Pow2 材質</span><span class="sxs-lookup"><span data-stu-id="6e054-362">Text shown in the vsglog Properties window - Full Non-Pow2 Texture Supported</span></span>

<span data-ttu-id="6e054-363"><span id="SUMMARYINFO_DepthAsTextureWithLessEqualComparisonFilterSupported"></span><span id="summaryinfo_depthastexturewithlessequalcomparisonfiltersupported"></span><span id="SUMMARYINFO_DEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTERSUPPORTED"></span>**SUMMARYINFO \_ DepthAsTextureWithLessEqualComparisonFilterSupported**</span><span class="sxs-lookup"><span data-stu-id="6e054-363"><span id="SUMMARYINFO_DepthAsTextureWithLessEqualComparisonFilterSupported"></span><span id="summaryinfo_depthastexturewithlessequalcomparisonfiltersupported"></span><span id="SUMMARYINFO_DEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTERSUPPORTED"></span>**SUMMARYINFO\_DepthAsTextureWithLessEqualComparisonFilterSupported**</span></span>  
<span data-ttu-id="6e054-364">Vsglog 屬性視窗深度中所顯示的文字，其為支援較不相等比較篩選的材質</span><span class="sxs-lookup"><span data-stu-id="6e054-364">Text shown in the vsglog Properties window - Depth As Texture With Less Equal Comparison Filter Supported</span></span>

<span data-ttu-id="6e054-365"><span id="SUMMARYINFO_SimpleInstancingSupported1"></span><span id="summaryinfo_simpleinstancingsupported1"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED1"></span>**SUMMARYINFO \_ SimpleInstancingSupported1**</span><span class="sxs-lookup"><span data-stu-id="6e054-365"><span id="SUMMARYINFO_SimpleInstancingSupported1"></span><span id="summaryinfo_simpleinstancingsupported1"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED1"></span>**SUMMARYINFO\_SimpleInstancingSupported1**</span></span>  
<span data-ttu-id="6e054-366">Vsglog 屬性視窗所顯示的文字-簡單的實例支援1</span><span class="sxs-lookup"><span data-stu-id="6e054-366">Text shown in the vsglog Properties window - Simple Instancing Supported 1</span></span>

<span data-ttu-id="6e054-367"><span id="SUMMARYINFO_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported"></span><span id="summaryinfo_texturecubefacerendertargetwithnoncubedepthstencilsupported"></span><span id="SUMMARYINFO_TEXTURECUBEFACERENDERTARGETWITHNONCUBEDEPTHSTENCILSUPPORTED"></span>**SUMMARYINFO \_ TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported**</span><span class="sxs-lookup"><span data-stu-id="6e054-367"><span id="SUMMARYINFO_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported"></span><span id="summaryinfo_texturecubefacerendertargetwithnoncubedepthstencilsupported"></span><span id="SUMMARYINFO_TEXTURECUBEFACERENDERTARGETWITHNONCUBEDEPTHSTENCILSUPPORTED"></span>**SUMMARYINFO\_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported**</span></span>  
<span data-ttu-id="6e054-368">Vsglog 屬性視窗紋理 Cube 臉部呈現目標中所顯示的文字，並支援非 Cube 深度樣板</span><span class="sxs-lookup"><span data-stu-id="6e054-368">Text shown in the vsglog Properties window - Texture Cube Face Render Target With Non-Cube Depth Stencil Supported</span></span>

<span data-ttu-id="6e054-369"><span id="SUMMARYINFO_DXGIFormat"></span><span id="summaryinfo_dxgiformat"></span><span id="SUMMARYINFO_DXGIFORMAT"></span>**SUMMARYINFO \_ DXGIFormat**</span><span class="sxs-lookup"><span data-stu-id="6e054-369"><span id="SUMMARYINFO_DXGIFormat"></span><span id="summaryinfo_dxgiformat"></span><span id="SUMMARYINFO_DXGIFORMAT"></span>**SUMMARYINFO\_DXGIFormat**</span></span>  
<span data-ttu-id="6e054-370">Vsglog 屬性視窗-DXGIFormat 中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-370">Text shown in the vsglog Properties window - DXGIFormat</span></span>

<span data-ttu-id="6e054-371"><span id="SUMMARYINFO_DXGIFormat1"></span><span id="summaryinfo_dxgiformat1"></span><span id="SUMMARYINFO_DXGIFORMAT1"></span>**SUMMARYINFO \_ DXGIFormat1**</span><span class="sxs-lookup"><span data-stu-id="6e054-371"><span id="SUMMARYINFO_DXGIFormat1"></span><span id="summaryinfo_dxgiformat1"></span><span id="SUMMARYINFO_DXGIFORMAT1"></span>**SUMMARYINFO\_DXGIFormat1**</span></span>  
<span data-ttu-id="6e054-372">Vsglog 屬性視窗-DXGIFormat1 中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-372">Text shown in the vsglog Properties window - DXGIFormat1</span></span>

<span data-ttu-id="6e054-373"><span id="SUMMARYINFO_MODULENAME"></span><span id="summaryinfo_modulename"></span>**SUMMARYINFO \_ MODULENAME**</span><span class="sxs-lookup"><span data-stu-id="6e054-373"><span id="SUMMARYINFO_MODULENAME"></span><span id="summaryinfo_modulename"></span>**SUMMARYINFO\_MODULENAME**</span></span>  
<span data-ttu-id="6e054-374">Vsglog 屬性視窗-MODULENAME 中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-374">Text shown in the vsglog Properties window - MODULENAME</span></span>

<span data-ttu-id="6e054-375"><span id="IDD_CONFIGURATION"></span><span id="idd_configuration"></span>**IDD \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="6e054-375"><span id="IDD_CONFIGURATION"></span><span id="idd_configuration"></span>**IDD\_CONFIGURATION**</span></span>  
<span data-ttu-id="6e054-376">VsGraphicsRemoteEngine 中 [設定防火牆] 對話方塊中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-376">Text shown in the Configure Firewall dialog in the VsGraphicsRemoteEngine</span></span>

<span data-ttu-id="6e054-377"><span id="IDC_STATIC_HEADER_ICON"></span><span id="idc_static_header_icon"></span>**IDC \_ 靜態 \_ 標頭 \_ 圖示**</span><span class="sxs-lookup"><span data-stu-id="6e054-377"><span id="IDC_STATIC_HEADER_ICON"></span><span id="idc_static_header_icon"></span>**IDC\_STATIC\_HEADER\_ICON**</span></span>  
<span data-ttu-id="6e054-378">[設定防火牆] 對話方塊控制項-靜態標頭圖示中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-378">Text shown in the Configure Firewall dialog control - Static Header Icon</span></span>

<span data-ttu-id="6e054-379"><span id="IDC_STATIC_HEADER"></span><span id="idc_static_header"></span>**IDC \_ 靜態 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="6e054-379"><span id="IDC_STATIC_HEADER"></span><span id="idc_static_header"></span>**IDC\_STATIC\_HEADER**</span></span>  
<span data-ttu-id="6e054-380">設定防火牆對話方塊控制項-靜態標頭中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-380">Text shown in the Configure Firewall dialog control - Static Header</span></span>

<span data-ttu-id="6e054-381"><span id="IDC_STATIC_FW_CONFIGURATION"></span><span id="idc_static_fw_configuration"></span>**IDC \_ 靜態 \_ FW \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="6e054-381"><span id="IDC_STATIC_FW_CONFIGURATION"></span><span id="idc_static_fw_configuration"></span>**IDC\_STATIC\_FW\_CONFIGURATION**</span></span>  
<span data-ttu-id="6e054-382">設定防火牆對話方塊控制項-靜態防火牆設定中所顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-382">Text shown in the Configure Firewall dialog control - Static Firewall Configuration</span></span>

<span data-ttu-id="6e054-383"><span id="IDC_STATIC_FW_ICON"></span><span id="idc_static_fw_icon"></span>**IDC \_ 靜態 \_ FW \_ 圖示**</span><span class="sxs-lookup"><span data-stu-id="6e054-383"><span id="IDC_STATIC_FW_ICON"></span><span id="idc_static_fw_icon"></span>**IDC\_STATIC\_FW\_ICON**</span></span>  
<span data-ttu-id="6e054-384">設定防火牆對話方塊控制項-靜態防火牆圖示中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-384">Text shown in the Configure Firewall dialog control - Static Firewall Icon</span></span>

<span data-ttu-id="6e054-385"><span id="IDC_STATIC_FW_HEADER"></span><span id="idc_static_fw_header"></span>**IDC \_ 靜態 \_ FW \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="6e054-385"><span id="IDC_STATIC_FW_HEADER"></span><span id="idc_static_fw_header"></span>**IDC\_STATIC\_FW\_HEADER**</span></span>  
<span data-ttu-id="6e054-386">設定防火牆對話方塊控制項-靜態防火牆標頭中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-386">Text shown in the Configure Firewall dialog control - Static Firewall Header</span></span>

<span data-ttu-id="6e054-387"><span id="IDC_STATIC_GROUPBOX_FW"></span><span id="idc_static_groupbox_fw"></span>**IDC \_ 靜態 \_ 分組帶 \_ FW**</span><span class="sxs-lookup"><span data-stu-id="6e054-387"><span id="IDC_STATIC_GROUPBOX_FW"></span><span id="idc_static_groupbox_fw"></span>**IDC\_STATIC\_GROUPBOX\_FW**</span></span>  
<span data-ttu-id="6e054-388">設定防火牆對話方塊控制項中顯示的文字-靜態群組方塊防火牆</span><span class="sxs-lookup"><span data-stu-id="6e054-388">Text shown in the Configure Firewall dialog control - Static Groupbox Firewall</span></span>

<span data-ttu-id="6e054-389"><span id="IDC_CHECK_FW_DOMAIN_NETWORKS"></span><span id="idc_check_fw_domain_networks"></span>**IDC \_ 檢查 \_ FW \_ 網域 \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="6e054-389"><span id="IDC_CHECK_FW_DOMAIN_NETWORKS"></span><span id="idc_check_fw_domain_networks"></span>**IDC\_CHECK\_FW\_DOMAIN\_NETWORKS**</span></span>  
<span data-ttu-id="6e054-390">設定防火牆對話方塊控制項-檢查防火牆網域網路中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-390">Text shown in the Configure Firewall dialog control - Check Firewall Domain Networks</span></span>

<span data-ttu-id="6e054-391"><span id="IDC_CHECK_FW_PRIVATE_NETWORKS"></span><span id="idc_check_fw_private_networks"></span>**IDC \_ 檢查 \_ FW \_ 專用 \_ 網**</span><span class="sxs-lookup"><span data-stu-id="6e054-391"><span id="IDC_CHECK_FW_PRIVATE_NETWORKS"></span><span id="idc_check_fw_private_networks"></span>**IDC\_CHECK\_FW\_PRIVATE\_NETWORKS**</span></span>  
<span data-ttu-id="6e054-392">設定防火牆對話方塊控制項中顯示的文字-檢查防火牆私人網路</span><span class="sxs-lookup"><span data-stu-id="6e054-392">Text shown in the Configure Firewall dialog control - Check Firewall Private Networks</span></span>

<span data-ttu-id="6e054-393"><span id="IDC_CHECK_FW_PUBLIC_NETWORKS"></span><span id="idc_check_fw_public_networks"></span>**IDC \_ 檢查 \_ FW \_ 公用 \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="6e054-393"><span id="IDC_CHECK_FW_PUBLIC_NETWORKS"></span><span id="idc_check_fw_public_networks"></span>**IDC\_CHECK\_FW\_PUBLIC\_NETWORKS**</span></span>  
<span data-ttu-id="6e054-394">設定防火牆對話方塊控制項-檢查防火牆公用網路中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-394">Text shown in the Configure Firewall dialog control - Check Firewall Public Networks</span></span>

<span data-ttu-id="6e054-395"><span id="IDC_BUTTON_CONFIGURE"></span><span id="idc_button_configure"></span>**IDC \_ 按鈕 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="6e054-395"><span id="IDC_BUTTON_CONFIGURE"></span><span id="idc_button_configure"></span>**IDC\_BUTTON\_CONFIGURE**</span></span>  
<span data-ttu-id="6e054-396">設定防火牆對話方塊控制項-按鈕設定中顯示的文字</span><span class="sxs-lookup"><span data-stu-id="6e054-396">Text shown in the Configure Firewall dialog control - Button Configure</span></span>

<span data-ttu-id="6e054-397"><span id="ID_CONFIGURATION_CANCEL"></span><span id="id_configuration_cancel"></span>**識別碼 \_ 設定 \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="6e054-397"><span id="ID_CONFIGURATION_CANCEL"></span><span id="id_configuration_cancel"></span>**ID\_CONFIGURATION\_CANCEL**</span></span>  
<span data-ttu-id="6e054-398">設定防火牆對話方塊控制項中顯示的文字-設定取消</span><span class="sxs-lookup"><span data-stu-id="6e054-398">Text shown in the Configure Firewall dialog control - Configuration Cancel</span></span>

<span data-ttu-id="6e054-399"><span id="IDS_TEXT_FW_NOT_CONFIGURED"></span><span id="ids_text_fw_not_configured"></span>**\_ \_ \_ 未設定識別碼文字 \_ FW**</span><span class="sxs-lookup"><span data-stu-id="6e054-399"><span id="IDS_TEXT_FW_NOT_CONFIGURED"></span><span id="ids_text_fw_not_configured"></span>**IDS\_TEXT\_FW\_NOT\_CONFIGURED**</span></span>  
<span data-ttu-id="6e054-400">[設定防火牆] 對話方塊中顯示的文字-未設定的文字防火牆</span><span class="sxs-lookup"><span data-stu-id="6e054-400">Text shown in the Configure Firewall dialog - Text Firewall Not Configured</span></span>

<span data-ttu-id="6e054-401"><span id="IDS_TEXT_FW_CONFIGURED"></span><span id="ids_text_fw_configured"></span>**設定的識別碼 \_ 文字 \_ FW \_**</span><span class="sxs-lookup"><span data-stu-id="6e054-401"><span id="IDS_TEXT_FW_CONFIGURED"></span><span id="ids_text_fw_configured"></span>**IDS\_TEXT\_FW\_CONFIGURED**</span></span>  
<span data-ttu-id="6e054-402">設定防火牆對話方塊中顯示的文字-已設定的文字防火牆</span><span class="sxs-lookup"><span data-stu-id="6e054-402">Text shown in the Configure Firewall dialog - Text Firewall Configured</span></span>

<span data-ttu-id="6e054-403"><span id="IDS_FIREWALL_RULE_NAME"></span><span id="ids_firewall_rule_name"></span>**IDS \_ 防火牆 \_ 規則 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="6e054-403"><span id="IDS_FIREWALL_RULE_NAME"></span><span id="ids_firewall_rule_name"></span>**IDS\_FIREWALL\_RULE\_NAME**</span></span>  
<span data-ttu-id="6e054-404">[設定防火牆] 對話方塊中顯示的文字-防火牆規則名稱</span><span class="sxs-lookup"><span data-stu-id="6e054-404">Text shown in the Configure Firewall dialog - Firewall Rule Name</span></span>

<span data-ttu-id="6e054-405"><span id="IDS_FIREWALL_RULE_DESCRIPTION"></span><span id="ids_firewall_rule_description"></span>**IDS \_ 防火牆 \_ 規則 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="6e054-405"><span id="IDS_FIREWALL_RULE_DESCRIPTION"></span><span id="ids_firewall_rule_description"></span>**IDS\_FIREWALL\_RULE\_DESCRIPTION**</span></span>  
<span data-ttu-id="6e054-406">[設定防火牆] 對話方塊中顯示的文字-防火牆規則描述</span><span class="sxs-lookup"><span data-stu-id="6e054-406">Text shown in the Configure Firewall dialog - Firewall Rule Description</span></span>

<span data-ttu-id="6e054-407"><span id="IDS_STATIC_HEADER"></span><span id="ids_static_header"></span>**ID \_ 靜態 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="6e054-407"><span id="IDS_STATIC_HEADER"></span><span id="ids_static_header"></span>**IDS\_STATIC\_HEADER**</span></span>  
<span data-ttu-id="6e054-408">[設定防火牆] 對話方塊中顯示的文字-靜態標頭</span><span class="sxs-lookup"><span data-stu-id="6e054-408">Text shown in the Configure Firewall dialog - Static Header</span></span>

<span data-ttu-id="6e054-409"><span id="IDS_CONFIGURATION_TITLE"></span><span id="ids_configuration_title"></span>**識別碼 \_ 設定 \_ 標題**</span><span class="sxs-lookup"><span data-stu-id="6e054-409"><span id="IDS_CONFIGURATION_TITLE"></span><span id="ids_configuration_title"></span>**IDS\_CONFIGURATION\_TITLE**</span></span>  
<span data-ttu-id="6e054-410">[設定防火牆] 對話方塊中顯示的文字-設定標題</span><span class="sxs-lookup"><span data-stu-id="6e054-410">Text shown in the Configure Firewall dialog - Configuration Title</span></span>

<span data-ttu-id="6e054-411"><span id="IDS_STATIC_FW_HEADER"></span><span id="ids_static_fw_header"></span>**識別碼 \_ 靜態 \_ FW \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="6e054-411"><span id="IDS_STATIC_FW_HEADER"></span><span id="ids_static_fw_header"></span>**IDS\_STATIC\_FW\_HEADER**</span></span>  
<span data-ttu-id="6e054-412">[設定防火牆] 對話方塊中顯示的文字-靜態防火牆標頭</span><span class="sxs-lookup"><span data-stu-id="6e054-412">Text shown in the Configure Firewall dialog - Static Firewall Header</span></span>

<span data-ttu-id="6e054-413"><span id="IDS_STATIC_GROUPBOX_FW"></span><span id="ids_static_groupbox_fw"></span>**識別碼 \_ 靜態 \_ 分組帶 \_ FW**</span><span class="sxs-lookup"><span data-stu-id="6e054-413"><span id="IDS_STATIC_GROUPBOX_FW"></span><span id="ids_static_groupbox_fw"></span>**IDS\_STATIC\_GROUPBOX\_FW**</span></span>  
<span data-ttu-id="6e054-414">[設定防火牆] 對話方塊中顯示的文字-靜態群組方塊防火牆</span><span class="sxs-lookup"><span data-stu-id="6e054-414">Text shown in the Configure Firewall dialog - Static Groupbox Firewall</span></span>

<span data-ttu-id="6e054-415"><span id="IDS_CHECK_FW_DOMAIN_NETWORKS"></span><span id="ids_check_fw_domain_networks"></span>**IDS \_ 檢查 \_ FW \_ 網域 \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="6e054-415"><span id="IDS_CHECK_FW_DOMAIN_NETWORKS"></span><span id="ids_check_fw_domain_networks"></span>**IDS\_CHECK\_FW\_DOMAIN\_NETWORKS**</span></span>  
<span data-ttu-id="6e054-416">[設定防火牆] 對話方塊中顯示的文字-檢查防火牆網域網路</span><span class="sxs-lookup"><span data-stu-id="6e054-416">Text shown in the Configure Firewall dialog - Check Firewall Domain Networks</span></span>

<span data-ttu-id="6e054-417"><span id="IDS_CHECK_FW_PRIVATE_NETWORKS"></span><span id="ids_check_fw_private_networks"></span>**IDS \_ 檢查 \_ FW \_ 專用 \_ 網**</span><span class="sxs-lookup"><span data-stu-id="6e054-417"><span id="IDS_CHECK_FW_PRIVATE_NETWORKS"></span><span id="ids_check_fw_private_networks"></span>**IDS\_CHECK\_FW\_PRIVATE\_NETWORKS**</span></span>  
<span data-ttu-id="6e054-418">[設定防火牆] 對話方塊中顯示的文字-檢查防火牆私人網路</span><span class="sxs-lookup"><span data-stu-id="6e054-418">Text shown in the Configure Firewall dialog - Check Firewall Private Networks</span></span>

<span data-ttu-id="6e054-419"><span id="IDS_CHECK_FW_PUBLIC_NETWORKS"></span><span id="ids_check_fw_public_networks"></span>**識別碼 \_ 檢查 \_ FW \_ 公用 \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="6e054-419"><span id="IDS_CHECK_FW_PUBLIC_NETWORKS"></span><span id="ids_check_fw_public_networks"></span>**IDS\_CHECK\_FW\_PUBLIC\_NETWORKS**</span></span>  
<span data-ttu-id="6e054-420">[設定防火牆] 對話方塊中顯示的文字-檢查防火牆公用網路</span><span class="sxs-lookup"><span data-stu-id="6e054-420">Text shown in the Configure Firewall dialog - Check Firewall public Networks</span></span>

<span data-ttu-id="6e054-421"><span id="IDS_BUTTON_CONFIGURE"></span><span id="ids_button_configure"></span>**識別碼 \_ 按鈕 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="6e054-421"><span id="IDS_BUTTON_CONFIGURE"></span><span id="ids_button_configure"></span>**IDS\_BUTTON\_CONFIGURE**</span></span>  
<span data-ttu-id="6e054-422">[設定防火牆] 對話方塊中顯示的文字-Include Confiture</span><span class="sxs-lookup"><span data-stu-id="6e054-422">Text shown in the Configure Firewall dialog - Buttom Confiture</span></span>

<span data-ttu-id="6e054-423"><span id="IDS_CONFIGURATION_CANCEL"></span><span id="ids_configuration_cancel"></span>**識別碼 \_ 設定 \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="6e054-423"><span id="IDS_CONFIGURATION_CANCEL"></span><span id="ids_configuration_cancel"></span>**IDS\_CONFIGURATION\_CANCEL**</span></span>  
<span data-ttu-id="6e054-424">[設定防火牆] 對話方塊中顯示的文字-Configuration Cancel</span><span class="sxs-lookup"><span data-stu-id="6e054-424">Text shown in the Configure Firewall dialog - Configuration Cancel</span></span>

<span data-ttu-id="6e054-425"><span id="IDS_CAPTURETOOLTIP_MESSAGE_CORESYSTEM"></span><span id="ids_capturetooltip_message_coresystem"></span>**識別碼 \_ CAPTURETOOLTIP \_ 訊息 \_ CORESYSTEM**</span><span class="sxs-lookup"><span data-stu-id="6e054-425"><span id="IDS_CAPTURETOOLTIP_MESSAGE_CORESYSTEM"></span><span id="ids_capturetooltip_message_coresystem"></span>**IDS\_CAPTURETOOLTIP\_MESSAGE\_CORESYSTEM**</span></span>  
<span data-ttu-id="6e054-426">字串的資源識別碼「使用 Visual Studio 中的 [捕捉] 按鈕來捕捉畫面 (s) ）。</span><span class="sxs-lookup"><span data-stu-id="6e054-426">Resource ID for string "Use the capture button in Visual Studio to capture frame(s)."</span></span>

<span data-ttu-id="6e054-427"><span id="IDS_ET_NONE"></span><span id="ids_et_none"></span>**識別碼 \_ ET \_ 無**</span><span class="sxs-lookup"><span data-stu-id="6e054-427"><span id="IDS_ET_NONE"></span><span id="ids_et_none"></span>**IDS\_ET\_NONE**</span></span>  
<span data-ttu-id="6e054-428">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-428">Not used.</span></span>

<span data-ttu-id="6e054-429"><span id="IDS_ET_SESSIONSTART"></span><span id="ids_et_sessionstart"></span>**識別碼 \_ ET \_ SESSIONSTART**</span><span class="sxs-lookup"><span data-stu-id="6e054-429"><span id="IDS_ET_SESSIONSTART"></span><span id="ids_et_sessionstart"></span>**IDS\_ET\_SESSIONSTART**</span></span>  
<span data-ttu-id="6e054-430">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-430">Not used.</span></span>

<span data-ttu-id="6e054-431"><span id="IDS_ET_SESSIONEND"></span><span id="ids_et_sessionend"></span>**識別碼 \_ ET \_ SESSIONEND**</span><span class="sxs-lookup"><span data-stu-id="6e054-431"><span id="IDS_ET_SESSIONEND"></span><span id="ids_et_sessionend"></span>**IDS\_ET\_SESSIONEND**</span></span>  
<span data-ttu-id="6e054-432">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-432">Not used.</span></span>

<span data-ttu-id="6e054-433"><span id="IDS_ET_PROCESSSTART"></span><span id="ids_et_processstart"></span>**識別碼 \_ ET \_ PROCESSSTART**</span><span class="sxs-lookup"><span data-stu-id="6e054-433"><span id="IDS_ET_PROCESSSTART"></span><span id="ids_et_processstart"></span>**IDS\_ET\_PROCESSSTART**</span></span>  
<span data-ttu-id="6e054-434">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-434">Not used.</span></span>

<span data-ttu-id="6e054-435"><span id="IDS_ET_PROCESSEND"></span><span id="ids_et_processend"></span>**識別碼 \_ ET \_ PROCESSEND**</span><span class="sxs-lookup"><span data-stu-id="6e054-435"><span id="IDS_ET_PROCESSEND"></span><span id="ids_et_processend"></span>**IDS\_ET\_PROCESSEND**</span></span>  
<span data-ttu-id="6e054-436">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-436">Not used.</span></span>

<span data-ttu-id="6e054-437"><span id="IDS_ET_FRAMEBEGIN"></span><span id="ids_et_framebegin"></span>**識別碼 \_ ET \_ FRAMEBEGIN**</span><span class="sxs-lookup"><span data-stu-id="6e054-437"><span id="IDS_ET_FRAMEBEGIN"></span><span id="ids_et_framebegin"></span>**IDS\_ET\_FRAMEBEGIN**</span></span>  
<span data-ttu-id="6e054-438">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-438">Not used.</span></span>

<span data-ttu-id="6e054-439"><span id="IDS_ET_FRAMEEND"></span><span id="ids_et_frameend"></span>**識別碼 \_ ET \_ FRAMEEND**</span><span class="sxs-lookup"><span data-stu-id="6e054-439"><span id="IDS_ET_FRAMEEND"></span><span id="ids_et_frameend"></span>**IDS\_ET\_FRAMEEND**</span></span>  
<span data-ttu-id="6e054-440">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-440">Not used.</span></span>

<span data-ttu-id="6e054-441"><span id="IDS_ET_USEREVENTBEGIN"></span><span id="ids_et_usereventbegin"></span>**識別碼 \_ ET \_ USEREVENTBEGIN**</span><span class="sxs-lookup"><span data-stu-id="6e054-441"><span id="IDS_ET_USEREVENTBEGIN"></span><span id="ids_et_usereventbegin"></span>**IDS\_ET\_USEREVENTBEGIN**</span></span>  
<span data-ttu-id="6e054-442">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-442">Not used.</span></span>

<span data-ttu-id="6e054-443"><span id="IDS_ET_USEREVENTEND"></span><span id="ids_et_usereventend"></span>**識別碼 \_ ET \_ USEREVENTEND**</span><span class="sxs-lookup"><span data-stu-id="6e054-443"><span id="IDS_ET_USEREVENTEND"></span><span id="ids_et_usereventend"></span>**IDS\_ET\_USEREVENTEND**</span></span>  
<span data-ttu-id="6e054-444">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-444">Not used.</span></span>

<span data-ttu-id="6e054-445"><span id="IDS_ET_USERMARKER"></span><span id="ids_et_usermarker"></span>**識別碼 \_ ET \_ USERMARKER**</span><span class="sxs-lookup"><span data-stu-id="6e054-445"><span id="IDS_ET_USERMARKER"></span><span id="ids_et_usermarker"></span>**IDS\_ET\_USERMARKER**</span></span>  
<span data-ttu-id="6e054-446">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-446">Not used.</span></span>

<span data-ttu-id="6e054-447"><span id="IDS_ET_CALL"></span><span id="ids_et_call"></span>**ID \_ ET \_ 呼叫**</span><span class="sxs-lookup"><span data-stu-id="6e054-447"><span id="IDS_ET_CALL"></span><span id="ids_et_call"></span>**IDS\_ET\_CALL**</span></span>  
<span data-ttu-id="6e054-448">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-448">Not used.</span></span>

<span data-ttu-id="6e054-449"><span id="IDS_ET_OBJECTPOPULATION"></span><span id="ids_et_objectpopulation"></span>**識別碼 \_ ET \_ OBJECTPOPULATION**</span><span class="sxs-lookup"><span data-stu-id="6e054-449"><span id="IDS_ET_OBJECTPOPULATION"></span><span id="ids_et_objectpopulation"></span>**IDS\_ET\_OBJECTPOPULATION**</span></span>  
<span data-ttu-id="6e054-450">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-450">Not used.</span></span>

<span data-ttu-id="6e054-451"><span id="IDS_ET_OBJECTCREATION"></span><span id="ids_et_objectcreation"></span>**識別碼 \_ ET \_ OBJECTCREATION**</span><span class="sxs-lookup"><span data-stu-id="6e054-451"><span id="IDS_ET_OBJECTCREATION"></span><span id="ids_et_objectcreation"></span>**IDS\_ET\_OBJECTCREATION**</span></span>  
<span data-ttu-id="6e054-452">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-452">Not used.</span></span>

<span data-ttu-id="6e054-453"><span id="IDS_ET_CALLSYNC"></span><span id="ids_et_callsync"></span>**識別碼 \_ ET \_ CALLSYNC**</span><span class="sxs-lookup"><span data-stu-id="6e054-453"><span id="IDS_ET_CALLSYNC"></span><span id="ids_et_callsync"></span>**IDS\_ET\_CALLSYNC**</span></span>  
<span data-ttu-id="6e054-454">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-454">Not used.</span></span>

<span data-ttu-id="6e054-455"><span id="IDS_ET_UNKNOWN"></span><span id="ids_et_unknown"></span>**識別碼 \_ ET \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="6e054-455"><span id="IDS_ET_UNKNOWN"></span><span id="ids_et_unknown"></span>**IDS\_ET\_UNKNOWN**</span></span>  
<span data-ttu-id="6e054-456">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-456">Not used.</span></span>

<span data-ttu-id="6e054-457"><span id="IDS_TRIGGER_NONE"></span><span id="ids_trigger_none"></span>**識別碼 \_ 觸發程式 \_ 無**</span><span class="sxs-lookup"><span data-stu-id="6e054-457"><span id="IDS_TRIGGER_NONE"></span><span id="ids_trigger_none"></span>**IDS\_TRIGGER\_NONE**</span></span>  
<span data-ttu-id="6e054-458">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-458">Not used.</span></span>

<span data-ttu-id="6e054-459"><span id="IDS_TRIGGER_PROGRAMSTART"></span><span id="ids_trigger_programstart"></span>**ID \_ 觸發程式 \_ PROGRAMSTART**</span><span class="sxs-lookup"><span data-stu-id="6e054-459"><span id="IDS_TRIGGER_PROGRAMSTART"></span><span id="ids_trigger_programstart"></span>**IDS\_TRIGGER\_PROGRAMSTART**</span></span>  
<span data-ttu-id="6e054-460">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-460">Not used.</span></span>

<span data-ttu-id="6e054-461"><span id="IDS_TRIGGER_FRAME"></span><span id="ids_trigger_frame"></span>**識別碼 \_ 觸發程式 \_ 框架**</span><span class="sxs-lookup"><span data-stu-id="6e054-461"><span id="IDS_TRIGGER_FRAME"></span><span id="ids_trigger_frame"></span>**IDS\_TRIGGER\_FRAME**</span></span>  
<span data-ttu-id="6e054-462">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-462">Not used.</span></span>

<span data-ttu-id="6e054-463"><span id="IDS_TRIGGER_TIME"></span><span id="ids_trigger_time"></span>**識別碼 \_ 觸發 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="6e054-463"><span id="IDS_TRIGGER_TIME"></span><span id="ids_trigger_time"></span>**IDS\_TRIGGER\_TIME**</span></span>  
<span data-ttu-id="6e054-464">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-464">Not used.</span></span>

<span data-ttu-id="6e054-465"><span id="IDS_TRIGGER_USERMARKER"></span><span id="ids_trigger_usermarker"></span>**ID \_ 觸發程式 \_ USERMARKER**</span><span class="sxs-lookup"><span data-stu-id="6e054-465"><span id="IDS_TRIGGER_USERMARKER"></span><span id="ids_trigger_usermarker"></span>**IDS\_TRIGGER\_USERMARKER**</span></span>  
<span data-ttu-id="6e054-466">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-466">Not used.</span></span>

<span data-ttu-id="6e054-467"><span id="IDS_TRIGGER_BEGINUSEREVENT"></span><span id="ids_trigger_beginuserevent"></span>**ID \_ 觸發程式 \_ BEGINUSEREVENT**</span><span class="sxs-lookup"><span data-stu-id="6e054-467"><span id="IDS_TRIGGER_BEGINUSEREVENT"></span><span id="ids_trigger_beginuserevent"></span>**IDS\_TRIGGER\_BEGINUSEREVENT**</span></span>  
<span data-ttu-id="6e054-468">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-468">Not used.</span></span>

<span data-ttu-id="6e054-469"><span id="IDS_TRIGGER_ENDUSEREVENT"></span><span id="ids_trigger_enduserevent"></span>**ID \_ 觸發程式 \_ ENDUSEREVENT**</span><span class="sxs-lookup"><span data-stu-id="6e054-469"><span id="IDS_TRIGGER_ENDUSEREVENT"></span><span id="ids_trigger_enduserevent"></span>**IDS\_TRIGGER\_ENDUSEREVENT**</span></span>  
<span data-ttu-id="6e054-470">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-470">Not used.</span></span>

<span data-ttu-id="6e054-471"><span id="IDS_TRIGGER_CAPTUREFRAME"></span><span id="ids_trigger_captureframe"></span>**ID \_ 觸發程式 \_ CAPTUREFRAME**</span><span class="sxs-lookup"><span data-stu-id="6e054-471"><span id="IDS_TRIGGER_CAPTUREFRAME"></span><span id="ids_trigger_captureframe"></span>**IDS\_TRIGGER\_CAPTUREFRAME**</span></span>  
<span data-ttu-id="6e054-472">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-472">Not used.</span></span>

<span data-ttu-id="6e054-473"><span id="IDS_TRIGGER_APICAPTURE"></span><span id="ids_trigger_apicapture"></span>**ID \_ 觸發程式 \_ APICAPTURE**</span><span class="sxs-lookup"><span data-stu-id="6e054-473"><span id="IDS_TRIGGER_APICAPTURE"></span><span id="ids_trigger_apicapture"></span>**IDS\_TRIGGER\_APICAPTURE**</span></span>  
<span data-ttu-id="6e054-474">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-474">Not used.</span></span>

<span data-ttu-id="6e054-475"><span id="IDS_ERROR_CALLDATA"></span><span id="ids_error_calldata"></span>**識別碼 \_ 錯誤 \_ CALLDATA**</span><span class="sxs-lookup"><span data-stu-id="6e054-475"><span id="IDS_ERROR_CALLDATA"></span><span id="ids_error_calldata"></span>**IDS\_ERROR\_CALLDATA**</span></span>  
<span data-ttu-id="6e054-476">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-476">Not used.</span></span>

<span data-ttu-id="6e054-477"><span id="IDS_ERROR_CREATINGLOG"></span><span id="ids_error_creatinglog"></span>**識別碼 \_ 錯誤 \_ CREATINGLOG**</span><span class="sxs-lookup"><span data-stu-id="6e054-477"><span id="IDS_ERROR_CREATINGLOG"></span><span id="ids_error_creatinglog"></span>**IDS\_ERROR\_CREATINGLOG**</span></span>  
<span data-ttu-id="6e054-478">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-478">Not used.</span></span>

<span data-ttu-id="6e054-479"><span id="IDS_UNKNOWNCALL"></span><span id="ids_unknowncall"></span>**識別碼 \_ UNKNOWNCALL**</span><span class="sxs-lookup"><span data-stu-id="6e054-479"><span id="IDS_UNKNOWNCALL"></span><span id="ids_unknowncall"></span>**IDS\_UNKNOWNCALL**</span></span>  
<span data-ttu-id="6e054-480">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-480">Not used.</span></span>

<span data-ttu-id="6e054-481"><span id="IDS_WARN_FEATURE_LEVEL_CHANGED"></span><span id="ids_warn_feature_level_changed"></span>**識別碼 \_ 警告 \_ 功能 \_ 層級 \_ 已變更**</span><span class="sxs-lookup"><span data-stu-id="6e054-481"><span id="IDS_WARN_FEATURE_LEVEL_CHANGED"></span><span id="ids_warn_feature_level_changed"></span>**IDS\_WARN\_FEATURE\_LEVEL\_CHANGED**</span></span>  
<span data-ttu-id="6e054-482">未使用。</span><span class="sxs-lookup"><span data-stu-id="6e054-482">Not used.</span></span>

<span data-ttu-id="6e054-483"><span id="ID_STATUS_FREQUENCY"></span><span id="id_status_frequency"></span>**識別碼 \_ 狀態 \_ 頻率**</span><span class="sxs-lookup"><span data-stu-id="6e054-483"><span id="ID_STATUS_FREQUENCY"></span><span id="id_status_frequency"></span>**ID\_STATUS\_FREQUENCY**</span></span>  

<span data-ttu-id="6e054-484"><span id="ID_DISABLE_HUD"></span><span id="id_disable_hud"></span>**ID \_ 停用 \_ 抬頭顯示器**</span><span class="sxs-lookup"><span data-stu-id="6e054-484"><span id="ID_DISABLE_HUD"></span><span id="id_disable_hud"></span>**ID\_DISABLE\_HUD**</span></span>  

<span data-ttu-id="6e054-485"><span id="ID_DISABLE_COMPAT"></span><span id="id_disable_compat"></span>**識別碼 \_ 停用 \_ 相容性**</span><span class="sxs-lookup"><span data-stu-id="6e054-485"><span id="ID_DISABLE_COMPAT"></span><span id="id_disable_compat"></span>**ID\_DISABLE\_COMPAT**</span></span>  

<span data-ttu-id="6e054-486"><span id="ID_COLLECT_CALLSTACKS"></span><span id="id_collect_callstacks"></span>**識別碼 \_ 收集 \_ 呼叫堆疊**</span><span class="sxs-lookup"><span data-stu-id="6e054-486"><span id="ID_COLLECT_CALLSTACKS"></span><span id="id_collect_callstacks"></span>**ID\_COLLECT\_CALLSTACKS**</span></span>  

<span data-ttu-id="6e054-487"><span id="ID_ENABLE_SDKERROR_STOP"></span><span id="id_enable_sdkerror_stop"></span>**識別碼 \_ 啟用 \_ SDKERROR \_ 停止**</span><span class="sxs-lookup"><span data-stu-id="6e054-487"><span id="ID_ENABLE_SDKERROR_STOP"></span><span id="id_enable_sdkerror_stop"></span>**ID\_ENABLE\_SDKERROR\_STOP**</span></span>  

## <a name="requirements"></a><span data-ttu-id="6e054-488">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e054-488">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6e054-489">標頭</span><span class="sxs-lookup"><span data-stu-id="6e054-489">Header</span></span></p></td><td><span data-ttu-id="6e054-490">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="6e054-490">Vspixengine.h</span></span></td></tr></tbody></table>

 

 




---
description: 在 debug 要求中產生著色器追蹤指令的要求。 以追蹤為基礎的偵錯工具會發生在 CPU (變形) ，而不是 GPU。
MS-HAID: vspixengine.IDebugShaderRequest2\_GenerateInstructions\_IPixErrorCallback\_ptr\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr\_IDebugShaderCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IDebugShaderRequest2：： GenerateInstructions 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50685D38-AA85-43D7-9199-12B3776708C2
api_name:
- IDebugShaderRequest2.GenerateInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9c1bc2f6b3f885159f21cd7e644545d7639d6b3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510126"
---
# <a name="span-idvspixengineidebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptrspanidebugshaderrequest2generateinstructions-method"></a><span data-ttu-id="350f1-104"><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>IDebugShaderRequest2：： GenerateInstructions 方法</span><span class="sxs-lookup"><span data-stu-id="350f1-104"><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>IDebugShaderRequest2::GenerateInstructions method</span></span>

<span data-ttu-id="350f1-105">在 debug 要求中產生著色器追蹤指令的要求。</span><span class="sxs-lookup"><span data-stu-id="350f1-105">Requests to generate shader trace instructions in a debug request.</span></span> <span data-ttu-id="350f1-106">以追蹤為基礎的偵錯工具會發生在 CPU (變形) ，而不是 GPU。</span><span class="sxs-lookup"><span data-stu-id="350f1-106">Trace-based debugging occurs on the CPU (warp) instead of the GPU.</span></span>

## <a name="syntax"></a><span data-ttu-id="350f1-107">語法</span><span class="sxs-lookup"><span data-stu-id="350f1-107">Syntax</span></span>


```C++
HRESULT GenerateInstructions(
   IPixErrorCallback *      errorCallback,
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory,
   IDebugShaderCallback *   pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="350f1-108">參數</span><span class="sxs-lookup"><span data-stu-id="350f1-108">Parameters</span></span>

<span data-ttu-id="350f1-109">*errorCallback* </span><span class="sxs-lookup"><span data-stu-id="350f1-109">*errorCallback* </span></span>  
<span data-ttu-id="350f1-110">產生著色器追蹤指令時可能發生之錯誤的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="350f1-110">The address of a callback for errors that might occur while generating shader trace instructions.</span></span>

<span data-ttu-id="350f1-111">*requestInfo* </span><span class="sxs-lookup"><span data-stu-id="350f1-111">*requestInfo* </span></span>  
<span data-ttu-id="350f1-112">描述要求的事件/頂點/圖元之 DebugShaderRequestInfo 結構的位址。</span><span class="sxs-lookup"><span data-stu-id="350f1-112">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

<span data-ttu-id="350f1-113">*pPixelHistory* </span><span class="sxs-lookup"><span data-stu-id="350f1-113">*pPixelHistory* </span></span>  
<span data-ttu-id="350f1-114">用來尋找關聯圖元以進行 debug 的圖元歷程記錄結果位址。</span><span class="sxs-lookup"><span data-stu-id="350f1-114">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="350f1-115">只適用于對圖元著色器進行調試時。</span><span class="sxs-lookup"><span data-stu-id="350f1-115">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="350f1-116">*pCallback* </span><span class="sxs-lookup"><span data-stu-id="350f1-116">*pCallback* </span></span>  
<span data-ttu-id="350f1-117">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="350f1-117">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="350f1-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="350f1-118">Return value</span></span>

<span data-ttu-id="350f1-119">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="350f1-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="350f1-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="350f1-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="350f1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="350f1-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="350f1-122">標頭</span><span class="sxs-lookup"><span data-stu-id="350f1-122">Header</span></span></p></td><td><span data-ttu-id="350f1-123">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="350f1-123">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="350f1-124"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="350f1-124"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="350f1-125">**IDebugShaderRequest2**</span><span class="sxs-lookup"><span data-stu-id="350f1-125">**IDebugShaderRequest2**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 

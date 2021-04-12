---
description: 針對指定的管線階段、圖元/頂點（如果適用、事件和框架）啟動著色器偵測會話的要求。
MS-HAID: vspixengine.IDebugShaderRequest\_BeginDebugShader\_IPixErrorCallback\_ptr\_EventID\_DWORD\_DWORD\_Point2D\_PipeLineStages\_PixelHistoryOperation\_ptr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IDebugShaderRequest：： BeginDebugShader 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC93D31C-8593-4B03-B974-87B886B9431D
api_name:
- IDebugShaderRequest.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b6512dc8aa67b3f4d128be3cd2dcd2b622ba2035
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109256"
---
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span data-ttu-id="11e82-103"><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>IDebugShaderRequest：： BeginDebugShader 方法</span><span class="sxs-lookup"><span data-stu-id="11e82-103"><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>IDebugShaderRequest::BeginDebugShader method</span></span>

<span data-ttu-id="11e82-104">針對指定的管線階段、圖元/頂點（如果適用、事件和框架）啟動著色器偵測會話的要求。</span><span class="sxs-lookup"><span data-stu-id="11e82-104">Requests to start a shader debugging session for the specified pipeline stage, pixel/vertex if applicable, event, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="11e82-105">語法</span><span class="sxs-lookup"><span data-stu-id="11e82-105">Syntax</span></span>


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback *     errorCallback,
   EventID                 eventID,
   DWORD                   frameNumber,
   DWORD                   vertex,
   Point2D                 pixel,
   PipeLineStages          stage,
   PixelHistoryOperation * pPixelHistory,
   DWORD *                 pDevice
);
```

## <a name="parameters"></a><span data-ttu-id="11e82-106">參數</span><span class="sxs-lookup"><span data-stu-id="11e82-106">Parameters</span></span>

<span data-ttu-id="11e82-107">*errorCallback* </span><span class="sxs-lookup"><span data-stu-id="11e82-107">*errorCallback* </span></span>  
<span data-ttu-id="11e82-108">偵錯工具期間可能發生的錯誤回呼位址。</span><span class="sxs-lookup"><span data-stu-id="11e82-108">The address of a callback for errors that might occur during debugging.</span></span>

<span data-ttu-id="11e82-109">*eventID* </span><span class="sxs-lookup"><span data-stu-id="11e82-109">*eventID* </span></span>  
<span data-ttu-id="11e82-110">指定的事件。</span><span class="sxs-lookup"><span data-stu-id="11e82-110">The specified event.</span></span>

<span data-ttu-id="11e82-111">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="11e82-111">*frameNumber* </span></span>  
<span data-ttu-id="11e82-112">指定的框架。</span><span class="sxs-lookup"><span data-stu-id="11e82-112">The specified frame.</span></span>

<span data-ttu-id="11e82-113">*頂點* </span><span class="sxs-lookup"><span data-stu-id="11e82-113">*vertex* </span></span>  
<span data-ttu-id="11e82-114">指定的頂點。</span><span class="sxs-lookup"><span data-stu-id="11e82-114">The specified vertex.</span></span> <span data-ttu-id="11e82-115">只適用于對頂點著色器進行調試時。</span><span class="sxs-lookup"><span data-stu-id="11e82-115">Only applies when debugging a vertex shader.</span></span>

<span data-ttu-id="11e82-116">*圖元* </span><span class="sxs-lookup"><span data-stu-id="11e82-116">*pixel* </span></span>  
<span data-ttu-id="11e82-117">指定的圖元。</span><span class="sxs-lookup"><span data-stu-id="11e82-117">The specified pixel.</span></span> <span data-ttu-id="11e82-118">只適用于對圖元著色器進行調試時。</span><span class="sxs-lookup"><span data-stu-id="11e82-118">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="11e82-119">*階段* </span><span class="sxs-lookup"><span data-stu-id="11e82-119">*stage* </span></span>  
<span data-ttu-id="11e82-120">指定的管線階段。</span><span class="sxs-lookup"><span data-stu-id="11e82-120">The specified pipeline stage.</span></span>

<span data-ttu-id="11e82-121">*pPixelHistory* </span><span class="sxs-lookup"><span data-stu-id="11e82-121">*pPixelHistory* </span></span>  
<span data-ttu-id="11e82-122">用來尋找關聯圖元以進行 debug 的圖元歷程記錄結果位址。</span><span class="sxs-lookup"><span data-stu-id="11e82-122">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="11e82-123">只適用于對圖元著色器進行調試時。</span><span class="sxs-lookup"><span data-stu-id="11e82-123">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="11e82-124">*pDevice* </span><span class="sxs-lookup"><span data-stu-id="11e82-124">*pDevice* </span></span>  
<span data-ttu-id="11e82-125">要傳遞至偵測引擎以便與此 (的偵測引擎進行通訊的位址) 的 readprocessmemory debug engine。</span><span class="sxs-lookup"><span data-stu-id="11e82-125">The address to pass to the debug engine for communicating with this debug session (debug engine readprocessmemory on this address).</span></span>

## <a name="return-value"></a><span data-ttu-id="11e82-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="11e82-126">Return value</span></span>

<span data-ttu-id="11e82-127">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="11e82-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="11e82-128">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="11e82-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="11e82-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="11e82-129">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="11e82-130">標頭</span><span class="sxs-lookup"><span data-stu-id="11e82-130">Header</span></span></p></td><td><span data-ttu-id="11e82-131">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="11e82-131">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="11e82-132"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="11e82-132"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="11e82-133">**IDebugShaderRequest**</span><span class="sxs-lookup"><span data-stu-id="11e82-133">**IDebugShaderRequest**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 

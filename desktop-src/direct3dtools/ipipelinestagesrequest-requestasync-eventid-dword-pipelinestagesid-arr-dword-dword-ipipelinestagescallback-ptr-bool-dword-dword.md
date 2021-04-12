---
description: 取得 [圖形管線階段] 視窗預覽影像的非同步要求。
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestAsync\_EventID\_DWORD\_PipeLineStagesID\_arr\_DWORD\_DWORD\_IPipeLineStagesCallback\_ptr\_BOOL\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B725E541-EAC8-49DE-9EE7-C20698FE4A1F
api_name:
- IPipeLineStagesRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 89c67689668aa1c4227b33d861495c2504e5d626
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510124"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dwordspanipipelinestagesrequestrequestasync-method"></a><span data-ttu-id="fe845-103"><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>IPipeLineStagesRequest：： RequestAsync 方法</span><span class="sxs-lookup"><span data-stu-id="fe845-103"><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>IPipeLineStagesRequest::RequestAsync method</span></span>

<span data-ttu-id="fe845-104">取得 [圖形管線階段] 視窗預覽影像的非同步要求。</span><span class="sxs-lookup"><span data-stu-id="fe845-104">An asynchronous request to get preview images for the graphics pipeline stages window.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe845-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe845-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   DWORD                     numStages,
   PipeLineStagesID []       count1_stageIds,
   DWORD                     width,
   DWORD                     height,
   IPipeLineStagesCallback * requestCallback,
   BOOL                      getMeshData,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="fe845-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe845-106">Parameters</span></span>

<span data-ttu-id="fe845-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="fe845-107">*eventID* </span></span>  
<span data-ttu-id="fe845-108">要求影像的圖形事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe845-108">The ID of the graphics event that images are being requested for.</span></span>

<span data-ttu-id="fe845-109">*numStages* </span><span class="sxs-lookup"><span data-stu-id="fe845-109">*numStages* </span></span>  
<span data-ttu-id="fe845-110">要求影像的管線階段數。</span><span class="sxs-lookup"><span data-stu-id="fe845-110">The number of pipeline stages that images are being requested for.</span></span>

<span data-ttu-id="fe845-111">*count1 \_ stageIds* </span><span class="sxs-lookup"><span data-stu-id="fe845-111">*count1\_stageIds* </span></span>  
<span data-ttu-id="fe845-112">要求影像的管線階段識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe845-112">IDs of the pipeline stages that images are being requested for.</span></span>

<span data-ttu-id="fe845-113">*寬度* </span><span class="sxs-lookup"><span data-stu-id="fe845-113">*width* </span></span>  
<span data-ttu-id="fe845-114">要求的影像寬度。</span><span class="sxs-lookup"><span data-stu-id="fe845-114">The width of the requested images.</span></span>

<span data-ttu-id="fe845-115">*高度* </span><span class="sxs-lookup"><span data-stu-id="fe845-115">*height* </span></span>  
<span data-ttu-id="fe845-116">要求之影像的高度。</span><span class="sxs-lookup"><span data-stu-id="fe845-116">The height of the requested images.</span></span>

<span data-ttu-id="fe845-117">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="fe845-117">*requestCallback* </span></span>  
<span data-ttu-id="fe845-118">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="fe845-118">The address of the callback used to notify the host of results.</span></span>

<span data-ttu-id="fe845-119">*getMeshData* </span><span class="sxs-lookup"><span data-stu-id="fe845-119">*getMeshData* </span></span>  
<span data-ttu-id="fe845-120">true 表示傳回網格資料;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="fe845-120">true to return mesh data; otherwise false.</span></span>

<span data-ttu-id="fe845-121">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="fe845-121">*requestCookie* </span></span>  
<span data-ttu-id="fe845-122">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="fe845-122">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="fe845-123">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="fe845-123">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="fe845-124">未使用。</span><span class="sxs-lookup"><span data-stu-id="fe845-124">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe845-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe845-125">Return value</span></span>

<span data-ttu-id="fe845-126">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="fe845-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fe845-127">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fe845-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe845-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe845-128">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fe845-129">標頭</span><span class="sxs-lookup"><span data-stu-id="fe845-129">Header</span></span></p></td><td><span data-ttu-id="fe845-130">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="fe845-130">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="fe845-131"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe845-131"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="fe845-132">**IPipeLineStagesRequest**</span><span class="sxs-lookup"><span data-stu-id="fe845-132">**IPipeLineStagesRequest**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 

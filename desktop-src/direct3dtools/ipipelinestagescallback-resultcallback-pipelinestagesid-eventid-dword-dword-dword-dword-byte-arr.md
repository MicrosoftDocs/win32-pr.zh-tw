---
description: 回呼，會通知主機 assocaited 要求所傳回的管線階段影像資訊。
MS-HAID: vspixengine.IPipeLineStagesCallback\_ResultCallback\_PipeLineStagesID\_EventID\_DWORD\_DWORD\_DWORD\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 922DBEE0-CE47-4292-A5E6-4503E6F77A23
api_name:
- IPipeLineStagesCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c9c09c0fe1e68dc0d0613589ff8b3d5037face9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317795"
---
# <a name="span-idvspixengineipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arrspanipipelinestagescallbackresultcallback-method"></a><span data-ttu-id="f54bf-103"><span id="vspixengine.ipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arr"></span>IPipeLineStagesCallback：： ResultCallback 方法</span><span class="sxs-lookup"><span data-stu-id="f54bf-103"><span id="vspixengine.ipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arr"></span>IPipeLineStagesCallback::ResultCallback method</span></span>

<span data-ttu-id="f54bf-104">回呼，會通知主機 assocaited 要求所傳回的管線階段影像資訊。</span><span class="sxs-lookup"><span data-stu-id="f54bf-104">A callback that notifies the host of pipeline stages image information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="f54bf-105">語法</span><span class="sxs-lookup"><span data-stu-id="f54bf-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   PipeLineStagesID stageId,
   EventID          eid,
   DWORD            width,
   DWORD            height,
   DWORD            format,
   DWORD            size,
   BYTE []          count5_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="f54bf-106">參數</span><span class="sxs-lookup"><span data-stu-id="f54bf-106">Parameters</span></span>

<span data-ttu-id="f54bf-107">*stageId* </span><span class="sxs-lookup"><span data-stu-id="f54bf-107">*stageId* </span></span>  
<span data-ttu-id="f54bf-108">結果中表示的管線階段。</span><span class="sxs-lookup"><span data-stu-id="f54bf-108">The pipeline stage represented in the results.</span></span>

<span data-ttu-id="f54bf-109">*開齋節* </span><span class="sxs-lookup"><span data-stu-id="f54bf-109">*eid* </span></span>  
<span data-ttu-id="f54bf-110">結果中表示的事件。</span><span class="sxs-lookup"><span data-stu-id="f54bf-110">The event represented in the results.</span></span>

<span data-ttu-id="f54bf-111">*寬度* </span><span class="sxs-lookup"><span data-stu-id="f54bf-111">*width* </span></span>  
<span data-ttu-id="f54bf-112">管線視覺效果影像的寬度。</span><span class="sxs-lookup"><span data-stu-id="f54bf-112">The width of the pipeline visualization image.</span></span>

<span data-ttu-id="f54bf-113">*高度* </span><span class="sxs-lookup"><span data-stu-id="f54bf-113">*height* </span></span>  
<span data-ttu-id="f54bf-114">管線視覺效果影像的高度。</span><span class="sxs-lookup"><span data-stu-id="f54bf-114">The height of the pipeline visualization image.</span></span>

<span data-ttu-id="f54bf-115">*格式* </span><span class="sxs-lookup"><span data-stu-id="f54bf-115">*format* </span></span>  
<span data-ttu-id="f54bf-116">管線視覺效果影像的格式。</span><span class="sxs-lookup"><span data-stu-id="f54bf-116">The format of the pipeline visualization image.</span></span>

<span data-ttu-id="f54bf-117">*大小* </span><span class="sxs-lookup"><span data-stu-id="f54bf-117">*size* </span></span>  
<span data-ttu-id="f54bf-118">影像的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f54bf-118">The size of the image in bytes.</span></span>

<span data-ttu-id="f54bf-119">*count5 \_ 緩衝區* </span><span class="sxs-lookup"><span data-stu-id="f54bf-119">*count5\_buffer* </span></span>  
<span data-ttu-id="f54bf-120">管線視覺效果影像。</span><span class="sxs-lookup"><span data-stu-id="f54bf-120">The pipeline visualization image.</span></span>

## <a name="return-value"></a><span data-ttu-id="f54bf-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="f54bf-121">Return value</span></span>

<span data-ttu-id="f54bf-122">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f54bf-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f54bf-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f54bf-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f54bf-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f54bf-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f54bf-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f54bf-125">Header</span></span></p></td><td><span data-ttu-id="f54bf-126">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="f54bf-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f54bf-127"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="f54bf-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f54bf-128">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="f54bf-128">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 

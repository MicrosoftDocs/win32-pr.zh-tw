---
description: 回呼，通知主機哪些管線階段無法針對相關要求中所指定的事件傳回網格資料。
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataNotAvailableCallback\_UINT\_PipeLineStageError\_arr\_UINT\_UINT\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback：： MeshDataNotAvailableCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A51E7C45-C1F0-4576-8638-9C3B185385BA
api_name:
- IPipeLineStagesCallback.MeshDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 42391c342e2f11b39d1535b5286a92e161d0fd9b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467907"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventidspanipipelinestagescallbackmeshdatanotavailablecallback-method"></a><span data-ttu-id="9fee4-103"><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>IPipeLineStagesCallback：： MeshDataNotAvailableCallback 方法</span><span class="sxs-lookup"><span data-stu-id="9fee4-103"><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>IPipeLineStagesCallback::MeshDataNotAvailableCallback method</span></span>

<span data-ttu-id="9fee4-104">回呼，通知主機哪些管線階段無法針對相關要求中所指定的事件傳回網格資料。</span><span class="sxs-lookup"><span data-stu-id="9fee4-104">A callback that notifies the host of which pipeline stages are not able to return mesh data for the event specified in the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fee4-105">語法</span><span class="sxs-lookup"><span data-stu-id="9fee4-105">Syntax</span></span>


```C++
HRESULT MeshDataNotAvailableCallback(
   UINT                  numberStages,
   PipeLineStageError [] count0_errors,
   UINT                  width,
   UINT                  height,
   EventID               eid
);
```

## <a name="parameters"></a><span data-ttu-id="9fee4-106">參數</span><span class="sxs-lookup"><span data-stu-id="9fee4-106">Parameters</span></span>

<span data-ttu-id="9fee4-107">*numberStages* </span><span class="sxs-lookup"><span data-stu-id="9fee4-107">*numberStages* </span></span>  
<span data-ttu-id="9fee4-108">傳回的階段錯誤數。</span><span class="sxs-lookup"><span data-stu-id="9fee4-108">The number of stage errors returned.</span></span>

<span data-ttu-id="9fee4-109">*count0 \_ 錯誤* </span><span class="sxs-lookup"><span data-stu-id="9fee4-109">*count0\_errors* </span></span>  
<span data-ttu-id="9fee4-110">管線階段錯誤。</span><span class="sxs-lookup"><span data-stu-id="9fee4-110">The pipeline stage errors.</span></span>

<span data-ttu-id="9fee4-111">*寬度* </span><span class="sxs-lookup"><span data-stu-id="9fee4-111">*width* </span></span>  
<span data-ttu-id="9fee4-112">使用繪製呼叫 assocaited 的交換鏈寬度。</span><span class="sxs-lookup"><span data-stu-id="9fee4-112">The width of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="9fee4-113">這是在要求管線預覽影像時使用。</span><span class="sxs-lookup"><span data-stu-id="9fee4-113">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="9fee4-114">*高度* </span><span class="sxs-lookup"><span data-stu-id="9fee4-114">*height* </span></span>  
<span data-ttu-id="9fee4-115">使用繪製呼叫 assocaited 交換鏈的高度。</span><span class="sxs-lookup"><span data-stu-id="9fee4-115">The height of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="9fee4-116">這是在要求管線預覽影像時使用。</span><span class="sxs-lookup"><span data-stu-id="9fee4-116">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="9fee4-117">*開齋節* </span><span class="sxs-lookup"><span data-stu-id="9fee4-117">*eid* </span></span>  
<span data-ttu-id="9fee4-118">結果中表示的事件。</span><span class="sxs-lookup"><span data-stu-id="9fee4-118">The event represented in the results.</span></span>

## <a name="return-value"></a><span data-ttu-id="9fee4-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="9fee4-119">Return value</span></span>

<span data-ttu-id="9fee4-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9fee4-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9fee4-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9fee4-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fee4-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fee4-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9fee4-123">標頭</span><span class="sxs-lookup"><span data-stu-id="9fee4-123">Header</span></span></p></td><td><span data-ttu-id="9fee4-124">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="9fee4-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9fee4-125"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="9fee4-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9fee4-126">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="9fee4-126">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 

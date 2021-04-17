---
description: 回呼，會通知主機 assocaited 要求的繪製呼叫所使用的管線階段。
MS-HAID: vspixengine.IPipeLineStagesCallback\_GetSupportedStages\_DWORD\_PipeLineStage\_arr\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback：： GetSupportedStages 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7046A41-5C9C-42FE-B1E2-879A47CE08E3
api_name:
- IPipeLineStagesCallback.GetSupportedStages
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c55c7f8bfa6b5b69ea2a46dd6023021a6b4ab6c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509945"
---
# <a name="span-idvspixengineipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uintspanipipelinestagescallbackgetsupportedstages-method"></a><span data-ttu-id="4eed5-103"><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>IPipeLineStagesCallback：： GetSupportedStages 方法</span><span class="sxs-lookup"><span data-stu-id="4eed5-103"><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>IPipeLineStagesCallback::GetSupportedStages method</span></span>

<span data-ttu-id="4eed5-104">回呼，會通知主機 assocaited 要求的繪製呼叫所使用的管線階段。</span><span class="sxs-lookup"><span data-stu-id="4eed5-104">A callback that notifies the host of which pipeline stages are used by the draw call of the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eed5-105">語法</span><span class="sxs-lookup"><span data-stu-id="4eed5-105">Syntax</span></span>


```C++
HRESULT GetSupportedStages(
   DWORD            numColumns,
   PipeLineStage [] count0_pStages,
   UINT             swapChainWidth,
   UINT             swapChainHeight
);
```

## <a name="parameters"></a><span data-ttu-id="4eed5-106">參數</span><span class="sxs-lookup"><span data-stu-id="4eed5-106">Parameters</span></span>

<span data-ttu-id="4eed5-107">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="4eed5-107">*numColumns* </span></span>  
<span data-ttu-id="4eed5-108">傳回的階段數。</span><span class="sxs-lookup"><span data-stu-id="4eed5-108">The number of stages returned.</span></span>

<span data-ttu-id="4eed5-109">*count0 \_ pStages* </span><span class="sxs-lookup"><span data-stu-id="4eed5-109">*count0\_pStages* </span></span>  
<span data-ttu-id="4eed5-110">管線階段。</span><span class="sxs-lookup"><span data-stu-id="4eed5-110">The pipeline stages.</span></span>

<span data-ttu-id="4eed5-111">*swapChainWidth* </span><span class="sxs-lookup"><span data-stu-id="4eed5-111">*swapChainWidth* </span></span>  
<span data-ttu-id="4eed5-112">使用繪製呼叫 assocaited 的交換鏈寬度。</span><span class="sxs-lookup"><span data-stu-id="4eed5-112">The width of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="4eed5-113">這是在要求管線預覽影像時使用。</span><span class="sxs-lookup"><span data-stu-id="4eed5-113">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="4eed5-114">*swapChainHeight* </span><span class="sxs-lookup"><span data-stu-id="4eed5-114">*swapChainHeight* </span></span>  
<span data-ttu-id="4eed5-115">使用繪製呼叫 assocaited 交換鏈的高度。</span><span class="sxs-lookup"><span data-stu-id="4eed5-115">The height of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="4eed5-116">這是在要求管線預覽影像時使用。</span><span class="sxs-lookup"><span data-stu-id="4eed5-116">This is used when requesting pipeline preview images.</span></span>

## <a name="return-value"></a><span data-ttu-id="4eed5-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="4eed5-117">Return value</span></span>

<span data-ttu-id="4eed5-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4eed5-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4eed5-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4eed5-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eed5-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4eed5-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4eed5-121">標頭</span><span class="sxs-lookup"><span data-stu-id="4eed5-121">Header</span></span></p></td><td><span data-ttu-id="4eed5-122">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="4eed5-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4eed5-123"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="4eed5-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4eed5-124">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="4eed5-124">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 

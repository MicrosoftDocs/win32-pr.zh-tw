---
description: 通知主機 ThreadData 無法用於特定管線階段和事件的回呼。
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataNotAvailableCallback\_PipeLineStageError\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback2：： ThreadDataNotAvailableCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 231DC830-5F1A-4DDA-B5D0-C7FBCEDCB2A0
api_name:
- IPipeLineStagesCallback2.ThreadDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a0c9cc0bc32b6d01394be1403e961d7ae37a1d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970303"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventidspanipipelinestagescallback2threaddatanotavailablecallback-method"></a><span data-ttu-id="49367-103"><span id="vspixengine.ipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventid"></span>IPipeLineStagesCallback2：： ThreadDataNotAvailableCallback 方法</span><span class="sxs-lookup"><span data-stu-id="49367-103"><span id="vspixengine.ipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventid"></span>IPipeLineStagesCallback2::ThreadDataNotAvailableCallback method</span></span>

<span data-ttu-id="49367-104">通知主機 ThreadData 無法用於特定管線階段和事件的回呼。</span><span class="sxs-lookup"><span data-stu-id="49367-104">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="49367-105">語法</span><span class="sxs-lookup"><span data-stu-id="49367-105">Syntax</span></span>


```C++
HRESULT ThreadDataNotAvailableCallback(
   PipeLineStageError error,
   EventID            eid
);
```

## <a name="parameters"></a><span data-ttu-id="49367-106">參數</span><span class="sxs-lookup"><span data-stu-id="49367-106">Parameters</span></span>

<span data-ttu-id="49367-107">*錯誤* </span><span class="sxs-lookup"><span data-stu-id="49367-107">*error* </span></span>  
<span data-ttu-id="49367-108">管線階段錯誤。</span><span class="sxs-lookup"><span data-stu-id="49367-108">The pipeline stage error.</span></span>

<span data-ttu-id="49367-109">*開齋節* </span><span class="sxs-lookup"><span data-stu-id="49367-109">*eid* </span></span>  
<span data-ttu-id="49367-110">結果中表示的事件。</span><span class="sxs-lookup"><span data-stu-id="49367-110">The event represented in the results.</span></span>

## <a name="return-value"></a><span data-ttu-id="49367-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="49367-111">Return value</span></span>

<span data-ttu-id="49367-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="49367-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="49367-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="49367-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="49367-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="49367-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="49367-115">標頭</span><span class="sxs-lookup"><span data-stu-id="49367-115">Header</span></span></p></td><td><span data-ttu-id="49367-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="49367-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="49367-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="49367-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="49367-118">**IPipeLineStagesCallback2**</span><span class="sxs-lookup"><span data-stu-id="49367-118">**IPipeLineStagesCallback2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 

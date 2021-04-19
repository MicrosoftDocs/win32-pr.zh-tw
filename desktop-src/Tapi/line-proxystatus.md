---
description: '\_當應用程式目前開啟的那一行上的可用 proxy 變更時，就會傳送 line PROXYSTATUS 訊息。'
ms.assetid: e20d4b48-a72a-4a83-ae04-a608791a1a3a
title: 'LINE_PROXYSTATUS 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb00c5df4f531309bdd1311fb7c34c3e9967a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994715"
---
# <a name="line_proxystatus-message"></a><span data-ttu-id="a03a3-103">行 \_ PROXYSTATUS 訊息</span><span class="sxs-lookup"><span data-stu-id="a03a3-103">LINE\_PROXYSTATUS message</span></span>

<span data-ttu-id="a03a3-104">當應用程式目前開啟的那一行上的可用 proxy 變更時，就會傳送 **line \_ PROXYSTATUS** 訊息。</span><span class="sxs-lookup"><span data-stu-id="a03a3-104">The **LINE\_PROXYSTATUS** message is sent when the available proxies change on a line that the application currently has open.</span></span>

<span data-ttu-id="a03a3-105">TAPISRV 會在使用 LINEPROXYSTATUS OPEN 和 LINEPROXYSTATUS ALLOPENFORACD 的 [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)函式中 \_ ， \_ 或 [](/windows/desktop/api/Tapi/nf-tapi-lineclose)使用 lineClose \_ CLOSE (所有 [**LINEPROXYSTATUS \_ 常數**](lineproxystatus--constants.md)) 來產生此訊息。</span><span class="sxs-lookup"><span data-stu-id="a03a3-105">TAPISRV generates this message during a [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) function using LINEPROXYSTATUS\_OPEN and LINEPROXYSTATUS\_ALLOPENFORACD or a [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) function using LINEPROXYSTATUS\_CLOSE (all [**LINEPROXYSTATUS\_ Constants**](lineproxystatus--constants.md)).</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="a03a3-106">參數</span><span class="sxs-lookup"><span data-stu-id="a03a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a03a3-107">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="a03a3-107">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a03a3-108">應用程式線路裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a03a3-108">The application's handle to the line device.</span></span> <span data-ttu-id="a03a3-109">這與代理程式處理常式相關。</span><span class="sxs-lookup"><span data-stu-id="a03a3-109">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="a03a3-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="a03a3-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="a03a3-111">開啟行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="a03a3-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="a03a3-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="a03a3-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="a03a3-113">指定已變更的佇列狀態。</span><span class="sxs-lookup"><span data-stu-id="a03a3-113">Specifies the queue status that has changed.</span></span> <span data-ttu-id="a03a3-114">可以是一或多個 [**LINEPROXYSTATUS \_ 常數**](lineproxystatus--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="a03a3-114">Can be one or more of the [**LINEPROXYSTATUS\_ constants**](lineproxystatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a03a3-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="a03a3-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="a03a3-116">如果 *dwParam1* 設為 LINEPROXYSTATUS \_ OPEN 或 LINEPROXYSTATUS \_ CLOSE， *dwParam2* 會指出相關的 proxy 要求類型，也就是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="a03a3-116">If *dwParam1* is set to LINEPROXYSTATUS\_OPEN or LINEPROXYSTATUS\_CLOSE, *dwParam2* indicates the related proxy request type, which is one of the following:</span></span>

-   <span data-ttu-id="a03a3-117">LINEPROXYREQUEST \_ SETAGENTGROUP</span><span class="sxs-lookup"><span data-stu-id="a03a3-117">LINEPROXYREQUEST\_SETAGENTGROUP</span></span>
-   <span data-ttu-id="a03a3-118">LINEPROXYREQUEST \_ SETAGENTSTATE</span><span class="sxs-lookup"><span data-stu-id="a03a3-118">LINEPROXYREQUEST\_SETAGENTSTATE</span></span>
-   <span data-ttu-id="a03a3-119">LINEPROXYREQUEST \_ SETAGENTACTIVITY</span><span class="sxs-lookup"><span data-stu-id="a03a3-119">LINEPROXYREQUEST\_SETAGENTACTIVITY</span></span>
-   <span data-ttu-id="a03a3-120">LINEPROXYREQUEST \_ GETAGENTCAPS</span><span class="sxs-lookup"><span data-stu-id="a03a3-120">LINEPROXYREQUEST\_GETAGENTCAPS</span></span>
-   <span data-ttu-id="a03a3-121">LINEPROXYREQUEST \_ GETAGENTSTATUS</span><span class="sxs-lookup"><span data-stu-id="a03a3-121">LINEPROXYREQUEST\_GETAGENTSTATUS</span></span>
-   <span data-ttu-id="a03a3-122">LINEPROXYREQUEST \_ AGENTSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="a03a3-122">LINEPROXYREQUEST\_AGENTSPECIFIC</span></span>
-   <span data-ttu-id="a03a3-123">LINEPROXYREQUEST \_ GETAGENTACTIVITYLIST</span><span class="sxs-lookup"><span data-stu-id="a03a3-123">LINEPROXYREQUEST\_GETAGENTACTIVITYLIST</span></span>
-   <span data-ttu-id="a03a3-124">LINEPROXYREQUEST \_ GETAGENTGROUPLIST</span><span class="sxs-lookup"><span data-stu-id="a03a3-124">LINEPROXYREQUEST\_GETAGENTGROUPLIST</span></span>
-   <span data-ttu-id="a03a3-125">LINEPROXYREQUEST \_ CREATEAGENT</span><span class="sxs-lookup"><span data-stu-id="a03a3-125">LINEPROXYREQUEST\_CREATEAGENT</span></span>
-   <span data-ttu-id="a03a3-126">LINEPROXYREQUEST \_ SETAGENTMEASUREMENTPERIOD</span><span class="sxs-lookup"><span data-stu-id="a03a3-126">LINEPROXYREQUEST\_SETAGENTMEASUREMENTPERIOD</span></span>
-   <span data-ttu-id="a03a3-127">LINEPROXYREQUEST \_ GETAGENTINFO</span><span class="sxs-lookup"><span data-stu-id="a03a3-127">LINEPROXYREQUEST\_GETAGENTINFO</span></span>
-   <span data-ttu-id="a03a3-128">LINEPROXYREQUEST \_ CREATEAGENTSESSION</span><span class="sxs-lookup"><span data-stu-id="a03a3-128">LINEPROXYREQUEST\_CREATEAGENTSESSION</span></span>
-   <span data-ttu-id="a03a3-129">LINEPROXYREQUEST \_ GETAGENTSESSIONLIST</span><span class="sxs-lookup"><span data-stu-id="a03a3-129">LINEPROXYREQUEST\_GETAGENTSESSIONLIST</span></span>
-   <span data-ttu-id="a03a3-130">LINEPROXYREQUEST \_ SETAGENTSESSIONSTATE</span><span class="sxs-lookup"><span data-stu-id="a03a3-130">LINEPROXYREQUEST\_SETAGENTSESSIONSTATE</span></span>
-   <span data-ttu-id="a03a3-131">LINEPROXYREQUEST \_ GETAGENTSESSIONINFO</span><span class="sxs-lookup"><span data-stu-id="a03a3-131">LINEPROXYREQUEST\_GETAGENTSESSIONINFO</span></span>
-   <span data-ttu-id="a03a3-132">LINEPROXYREQUEST \_ GETQUEUELIST</span><span class="sxs-lookup"><span data-stu-id="a03a3-132">LINEPROXYREQUEST\_GETQUEUELIST</span></span>
-   <span data-ttu-id="a03a3-133">LINEPROXYREQUEST \_ SETQUEUEMEASUREMENTPERIOD</span><span class="sxs-lookup"><span data-stu-id="a03a3-133">LINEPROXYREQUEST\_SETQUEUEMEASUREMENTPERIOD</span></span>
-   <span data-ttu-id="a03a3-134">LINEPROXYREQUEST \_ GETQUEUEINFO</span><span class="sxs-lookup"><span data-stu-id="a03a3-134">LINEPROXYREQUEST\_GETQUEUEINFO</span></span>
-   <span data-ttu-id="a03a3-135">LINEPROXYREQUEST \_ GETGROUPLIST</span><span class="sxs-lookup"><span data-stu-id="a03a3-135">LINEPROXYREQUEST\_GETGROUPLIST</span></span>
-   <span data-ttu-id="a03a3-136">LINEPROXYREQUEST \_ SETAGENTSTATEEX</span><span class="sxs-lookup"><span data-stu-id="a03a3-136">LINEPROXYREQUEST\_SETAGENTSTATEEX</span></span>

<span data-ttu-id="a03a3-137">否則， *dwParam2* 會設為零。</span><span class="sxs-lookup"><span data-stu-id="a03a3-137">Otherwise, *dwParam2* is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a03a3-138">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="a03a3-138">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="a03a3-139">保留的。</span><span class="sxs-lookup"><span data-stu-id="a03a3-139">Reserved.</span></span> <span data-ttu-id="a03a3-140">設定為零。</span><span class="sxs-lookup"><span data-stu-id="a03a3-140">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a03a3-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="a03a3-141">Requirements</span></span>



| <span data-ttu-id="a03a3-142">需求</span><span class="sxs-lookup"><span data-stu-id="a03a3-142">Requirement</span></span> | <span data-ttu-id="a03a3-143">值</span><span class="sxs-lookup"><span data-stu-id="a03a3-143">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a03a3-144">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="a03a3-144">TAPI version</span></span><br/> | <span data-ttu-id="a03a3-145">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="a03a3-145">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="a03a3-146">標頭</span><span class="sxs-lookup"><span data-stu-id="a03a3-146">Header</span></span><br/>       | <dl> <span data-ttu-id="a03a3-147"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="a03a3-147"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a03a3-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a03a3-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a03a3-149">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="a03a3-149">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="a03a3-150">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="a03a3-150">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="a03a3-151">**行 \_ PROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="a03a3-151">**LINE\_PROXYREQUEST**</span></span>](line-proxyrequest.md)
</dt> <dt>

[<span data-ttu-id="a03a3-152">**LINEPROXYREQUEST \_ 常數**</span><span class="sxs-lookup"><span data-stu-id="a03a3-152">**LINEPROXYREQUEST\_ Constants**</span></span>](lineproxyrequest--constants.md)
</dt> </dl>

 

 





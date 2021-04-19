---
description: LINECALLFEATURE2 \_ 常數列出可用於會議、傳輸和停車通話的補充功能。
ms.assetid: 67a3b587-dd5b-4ccf-ab69-2137604706b8
title: 'LINECALLFEATURE2_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977e71f722fba34da6b2ecbd6a3e914c34a0aae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989597"
---
# <a name="linecallfeature2_-constants"></a><span data-ttu-id="08f2f-103">LINECALLFEATURE2 \_ 常數</span><span class="sxs-lookup"><span data-stu-id="08f2f-103">LINECALLFEATURE2\_ Constants</span></span>

<span data-ttu-id="08f2f-104">**LINECALLFEATURE2 \_** 常數列出可用於會議、傳輸和停車通話的補充功能。</span><span class="sxs-lookup"><span data-stu-id="08f2f-104">The **LINECALLFEATURE2\_** constants list the supplemental features available for conferencing, transferring, and parking calls.</span></span>

<dl> <dt>

<span data-ttu-id="08f2f-105"><span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2 \_ COMPLCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="08f2f-105"><span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2\_COMPLCALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="08f2f-106">如果這個位是 on，則可以使用 LINECOMPLMODE 回呼選項搭配 LineCompleteCall 來叫用「回呼」功能 \_ 。 [](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)</span><span class="sxs-lookup"><span data-stu-id="08f2f-106">If this bit is on, the "callback" feature can be invoked by using the LINECOMPLMODE\_CALLBACK option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="08f2f-107">LINECALLFEATURE \_ COMPLETECALL 位也會在 **dwCallFeatures** 成員中開啟。</span><span class="sxs-lookup"><span data-stu-id="08f2f-107">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08f2f-108"><span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2 \_ COMPLCAMPON**</span><span class="sxs-lookup"><span data-stu-id="08f2f-108"><span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2\_COMPLCAMPON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="08f2f-109">如果這個位開啟，可以使用 LINECOMPLMODE CAMPON 選項搭配 LineCompleteCall 來叫用「camp 開啟」功能 \_ 。 [](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)</span><span class="sxs-lookup"><span data-stu-id="08f2f-109">If this bit is on, the "camp on" feature can be invoked by using the LINECOMPLMODE\_CAMPON option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="08f2f-110">LINECALLFEATURE \_ COMPLETECALL 位也會在 **dwCallFeatures** 成員中開啟。</span><span class="sxs-lookup"><span data-stu-id="08f2f-110">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08f2f-111"><span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2 \_ COMPLINTRUDE**</span><span class="sxs-lookup"><span data-stu-id="08f2f-111"><span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2\_COMPLINTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="08f2f-112">如果這個位是 on，則可以使用 LINECOMPLMODE intrude 選項搭配 LineCompleteCall 來叫用 "intrude" 功能 \_ 。 [](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)</span><span class="sxs-lookup"><span data-stu-id="08f2f-112">If this bit is on, the "intrude" feature can be invoked by using the LINECOMPLMODE\_INTRUDE option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="08f2f-113">LINECALLFEATURE \_ COMPLETECALL 位也會在 **dwCallFeatures** 成員中開啟。</span><span class="sxs-lookup"><span data-stu-id="08f2f-113">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08f2f-114"><span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2 \_ COMPLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="08f2f-114"><span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2\_COMPLMESSAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="08f2f-115">如果這個位是 on，則可以使用 LINECOMPLMODE message 選項搭配 LineCompleteCall 來叫用「離開訊息」功能 \_ 。 [](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)</span><span class="sxs-lookup"><span data-stu-id="08f2f-115">If this bit is on, the "leave message" feature can be invoked by using the LINECOMPLMODE\_MESSAGE option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="08f2f-116">LINECALLFEATURE \_ COMPLETECALL 位也會在 **dwCallFeatures** 成員中開啟。</span><span class="sxs-lookup"><span data-stu-id="08f2f-116">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08f2f-117"><span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2 \_ NOHOLDCONFERENCE**</span><span class="sxs-lookup"><span data-stu-id="08f2f-117"><span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2\_NOHOLDCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="08f2f-118">如果這個位是 on，則可以使用 LINECALLPARAMFLAGS NOHOLDCONFERENCE 選項搭配 LineSetupConference 來建立「無保留會議」 \_ 。 [](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)</span><span class="sxs-lookup"><span data-stu-id="08f2f-118">If this bit is on, a "no hold conference" can be created by using the LINECALLPARAMFLAGS\_NOHOLDCONFERENCE option with [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference).</span></span> <span data-ttu-id="08f2f-119">LINECALLFEATURE \_ SETUPCONF 位也會在 **dwCallFeatures** 成員中開啟。</span><span class="sxs-lookup"><span data-stu-id="08f2f-119">The LINECALLFEATURE\_SETUPCONF bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08f2f-120"><span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2 \_ ONESTEPTRANSFER**</span><span class="sxs-lookup"><span data-stu-id="08f2f-120"><span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2\_ONESTEPTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="08f2f-121">如果這個位是 on，則可以使用 LINECALLPARAMFLAGS ONESTEPTRANSFER 選項搭配 LineSetupTransfer 來建立「單一步驟轉移」 \_ 。 [](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)</span><span class="sxs-lookup"><span data-stu-id="08f2f-121">If this bit is on, "one step transfer" can be created by using the LINECALLPARAMFLAGS\_ONESTEPTRANSFER option with [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span></span> <span data-ttu-id="08f2f-122">LINECALLFEATURE \_ SETUPTRANSFER 位也會在 **dwCallFeatures** 成員中開啟。</span><span class="sxs-lookup"><span data-stu-id="08f2f-122">The LINECALLFEATURE\_SETUPTRANSFER bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="08f2f-123">如果 [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)中的 **dwCallFeatures2** 成員未指定任何 "COMPL" 位，但指定了 LINECALLFEATURE COMPLETECALL，則其中任何一項都 \_ 可以運作，但服務提供者尚未指定。</span><span class="sxs-lookup"><span data-stu-id="08f2f-123">If none of the "COMPL" bits is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_COMPLETECALL is specified, then it is possible that any of them will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="08f2f-124"><span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2 \_ TRANSFERCONF**</span><span class="sxs-lookup"><span data-stu-id="08f2f-124"><span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2\_TRANSFERCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="08f2f-125">如果這個位開啟， [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) 函式就可以用來將傳輸解析為三向會議。</span><span class="sxs-lookup"><span data-stu-id="08f2f-125">If this bit is on, the [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) function can be used to resolve the transfer as a three-way conference.</span></span> <span data-ttu-id="08f2f-126">LINECALLFEATURE \_ COMPLETETRANSF 位也會在 **dwCallFeatures** 成員中開啟。</span><span class="sxs-lookup"><span data-stu-id="08f2f-126">The LINECALLFEATURE\_COMPLETETRANSF bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08f2f-127"><span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2 \_ TRANSFERNORM**</span><span class="sxs-lookup"><span data-stu-id="08f2f-127"><span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2\_TRANSFERNORM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="08f2f-128">如果這個位是 on， [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) 函式可以用來將傳輸解析為一般傳輸。</span><span class="sxs-lookup"><span data-stu-id="08f2f-128">If this bit is on, the [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) function can be used to resolve the transfer as a normal transfer.</span></span> <span data-ttu-id="08f2f-129">LINECALLFEATURE \_ COMPLETETRANSF 位也會在 **dwCallFeatures** 成員中開啟。</span><span class="sxs-lookup"><span data-stu-id="08f2f-129">The LINECALLFEATURE\_COMPLETETRANSF bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="08f2f-130">如果 [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)中的 **dwCallFeatures2** 成員未指定 TRANSFERNORM 或 TRANSFERCONF，但指定了 LINECALLFEATURE \_ COMPLETETRANSF，則可能會有任何作用，但服務提供者尚未指定。</span><span class="sxs-lookup"><span data-stu-id="08f2f-130">If neither TRANSFERNORM nor TRANSFERCONF is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_COMPLETETRANSF is specified, then it is possible that either will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="08f2f-131"><span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2 \_ PARKDIRECT**</span><span class="sxs-lookup"><span data-stu-id="08f2f-131"><span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2\_PARKDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="08f2f-132">如果這個位開啟，則可以使用 LINEPARKMODE 導向選項搭配 LinePark 來叫用「導向的公園」功能 \_ 。 [](/windows/desktop/api/Tapi/nf-tapi-linepark)</span><span class="sxs-lookup"><span data-stu-id="08f2f-132">If this bit is on, the "directed park" feature can be invoked by using the LINEPARKMODE\_DIRECTED option with [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span></span> <span data-ttu-id="08f2f-133">LINECALLFEATURE \_ 公園位也會在 **dwCallFeatures** 成員中開啟。</span><span class="sxs-lookup"><span data-stu-id="08f2f-133">The LINECALLFEATURE\_PARK bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08f2f-134"><span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2 \_ PARKNONDIRECT**</span><span class="sxs-lookup"><span data-stu-id="08f2f-134"><span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2\_PARKNONDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="08f2f-135">如果這個位開啟，則可以使用 LINEPARKMODE NONDIRECTED 選項搭配 LinePark 來叫用「非導向的公園」功能 \_ 。 [](/windows/desktop/api/Tapi/nf-tapi-linepark)</span><span class="sxs-lookup"><span data-stu-id="08f2f-135">If this bit is on, the "non-directed park" feature can be invoked by using the LINEPARKMODE\_NONDIRECTED option with [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span></span> <span data-ttu-id="08f2f-136">LINECALLFEATURE \_ 公園位也會在 **dwCallFeatures** 成員中開啟。</span><span class="sxs-lookup"><span data-stu-id="08f2f-136">The LINECALLFEATURE\_PARK bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="08f2f-137">如果 [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)中的 **dwCallFeatures2** 成員未指定 PARKDIRECT 或 PARKNONDIRECT，但指定了 LINECALLFEATURE \_ 公園，則可能會有任何作用，但服務提供者尚未指定。</span><span class="sxs-lookup"><span data-stu-id="08f2f-137">If neither PARKDIRECT nor PARKNONDIRECT is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_PARK is specified, then it is possible that either will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08f2f-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="08f2f-138">Requirements</span></span>



| <span data-ttu-id="08f2f-139">需求</span><span class="sxs-lookup"><span data-stu-id="08f2f-139">Requirement</span></span> | <span data-ttu-id="08f2f-140">值</span><span class="sxs-lookup"><span data-stu-id="08f2f-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="08f2f-141">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="08f2f-141">TAPI version</span></span><br/> | <span data-ttu-id="08f2f-142">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="08f2f-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="08f2f-143">標頭</span><span class="sxs-lookup"><span data-stu-id="08f2f-143">Header</span></span><br/>       | <dl> <span data-ttu-id="08f2f-144"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="08f2f-144"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08f2f-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08f2f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08f2f-146">**LINECALLSTATUS**</span><span class="sxs-lookup"><span data-stu-id="08f2f-146">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="08f2f-147">**lineCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="08f2f-147">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[<span data-ttu-id="08f2f-148">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="08f2f-148">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="08f2f-149">**linePark**</span><span class="sxs-lookup"><span data-stu-id="08f2f-149">**linePark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepark)
</dt> <dt>

[<span data-ttu-id="08f2f-150">**lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="08f2f-150">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[<span data-ttu-id="08f2f-151">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="08f2f-151">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 





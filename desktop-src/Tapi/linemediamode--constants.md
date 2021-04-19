---
description: LINEMEDIAMODE \_ 常數描述通訊會話或呼叫)  (或模式的媒體類型。
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: 'LINEMEDIAMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550a31da0d6de556e28ded14ce0803030be075ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996226"
---
# <a name="linemediamode_-constants"></a><span data-ttu-id="55d0e-103">LINEMEDIAMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="55d0e-103">LINEMEDIAMODE\_ Constants</span></span>

<span data-ttu-id="55d0e-104">**LINEMEDIAMODE \_** 常數描述通訊會話或呼叫)  (或模式的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="55d0e-104">The **LINEMEDIAMODE\_** constants describe media types (or modes)of a communications session or call.</span></span>

<dl> <dt>

<span data-ttu-id="55d0e-105"><span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE \_ AUTOMATEDVOICE**</span><span class="sxs-lookup"><span data-stu-id="55d0e-105"><span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE\_AUTOMATEDVOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55d0e-106">在電話上偵測到語音能源，並由自動化的應用程式（例如與回應機器應用程式）在本機處理語音。</span><span class="sxs-lookup"><span data-stu-id="55d0e-106">Voice energy was detected on the call, and the voice is locally handled by an automated application such as with an answering machine application.</span></span> <span data-ttu-id="55d0e-107">當服務提供者無法分辨來電的互動式和自動語音時，它會將通話報告為互動式語音。</span><span class="sxs-lookup"><span data-stu-id="55d0e-107">When a service provider cannot distinguish between interactive and automated voice on an incoming call, it will report the call as interactive voice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55d0e-108"><span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE \_ DATAMODEM**</span><span class="sxs-lookup"><span data-stu-id="55d0e-108"><span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE\_DATAMODEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55d0e-109">呼叫上的資料數據機會話。</span><span class="sxs-lookup"><span data-stu-id="55d0e-109">A data modem session on the call.</span></span> <span data-ttu-id="55d0e-110">目前的數據機通訊協定需要被呼叫的工作站起始交握。</span><span class="sxs-lookup"><span data-stu-id="55d0e-110">Current modem protocols require the called station to initiate the handshake.</span></span> <span data-ttu-id="55d0e-111">針對傳入的資料數據機呼叫，應用程式通常不會進行正面的偵測。</span><span class="sxs-lookup"><span data-stu-id="55d0e-111">For an incoming data modem call, the application can typically make no positive detection.</span></span> <span data-ttu-id="55d0e-112">服務提供者如何做出這項決定。</span><span class="sxs-lookup"><span data-stu-id="55d0e-112">How the service provider makes this determination is its choice.</span></span> <span data-ttu-id="55d0e-113">例如，在接聽撥入電話之後的一段時間，就可以用來做為判斷這可能是資料數據機呼叫的啟發式。</span><span class="sxs-lookup"><span data-stu-id="55d0e-113">For example, a period of silence just after answering an incoming call can be used as a heuristic to decide that this might be a data modem call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55d0e-114"><span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE \_ ADSI**</span><span class="sxs-lookup"><span data-stu-id="55d0e-114"><span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE\_ADSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55d0e-115">ADSI (類比顯示服務介面) 會話的呼叫。</span><span class="sxs-lookup"><span data-stu-id="55d0e-115">An ADSI (Analog Display Services Interface) session on the call.</span></span> <span data-ttu-id="55d0e-116">ADSI 會使用下載至手機的英數位元資訊，以及在手機上使用軟按鈕的方式來增強語音通話。</span><span class="sxs-lookup"><span data-stu-id="55d0e-116">ADSI enhances voice calls with alphanumeric information downloaded to the phone and the use of soft buttons on the phone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55d0e-117"><span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE \_ DIGITALDATA**</span><span class="sxs-lookup"><span data-stu-id="55d0e-117"><span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE\_DIGITALDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55d0e-118">未指定格式的數位資料流程。</span><span class="sxs-lookup"><span data-stu-id="55d0e-118">A digital data stream of unspecified format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55d0e-119"><span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE \_ G3FAX**</span><span class="sxs-lookup"><span data-stu-id="55d0e-119"><span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE\_G3FAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55d0e-120">透過呼叫傳送或接收群組3傳真。</span><span class="sxs-lookup"><span data-stu-id="55d0e-120">A group 3 fax is being sent or received over the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55d0e-121"><span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE \_ G4FAX**</span><span class="sxs-lookup"><span data-stu-id="55d0e-121"><span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE\_G4FAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55d0e-122">正在透過呼叫傳送或接收群組4傳真。</span><span class="sxs-lookup"><span data-stu-id="55d0e-122">A group 4 fax is being sent or received over the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55d0e-123"><span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE \_ INTERACTIVEVOICE**</span><span class="sxs-lookup"><span data-stu-id="55d0e-123"><span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE\_INTERACTIVEVOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55d0e-124">在通話上偵測到語音能源，並以人類的互動式語音通話來處理這兩個端點的電話。</span><span class="sxs-lookup"><span data-stu-id="55d0e-124">Voice energy was detected on the call, and the call is handled as an interactive voice call with humans on both ends.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55d0e-125"><span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE \_ 混合**</span><span class="sxs-lookup"><span data-stu-id="55d0e-125"><span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE\_MIXED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55d0e-126">呼叫上的混合會話。</span><span class="sxs-lookup"><span data-stu-id="55d0e-126">A mixed session on the call.</span></span> <span data-ttu-id="55d0e-127">Mixed 是其中一項 ISDN telematic 服務。</span><span class="sxs-lookup"><span data-stu-id="55d0e-127">Mixed is one of the ISDN telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55d0e-128"><span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE \_ TDD**</span><span class="sxs-lookup"><span data-stu-id="55d0e-128"><span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE\_TDD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55d0e-129">TDD (電話語音裝置的電話語音) 裝置。</span><span class="sxs-lookup"><span data-stu-id="55d0e-129">A TDD (Telephony Devices for the Deaf) session on the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55d0e-130"><span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE \_ TELETEX**</span><span class="sxs-lookup"><span data-stu-id="55d0e-130"><span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE\_TELETEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55d0e-131">呼叫上的 teletex 會話。</span><span class="sxs-lookup"><span data-stu-id="55d0e-131">A teletex session on the call.</span></span> <span data-ttu-id="55d0e-132">Teletex 是 telematic 服務之一。</span><span class="sxs-lookup"><span data-stu-id="55d0e-132">Teletex is one of the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55d0e-133"><span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**LINEMEDIAMODE \_ 電傳**</span><span class="sxs-lookup"><span data-stu-id="55d0e-133"><span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**LINEMEDIAMODE\_TELEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55d0e-134">呼叫上的電傳會話。</span><span class="sxs-lookup"><span data-stu-id="55d0e-134">A telex session on the call.</span></span> <span data-ttu-id="55d0e-135">電傳是其中一項 telematic 服務。</span><span class="sxs-lookup"><span data-stu-id="55d0e-135">Telex is one of the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55d0e-136"><span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**LINEMEDIAMODE \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="55d0e-136"><span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**LINEMEDIAMODE\_VIDEO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55d0e-137">通話的媒體類型是 video。</span><span class="sxs-lookup"><span data-stu-id="55d0e-137">The media type of the call is video.</span></span> <span data-ttu-id="55d0e-138"> (TAPI 2.1 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="55d0e-138">(TAPI versions 2.1 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55d0e-139"><span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE \_ VIDEOTEX**</span><span class="sxs-lookup"><span data-stu-id="55d0e-139"><span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE\_VIDEOTEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55d0e-140">呼叫上的 videotex 會話。</span><span class="sxs-lookup"><span data-stu-id="55d0e-140">A videotex session on the call.</span></span> <span data-ttu-id="55d0e-141">Videotex 是 telematic 服務之一。</span><span class="sxs-lookup"><span data-stu-id="55d0e-141">Videotex is one the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55d0e-142"><span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE \_ VOICEVIEW**</span><span class="sxs-lookup"><span data-stu-id="55d0e-142"><span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE\_VOICEVIEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55d0e-143">呼叫的媒體類型為 VoiceView。</span><span class="sxs-lookup"><span data-stu-id="55d0e-143">The media type of the call is VoiceView.</span></span> <span data-ttu-id="55d0e-144"> (TAPI 1.4 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="55d0e-144">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55d0e-145"><span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="55d0e-145"><span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55d0e-146">媒體資料流程存在，但其模式目前不是已知的，可能會在稍後變成已知。</span><span class="sxs-lookup"><span data-stu-id="55d0e-146">A media stream exists but its mode is not currently known and may become known later.</span></span> <span data-ttu-id="55d0e-147">這會對應至具有非分類媒體類型的呼叫。</span><span class="sxs-lookup"><span data-stu-id="55d0e-147">This would correspond to a call with an unclassified media type.</span></span> <span data-ttu-id="55d0e-148">在典型的類比電話語音環境中，連入通話的媒體類型可能會是未知的，直到來電獲得回應並篩選出媒體串流以進行判斷為止。</span><span class="sxs-lookup"><span data-stu-id="55d0e-148">In typical analog telephony environments, an incoming call's media type may be unknown until after the call has been answered and the media stream has been filtered to make a determination.</span></span>

<span data-ttu-id="55d0e-149">如果設定了不明的媒體模式旗標，也可以設定其他媒體旗標。</span><span class="sxs-lookup"><span data-stu-id="55d0e-149">If the unknown media-mode flag is set, other media flags can also be set.</span></span> <span data-ttu-id="55d0e-150">這是用來表示媒體不明，但它可能是其他選取的媒體類型之一。</span><span class="sxs-lookup"><span data-stu-id="55d0e-150">This is used to signify that the media is unknown but that it is likely to be one of the other selected media types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55d0e-151">備註</span><span class="sxs-lookup"><span data-stu-id="55d0e-151">Remarks</span></span>

<span data-ttu-id="55d0e-152">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="55d0e-152">All 32 bits are reserved.</span></span>

<span data-ttu-id="55d0e-153">請注意，持有人模式和媒體類型是不同的概念。</span><span class="sxs-lookup"><span data-stu-id="55d0e-153">Note that bearer mode and media type are different notions.</span></span> <span data-ttu-id="55d0e-154">來電的持有人模式是指出網路連線的品質，其主要是由網路所提供。</span><span class="sxs-lookup"><span data-stu-id="55d0e-154">The bearer mode of a call is an indication of the quality of the telephone connection as provided primarily by the network.</span></span> <span data-ttu-id="55d0e-155">呼叫的媒體類型表示透過該呼叫交換的資訊資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="55d0e-155">The media type of a call is an indication of the type of information stream that is exchanged over that call.</span></span> <span data-ttu-id="55d0e-156">群組3傳真或資料數據機是使用具有 3.1 kHz 語音持有人模式之呼叫的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="55d0e-156">Group 3 fax or data modem are media types that use a call with a 3.1 kHz voice bearer mode.</span></span>

<span data-ttu-id="55d0e-157">為了回溯相容性，服務提供者必須負責檢查該行上的已協商 API 版本，如果協商的版本不支援，則不會使用這個 LINEMEDIAMODE \_ 值。</span><span class="sxs-lookup"><span data-stu-id="55d0e-157">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use this LINEMEDIAMODE\_ value if not supported on the negotiated version.</span></span>

## <a name="requirements"></a><span data-ttu-id="55d0e-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="55d0e-158">Requirements</span></span>



| <span data-ttu-id="55d0e-159">需求</span><span class="sxs-lookup"><span data-stu-id="55d0e-159">Requirement</span></span> | <span data-ttu-id="55d0e-160">值</span><span class="sxs-lookup"><span data-stu-id="55d0e-160">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="55d0e-161">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="55d0e-161">TAPI version</span></span><br/> | <span data-ttu-id="55d0e-162">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="55d0e-162">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="55d0e-163">標頭</span><span class="sxs-lookup"><span data-stu-id="55d0e-163">Header</span></span><br/>       | <dl> <span data-ttu-id="55d0e-164"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="55d0e-164"><dt>Tapi.h</dt></span></span> </dl> |



 

 





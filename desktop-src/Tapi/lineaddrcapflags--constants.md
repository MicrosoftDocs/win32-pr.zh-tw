---
description: LINEADDRCAPFLAGS \_ 位旗標常數用於 LINEADDRESSCAPS 資料結構的 dwAddrCapFlags 成員，以描述各種布林值位址功能。
ms.assetid: 530af273-82ba-4310-8aac-266d657e1bfe
title: 'LINEADDRCAPFLAGS_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce6c8bebb5683d5ecb7d576ff7d376ad0d62cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001812"
---
# <a name="lineaddrcapflags_-constants"></a><span data-ttu-id="479e1-103">LINEADDRCAPFLAGS \_ 常數</span><span class="sxs-lookup"><span data-stu-id="479e1-103">LINEADDRCAPFLAGS\_ Constants</span></span>

<span data-ttu-id="479e1-104">**LINEADDRCAPFLAGS** \_ 位旗標常數用於 [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)資料結構的 **DwAddrCapFlags** 成員，以描述各種布林值位址功能。</span><span class="sxs-lookup"><span data-stu-id="479e1-104">The **LINEADDRCAPFLAGS**\_ bit-flag constants are used in the **dwAddrCapFlags** member of the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) data structure to describe various Boolean address capabilities.</span></span>

<dl> <dt>

<span data-ttu-id="479e1-105"><span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS \_ ACCEPTTOALERT**</span><span class="sxs-lookup"><span data-stu-id="479e1-105"><span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS\_ACCEPTTOALERT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-106">**如果必須** 使用 [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) 接受供應專案呼叫，請使用此專案來開始在呼叫的兩端發出警示的使用者。否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="479e1-106">**TRUE** if an offering call must be accepted using [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) to start alerting the users at both ends of the call; otherwise, **FALSE**.</span></span> <span data-ttu-id="479e1-107">這通常僅適用于 ISDN。</span><span class="sxs-lookup"><span data-stu-id="479e1-107">This is typically only used with ISDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-108"><span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS \_ ACDGROUP**</span><span class="sxs-lookup"><span data-stu-id="479e1-108"><span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS\_ACDGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-109">此位址支援與撥接中心作業連接的 [ACD 群組](about-call-center-controls.md#acd-group-object) 。</span><span class="sxs-lookup"><span data-stu-id="479e1-109">The address supports [ACD Groups](about-call-center-controls.md#acd-group-object) in connection with call center operations.</span></span> <span data-ttu-id="479e1-110">如需 ACD 群組的詳細資訊，請參閱「 [關於電話中心」控制項](./about-call-center-controls.md) 。</span><span class="sxs-lookup"><span data-stu-id="479e1-110">See [About Call Center Controls](./about-call-center-controls.md) for additional information on ACD groups.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-111"><span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS \_ AUTORECONNECT**</span><span class="sxs-lookup"><span data-stu-id="479e1-111"><span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS\_AUTORECONNECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-112">指定卸載諮詢通話是否會自動重新連線到諮詢保留的呼叫。</span><span class="sxs-lookup"><span data-stu-id="479e1-112">Specifies whether dropping a consultation call automatically reconnects to the call on consultation hold.</span></span> <span data-ttu-id="479e1-113">如果自動重新連線發生，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="479e1-113">**TRUE** if reconnect happens automatically; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-114"><span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS \_ BLOCKIDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="479e1-114"><span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS\_BLOCKIDDEFAULT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-115">指定當對此位址進行呼叫時，網路預設是否傳送或封鎖呼叫端識別碼資訊。</span><span class="sxs-lookup"><span data-stu-id="479e1-115">Specifies whether the network by default sends or blocks caller ID information when making a call on this address.</span></span> <span data-ttu-id="479e1-116">若 **為 TRUE**，則預設會封鎖識別碼資訊;如果 **為 FALSE**，則預設會傳輸識別碼資訊。</span><span class="sxs-lookup"><span data-stu-id="479e1-116">If **TRUE**, identifier information is blocked by default; if **FALSE**, identifier information is transmitted by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-117"><span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS \_ BLOCKIDOVERRIDE**</span><span class="sxs-lookup"><span data-stu-id="479e1-117"><span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS\_BLOCKIDOVERRIDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-118">指定是否可以覆寫每個呼叫的傳送或封鎖呼叫者識別碼資訊的預設設定。</span><span class="sxs-lookup"><span data-stu-id="479e1-118">Specifies whether the default setting for sending or blocking of caller ID information can be overridden per call.</span></span> <span data-ttu-id="479e1-119">若 **為 TRUE**，則可能覆寫;如果 **為 FALSE**，則表示不可能覆寫。</span><span class="sxs-lookup"><span data-stu-id="479e1-119">If **TRUE**, override is possible; if **FALSE**, override is not possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-120"><span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**LINEADDRCAPFLAGS \_ COMPLETIONID**</span><span class="sxs-lookup"><span data-stu-id="479e1-120"><span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**LINEADDRCAPFLAGS\_COMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-121">指定 [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) 傳回的完成識別碼是否有用且不重複。</span><span class="sxs-lookup"><span data-stu-id="479e1-121">Specifies whether the completion identifiers returned by [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) are useful and unique.</span></span> <span data-ttu-id="479e1-122">如果有用處，**則為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="479e1-122">**TRUE** if useful; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-123"><span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS \_ CONFDROP**</span><span class="sxs-lookup"><span data-stu-id="479e1-123"><span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS\_CONFDROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-124">如果在會議呼叫父系上的 [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)也具有卸載 (也就是中斷與參與會議通話的其他合作物件) 的副作用，則 **為 TRUE** 。如果卸載會議通話仍允許其他人在彼此之間交談，則 **為 FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="479e1-124">**TRUE** if [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) on a conference call parent also has the side effect of dropping (that is, disconnecting) the other parties involved in the conference call; **FALSE** if dropping a conference call still allows the other parties to talk among themselves.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-125"><span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS \_ CONFERENCEHELD**</span><span class="sxs-lookup"><span data-stu-id="479e1-125"><span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS\_CONFERENCEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-126">指定是否可以將硬式呼叫 conferenced 至。</span><span class="sxs-lookup"><span data-stu-id="479e1-126">Specifies whether a hard-held call can be conferenced to.</span></span> <span data-ttu-id="479e1-127">通常，只有諮詢保留的呼叫可以新增為會議通話。</span><span class="sxs-lookup"><span data-stu-id="479e1-127">Often, only calls on consultation hold can be added to as a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-128"><span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS \_ CONFERENCEMAKE**</span><span class="sxs-lookup"><span data-stu-id="479e1-128"><span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS\_CONFERENCEMAKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-129">指定是否可以建立全新的呼叫，以作為諮詢電話， (在會議上新增) 。</span><span class="sxs-lookup"><span data-stu-id="479e1-129">Specifies whether an entirely new call can be established for use as a consultation call (to add) on conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-130"><span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS \_ DESTOFFHOOK**</span><span class="sxs-lookup"><span data-stu-id="479e1-130"><span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS\_DESTOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-131">指定呼叫方的電話是否可以在進行呼叫時自動強制 offhook。</span><span class="sxs-lookup"><span data-stu-id="479e1-131">Specifies whether the called party's phone can automatically be forced offhook when making calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-132"><span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS \_ 撥號**</span><span class="sxs-lookup"><span data-stu-id="479e1-132"><span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS\_DIALED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-133">指定是否可在此位址上撥打目的地位址以進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="479e1-133">Specifies whether a destination address can be dialed on this address for making a call.</span></span> <span data-ttu-id="479e1-134">如果必須撥打目的地位址，則 **為 TRUE** ;如果目的地位址是固定的，則為 **FALSE** ， (為「熱電話」 ) 。</span><span class="sxs-lookup"><span data-stu-id="479e1-134">**TRUE** if a destination address must be dialed; **FALSE** if the destination address is fixed (as with a "hot phone").</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-135"><span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS \_ FWDBUSYNAADDR**</span><span class="sxs-lookup"><span data-stu-id="479e1-135"><span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS\_FWDBUSYNAADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-136">指定是否忙碌的呼叫轉送，而且沒有任何答案可以使用不同的轉送位址。</span><span class="sxs-lookup"><span data-stu-id="479e1-136">Specifies whether call forwarding for busy and for no answer can use different forwarding addresses.</span></span> <span data-ttu-id="479e1-137">只有在忙碌和沒有答案的轉送可以個別控制時，此旗標才有意義。</span><span class="sxs-lookup"><span data-stu-id="479e1-137">This flag is meaningful only if forwarding for busy and for no answer can be controlled separately.</span></span> <span data-ttu-id="479e1-138">如果轉送忙碌且沒有答案可以使用不同的目的地位址，則此旗標為 **TRUE** 。否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="479e1-138">This flag is **TRUE** if forwarding for busy and for no answer can use different destination addresses; otherwise, it is **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-139"><span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS \_ FWDCONSULT**</span><span class="sxs-lookup"><span data-stu-id="479e1-139"><span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS\_FWDCONSULT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-140">指定呼叫轉送是否牽涉到建立諮詢電話。</span><span class="sxs-lookup"><span data-stu-id="479e1-140">Specifies whether call forwarding involves the establishment of a consultation call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-141"><span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS \_ FWDINTEXTADDR**</span><span class="sxs-lookup"><span data-stu-id="479e1-141"><span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS\_FWDINTEXTADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-142">指定是否可以將內部和外部呼叫轉送至不同的轉送位址。</span><span class="sxs-lookup"><span data-stu-id="479e1-142">Specifies whether internal and external calls can be forwarded to different forwarding addresses.</span></span> <span data-ttu-id="479e1-143">只有在可以個別控制內部和外部呼叫的轉送時，此旗標才有意義。</span><span class="sxs-lookup"><span data-stu-id="479e1-143">This flag is meaningful only if forwarding of internal and external calls can be controlled separately.</span></span> <span data-ttu-id="479e1-144">如果內部和外部呼叫可以轉送至不同的目的地位址，則此旗標為 **TRUE** ;否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="479e1-144">This flag is **TRUE** if internal and external calls can be forwarded to different destination addresses; otherwise, it is **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-145"><span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS \_ FWDNUMRINGS**</span><span class="sxs-lookup"><span data-stu-id="479e1-145"><span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS\_FWDNUMRINGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-146">指定當轉送呼叫未接聽時，是否可指定無回應的環形數目。</span><span class="sxs-lookup"><span data-stu-id="479e1-146">Specifies whether the number of rings for a no-answer can be specified when forwarding calls on no answer.</span></span> <span data-ttu-id="479e1-147">若 **為 TRUE**，則會在 [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)結構的 **dwMinFwdNumRings** 和 **dwMaxFwdNumRings** 成員中提供有效的範圍。</span><span class="sxs-lookup"><span data-stu-id="479e1-147">If **TRUE**, the valid range is provided in the **dwMinFwdNumRings** and **dwMaxFwdNumRings** members of the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-148"><span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS \_ FWDSTATUSVALID**</span><span class="sxs-lookup"><span data-stu-id="479e1-148"><span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS\_FWDSTATUSVALID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-149">指定此位址的 [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) 結構中的轉送狀態是有效的，或最多為「最佳的估計值」，指出交換器或網路沒有正確的確認。</span><span class="sxs-lookup"><span data-stu-id="479e1-149">Specifies whether the forwarding status in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure for this address is valid or is at most a "best estimate," given absence of accurate confirmation by the switch or network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-150"><span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS \_ HOLDMAKESNEW**</span><span class="sxs-lookup"><span data-stu-id="479e1-150"><span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS\_HOLDMAKESNEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-151">使用 [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) 或外部動作) 將此位址上的呼叫放置在保存 (時，會自動建立新的呼叫 (最有可能在 LINECALLSTATE 的 \_ 撥號程式) 。</span><span class="sxs-lookup"><span data-stu-id="479e1-151">When a call on this address is placed on hold (using [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) or external action), a new call is automatically created (most likely in LINECALLSTATE\_DIALTONE).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-152"><span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS \_ NOEXTERNALCALLS**</span><span class="sxs-lookup"><span data-stu-id="479e1-152"><span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS\_NOEXTERNALCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-153">位址會與 PBX 上的內部線路相關聯，而這種方式不能用來對交換器以外的位址進行呼叫， (例如，它是對講機) 。</span><span class="sxs-lookup"><span data-stu-id="479e1-153">The address is associated with an internal line on a PBX that is restricted in such a way that it cannot be used to place calls to an address outside the switch (for example, it is an intercom).</span></span> <span data-ttu-id="479e1-154">應用程式可以使用此指示，協助使用者選取正確的呼叫外觀以用來進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="479e1-154">The application can use this indication to assist the user in selecting the correct call appearance to use for making a call.</span></span> <span data-ttu-id="479e1-155">當這個位關閉時，不一定會指出位址可以用來進行外部呼叫，因為服務提供者可能不是行類型的 cognizant。</span><span class="sxs-lookup"><span data-stu-id="479e1-155">When this bit is off, it does not necessarily indicate that the address can be used to make external calls, because the service provider may not be cognizant of the line type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-156"><span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS \_ NOINTERNALCALLS**</span><span class="sxs-lookup"><span data-stu-id="479e1-156"><span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS\_NOINTERNALCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-157">位址會與 (主幹) 的直接 CO 線相關聯，而且無法用來在 PBX 上進行內部呼叫。</span><span class="sxs-lookup"><span data-stu-id="479e1-157">The address is associated with a direct CO line (trunk), and cannot be used to make internal calls on a PBX.</span></span> <span data-ttu-id="479e1-158">應用程式可以使用此指示，協助使用者選取正確的呼叫外觀以用來進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="479e1-158">The application can use this indication to assist the user in selecting the correct call appearance to use for making a call.</span></span> <span data-ttu-id="479e1-159">當這個位關閉時，不一定表示位址可以用來進行內部呼叫，因為服務提供者可能不是行類型的 cognizant。</span><span class="sxs-lookup"><span data-stu-id="479e1-159">When this bit is off, it does not necessarily indicate that the address can be used to make internal calls, because the service provider may not be cognizant of the line type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-160"><span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS \_ NOPSTNADDRESSTRANSLATION**</span><span class="sxs-lookup"><span data-stu-id="479e1-160"><span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS\_NOPSTNADDRESSTRANSLATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-161">此位址不支援公用交換電話網路位址轉譯。</span><span class="sxs-lookup"><span data-stu-id="479e1-161">This address does not support public switched telephone network address translation.</span></span> <span data-ttu-id="479e1-162">此旗標只會公開給協調 TAPI 3.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="479e1-162">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-163"><span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS \_ ORIGOFFHOOK**</span><span class="sxs-lookup"><span data-stu-id="479e1-163"><span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS\_ORIGOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-164">指定進行呼叫時，是否可以自動 offhook 原始合作物件的電話。</span><span class="sxs-lookup"><span data-stu-id="479e1-164">Specifies whether the originating party's phone can automatically be taken offhook when making calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-165"><span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS \_ PARTIALDIAL**</span><span class="sxs-lookup"><span data-stu-id="479e1-165"><span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS\_PARTIALDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-166">指定是否可使用部分撥號。</span><span class="sxs-lookup"><span data-stu-id="479e1-166">Specifies whether partial dialing is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-167"><span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS \_ PICKUPCALLWAIT**</span><span class="sxs-lookup"><span data-stu-id="479e1-167"><span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS\_PICKUPCALLWAIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-168">如果 [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)可以用來挑選使用者偵測到的呼叫做為呼叫等候呼叫，**則為 TRUE** 。否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="479e1-168">**TRUE** if [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) can be used to pick up a call detected by the user as a call-waiting call; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-169"><span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS \_ PICKUPGROUPID**</span><span class="sxs-lookup"><span data-stu-id="479e1-169"><span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS\_PICKUPGROUPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-170">指定呼叫取貨是否需要群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="479e1-170">Specifies whether a group identifier is required for call pickup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-171"><span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS \_ PREDICTIVEDIALER**</span><span class="sxs-lookup"><span data-stu-id="479e1-171"><span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS\_PREDICTIVEDIALER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-172">此位址具有增強的呼叫進度監視功能，可套用至連出呼叫以判斷撥號狀態（例如 *回電*、 *忙碌*、 *specialinfo* 和 *連線*），或接聽通話的裝置媒體類型。</span><span class="sxs-lookup"><span data-stu-id="479e1-172">This address has enhanced call progress monitoring capabilities which can be applied to outgoing calls to determine call states such as *ringback*, *busy*, *specialinfo*, and *connected*, or the media type of the device answering the call.</span></span> <span data-ttu-id="479e1-173">它也可以在呼叫到達任何一組預先定義的狀態時，自動將撥出電話傳送到另一個位址。</span><span class="sxs-lookup"><span data-stu-id="479e1-173">It may also have the ability to automatically transfer outgoing calls to another address when a call reaches any of a predefined set of states.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-174"><span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**LINEADDRCAPFLAGS \_ 佇列**</span><span class="sxs-lookup"><span data-stu-id="479e1-174"><span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**LINEADDRCAPFLAGS\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-175">此位址不會與特定的工作站或實體裝置相關聯，而是呼叫等候進一步處理的位置。</span><span class="sxs-lookup"><span data-stu-id="479e1-175">This address is not associated with a particular station or physical device, but is a holding place where calls wait for further processing.</span></span> <span data-ttu-id="479e1-176">放置在佇列中的呼叫可能會收到特定的處理。</span><span class="sxs-lookup"><span data-stu-id="479e1-176">The calls placed in the queue may receive a particular treatment.</span></span> <span data-ttu-id="479e1-177">當特定資源變成可用時，它們也可能會自動傳輸 (例如，如果佇列是 ACD 佇列，而呼叫正在等候可用的代理程式) 。</span><span class="sxs-lookup"><span data-stu-id="479e1-177">They may also be automatically transferred when a particular resource becomes available (for example, if the queue is an ACD queue and calls are waiting for an available agent).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-178"><span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS \_ ROUTEPOINT**</span><span class="sxs-lookup"><span data-stu-id="479e1-178"><span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS\_ROUTEPOINT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-179">此位址不會與特定的工作站或實體裝置相關聯，而是由應用程式呼叫等候路由的位置， (應用程式會檢查呼叫的位址，並可將呼叫重新導向至另一個位址) 。</span><span class="sxs-lookup"><span data-stu-id="479e1-179">This address is not associated with a particular station or physical device, but is a holding place where calls wait for routing by the application (the application examines the called address, and can redirect the call to another address).</span></span> <span data-ttu-id="479e1-180">如果路由超時過期，則也會自動傳送呼叫 (切換通常會假設預設路由) 。</span><span class="sxs-lookup"><span data-stu-id="479e1-180">The call can also be automatically transferred if a routing timeout expires (the switch usually assumes a default routing).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-181"><span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS \_ 安全**</span><span class="sxs-lookup"><span data-stu-id="479e1-181"><span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS\_SECURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-182">指定是否可在呼叫設定時，將此位址上的呼叫設為安全。</span><span class="sxs-lookup"><span data-stu-id="479e1-182">Specifies whether calls on this address can be made secure at call-setup time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-183"><span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS \_ SETCALLINGID**</span><span class="sxs-lookup"><span data-stu-id="479e1-183"><span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS\_SETCALLINGID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-184">當呼叫 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)和其他接受 **LINECALLPARAMS** 結構的函式時，應用程式可以選擇在 [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)中設定 **CallingPartyID** 成員。</span><span class="sxs-lookup"><span data-stu-id="479e1-184">The application can choose to set the **CallingPartyID** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) when calling [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) and other functions that accept a **LINECALLPARAMS** structure.</span></span> <span data-ttu-id="479e1-185">如果識別碼的內容是可接受的，且有可用的路徑，服務提供者將會將識別碼傳遞給被呼叫的合作物件，以指出呼叫方的身分識別。</span><span class="sxs-lookup"><span data-stu-id="479e1-185">The service provider will, if the content of the identifier is acceptable and a path is available, pass the identifier along to the called party to indicate the identity of the calling party.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-186"><span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS \_ SETUPCONFNull**</span><span class="sxs-lookup"><span data-stu-id="479e1-186"><span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS\_SETUPCONFNULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-187">指定是否要從初始呼叫開始設定會議通話 (**FALSE**) 或沒有初始呼叫 (**TRUE**) 。</span><span class="sxs-lookup"><span data-stu-id="479e1-187">Specifies whether setting up a conference call starts out with an initial call (**FALSE**) or with no initial call (**TRUE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-188"><span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS \_ TRANSFERHELD**</span><span class="sxs-lookup"><span data-stu-id="479e1-188"><span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS\_TRANSFERHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-189">指定是否可以傳送硬式通話。</span><span class="sxs-lookup"><span data-stu-id="479e1-189">Specifies whether a hard-held call can be transferred.</span></span> <span data-ttu-id="479e1-190">通常，只有諮詢保留的呼叫可以轉移。</span><span class="sxs-lookup"><span data-stu-id="479e1-190">Often, only calls on consultation hold can be transferred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="479e1-191"><span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS \_ TRANSFERMAKE**</span><span class="sxs-lookup"><span data-stu-id="479e1-191"><span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS\_TRANSFERMAKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="479e1-192">指定是否可以建立全新的呼叫，以作為傳輸時的諮詢通話。</span><span class="sxs-lookup"><span data-stu-id="479e1-192">Specifies whether an entirely new call can be established for use as a consultation call on transfer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="479e1-193">備註</span><span class="sxs-lookup"><span data-stu-id="479e1-193">Remarks</span></span>

<span data-ttu-id="479e1-194">無延伸。</span><span class="sxs-lookup"><span data-stu-id="479e1-194">No extensibility.</span></span> <span data-ttu-id="479e1-195">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="479e1-195">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="479e1-196">規格需求</span><span class="sxs-lookup"><span data-stu-id="479e1-196">Requirements</span></span>



| <span data-ttu-id="479e1-197">需求</span><span class="sxs-lookup"><span data-stu-id="479e1-197">Requirement</span></span> | <span data-ttu-id="479e1-198">值</span><span class="sxs-lookup"><span data-stu-id="479e1-198">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="479e1-199">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="479e1-199">TAPI version</span></span><br/> | <span data-ttu-id="479e1-200">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="479e1-200">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="479e1-201">標頭</span><span class="sxs-lookup"><span data-stu-id="479e1-201">Header</span></span><br/>       | <dl> <span data-ttu-id="479e1-202"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="479e1-202"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="479e1-203">另請參閱</span><span class="sxs-lookup"><span data-stu-id="479e1-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="479e1-204">**lineAccept**</span><span class="sxs-lookup"><span data-stu-id="479e1-204">**lineAccept**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaccept)
</dt> <dt>

[<span data-ttu-id="479e1-205">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="479e1-205">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="479e1-206">**LINEADDRESSSTATUS**</span><span class="sxs-lookup"><span data-stu-id="479e1-206">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="479e1-207">**LINECALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="479e1-207">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="479e1-208">**lineCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="479e1-208">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[<span data-ttu-id="479e1-209">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="479e1-209">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="479e1-210">**lineHold**</span><span class="sxs-lookup"><span data-stu-id="479e1-210">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> <dt>

[<span data-ttu-id="479e1-211">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="479e1-211">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="479e1-212">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="479e1-212">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 


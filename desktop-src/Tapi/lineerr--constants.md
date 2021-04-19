---
description: 以下是當叫用線路、位址或呼叫上的作業時，TAPI 可以傳回的錯誤碼清單。
ms.assetid: bdaf60d1-6ff2-4bd6-b246-8556d6cae644
title: 'LINEERR_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ed7757377d26dbde832b7ef50f275b45e21760d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999735"
---
# <a name="lineerr_-constants"></a><span data-ttu-id="e091d-103">LINEERR \_ 常數</span><span class="sxs-lookup"><span data-stu-id="e091d-103">LINEERR\_ Constants</span></span>

<span data-ttu-id="e091d-104">以下是當叫用線路、位址或呼叫上的作業時，TAPI 可以傳回的錯誤碼清單。</span><span class="sxs-lookup"><span data-stu-id="e091d-104">The following is a list of error codes that TAPI can return when invoking operations on lines, addresses, or calls.</span></span> <span data-ttu-id="e091d-105">如需如何判斷特定函式可以傳回哪些錯誤碼的詳細資訊，請參閱個別的函數描述。</span><span class="sxs-lookup"><span data-stu-id="e091d-105">For more information about how to determine which of these error codes a particular function can return, see the individual function descriptions.</span></span>

<dl> <dt>

<span data-ttu-id="e091d-106"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**</span><span class="sxs-lookup"><span data-stu-id="e091d-106"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR\_ADDRESSBLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-107">無法在指定的呼叫上撥打指定的位址。</span><span class="sxs-lookup"><span data-stu-id="e091d-107">The specified address is blocked from being dialed on the specified call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-108"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**</span><span class="sxs-lookup"><span data-stu-id="e091d-108"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR\_ADDRESSBLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-109">目標呼叫位址已啟用呼叫封鎖。</span><span class="sxs-lookup"><span data-stu-id="e091d-109">The target call address has call blocking enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-110"><span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR \_ 已配置**</span><span class="sxs-lookup"><span data-stu-id="e091d-110"><span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-111">因為持續性狀況，導致無法開啟這一行，例如，其他進程會以獨佔方式開啟序列埠。</span><span class="sxs-lookup"><span data-stu-id="e091d-111">The line cannot be opened due to a persistent condition, such as that of a serial port being exclusively opened by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-112"><span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR \_ BADDEVICEID**</span><span class="sxs-lookup"><span data-stu-id="e091d-112"><span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR\_BADDEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-113">指定的裝置識別碼或線路裝置識別碼，例如在 *dwDeviceID* 參數中無效或超出範圍。</span><span class="sxs-lookup"><span data-stu-id="e091d-113">The specified device identifier or line device identifier, such as in a *dwDeviceID* parameter, is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-114"><span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR \_ BEARERMODEUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="e091d-114"><span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR\_BEARERMODEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-115">[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)中的持有人模式成員無效、在 **LINECALLPARAMS** 中指定的持有人模式無法使用，或呼叫持有人模式無法變更為指定的持有人模式。</span><span class="sxs-lookup"><span data-stu-id="e091d-115">The bearer mode member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) is invalid, the bearer mode specified in **LINECALLPARAMS** is not available, or the call bearer mode cannot be changed to the specified bearer mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-116"><span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR \_ BILLINGREJECTED**</span><span class="sxs-lookup"><span data-stu-id="e091d-116"><span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR\_BILLINGREJECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-117">已拒絕通話的計費模式。</span><span class="sxs-lookup"><span data-stu-id="e091d-117">The billing mode of the call was rejected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-118"><span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR \_ CALLUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="e091d-118"><span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR\_CALLUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-119">指定位址上的所有呼叫外觀目前都在使用中。</span><span class="sxs-lookup"><span data-stu-id="e091d-119">All call appearances on the specified address are currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-120"><span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**LINEERR \_ COMPLETIONOVERRUN**</span><span class="sxs-lookup"><span data-stu-id="e091d-120"><span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**LINEERR\_COMPLETIONOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-121">已超過未完成通話完成的最大數目。</span><span class="sxs-lookup"><span data-stu-id="e091d-121">The maximum number of outstanding call completions has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-122"><span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR \_ CONFERENCEFULL**</span><span class="sxs-lookup"><span data-stu-id="e091d-122"><span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR\_CONFERENCEFULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-123">已達到會議合作物件的最大數目，或無法滿足要求的合作物件數目。</span><span class="sxs-lookup"><span data-stu-id="e091d-123">The maximum number of parties for a conference has been reached, or the requested number of parties cannot be satisfied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-124"><span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR \_ DIALBILLING**</span><span class="sxs-lookup"><span data-stu-id="e091d-124"><span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-125">可以撥出的位址參數包含服務提供者未處理的撥號控制字元。</span><span class="sxs-lookup"><span data-stu-id="e091d-125">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-126"><span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR \_ DIALDIALTONE**</span><span class="sxs-lookup"><span data-stu-id="e091d-126"><span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-127">可以撥出的位址參數包含服務提供者未處理的撥號控制字元。</span><span class="sxs-lookup"><span data-stu-id="e091d-127">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-128"><span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR \_ DIALPROMPT**</span><span class="sxs-lookup"><span data-stu-id="e091d-128"><span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR\_DIALPROMPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-129">可以撥出的位址參數包含服務提供者未處理的撥號控制字元。</span><span class="sxs-lookup"><span data-stu-id="e091d-129">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-130"><span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR \_ DIALQUIET**</span><span class="sxs-lookup"><span data-stu-id="e091d-130"><span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-131">可以撥出的位址參數包含服務提供者未處理的撥號控制字元。</span><span class="sxs-lookup"><span data-stu-id="e091d-131">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-132"><span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR \_ DIALVOICEDETECT**</span><span class="sxs-lookup"><span data-stu-id="e091d-132"><span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR\_DIALVOICEDETECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-133">不支援使用撥號修飾詞 (： ) 。</span><span class="sxs-lookup"><span data-stu-id="e091d-133">Use of the dial modifier (:) is not supported.</span></span> <span data-ttu-id="e091d-134">此值只會公開給協調 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e091d-134">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-135"><span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR 已 \_ 中斷連線**</span><span class="sxs-lookup"><span data-stu-id="e091d-135"><span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-136">呼叫已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="e091d-136">The call has been disconnected.</span></span> <span data-ttu-id="e091d-137">此值只會公開給協調 TAPI 2.2 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e091d-137">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-138"><span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR \_ INCOMPATIBLEAPIVERSION**</span><span class="sxs-lookup"><span data-stu-id="e091d-138"><span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR\_INCOMPATIBLEAPIVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-139">應用程式要求的 TAPI 版本或版本範圍，與電話語音 API 的執行和對應的服務提供者不相容或不支援。</span><span class="sxs-lookup"><span data-stu-id="e091d-139">The application requested a TAPI version or version range that is either incompatible with, or cannot be supported by, the Telephony API implementation and the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-140"><span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR \_ INCOMPATIBLEEXTVERSION**</span><span class="sxs-lookup"><span data-stu-id="e091d-140"><span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR\_INCOMPATIBLEEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-141">應用程式要求的延伸模組版本範圍可能無效，或對應的服務提供者無法支援此範圍。</span><span class="sxs-lookup"><span data-stu-id="e091d-141">The application requested an extension version range that is either invalid or cannot be supported by the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-142"><span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR \_ INIFILECORRUPT**</span><span class="sxs-lookup"><span data-stu-id="e091d-142"><span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR\_INIFILECORRUPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-143">因為內部不一致或格式化問題，所以 TAPI 無法正確讀取或瞭解 Telephon.ini 檔案。</span><span class="sxs-lookup"><span data-stu-id="e091d-143">The Telephon.ini file cannot be read or understood properly by TAPI because of internal inconsistencies or formatting problems.</span></span> <span data-ttu-id="e091d-144">例如，Telephon.ini 檔案的 [ \[ 位置]、[卡片] 或 [ \] \[ \] 國家（地區）] \[ \] 區段可能已損毀或不一致。</span><span class="sxs-lookup"><span data-stu-id="e091d-144">For example, the \[Locations\], \[Cards\], or \[Countries\] section of the Telephon.ini file may be corrupted or inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-145"><span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR \_ INUSE**</span><span class="sxs-lookup"><span data-stu-id="e091d-145"><span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR\_INUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-146">線路裝置正在使用中，且目前無法設定、允許加入合作物件、允許呼叫、允許呼叫，或允許傳送呼叫的功能。</span><span class="sxs-lookup"><span data-stu-id="e091d-146">The line device is in use and cannot currently be configured, allow a party to be added, allow a call to be answered, allow a call to be placed, or allow a call to be transferred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-147"><span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR \_ INVALADDRESS**</span><span class="sxs-lookup"><span data-stu-id="e091d-147"><span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR\_INVALADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-148">指定的位址無效或不允許。</span><span class="sxs-lookup"><span data-stu-id="e091d-148">A specified address is either invalid or not allowed.</span></span> <span data-ttu-id="e091d-149">如果無效，位址包含不正確字元或數位，或目的地位址包含服務提供者不支援的撥號控制字元 (W、@、$ 或？ ) 。</span><span class="sxs-lookup"><span data-stu-id="e091d-149">If invalid, the address contains invalid characters or digits, or the destination address contains dialing control characters (W, @, $, or ?) that are not supported by the service provider.</span></span> <span data-ttu-id="e091d-150">如果不允許，指定的位址可能未指派給指定的行，或對位址重新導向而言無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-150">If not allowed, the specified address is either not assigned to the specified line or is not valid for address redirection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-151"><span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR \_ INVALADDRESSID**</span><span class="sxs-lookup"><span data-stu-id="e091d-151"><span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR\_INVALADDRESSID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-152">指定的位址識別碼無效或超出範圍。</span><span class="sxs-lookup"><span data-stu-id="e091d-152">The specified address identifier is either invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-153"><span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR \_ INVALADDRESSMODE**</span><span class="sxs-lookup"><span data-stu-id="e091d-153"><span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR\_INVALADDRESSMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-154">指定的位址模式無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-154">The specified address mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-155"><span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR \_ INVALADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="e091d-155"><span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR\_INVALADDRESSSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-156">指定的位址狀態包含一或多個不是 [**LINEADDRESSSTATE \_ 常數**](lineaddressstate--constants.md)的位。</span><span class="sxs-lookup"><span data-stu-id="e091d-156">The specified address state contains one or more bits that are not [**LINEADDRESSSTATE\_ constants**](lineaddressstate--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-157"><span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR \_ INVALADDRESSTYPE**</span><span class="sxs-lookup"><span data-stu-id="e091d-157"><span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR\_INVALADDRESSTYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-158">應用程式參考的網址類別型無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-158">The application referenced an address type that is not valid.</span></span> <span data-ttu-id="e091d-159">此值只會公開給協調 TAPI 3.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e091d-159">This value is exposed only to applications that negotiate a TAPI version of 3.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-160"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**</span><span class="sxs-lookup"><span data-stu-id="e091d-160"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR\_INVALAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-161">指定的代理程式活動無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-161">The specified agent activity is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-162"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**</span><span class="sxs-lookup"><span data-stu-id="e091d-162"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR\_INVALAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-163">叫用這項作業的應用程式是間接交付的目標。</span><span class="sxs-lookup"><span data-stu-id="e091d-163">The application invoking this operation is the target of the indirect handoff.</span></span> <span data-ttu-id="e091d-164">也就是說，TAPI 判斷呼叫的應用程式也是指定媒體類型的最高優先順序應用程式。</span><span class="sxs-lookup"><span data-stu-id="e091d-164">That is, TAPI has determined that the calling application is also the highest priority application for the given media type.</span></span> <span data-ttu-id="e091d-165">此值只會公開給協調 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e091d-165">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-166"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**</span><span class="sxs-lookup"><span data-stu-id="e091d-166"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR\_INVALAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-167">指定的代理程式群組資訊無效或包含錯誤。</span><span class="sxs-lookup"><span data-stu-id="e091d-167">The specified agent group information is not valid or contains errors.</span></span> <span data-ttu-id="e091d-168">尚未執行要求的動作。</span><span class="sxs-lookup"><span data-stu-id="e091d-168">The requested action has not been performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-169"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**</span><span class="sxs-lookup"><span data-stu-id="e091d-169"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR\_INVALAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-170">應用程式參考了不正確代理程式群組。</span><span class="sxs-lookup"><span data-stu-id="e091d-170">The application referenced an agent group that is not valid.</span></span> <span data-ttu-id="e091d-171">此值只會公開給協調 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e091d-171">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-172"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**</span><span class="sxs-lookup"><span data-stu-id="e091d-172"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR\_INVALAGENTID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-173">指定的代理程式識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-173">The specified agent identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-174"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**</span><span class="sxs-lookup"><span data-stu-id="e091d-174"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR\_INVALAGENTID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-175">使用的代理程式識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-175">An invalid agent identifier was used.</span></span> <span data-ttu-id="e091d-176">此值只會公開給協調 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e091d-176">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-177"><span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR \_ INVALAGENTSESSIONSTATE**</span><span class="sxs-lookup"><span data-stu-id="e091d-177"><span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR\_INVALAGENTSESSIONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-178">代理程式會話狀態無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-178">The agent session state is invalid.</span></span> <span data-ttu-id="e091d-179">此值只會公開給協調 TAPI 2.2 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e091d-179">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-180"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**</span><span class="sxs-lookup"><span data-stu-id="e091d-180"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR\_INVALAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-181">指定的代理程式狀態無效或包含錯誤。</span><span class="sxs-lookup"><span data-stu-id="e091d-181">The specified agent state is not valid or contains errors.</span></span> <span data-ttu-id="e091d-182">指定之位址的代理程式狀態未進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="e091d-182">No changes have been made to the agent state of the specified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-183"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**</span><span class="sxs-lookup"><span data-stu-id="e091d-183"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR\_INVALAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-184">應用程式參考的代理程式狀態無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-184">The application referenced an agent state that is not valid.</span></span> <span data-ttu-id="e091d-185">此值只會公開給協調 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e091d-185">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-186"><span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR \_ INVALAPPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="e091d-186"><span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR\_INVALAPPHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-187">應用程式處理 (如 *hLineApp* 參數所指定) 或應用程式註冊控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-187">The application handle (such as specified by a *hLineApp* parameter) or the application registration handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-188"><span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR \_ INVALAPPNAME**</span><span class="sxs-lookup"><span data-stu-id="e091d-188"><span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR\_INVALAPPNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-189">指定的應用程式名稱無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-189">The specified application name is invalid.</span></span> <span data-ttu-id="e091d-190">如果應用程式名稱是由應用程式所指定，則會假設字串不包含任何不可顯示的字元，而且會以零結束。</span><span class="sxs-lookup"><span data-stu-id="e091d-190">If an application name is specified by the application, it is assumed that the string does not contain any non-displayable characters, and is zero-terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-191"><span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR \_ INVALBEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="e091d-191"><span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR\_INVALBEARERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-192">指定的持有人模式無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-192">The specified bearer mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-193"><span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR \_ INVALCALLCOMPLMODE**</span><span class="sxs-lookup"><span data-stu-id="e091d-193"><span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR\_INVALCALLCOMPLMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-194">指定的完成無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-194">The specified completion is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-195"><span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR \_ INVALCALLHANDLE**</span><span class="sxs-lookup"><span data-stu-id="e091d-195"><span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR\_INVALCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-196">指定的呼叫控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-196">The specified call handle is not valid.</span></span> <span data-ttu-id="e091d-197">例如，控制碼不是 **Null** ，但不屬於指定的行。</span><span class="sxs-lookup"><span data-stu-id="e091d-197">For example, the handle is not **NULL** but does not belong to the given line.</span></span> <span data-ttu-id="e091d-198">在某些情況下，指定的撥號裝置控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-198">In some cases, the specified call device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-199"><span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR \_ INVALCALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="e091d-199"><span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR\_INVALCALLPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-200">指定的呼叫參數無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-200">The specified call parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-201"><span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR \_ INVALCALLPRIVILEGE**</span><span class="sxs-lookup"><span data-stu-id="e091d-201"><span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR\_INVALCALLPRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-202">指定的呼叫許可權參數無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-202">The specified call privilege parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-203"><span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR \_ INVALCALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="e091d-203"><span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR\_INVALCALLSELECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-204">指定的 select 參數無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-204">The specified select parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-205"><span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR \_ INVALCALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="e091d-205"><span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR\_INVALCALLSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-206">呼叫的目前狀態不是所要求作業的有效狀態。</span><span class="sxs-lookup"><span data-stu-id="e091d-206">The current state of a call is not in a valid state for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-207"><span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR \_ INVALCALLSTATELIST**</span><span class="sxs-lookup"><span data-stu-id="e091d-207"><span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR\_INVALCALLSTATELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-208">指定的撥號狀態清單無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-208">The specified call state list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-209"><span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR \_ INVALCARD**</span><span class="sxs-lookup"><span data-stu-id="e091d-209"><span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR\_INVALCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-210">在登錄的 [卡片] 區段中的任何專案中，找不到在 *dwCard* 中指定的永久卡識別碼 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="e091d-210">The permanent card identifier specified in *dwCard* could not be found in any entry in the \[Cards\] section in the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-211"><span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR \_ INVALCOMPLETIONID**</span><span class="sxs-lookup"><span data-stu-id="e091d-211"><span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR\_INVALCOMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-212">完成識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-212">The completion identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-213"><span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR \_ INVALCONFCALLHANDLE**</span><span class="sxs-lookup"><span data-stu-id="e091d-213"><span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR\_INVALCONFCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-214">會議通話的指定呼叫控制碼無效，或不是會議通話的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e091d-214">The specified call handle for the conference call is invalid or is not a handle for a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-215"><span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR \_ INVALCONSULTCALLHANDLE**</span><span class="sxs-lookup"><span data-stu-id="e091d-215"><span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR\_INVALCONSULTCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-216">指定的諮詢呼叫控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-216">The specified consultation call handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-217"><span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR \_ INVALCOUNTRYCODE**</span><span class="sxs-lookup"><span data-stu-id="e091d-217"><span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR\_INVALCOUNTRYCODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-218">指定的國家或地區代碼無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-218">The specified country or region code is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-219"><span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR \_ INVALDEVICECLASS**</span><span class="sxs-lookup"><span data-stu-id="e091d-219"><span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR\_INVALDEVICECLASS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-220">線路裝置對於指定的裝置類別沒有相關聯的裝置，或指定的行不支援指定的裝置類別。</span><span class="sxs-lookup"><span data-stu-id="e091d-220">The line device has no associated device for the given device class, or the specified line does not support the indicated device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-221"><span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR \_ INVALDEVICEHANDLE**</span><span class="sxs-lookup"><span data-stu-id="e091d-221"><span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR\_INVALDEVICEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-222">線路裝置控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-222">The line device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-223"><span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR \_ INVALDIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="e091d-223"><span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR\_INVALDIALPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-224">撥號參數無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-224">The dialing parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-225"><span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR \_ INVALDIGITLIST**</span><span class="sxs-lookup"><span data-stu-id="e091d-225"><span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR\_INVALDIGITLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-226">指定的數位清單無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-226">The specified digit list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-227"><span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR \_ INVALDIGITMODE**</span><span class="sxs-lookup"><span data-stu-id="e091d-227"><span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR\_INVALDIGITMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-228">指定的位數模式無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-228">The specified digit mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-229"><span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR \_ INVALDIGITS**</span><span class="sxs-lookup"><span data-stu-id="e091d-229"><span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR\_INVALDIGITS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-230">指定的終止位數無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-230">The specified termination digits are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-231"><span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR \_ INVALEXTVERSION**</span><span class="sxs-lookup"><span data-stu-id="e091d-231"><span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR\_INVALEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-232">服務提供者延伸模組版本號碼無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-232">The service provider extension version number is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-233"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**</span><span class="sxs-lookup"><span data-stu-id="e091d-233"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR\_INVALFEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-234">*DwFeature* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-234">The *dwFeature* parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-235"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**</span><span class="sxs-lookup"><span data-stu-id="e091d-235"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR\_INVALFEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-236">應用程式叫用了這一行未提供的功能。</span><span class="sxs-lookup"><span data-stu-id="e091d-236">The application invoked a feature that is not available on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-237"><span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR \_ INVALGROUPID**</span><span class="sxs-lookup"><span data-stu-id="e091d-237"><span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR\_INVALGROUPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-238">指定的群組識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-238">The specified group identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-239"><span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR \_ INVALLINEHANDLE**</span><span class="sxs-lookup"><span data-stu-id="e091d-239"><span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR\_INVALLINEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-240">指定的呼叫、裝置、行裝置或線條控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-240">The specified call, device, line device, or line handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-241"><span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR \_ INVALLINESTATE**</span><span class="sxs-lookup"><span data-stu-id="e091d-241"><span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR\_INVALLINESTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-242">裝置設定在目前的線路狀態中可能不會變更。</span><span class="sxs-lookup"><span data-stu-id="e091d-242">The device configuration may not be changed in the current line state.</span></span> <span data-ttu-id="e091d-243">該行可能正由另一個應用程式使用中，或 *dwLineStates* 參數包含一或多個非 [LINEDEVSTATE \_ 常數](linedevstate--constants.md)的位。</span><span class="sxs-lookup"><span data-stu-id="e091d-243">The line may be in use by another application or a *dwLineStates* parameter contains one or more bits that are not [LINEDEVSTATE\_ constants](linedevstate--constants.md).</span></span> <span data-ttu-id="e091d-244">**LINEERR \_ INVALLINESTATE** 值也可以指出裝置已中斷連線或服務中斷。</span><span class="sxs-lookup"><span data-stu-id="e091d-244">The **LINEERR\_INVALLINESTATE** value can also indicate that the device is disconnected or out of service.</span></span> <span data-ttu-id="e091d-245">這些狀態是藉由在 [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)函式所傳回之 [**LineGetLineDevStatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)結構的 **dwDevStatusFlags** 成員中，將對應于 *LINEDEVSTATUSFLAGS \_ CONNECTED* 和 *LINEDEVSTATUSFLAGS \_ INSERVICE* 值的位設定為0來表示。</span><span class="sxs-lookup"><span data-stu-id="e091d-245">These states are indicated by setting the bits corresponding to the *LINEDEVSTATUSFLAGS\_CONNECTED* and *LINEDEVSTATUSFLAGS\_INSERVICE* values to 0 in the **dwDevStatusFlags** member of the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) structure returned by the [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-246"><span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**LINEERR \_ INVALLOCATION**</span><span class="sxs-lookup"><span data-stu-id="e091d-246"><span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**LINEERR\_INVALLOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-247">在登錄的 [位置] 區段中的任何專案中，找不到在 *dwLocation* 中指定的永久位置識別碼 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="e091d-247">The permanent location identifier specified in *dwLocation* could not be found in any entry in the \[Locations\] section in the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-248"><span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR \_ INVALMEDIALIST**</span><span class="sxs-lookup"><span data-stu-id="e091d-248"><span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR\_INVALMEDIALIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-249">指定的媒體清單無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-249">The specified media list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-250"><span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR \_ INVALMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="e091d-250"><span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR\_INVALMEDIAMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-251">要監視)  (模式的媒體類型清單包含不正確資訊、指定的媒體類型參數無效，或服務提供者不支援指定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e091d-251">The list of media types (modes) to be monitored contains invalid information, the specified media type parameter is invalid, or the service provider does not support the specified media type.</span></span> <span data-ttu-id="e091d-252">這一行所支援的媒體類型會列在 [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)結構的 **dwMediaModes** 成員中。</span><span class="sxs-lookup"><span data-stu-id="e091d-252">The media types supported on the line are listed in the **dwMediaModes** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-253"><span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR \_ INVALMESSAGEID**</span><span class="sxs-lookup"><span data-stu-id="e091d-253"><span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR\_INVALMESSAGEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-254">在 *dwMessageID* 中指定的數位超出 [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)結構中 **dwNumCompletionMessages** 成員所指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="e091d-254">The number given in *dwMessageID* is outside the range specified by the **dwNumCompletionMessages** member in the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-255"><span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR \_ INVALPARAM**</span><span class="sxs-lookup"><span data-stu-id="e091d-255"><span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR\_INVALPARAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-256">參數所指向的參數或結構包含不正確資訊、國家或地區代碼無效、視窗控制碼無效，或指定的轉送清單參數包含不正確資訊。</span><span class="sxs-lookup"><span data-stu-id="e091d-256">A parameter or structure that a parameter points to contains invalid information, a country or region code is invalid, a window handle is invalid, or the specified forward list parameter contains invalid information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-257"><span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR \_ INVALPARKID**</span><span class="sxs-lookup"><span data-stu-id="e091d-257"><span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR\_INVALPARKID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-258">公園識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-258">The park identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-259"><span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR \_ INVALPARKMODE**</span><span class="sxs-lookup"><span data-stu-id="e091d-259"><span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR\_INVALPARKMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-260">指定的公園模式無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-260">The specified park mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-261"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**</span><span class="sxs-lookup"><span data-stu-id="e091d-261"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR\_INVALPASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-262">指定的密碼不正確，而且尚未執行要求的動作。</span><span class="sxs-lookup"><span data-stu-id="e091d-262">The specified password is not correct and the requested action has not been carried out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-263"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**</span><span class="sxs-lookup"><span data-stu-id="e091d-263"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR\_INVALPASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-264">應用程式使用了不正確密碼。</span><span class="sxs-lookup"><span data-stu-id="e091d-264">The application used an invalid password.</span></span> <span data-ttu-id="e091d-265">此值只會公開給協調 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e091d-265">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-266"><span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR \_ INVALPOINTER**</span><span class="sxs-lookup"><span data-stu-id="e091d-266"><span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR\_INVALPOINTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-267">一或多個指定的指標參數 (例如 *lpCallList*、 *lpdwAPIVersion*、 *lpExtensionID*、 *lpdwExtVersion*、 *lphIcon*、 *lpLineDevCaps* 和 *lpToneList*) 無效，或 output 參數的必要指標為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e091d-267">One or more of the specified pointer parameters (such as *lpCallList*, *lpdwAPIVersion*, *lpExtensionID*, *lpdwExtVersion*, *lphIcon*, *lpLineDevCaps*, and *lpToneList*) are invalid, or a required pointer to an output parameter is **NULL**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-268"><span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR \_ INVALPRIVSELECT**</span><span class="sxs-lookup"><span data-stu-id="e091d-268"><span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR\_INVALPRIVSELECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-269">為 *dwPrivileges* 參數設定了不正確旗標或旗標組合。</span><span class="sxs-lookup"><span data-stu-id="e091d-269">An invalid flag or combination of flags was set for the *dwPrivileges* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-270"><span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**LINEERR \_ INVALRATE**</span><span class="sxs-lookup"><span data-stu-id="e091d-270"><span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**LINEERR\_INVALRATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-271">指定的速率無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-271">The specified rate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-272"><span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR \_ INVALREQUESTMODE**</span><span class="sxs-lookup"><span data-stu-id="e091d-272"><span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR\_INVALREQUESTMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-273">[**LINEREQUESTMODE**](linerequestmode--constants.md)指標無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-273">The [**LINEREQUESTMODE**](linerequestmode--constants.md) indicator is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-274"><span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR \_ INVALTERMINALID**</span><span class="sxs-lookup"><span data-stu-id="e091d-274"><span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR\_INVALTERMINALID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-275">指定的終端機識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-275">The specified terminal identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-276"><span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR \_ INVALTERMINALMODE**</span><span class="sxs-lookup"><span data-stu-id="e091d-276"><span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR\_INVALTERMINALMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-277">指定的終端模式參數無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-277">The specified terminal modes parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-278"><span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR \_ INVALTIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="e091d-278"><span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR\_INVALTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-279">不支援超時，或值落在 [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)中指定的有效範圍之外。</span><span class="sxs-lookup"><span data-stu-id="e091d-279">Timeouts are not supported or a value falls outside the valid range specified in [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-280"><span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR \_ INVALTONE**</span><span class="sxs-lookup"><span data-stu-id="e091d-280"><span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR\_INVALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-281">指定的自訂色調不代表有效的色調，或由太多頻率所組成，或指定的色調結構未描述有效的色調。</span><span class="sxs-lookup"><span data-stu-id="e091d-281">The specified custom tone does not represent a valid tone or is made up of too many frequencies or the specified tone structure does not describe a valid tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-282"><span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR \_ INVALTONELIST**</span><span class="sxs-lookup"><span data-stu-id="e091d-282"><span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR\_INVALTONELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-283">指定的音調清單無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-283">The specified tone list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-284"><span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR \_ INVALTONEMODE**</span><span class="sxs-lookup"><span data-stu-id="e091d-284"><span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR\_INVALTONEMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-285">指定的色調模式參數無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-285">The specified tone mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-286"><span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR \_ INVALTRANSFERMODE**</span><span class="sxs-lookup"><span data-stu-id="e091d-286"><span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR\_INVALTRANSFERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-287">指定的傳輸模式參數無效。</span><span class="sxs-lookup"><span data-stu-id="e091d-287">The specified transfer mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-288"><span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR \_ LINEMAPPERFAILED**</span><span class="sxs-lookup"><span data-stu-id="e091d-288"><span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR\_LINEMAPPERFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-289">LINEMAPPER 是傳入 *dwDeviceID* 參數的值，但是找不到符合 *lpCallParams* 參數中所指定之需求的行。</span><span class="sxs-lookup"><span data-stu-id="e091d-289">LINEMAPPER was the value passed in the *dwDeviceID* parameter, but no lines were found that match the requirements specified in the *lpCallParams* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-290"><span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR \_ NOCONFERENCE**</span><span class="sxs-lookup"><span data-stu-id="e091d-290"><span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR\_NOCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-291">指定的呼叫不是會議呼叫控制碼或參與者呼叫。</span><span class="sxs-lookup"><span data-stu-id="e091d-291">The specified call is not a conference call handle or a participant call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-292"><span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR \_ NODEVICE**</span><span class="sxs-lookup"><span data-stu-id="e091d-292"><span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR\_NODEVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-293">因為自從上一次初始化 TAPI 之後，已從系統移除相關聯的裝置，所以不再接受指定的裝置識別碼（先前為有效的裝置識別碼）。</span><span class="sxs-lookup"><span data-stu-id="e091d-293">The specified device identifier, which was previously valid, is no longer accepted because the associated device has been removed from the system since TAPI was last initialized.</span></span> <span data-ttu-id="e091d-294">或者，線路裝置對於指定的裝置類別沒有相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="e091d-294">Alternately, the line device has no associated device for the given device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-295"><span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR \_ NODRIVER**</span><span class="sxs-lookup"><span data-stu-id="e091d-295"><span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR\_NODRIVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-296">找不到 Tapiaddr.dll 找不到，或指定裝置的電話服務提供者發現其中一個元件遺失或損毀，無法在初始化時偵測到。</span><span class="sxs-lookup"><span data-stu-id="e091d-296">Either Tapiaddr.dll could not be located or the telephone service provider for the specified device found that one of its components is missing or corrupt in a way that was not detected at initialization time.</span></span> <span data-ttu-id="e091d-297">應建議使用者使用電話語音主控台修正問題。</span><span class="sxs-lookup"><span data-stu-id="e091d-297">The user should be advised to use the Telephony Control Panel to correct the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-298"><span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**LINEERR \_ NOMEM**</span><span class="sxs-lookup"><span data-stu-id="e091d-298"><span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**LINEERR\_NOMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-299">記憶體不足，無法執行操作或無法鎖定記憶體。</span><span class="sxs-lookup"><span data-stu-id="e091d-299">Insufficient memory to perform the operation, or unable to lock memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-300"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="e091d-300"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR\_NOMULTIPLEINSTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-301">不支援多個實例的電話語音服務提供者在登錄的 [提供者] 區段中列出了一次以上 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="e091d-301">A telephony service provider that does not support multiple instances is listed more than once in the \[Providers\] section in the registry.</span></span> <span data-ttu-id="e091d-302">應用程式應通知使用者使用電話語音主控台移除重複的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="e091d-302">The application should advise the user to use the Telephony Control Panel to remove the duplicated driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-303"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="e091d-303"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR\_NOMULTIPLEINSTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-304">不允許此服務提供者的多個實例。</span><span class="sxs-lookup"><span data-stu-id="e091d-304">Multiple instances of this service provider are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-305"><span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR \_ NOREQUEST**</span><span class="sxs-lookup"><span data-stu-id="e091d-305"><span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR\_NOREQUEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-306">目前沒有任何要求暫止于指定的模式，或應用程式不再是指定要求模式的最高優先順序應用程式。</span><span class="sxs-lookup"><span data-stu-id="e091d-306">There currently is no request pending of the indicated mode, or the application is no longer the highest-priority application for the specified request mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-307"><span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR \_ NOTOWNER**</span><span class="sxs-lookup"><span data-stu-id="e091d-307"><span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR\_NOTOWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-308">應用程式沒有指定之呼叫的擁有者許可權。</span><span class="sxs-lookup"><span data-stu-id="e091d-308">The application does not have owner privilege to the specified call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-309"><span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR \_ NOTREGISTERED**</span><span class="sxs-lookup"><span data-stu-id="e091d-309"><span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR\_NOTREGISTERED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-310">應用程式未註冊為指定要求模式的要求收件者。</span><span class="sxs-lookup"><span data-stu-id="e091d-310">The application is not registered as a request recipient for the indicated request mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-311"><span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR \_ OPERATIONFAILED**</span><span class="sxs-lookup"><span data-stu-id="e091d-311"><span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR\_OPERATIONFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-312">因為未指定或未知的原因，導致作業失敗。</span><span class="sxs-lookup"><span data-stu-id="e091d-312">The operation failed for an unspecified or unknown reason.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-313"><span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR \_ OPERATIONUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="e091d-313"><span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR\_OPERATIONUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-314">無法使用作業，例如指定的裝置或指定的行。</span><span class="sxs-lookup"><span data-stu-id="e091d-314">The operation is not available, such as for the given device or specified line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-315"><span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR \_ RATEUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="e091d-315"><span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR\_RATEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-316">服務提供者目前沒有足夠的頻寬可達指定的速率。</span><span class="sxs-lookup"><span data-stu-id="e091d-316">The service provider currently does not have enough bandwidth available for the specified rate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-317"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR \_ 重新初始化**</span><span class="sxs-lookup"><span data-stu-id="e091d-317"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-318">如果已要求 TAPI 重新初始化（例如新增或移除電話語音服務提供者的結果），則 [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)、 [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)或 [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) 要求會因為此錯誤而被拒絕，直到最後一個應用程式使用 [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)) 來關閉其 API (為止，此時新的設定就會生效，而應用程式會再次被允許呼叫 **lineInitialize** 或 **lineInitializeEx**。</span><span class="sxs-lookup"><span data-stu-id="e091d-318">If TAPI reinitialization has been requested, for example as a result of adding or removing a telephony service provider, then [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), or [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) requests are rejected with this error until the last application shuts down its usage of the API (using [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), at which time the new configuration becomes effective and applications are once again permitted to call **lineInitialize** or **lineInitializeEx**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-319"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR \_ 重新初始化**</span><span class="sxs-lookup"><span data-stu-id="e091d-319"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-320">應用程式嘗試初始化 TAPI 兩次。</span><span class="sxs-lookup"><span data-stu-id="e091d-320">The application attempted to initialize TAPI twice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-321"><span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR \_ REQUESTOVERRUN**</span><span class="sxs-lookup"><span data-stu-id="e091d-321"><span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR\_REQUESTOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-322">有更多的要求擱置中，而不是裝置可以處理的要求。</span><span class="sxs-lookup"><span data-stu-id="e091d-322">More requests are pending than the device can handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-323"><span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR \_ RESOURCEUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="e091d-323"><span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR\_RESOURCEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-324">資源不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="e091d-324">Insufficient resources to complete the operation.</span></span> <span data-ttu-id="e091d-325">例如，因為動態資源 overcommitment，所以無法開啟一行。</span><span class="sxs-lookup"><span data-stu-id="e091d-325">For example, a line cannot be opened due to a dynamic resource overcommitment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-326"><span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR \_ STRUCTURETOOSMALL**</span><span class="sxs-lookup"><span data-stu-id="e091d-326"><span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR\_STRUCTURETOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-327">結構的 **dwTotalSize** 成員未指定足夠的記憶體來包含指定結構的固定部分。</span><span class="sxs-lookup"><span data-stu-id="e091d-327">The **dwTotalSize** member of a structure does not specify enough memory to contain the fixed portion of the specified structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-328"><span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR \_ TARGETNOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="e091d-328"><span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR\_TARGETNOTFOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-329">找不到呼叫切換的目標。</span><span class="sxs-lookup"><span data-stu-id="e091d-329">A target for the call handoff was not found.</span></span> <span data-ttu-id="e091d-330">如果命名的應用程式未 \_ 在 [**LineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)的 *DWPRIVILEGES* 參數中以 LINECALLPRIVILEGE 擁有者位開啟同一行，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="e091d-330">This can occur if the named application did not open the same line with the LINECALLPRIVILEGE\_OWNER bit in the *dwPrivileges* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span></span> <span data-ttu-id="e091d-331">或者，在媒體模式的提交案例中，沒有任何應用程式在 \_ [**LineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)的 *DWPRIVILEGES* 參數中以 LINECALLPRIVILEGE 擁有者位開啟同一行，而 *dwMediaMode* 參數中指定的媒體類型已在 [**dwMediaModes**](/windows/desktop/api/Tapi/nf-tapi-lineopen)的 *lineOpen* 參數中指定。</span><span class="sxs-lookup"><span data-stu-id="e091d-331">Or, in the case of media-mode handoff, no application has opened the same line with the LINECALLPRIVILEGE\_OWNER bit in the *dwPrivileges* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) and with the media type specified in the *dwMediaMode* parameter having been specified in the *dwMediaModes* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-332"><span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR \_ TARGETSELF**</span><span class="sxs-lookup"><span data-stu-id="e091d-332"><span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR\_TARGETSELF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-333">叫用這項作業的應用程式是間接交付的目標。</span><span class="sxs-lookup"><span data-stu-id="e091d-333">The application invoking this operation is the target of the indirect handoff.</span></span> <span data-ttu-id="e091d-334">也就是說，TAPI 判斷呼叫的應用程式也是指定媒體類型的最高優先順序應用程式。</span><span class="sxs-lookup"><span data-stu-id="e091d-334">That is, TAPI has determined that the calling application is also the highest priority application for the given media type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-335"><span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR \_ 未初始化**</span><span class="sxs-lookup"><span data-stu-id="e091d-335"><span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR\_UNINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-336">作業是在任何名為 [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) 或 [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)的應用程式之前叫用。</span><span class="sxs-lookup"><span data-stu-id="e091d-336">The operation was invoked before any application called [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-337"><span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR \_ USERCANCELLED**</span><span class="sxs-lookup"><span data-stu-id="e091d-337"><span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR\_USERCANCELLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-338">使用者已取消通話。</span><span class="sxs-lookup"><span data-stu-id="e091d-338">The user cancelled the call.</span></span> <span data-ttu-id="e091d-339">此值只會公開給協調 TAPI 2.2 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e091d-339">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e091d-340"><span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR \_ USERUSERINFOTOOBIG**</span><span class="sxs-lookup"><span data-stu-id="e091d-340"><span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR\_USERUSERINFOTOOBIG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e091d-341">包含使用者使用者資訊的字串超過 [**dwUUISendUserUserInfoSize**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)的 **dwUUIAcceptSize**、 **dwUUIAnswerSize**、 **dwUUIDropSize**、 **dwUUIMakeCallSize** 或 **LINEDEVCAPS** 成員中指定的最大位元組數目，或包含使用者資訊的字串太長。</span><span class="sxs-lookup"><span data-stu-id="e091d-341">The string containing user-user information exceeds the maximum number of bytes specified in the **dwUUIAcceptSize**, **dwUUIAnswerSize**, **dwUUIDropSize**, **dwUUIMakeCallSize**, or **dwUUISendUserUserInfoSize** member of [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps), or the string containing user-user information is too long.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e091d-342">備註</span><span class="sxs-lookup"><span data-stu-id="e091d-342">Remarks</span></span>

<span data-ttu-id="e091d-343">0xC0000000 至0xFFFFFFFF 的值適用于裝置專屬的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="e091d-343">The values 0xC0000000 through 0xFFFFFFFF are available for device-specific extensions.</span></span> <span data-ttu-id="e091d-344">透過0xBFFFFFFF 的值0x80000000 是保留的，而0x00000000 到0x7FFFFFFF 則是用來作為要求識別碼。</span><span class="sxs-lookup"><span data-stu-id="e091d-344">The values 0x80000000 through 0xBFFFFFFF are reserved, while 0x00000000 through 0x7FFFFFFF are used as request identifiers.</span></span>

<span data-ttu-id="e091d-345">如果應用程式收到錯誤訊息，指出它不會明確處理 (（例如裝置專屬延伸模組所定義的錯誤）) ，則應該將錯誤視為 LINEERR \_ OPERATIONFAILED (，以找出未指定原因) 。</span><span class="sxs-lookup"><span data-stu-id="e091d-345">If an application gets an error return that it does not specifically handle (such as an error defined by a device-specific extension), it should treat the error as a LINEERR\_OPERATIONFAILED (for an unspecified reason).</span></span>

<span data-ttu-id="e091d-346">叫 \_ 用 TAPI 3.0 的新 LINEERR 常數時，必須使用新的訊息更新 Tapierr.mc 檔案。</span><span class="sxs-lookup"><span data-stu-id="e091d-346">When invoking the LINEERR\_constants which are new with TAPI 3.0, the Tapierr.mc file must be updated with new messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="e091d-347">規格需求</span><span class="sxs-lookup"><span data-stu-id="e091d-347">Requirements</span></span>



| <span data-ttu-id="e091d-348">需求</span><span class="sxs-lookup"><span data-stu-id="e091d-348">Requirement</span></span> | <span data-ttu-id="e091d-349">值</span><span class="sxs-lookup"><span data-stu-id="e091d-349">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e091d-350">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="e091d-350">TAPI version</span></span><br/> | <span data-ttu-id="e091d-351">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e091d-351">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e091d-352">標頭</span><span class="sxs-lookup"><span data-stu-id="e091d-352">Header</span></span><br/>       | <dl> <span data-ttu-id="e091d-353"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="e091d-353"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e091d-354">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e091d-354">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e091d-355">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="e091d-355">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="e091d-356">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="e091d-356">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="e091d-357">**LINEDEVSTATUS**</span><span class="sxs-lookup"><span data-stu-id="e091d-357">**LINEDEVSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[<span data-ttu-id="e091d-358">**lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="e091d-358">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[<span data-ttu-id="e091d-359">**lineInitialize**</span><span class="sxs-lookup"><span data-stu-id="e091d-359">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="e091d-360">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="e091d-360">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> <dt>

[<span data-ttu-id="e091d-361">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="e091d-361">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="e091d-362">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="e091d-362">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 





---
title: 要求者 API 呼叫順序
description: 瞭解要求者 API 呼叫順序。 查看通話順序的總覽，並查看其他可用的資源。
ms.assetid: 83276783-aee5-43ac-982d-1144df982a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c93afea6dbf4c3220bbeaec4f6278eb3d0b756
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933629"
---
# <a name="supplicant-api-call-sequence"></a><span data-ttu-id="c6135-104">要求者 API 呼叫順序</span><span class="sxs-lookup"><span data-stu-id="c6135-104">Supplicant API Call Sequence</span></span>

<span data-ttu-id="c6135-105">本主題提供要求者 API 的特定呼叫順序。</span><span class="sxs-lookup"><span data-stu-id="c6135-105">This topic provides the specific call sequence for the supplicant API.</span></span>

## <a name="supplicant-api-call-sequence-overview"></a><span data-ttu-id="c6135-106">要求者 API 呼叫順序總覽</span><span class="sxs-lookup"><span data-stu-id="c6135-106">Supplicant API Call Sequence Overview</span></span>

<span data-ttu-id="c6135-107">當要求者從提供者（例如存取點）接收 EAP 封包時，通常會發生下列要求者 API 呼叫流程。</span><span class="sxs-lookup"><span data-stu-id="c6135-107">When the supplicant receives an EAP packet from a provider, such as an access point, the following supplicant API call flow typically occurs.</span></span>

-   <span data-ttu-id="c6135-108">應用程式會使用 EAPHost 設定資料和使用者資料來呼叫 [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 。</span><span class="sxs-lookup"><span data-stu-id="c6135-108">The application calls [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) with EAPHost configuration data and user data.</span></span> <span data-ttu-id="c6135-109">成功的呼叫會傳回 **EAP \_ 會話 \_ 句** 柄會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="c6135-109">A successful call returns an **EAP\_SESSION\_HANDLE** session handle.</span></span>
-   <span data-ttu-id="c6135-110">要求者接收的每個封包都會透過呼叫 [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket)來處理。</span><span class="sxs-lookup"><span data-stu-id="c6135-110">Each packet received by the supplicant is processed by a call to [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket).</span></span> <span data-ttu-id="c6135-111">然後，要求者會呼叫對應至函式所傳回之動作程式碼的函式。</span><span class="sxs-lookup"><span data-stu-id="c6135-111">The supplicant then calls the function corresponding to the action code returned by the function.</span></span>
-   <span data-ttu-id="c6135-112">如果動作碼是 **EapHostPeerResponseSend**，要求者會呼叫 [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket) 來取得要傳送給驗證器的回應。</span><span class="sxs-lookup"><span data-stu-id="c6135-112">If the action code is **EapHostPeerResponseSend**, then the supplicant calls [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket) to obtain the response to be sent to the authenticator.</span></span>
-   <span data-ttu-id="c6135-113">如果在會話期間，傳回給要求者的動作程式碼是 **EapHostPeerResponseRespond**，則表示 EAP 屬性可供使用。</span><span class="sxs-lookup"><span data-stu-id="c6135-113">If during the session, the action code returned to the supplicant is **EapHostPeerResponseRespond**, it indicates that EAP attributes are available.</span></span> <span data-ttu-id="c6135-114">要求者接著會呼叫 [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) 來取得它們。</span><span class="sxs-lookup"><span data-stu-id="c6135-114">The supplicant then calls [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) to obtain them.</span></span> <span data-ttu-id="c6135-115">這些屬性包含在驗證過程中所使用的補充資料。</span><span class="sxs-lookup"><span data-stu-id="c6135-115">These attributes contain supplemental data used during the authentication process.</span></span> <span data-ttu-id="c6135-116">在要求者完成處理屬性之後，它會呼叫 [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) 來更新資料。</span><span class="sxs-lookup"><span data-stu-id="c6135-116">After supplicant completes processing the attributes it calls [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) which updates the data.</span></span> <span data-ttu-id="c6135-117">此函式會傳回動作碼，以決定要求者的下一個動作。</span><span class="sxs-lookup"><span data-stu-id="c6135-117">This function returns an action code which determines the supplicant's next action.</span></span>
-   <span data-ttu-id="c6135-118">如果動作程式碼 **EapHostPeerResponseInvokeUI** ，要求者會引發使用者介面對話方塊來取得使用者的互動式資料，例如認證或身分識別資訊。</span><span class="sxs-lookup"><span data-stu-id="c6135-118">If the action code is **EapHostPeerResponseInvokeUI** the supplicant raises a user interface dialog to obtain interactive data from the user, such as credentials or identity information.</span></span> <span data-ttu-id="c6135-119">請參閱下面的要求者 API 呼叫流程使用者互動。</span><span class="sxs-lookup"><span data-stu-id="c6135-119">See User Interaction with the Supplicant API Call Flow below.</span></span>
-   <span data-ttu-id="c6135-120">如果動作碼是 **EapHostPeerResponseResult**，則表示驗證會話的結果可供要求者使用。</span><span class="sxs-lookup"><span data-stu-id="c6135-120">If the action code is **EapHostPeerResponseResult**, it indicates that the results of the authentication session are available to the supplicant.</span></span> <span data-ttu-id="c6135-121">要求者接著會呼叫 [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult) 來取得結果。</span><span class="sxs-lookup"><span data-stu-id="c6135-121">The supplicant then calls [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult) to obtain the results.</span></span> <span data-ttu-id="c6135-122">無論結果是表示成功還是失敗，要求者都會呼叫 [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession)。</span><span class="sxs-lookup"><span data-stu-id="c6135-122">Regardless of whether the results indicate success or failure, the supplicant calls [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession).</span></span> <span data-ttu-id="c6135-123">在失敗的情況下，您可以使用 EAPHost 開啟另一個會話並提供新的身分識別，或再次嘗試使用原始身分識別進行驗證，來嘗試重新驗證。</span><span class="sxs-lookup"><span data-stu-id="c6135-123">In the case of failure, re-authentication can be attempted by opening another session with EAPHost and providing a new identity, or attempting authentication with the original identity again.</span></span>

## <a name="user-interaction-with-the-supplicant-api-call-flow"></a><span data-ttu-id="c6135-124">使用者與要求者 API 呼叫流程的互動</span><span class="sxs-lookup"><span data-stu-id="c6135-124">User Interaction with the Supplicant API Call Flow</span></span>

<span data-ttu-id="c6135-125">在某些情況下，要求者需要取得使用者的資訊，才能繼續進行驗證程式。</span><span class="sxs-lookup"><span data-stu-id="c6135-125">In certain cases, the supplicant needs to obtain information from the user to continue the authentication process.</span></span>

<span data-ttu-id="c6135-126">下列清單示範啟用互動式輸入所需的要求者和 EAPHost UI 進程的呼叫順序。</span><span class="sxs-lookup"><span data-stu-id="c6135-126">The following list demonstrates the sequence of calls on the supplicant and EAPHost UI process necessary to enable interactive input.</span></span>

1.  <span data-ttu-id="c6135-127">要求者藉由呼叫 [**EapHostPeerGetUICoNtext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)來取得目前的使用者介面內容。</span><span class="sxs-lookup"><span data-stu-id="c6135-127">The supplicant obtains the current user interface context by calling [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext).</span></span>
2.  <span data-ttu-id="c6135-128">要求者接著將 UI 內容資料傳送給要求者 UI 進程。</span><span class="sxs-lookup"><span data-stu-id="c6135-128">The supplicant then sends the UI context data to the supplicant UI process.</span></span>
    > [!Note]  
    > <span data-ttu-id="c6135-129">UI 進程通常會收集 UI 或處理互動式 UI，與要求者進程不同。</span><span class="sxs-lookup"><span data-stu-id="c6135-129">The UI process, which typically collects UI or handles interactive UI, is separate from the supplicant process.</span></span> <span data-ttu-id="c6135-130">分隔這兩個程式並不是 EAPHost 的需求，但這麼做的優點是可以讓 UI 進程與桌面互動。</span><span class="sxs-lookup"><span data-stu-id="c6135-130">Separating the two processes is not a requirement of EAPHost, but doing so has the advantage of allowing the UI process to interact with the desktop.</span></span>

     

3.  <span data-ttu-id="c6135-131">如果要求者想要自行轉譯 UI，則會呼叫 [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) 函式來取得要引發之互動式 UI 元件的輸入欄位。</span><span class="sxs-lookup"><span data-stu-id="c6135-131">If the supplicant wants to render the UI by itself then it calls the [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) function to obtain the input fields for interactive UI components to be raised.</span></span> <span data-ttu-id="c6135-132">否則，它會遵循傳統的叫用方法互動式 UI 的模型，方法是呼叫 [ **EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)</span><span class="sxs-lookup"><span data-stu-id="c6135-132">Otherwise, it follows the traditional model of invoking method interactive UI by calling [**EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)</span></span>
    > [!Note]  
    > <span data-ttu-id="c6135-133">如果傳回的是 [**\_ \_ \_ \_ \_ 不 \_ 支援的 EAP E EAPHOST 方法**](eap-related-error-and-information-constants.md) 作業，要求者必須藉由呼叫 [**EAPHOSTPEERINVOKEINTERACTIVEUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)來遵循傳統的叫用方法互動式 UI 模型。</span><span class="sxs-lookup"><span data-stu-id="c6135-133">If [**EAP\_E\_EAPHOST\_METHOD\_OPERATION\_NOT\_SUPPORTED**](eap-related-error-and-information-constants.md) is returned, the supplicant must follow the traditional model of invoking method interactive UI by calling [**EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui).</span></span> <span data-ttu-id="c6135-134">如果發生錯誤， [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) 會傳回 **Null** 以外的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="c6135-134">If there is an error, [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) will return a return code other than **NULL**.</span></span>

     

4.  <span data-ttu-id="c6135-135">當要求者呼叫 [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) 或 [**EaphostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) UI 進程時，會傳遞現有的內容資料並載入 Eappcfg.dll。</span><span class="sxs-lookup"><span data-stu-id="c6135-135">Whether the supplicant calls [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) or [**EaphostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) the UI process passes the existing context data and loads Eappcfg.dll.</span></span> <span data-ttu-id="c6135-136">引發適當的 UI 來收集新的資料。</span><span class="sxs-lookup"><span data-stu-id="c6135-136">Appropriate UI is raised to collect the new data.</span></span> <span data-ttu-id="c6135-137">新的 UI 內容資料（現在可能包含使用者輸入）會進行複製，而舊的內容資料會透過呼叫 [**EapPeerFreeMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory)來釋放。</span><span class="sxs-lookup"><span data-stu-id="c6135-137">The new UI context data, which may now contain user input, is copied, and the old context data is released with a call to [**EapPeerFreeMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory).</span></span>
5.  <span data-ttu-id="c6135-138">UI 進程會將新的內容資料傳回給要求者，以呼叫 [**EapHostPeerSetUICoNtext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) 來設定它。</span><span class="sxs-lookup"><span data-stu-id="c6135-138">The UI process returns the new context data to the supplicant, which calls [**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) to set it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6135-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="c6135-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6135-140">對等方法 API 呼叫順序</span><span class="sxs-lookup"><span data-stu-id="c6135-140">Peer Method API Call Sequence</span></span>](peer-method-api-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="c6135-141">驗證者方法 API 呼叫順序</span><span class="sxs-lookup"><span data-stu-id="c6135-141">Authenticator Method API Call Sequence</span></span>](authenticator-method-api-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="c6135-142">EAPHost 呼叫順序</span><span class="sxs-lookup"><span data-stu-id="c6135-142">EAPHost Call Sequence</span></span>](about-eaphost-call-sequences.md)
</dt> <dt>

[<span data-ttu-id="c6135-143">EAPHost 要求者</span><span class="sxs-lookup"><span data-stu-id="c6135-143">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 





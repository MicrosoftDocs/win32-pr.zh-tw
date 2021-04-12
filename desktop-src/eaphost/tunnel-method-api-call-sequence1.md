---
title: 通道方法 API 呼叫順序
description: 瞭解通道方法的 API 呼叫順序。 請參閱總覽並查看其他可用的資源。
ms.assetid: 48aad213-1d29-4809-9599-b56325b2b8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5f6b30fda111162585fb5c8b2aa370fa6af61e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316504"
---
# <a name="tunnel-method-api-call-sequence"></a><span data-ttu-id="b0cae-104">通道方法 API 呼叫順序</span><span class="sxs-lookup"><span data-stu-id="b0cae-104">Tunnel Method API Call Sequence</span></span>

<span data-ttu-id="b0cae-105">本主題涵蓋通道方法的 API 呼叫順序</span><span class="sxs-lookup"><span data-stu-id="b0cae-105">This topic covers the API call sequence for Tunnel Methods</span></span>

## <a name="tunnel-method-call-sequence-overview"></a><span data-ttu-id="b0cae-106">通道方法呼叫順序總覽</span><span class="sxs-lookup"><span data-stu-id="b0cae-106">Tunnel Method Call Sequence Overview</span></span>

<span data-ttu-id="b0cae-107">當要求者取得使用者身分識別和使用者資料的要求時，通常會發生下列 API 呼叫流程。</span><span class="sxs-lookup"><span data-stu-id="b0cae-107">When Supplicant gets request for user identity and user data the following API call flow typically occurs.</span></span>

-   <span data-ttu-id="b0cae-108">要求者在 EapHost 上呼叫 EapHostPeerProcessReceivedPacket，以處理從驗證器收到的封包。</span><span class="sxs-lookup"><span data-stu-id="b0cae-108">The Supplicant calls EapHostPeerProcessReceivedPacket on EapHost, to process the packet received from the authenticator.</span></span>
-   <span data-ttu-id="b0cae-109">處理此封包時，EAPHost 會將它判斷為 IdentityRequest 封包，並在通道方法上呼叫 [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) ，以取得要用於驗證的使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="b0cae-109">Upon processing this packet, EAPHost determines it as IdentityRequest packet and calls [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) on tunnel method to obtain the user identity to use for authentication.</span></span>
-   <span data-ttu-id="b0cae-110">如果通道方法需要從內部方法取得使用者身分識別，它會在內部 EAPHost 上呼叫 [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) ，然後再呼叫內部方法上的 [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) 。</span><span class="sxs-lookup"><span data-stu-id="b0cae-110">If tunnel method needs to obtain user identity from the inner method, it calls [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) on inner EAPHost, which in turn calls [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) on the inner method.</span></span>

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a><span data-ttu-id="b0cae-111">使用者與通道方法 API 呼叫流程的互動</span><span class="sxs-lookup"><span data-stu-id="b0cae-111">User Interaction with the Tunnel Methods API Call Flow</span></span>

<span data-ttu-id="b0cae-112">在某些情況下，當身分識別無法使用，或當使用者必須提供其他資訊時，Eap 方法會在要求者上引發使用者介面對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b0cae-112">In certain cases, when the identity is not available, or when the user must provide additional information, Eap Method raises an user interface dialog box on the supplicant.</span></span>

<span data-ttu-id="b0cae-113">在這種情況下，通常會發生呼叫順序，以便直接從使用者取得資訊。</span><span class="sxs-lookup"><span data-stu-id="b0cae-113">In such cases following call sequence typically takes place to get information directly from the user.</span></span>

-   <span data-ttu-id="b0cae-114">通道 Eap 方法會傳回動作程式碼，以叫用 UI 來 EapHost。</span><span class="sxs-lookup"><span data-stu-id="b0cae-114">Tunnel Eap Method returns action code to invoke UI to EapHost.</span></span> <span data-ttu-id="b0cae-115">要求者呼叫 [**EapHostPeerGetUICoNtext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)來取得使用者介面對話方塊的目前使用者介面內容資訊。</span><span class="sxs-lookup"><span data-stu-id="b0cae-115">Supplicant calls [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)to obtain the current user interface context information for the user interface dialog box.</span></span>
-   <span data-ttu-id="b0cae-116">然後要求者呼叫 [ **EapHostPeerInvokeInteractiveUI。**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)</span><span class="sxs-lookup"><span data-stu-id="b0cae-116">Supplicant then calls [**EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)</span></span> <span data-ttu-id="b0cae-117">此函式會使用 UI 內容資訊來引發互動式使用者介面，此介面是用來從使用者取得認證資訊。</span><span class="sxs-lookup"><span data-stu-id="b0cae-117">This function uses the UI context information to raise an interactive user interface which is used to get credential information from the user.</span></span> <span data-ttu-id="b0cae-118">UI 進程會載入 Eappcfg.dll，並取得 EapPeerInvokeInteractiveUI 和 EapPeerFreeMemory 的指標。</span><span class="sxs-lookup"><span data-stu-id="b0cae-118">The UI process loads Eappcfg.dll and obtains the pointers to EapPeerInvokeInteractiveUI and EapPeerFreeMemory.</span></span>
    > [!Note]  
    > <span data-ttu-id="b0cae-119">UI 程式通常會收集 UI 或處理互動式 UI，並與要求者進程分開。</span><span class="sxs-lookup"><span data-stu-id="b0cae-119">UI process typically collects UI or handles interactive UI and is separate from the supplicant process.</span></span> <span data-ttu-id="b0cae-120">分隔這兩個程式並不是 EAPHost 的需求，但這麼做的優點是可以讓 UI 進程與桌面互動。</span><span class="sxs-lookup"><span data-stu-id="b0cae-120">Separating the two processes is not a requirement of EAPHost, but doing so has the advantage of allowing the UI process to interact with the desktop.</span></span>

     

-   <span data-ttu-id="b0cae-121">EapHost 會呼叫通道方法上的 [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) 來取得使用者身分識別資訊。</span><span class="sxs-lookup"><span data-stu-id="b0cae-121">EapHost calls [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) on tunnel method to obtain user identity information.</span></span>
-   <span data-ttu-id="b0cae-122">為了從內部方法取得使用者身分識別，通道方法會在內部 EAPHost 上呼叫 [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) 。</span><span class="sxs-lookup"><span data-stu-id="b0cae-122">In order to obtain user identity from inner method, tunnel method calls [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) on inner EAPHost.</span></span>
-   <span data-ttu-id="b0cae-123">內部 EAPHost 會呼叫內部方法上的 [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) 來叫用使用者身分識別 UI。</span><span class="sxs-lookup"><span data-stu-id="b0cae-123">Inner EAPHost calls [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) on inner method to invoke user identity UI.</span></span>
-   <span data-ttu-id="b0cae-124">[**EapHostPeerSetUICoNtext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) 會在引發 ui 之後，提供新的或更新的 ui 內容資訊給 EAPHost 上載入的 EAP 對等方法。</span><span class="sxs-lookup"><span data-stu-id="b0cae-124">[**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) provides a new or updated UI context information to the EAP peer method loaded on EAPHost after the UI has been raised.</span></span>

<span data-ttu-id="b0cae-125">下圖說明通道方法的 API 呼叫順序</span><span class="sxs-lookup"><span data-stu-id="b0cae-125">Following diagram explains the API Call Sequence for Tunnel Methods</span></span>

![通道方法 api 呼叫順序](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a><span data-ttu-id="b0cae-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="b0cae-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0cae-128">EAPHost 呼叫順序</span><span class="sxs-lookup"><span data-stu-id="b0cae-128">EAPHost Call Sequence</span></span>](about-eaphost-call-sequences.md)
</dt> <dt>

[<span data-ttu-id="b0cae-129">要求者 API 呼叫順序</span><span class="sxs-lookup"><span data-stu-id="b0cae-129">Supplicant API Call Sequence</span></span>](supplicant-api-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="b0cae-130">EAPHost 要求者 API 參考</span><span class="sxs-lookup"><span data-stu-id="b0cae-130">EAPHost Supplicant API Reference</span></span>](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 





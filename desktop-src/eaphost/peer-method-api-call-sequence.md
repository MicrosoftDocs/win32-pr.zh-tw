---
title: 對等方法 API 呼叫順序
description: 深入瞭解對等方法 API 呼叫順序。 請參閱清單，以示範 EAPHost 在 EAP 對等方法上所做的呼叫順序。
ms.assetid: aac69e89-249d-4bc8-baef-1f0681f9f7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac9be0f6de228fd5b1ebf2d2c28320baf76e914
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093312"
---
# <a name="peer-method-api-call-sequence"></a><span data-ttu-id="96cad-104">對等方法 API 呼叫順序</span><span class="sxs-lookup"><span data-stu-id="96cad-104">Peer Method API Call Sequence</span></span>

<span data-ttu-id="96cad-105">本主題提供對等方法 API 的特定呼叫順序。</span><span class="sxs-lookup"><span data-stu-id="96cad-105">This topic provides the specific call sequence for the peer method API.</span></span> <span data-ttu-id="96cad-106">在一般 EAP 驗證會話 EAPHost 期間，會在 EAP 方法上進行一些呼叫，以執行 EAPHost 對等方法 API。</span><span class="sxs-lookup"><span data-stu-id="96cad-106">During a typical EAP authentication session EAPHost makes a number of calls on EAP methods to implement the EAPHost peer method API.</span></span>

<span data-ttu-id="96cad-107">下列清單示範 EAPHost 在 EAP 對等方法上所做的呼叫順序。</span><span class="sxs-lookup"><span data-stu-id="96cad-107">The following list demonstrates the sequence of calls made by EAPHost on an EAP peer method.</span></span>

-   <span data-ttu-id="96cad-108">載入用於驗證的 EAP 對等方法 DLL。</span><span class="sxs-lookup"><span data-stu-id="96cad-108">Loads the EAP peer method DLL used for the authentication.</span></span>
-   <span data-ttu-id="96cad-109">呼叫方法上的 [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) ，以取得在 DLL 上所執行之函式的指標清單。</span><span class="sxs-lookup"><span data-stu-id="96cad-109">Calls [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) on the method to obtain a list of pointers to functions implemented on the DLL.</span></span> <span data-ttu-id="96cad-110">EAPHost 對等 (用戶端) 的後續函式呼叫會假設在 DLL 上執行。</span><span class="sxs-lookup"><span data-stu-id="96cad-110">Subsequent function calls by the EAPHost peer (client) are assumed to be implemented on the DLL.</span></span>
-   <span data-ttu-id="96cad-111">呼叫 [**EapPeerInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) ，以指示 EAP 方法程式庫使用此對等方法來準備至少一個驗證會話。</span><span class="sxs-lookup"><span data-stu-id="96cad-111">Calls [**EapPeerInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) to instruct the EAP Method Library to prepare for at least one authentication session using this peer method.</span></span>
-   <span data-ttu-id="96cad-112">呼叫 [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) 來建立唯一的驗證會話。</span><span class="sxs-lookup"><span data-stu-id="96cad-112">Calls [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) to establish a unique authentication session.</span></span>
-   <span data-ttu-id="96cad-113">呼叫 [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) 以取得要用於驗證的身分識別。</span><span class="sxs-lookup"><span data-stu-id="96cad-113">Calls [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) to obtain the identity to use for authentication.</span></span> <span data-ttu-id="96cad-114">如果無法使用身分識別，或是使用者必須提供其他資訊，EAPHost 會呼叫 [ **EapPeerGetUICoNtext。**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext)</span><span class="sxs-lookup"><span data-stu-id="96cad-114">If the identity is not available, or if the user must provide additional information, EAPHost calls [**EapPeerGetUIContext.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext)</span></span> <span data-ttu-id="96cad-115">此函式會取得使用者介面對話方塊的內容資訊，此對話方塊會在要求者上引發。</span><span class="sxs-lookup"><span data-stu-id="96cad-115">This function obtains the context information for the user interface dialog box that will be raised on the supplicant.</span></span> <span data-ttu-id="96cad-116">在使用者提交身分識別資訊之後，使用者身分識別會透過呼叫 [**EapPeerSetUICoNtext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)來設定，並透過呼叫 **EapPeerGetIdentity** 取得。</span><span class="sxs-lookup"><span data-stu-id="96cad-116">After the user has submitted the identity information, the user identity is set with a call to [**EapPeerSetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext), and obtained by a call to **EapPeerGetIdentity**.</span></span>
-   <span data-ttu-id="96cad-117">重複執行下列步驟，直到 [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) 指出有可用的驗證結果。</span><span class="sxs-lookup"><span data-stu-id="96cad-117">Repeats the following steps until [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) indicates that an authentication result is available.</span></span>
    -   <span data-ttu-id="96cad-118">使用要傳遞給要求者的要求封包指標來呼叫 [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) 。</span><span class="sxs-lookup"><span data-stu-id="96cad-118">Calls [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) with the pointer of a request packet to pass to the supplicant.</span></span>
    -   <span data-ttu-id="96cad-119">呼叫 **EapPeerGetResponsePacket** 以取得要傳送給驗證器的回應封包。</span><span class="sxs-lookup"><span data-stu-id="96cad-119">Calls **EapPeerGetResponsePacket** to retrieve the response packet to send to the authenticator.</span></span>
    -   <span data-ttu-id="96cad-120">（選擇性）如果在驗證會話期間需要抓取或傳送 EAP 屬性，EAPHost 會分別呼叫 [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) 和 [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) 。</span><span class="sxs-lookup"><span data-stu-id="96cad-120">Optionally, if EAP attributes need to be retrieved or sent during the authentication session, EAPHost calls [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) and [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) respectively.</span></span>
-   <span data-ttu-id="96cad-121">當驗證器傳送指出驗證已完成的動作程式碼時，EAPHost 會呼叫 [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult) 並取得驗證的結果。</span><span class="sxs-lookup"><span data-stu-id="96cad-121">When the authenticator sends an action code that indicates authentication is complete, EAPHost calls [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult) and obtains the results of the authentication.</span></span>
-   <span data-ttu-id="96cad-122">呼叫 [**EapPeerEndSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) 以結束驗證會話。</span><span class="sxs-lookup"><span data-stu-id="96cad-122">Calls [**EapPeerEndSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) to end the authentication session.</span></span>
-   <span data-ttu-id="96cad-123">呼叫 [**EapPeerShutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown) 以卸載對等方法 DLL。</span><span class="sxs-lookup"><span data-stu-id="96cad-123">Calls [**EapPeerShutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown) to unload the peer method DLL.</span></span>
-   <span data-ttu-id="96cad-124">卸載 EAP 方法程式庫。</span><span class="sxs-lookup"><span data-stu-id="96cad-124">Unloads the EAP Method Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96cad-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="96cad-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96cad-126">要求者 API 呼叫順序</span><span class="sxs-lookup"><span data-stu-id="96cad-126">Supplicant API Call Sequence</span></span>](supplicant-api-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="96cad-127">驗證者方法 API 呼叫順序</span><span class="sxs-lookup"><span data-stu-id="96cad-127">Authenticator Method API Call Sequence</span></span>](authenticator-method-api-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="96cad-128">EAPHost 呼叫順序</span><span class="sxs-lookup"><span data-stu-id="96cad-128">EAPHost Call Sequences</span></span>](about-eaphost-call-sequences.md)
</dt> </dl>

 

 





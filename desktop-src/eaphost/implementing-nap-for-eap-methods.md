---
title: 為 EAP 方法執行 NAP 支援
description: 瞭解如何為 EAPHost 要求者實行 NAP 支援。 請參閱 EAPHost 相關的 NAP 主題，並查看其他可用的資源。
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e5f0bc8900ee3d9cb01edb79b64b8ef5a68df4c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "104024365"
---
# <a name="implementing-nap-support-for-eap-methods"></a><span data-ttu-id="75602-104">為 EAP 方法執行 NAP 支援</span><span class="sxs-lookup"><span data-stu-id="75602-104">Implementing NAP Support for EAP Methods</span></span>

<span data-ttu-id="75602-105">本主題說明如何為 EAPHost 要求者執行 NAP。</span><span class="sxs-lookup"><span data-stu-id="75602-105">This topic explains how to implement NAP for an EAPHost supplicant.</span></span> <span data-ttu-id="75602-106">在 Windows Vista 和 Windows Server 2008 中，NAP 強制用戶端 (NAP EC) 適用于 [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) 驗證連接。</span><span class="sxs-lookup"><span data-stu-id="75602-106">In Windows Vista and Windows Server 2008 a NAP Enforcement Client (NAP EC) is available for [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) authenticated connections.</span></span>

## <a name="implementing-network-access-protection-nap"></a><span data-ttu-id="75602-107"> (NAP) 執行網路存取保護</span><span class="sxs-lookup"><span data-stu-id="75602-107">Implementing Network Access Protection (NAP)</span></span>

<span data-ttu-id="75602-108">為了支援 NAP，EAPHost 要求者會執行符合 [**NotificationHandler**](/previous-versions/windows/desktop/api) 回呼原型的回呼函式，而且必須在呼叫 [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)時提供此回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="75602-108">To support NAP, an EAPHost supplicant implements a callback function matching the [**NotificationHandler**](/previous-versions/windows/desktop/api) callback prototype and must provide a pointer to this callback function when calling [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span></span>

<span data-ttu-id="75602-109">回呼函式會採用兩個參數。</span><span class="sxs-lookup"><span data-stu-id="75602-109">The callback function takes two parameters.</span></span>

-   <span data-ttu-id="75602-110">GUID，可唯一識別與驗證相關聯的介面。</span><span class="sxs-lookup"><span data-stu-id="75602-110">A GUID that uniquely identifies the interface associated with the authentication.</span></span>
-   <span data-ttu-id="75602-111">要求者所提供之不透明資料結構的 VOID 指標。</span><span class="sxs-lookup"><span data-stu-id="75602-111">A VOID pointer to an opaque data structure that is supplied by the supplicant.</span></span>

<span data-ttu-id="75602-112">當機器的隔離狀態變更時，EAPHost 會呼叫要求者提供的回呼函式，並搭配唯一的介面 GUID 和 VOID 指標。</span><span class="sxs-lookup"><span data-stu-id="75602-112">EAPHost will call the supplicant-provided callback function with the unique interface GUID and the VOID pointer when the quarantine state of the machine changes.</span></span> <span data-ttu-id="75602-113">當 EAPHost 呼叫要求者提供的回呼函式時，要求者會藉由卸載 interface GUID/VOID 指標所識別的邏輯網路連線，並使用 **EapHostPeerBeginSession** 再次開始驗證，來回應。</span><span class="sxs-lookup"><span data-stu-id="75602-113">When EAPHost calls the supplicant-provided callback function, the supplicant responds by tearing down the logical network connection identified by the interface GUID/VOID pointer and begins authentication again using **EapHostPeerBeginSession**.</span></span>

<span data-ttu-id="75602-114">EAPHost 可能會在任何時間呼叫要求者提供的回呼函式：在主動驗證期間，或在完成驗證之後 (在呼叫 [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) 之後，但在呼叫 [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) 之前未呼叫過，) 。</span><span class="sxs-lookup"><span data-stu-id="75602-114">EAPHost may call the supplicant-supplied callback function at any time: before, during an active authentication, or after the authentication has been completed (after [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) has been called but not before [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) has been called).</span></span> <span data-ttu-id="75602-115">要求者應該一律透過卸載邏輯網路連線並重新驗證，來回應。</span><span class="sxs-lookup"><span data-stu-id="75602-115">The supplicant should always respond by tearing down the logical network connection and re-authenticating.</span></span>

<span data-ttu-id="75602-116">如果要求者正在關閉或選擇不再收到隔離狀態變更的通知，要求者應該呼叫 [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) 並指定適當的介面 GUID。</span><span class="sxs-lookup"><span data-stu-id="75602-116">If the supplicant is shutting down or choosing to no longer receive notification of isolation state changes, the supplicant should call [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) and specify the appropriate interface GUID.</span></span> <span data-ttu-id="75602-117">如果要求者想要判斷邏輯網路連接的隔離，要求者可以從 [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult)取得 [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)時，從 **EapHostPeerMethodResult** 取得該資訊。</span><span class="sxs-lookup"><span data-stu-id="75602-117">If the supplicant wishes to determine the isolation of the logical network connection, the supplicant can obtain that information from **EapHostPeerMethodResult.isolationState** when the [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) is obtained from [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).</span></span>

## <a name="eaphost-related-nap-information"></a><span data-ttu-id="75602-118">EAPHost 相關的 NAP 資訊</span><span class="sxs-lookup"><span data-stu-id="75602-118">EAPHost Related NAP Information</span></span>

<span data-ttu-id="75602-119">如需 EAPHost API 相關 NAP 資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="75602-119">For EAPHost API related NAP information refer to the following topics.</span></span>

-   [<span data-ttu-id="75602-120">**EAP \_ 屬性 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="75602-120">**EAP\_ATTRIBUTE\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [<span data-ttu-id="75602-121">**EAP \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="75602-121">**EAP\_ERROR**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [<span data-ttu-id="75602-122">EAPHost 要求者的常見問題</span><span class="sxs-lookup"><span data-stu-id="75602-122">EAPHost Supplicant Frequently Asked Questions</span></span>](eaphost-supplicant-frequently-asked-questions.md)
-   [<span data-ttu-id="75602-123">**EAP 方法屬性**</span><span class="sxs-lookup"><span data-stu-id="75602-123">**EAP Method Properties**</span></span>](eap-method-properties.md)
-   [<span data-ttu-id="75602-124">**EapHostPeerBeginSession**</span><span class="sxs-lookup"><span data-stu-id="75602-124">**EapHostPeerBeginSession**</span></span>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [<span data-ttu-id="75602-125">**EAP 相關的錯誤和資訊常數**</span><span class="sxs-lookup"><span data-stu-id="75602-125">**EAP Related Error and Information Constants**</span></span>](eap-related-error-and-information-constants.md)
-   [<span data-ttu-id="75602-126">**隔離 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="75602-126">**ISOLATION\_STATE**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [<span data-ttu-id="75602-127">**NotificationHandler**</span><span class="sxs-lookup"><span data-stu-id="75602-127">**NotificationHandler**</span></span>](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a><span data-ttu-id="75602-128">其他資源</span><span class="sxs-lookup"><span data-stu-id="75602-128">Additional Resources</span></span>


-   <span data-ttu-id="75602-129">如需 NAP 資源的清單，請參閱 [網路存取保護](https://go.microsoft.com/fwlink/p/?linkid=84107)。</span><span class="sxs-lookup"><span data-stu-id="75602-129">For a list of NAP resources, see [Network Access Protection](https://go.microsoft.com/fwlink/p/?linkid=84107).</span></span>
-   <span data-ttu-id="75602-130">如需健康狀態資訊的聲明，請參閱「 [網路存取保護」 (NAP) 健康狀態聲明 (SoH) 訊息](https://go.microsoft.com/fwlink/p/?linkid=83918)。</span><span class="sxs-lookup"><span data-stu-id="75602-130">For Statement of Health information, see [Network Access Protection (NAP) Statement of Health (SoH) Messages](https://go.microsoft.com/fwlink/p/?linkid=83918).</span></span>
-   <span data-ttu-id="75602-131">如需商業網路群組網頁和 blog，請參閱 [網路存取保護 (NAP) ](https://go.microsoft.com/fwlink/p/?linkid=83845)。</span><span class="sxs-lookup"><span data-stu-id="75602-131">For the Enterprise Networking Group webpage and blog, see [Network Access Protection (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).</span></span>
-   <span data-ttu-id="75602-132">如需 NAP API 資訊，請參閱 [網路存取保護](/windows/desktop/NAP/network-access-protection-start-page)。</span><span class="sxs-lookup"><span data-stu-id="75602-132">For NAP API information, see [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page).</span></span>


## <a name="related-topics"></a><span data-ttu-id="75602-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="75602-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75602-134">設定 EAP 方法消費者介面</span><span class="sxs-lookup"><span data-stu-id="75602-134">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="75602-135">啟用群組原則</span><span class="sxs-lookup"><span data-stu-id="75602-135">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="75602-136">為 EAP 方法執行 In-Band NAP 支援</span><span class="sxs-lookup"><span data-stu-id="75602-136">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="75602-137">在要求者和 EAP 方法之間傳送資料</span><span class="sxs-lookup"><span data-stu-id="75602-137">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="75602-138">EAPHost 要求者</span><span class="sxs-lookup"><span data-stu-id="75602-138">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 
---
title: SSO EAPHost 案例總覽
description: 包含兩種案例，示範單一登入 (SSO) 已啟用要求者的優點。
ms.assetid: 2a5cbcae-74fe-4241-9e20-ec1ec5d9ed8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975310489758e299d1100584551296476c4690ca
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104092475"
---
# <a name="sso-eaphost-scenario-overview"></a><span data-ttu-id="29f1c-103">SSO EAPHost 案例總覽</span><span class="sxs-lookup"><span data-stu-id="29f1c-103">SSO EAPHost Scenario Overview</span></span>

<span data-ttu-id="29f1c-104">下列主題包含兩個案例，示範單一登入 (SSO) 已啟用要求者的優點。</span><span class="sxs-lookup"><span data-stu-id="29f1c-104">The following topic contains two scenarios that demonstrate the advantages of a Single-Sign-On (SSO) enabled supplicant.</span></span>

## <a name="about-the-scenarios"></a><span data-ttu-id="29f1c-105">關於案例</span><span class="sxs-lookup"><span data-stu-id="29f1c-105">About the Scenarios</span></span>

<span data-ttu-id="29f1c-106">SSO 提供的功能可保留比傳統儲存在 EAP 使用者 BLOB 中更多的使用者認證資訊。</span><span class="sxs-lookup"><span data-stu-id="29f1c-106">SSO provides functionality to retain additional user credential information than is traditionally stored in the EAP user BLOB.</span></span> <span data-ttu-id="29f1c-107">與其他認證程式不同的是，啟用 SSO 的要求者可以解決登入情況（例如 AP 漫遊）和密碼變更，而不需要使用者介入。</span><span class="sxs-lookup"><span data-stu-id="29f1c-107">Unlike other credential processes, SSO-enabled supplicants can resolve login situations like AP roaming, and password change without user intervention.</span></span>

## <a name="sso-eap-tls-pin-caching-behavior"></a><span data-ttu-id="29f1c-108">SSO EAP-TLS PIN 快取行為</span><span class="sxs-lookup"><span data-stu-id="29f1c-108">SSO EAP-TLS PIN Caching Behavior</span></span>

<span data-ttu-id="29f1c-109">要求者可以使用以智慧卡為基礎的 EAP 方法（例如可延伸的驗證通訊協定傳輸層安全性 (EAP-TLS) ）來嘗試進行網路驗證。</span><span class="sxs-lookup"><span data-stu-id="29f1c-109">A supplicant can attempt network authentication using a smartcard-based EAP method such as Extensible Authentication Protocol Transport Layer Security (EAP-TLS).</span></span> <span data-ttu-id="29f1c-110">在這種與類似的案例中，要求者會取得使用者的智慧卡 PIN，並取得使用者憑證以進行網路驗證，接著再呼叫本機電腦上的 WinLogin。</span><span class="sxs-lookup"><span data-stu-id="29f1c-110">In this and similar scenarios, the supplicant obtains the smartcard PIN from the user and retrieves a user certificate for network authentication followed by a call to WinLogin on the local computer.</span></span> <span data-ttu-id="29f1c-111">成功驗證之後，要求者會快取使用者 BLOB，而且不會儲存使用者 PIN 資訊。</span><span class="sxs-lookup"><span data-stu-id="29f1c-111">After successful authentication the supplicant caches the user BLOB, and does not store user PIN information.</span></span>

<span data-ttu-id="29f1c-112">當使用者漫遊到不同的位置會話繼續時，就必須重新驗證。</span><span class="sxs-lookup"><span data-stu-id="29f1c-112">When the user roams to a different location session resumption and re-authentication must occur.</span></span> <span data-ttu-id="29f1c-113">由於憑證無法儲存預先登入，使用者驗證將會失敗，而要求者會排清使用者 BLOB。</span><span class="sxs-lookup"><span data-stu-id="29f1c-113">Since the certificate cannot be stored pre-logon, the user authentication will fail and the supplicant flushes the user BLOB.</span></span> <span data-ttu-id="29f1c-114">此時需要使用者 PIN 才能從智慧卡取出使用者憑證，以進行網路驗證。</span><span class="sxs-lookup"><span data-stu-id="29f1c-114">At this point the user PIN is required to retrieve the user certificate from the smartcard for network authentication.</span></span> <span data-ttu-id="29f1c-115">因為 SSO 會快取 PIN，所以不需要使用者介入即可取出憑證。</span><span class="sxs-lookup"><span data-stu-id="29f1c-115">Because SSO caches the PIN, the certificate can be retrieved without user intervention.</span></span> <span data-ttu-id="29f1c-116">如果沒有 SSO，EAP-TLS 就必須再次引發 PIN 集合 UI。</span><span class="sxs-lookup"><span data-stu-id="29f1c-116">Without SSO, EAP-TLS would have to raise a PIN collection UI again.</span></span>

<span data-ttu-id="29f1c-117">如需逐步方法，請參閱 [SSO EAP-TLS PIN](sso-eap-tls-pin-caching-behavior-.md)快取行為。</span><span class="sxs-lookup"><span data-stu-id="29f1c-117">For a step-by-step approach, see [SSO EAP-TLS PIN Caching Behavior](sso-eap-tls-pin-caching-behavior-.md).</span></span>

## <a name="sso-password-change-behavior"></a><span data-ttu-id="29f1c-118">SSO 密碼變更行為</span><span class="sxs-lookup"><span data-stu-id="29f1c-118">SSO Password Change Behavior</span></span>

<span data-ttu-id="29f1c-119">要求者可以使用以密碼為基礎的 EAP 方法（例如 Microsoft 挑戰交握驗證通訊協定2.0 版 (CHAPv2) ，設定為使用 WinLogin 認證）來嘗試網路驗證。</span><span class="sxs-lookup"><span data-stu-id="29f1c-119">A supplicant can attempt network authentication using a password-based EAP method such as Microsoft Challenge Handshake Authentication Protocol version 2.0 (MS-CHAPv2), configured to use WinLogin credentials.</span></span> <span data-ttu-id="29f1c-120">在此案例中，要求者會收集一次使用者認證，並將其提供給 EAPHost 進行網路驗證。</span><span class="sxs-lookup"><span data-stu-id="29f1c-120">In this scenario, the supplicant collects user credentials once and provides them to EAPHost for network authentication.</span></span> <span data-ttu-id="29f1c-121">成功驗證網路之後，要求者會針對 WinLogin 使用同一組認證。</span><span class="sxs-lookup"><span data-stu-id="29f1c-121">After successful network authentication the supplicant uses the same set of credentials for WinLogin.</span></span>

<span data-ttu-id="29f1c-122">但是，如果在未啟用 SSO 的要求者的網路驗證期間變更了使用者密碼等認證，後續的 WinLogin 呼叫將會導致失敗。</span><span class="sxs-lookup"><span data-stu-id="29f1c-122">However, if credentials such as the user password were changed during network authentication without an SSO-enabled supplicant, the subsequent WinLogin call will result in failure.</span></span> <span data-ttu-id="29f1c-123">SSO 會保留新的認證，並允許成功的 WinLogin，而不需要額外的使用者介入。</span><span class="sxs-lookup"><span data-stu-id="29f1c-123">SSO retains the new credentials and allows a successful WinLogin without additional user intervention.</span></span>

<span data-ttu-id="29f1c-124">如需逐步方法，請參閱 [SSO 密碼變更行為](sso-password-change-behavior-.md)。</span><span class="sxs-lookup"><span data-stu-id="29f1c-124">For a step-by-step approach, see [SSO Password Change Behavior](sso-password-change-behavior-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="29f1c-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="29f1c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29f1c-126">SSO 和 PLAP</span><span class="sxs-lookup"><span data-stu-id="29f1c-126">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 





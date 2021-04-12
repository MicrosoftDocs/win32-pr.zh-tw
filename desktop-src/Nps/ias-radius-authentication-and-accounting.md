---
title: RADIUS 驗證、授權和帳戶處理
description: NPS 完全支援 (RADIUS) 通訊協定遠端驗證撥入消費者服務。 RADIUS 通訊協定是遠端使用者驗證的標準標準，並記載于 RFC 2865 和 RFC 2866 中。
ms.assetid: 3e00d555-355c-4a4c-a389-ab44e9ed9ca9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cce45bbc6e4802ed5137849a5b22520c8a4badbb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376068"
---
# <a name="radius-authentication-authorization-and-accounting"></a><span data-ttu-id="61cdd-104">RADIUS 驗證、授權和帳戶處理</span><span class="sxs-lookup"><span data-stu-id="61cdd-104">RADIUS Authentication, Authorization, and Accounting</span></span>

> [!Note]  
> <span data-ttu-id="61cdd-105">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="61cdd-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="61cdd-106">本主題的內容適用于 IAS 和 NPS。</span><span class="sxs-lookup"><span data-stu-id="61cdd-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="61cdd-107">在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。</span><span class="sxs-lookup"><span data-stu-id="61cdd-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="61cdd-108">NPS 完全支援 (RADIUS) 通訊協定遠端驗證撥入消費者服務。</span><span class="sxs-lookup"><span data-stu-id="61cdd-108">NPS fully supports the Remote Authentication Dial-In User Service (RADIUS) protocol.</span></span> <span data-ttu-id="61cdd-109">RADIUS 通訊協定是遠端使用者驗證的標準標準，並記載于 [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) 和 [rfc 2866](https://www.ietf.org/rfc/rfc2866.txt)中。</span><span class="sxs-lookup"><span data-stu-id="61cdd-109">The RADIUS protocol is the de facto standard for remote user authentication and it is documented in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) and [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

## <a name="radius-authentication-and-authorization"></a><span data-ttu-id="61cdd-110">RADIUS 驗證與授權</span><span class="sxs-lookup"><span data-stu-id="61cdd-110">RADIUS Authentication and Authorization</span></span>

<span data-ttu-id="61cdd-111">下圖顯示驗證用戶端 ( 「使用者」 ) 使用點對點通訊協定 (PPP)  (PPP) ，透過撥號連線 (NAS) 連接到網路存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="61cdd-111">The following diagram shows an authenticating client ("User") connecting to a Network Access Server (NAS) over a dial-up connection, using the Point-to-Point Protocol (PPP).</span></span> <span data-ttu-id="61cdd-112">為了驗證使用者，NAS 會與執行 NPS 的遠端伺服器聯繫。</span><span class="sxs-lookup"><span data-stu-id="61cdd-112">In order to authenticate the User, the NAS contacts a remote server running NPS.</span></span> <span data-ttu-id="61cdd-113">NAS 和 NPS 伺服器使用 RADIUS 通訊協定進行通訊。</span><span class="sxs-lookup"><span data-stu-id="61cdd-113">The NAS and the NPS server communicate using the RADIUS protocol.</span></span>

![遠端使用者驗證](images/ias01.png)

<span data-ttu-id="61cdd-115">NAS 會以支援 RADIUS 通訊協定的伺服器或伺服器用戶端的形式運作。</span><span class="sxs-lookup"><span data-stu-id="61cdd-115">A NAS operates as a client of a server or servers that support the RADIUS protocol.</span></span> <span data-ttu-id="61cdd-116">支援 RADIUS 通訊協定的伺服器通常稱為 RADIUS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="61cdd-116">Servers that support the RADIUS protocol are generally referred to as the RADIUS servers.</span></span> <span data-ttu-id="61cdd-117">RADIUS 用戶端（也就是 NAS）會將使用者的相關資訊傳遞給指定的 RADIUS 伺服器，然後對伺服器傳回的回應採取行動。</span><span class="sxs-lookup"><span data-stu-id="61cdd-117">The RADIUS client, that is, the NAS, passes information about the User to designated RADIUS servers, and then acts on the response that the servers return.</span></span> <span data-ttu-id="61cdd-118">由 NAS 傳送至 RADIUS 伺服器以驗證使用者的要求通常稱為「驗證要求」。</span><span class="sxs-lookup"><span data-stu-id="61cdd-118">The request sent by the NAS to the RADIUS server in order to authenticate the User is generally called an "authentication request."</span></span>

<span data-ttu-id="61cdd-119">如果 RADIUS 伺服器成功驗證使用者，RADIUS 伺服器會將設定資訊傳回到 NAS，讓它可以為使用者提供網路服務。</span><span class="sxs-lookup"><span data-stu-id="61cdd-119">If a RADIUS server authenticates the User successfully, the RADIUS server returns configuration information to the NAS so that it can provide network service to the user.</span></span> <span data-ttu-id="61cdd-120">這項設定資訊是由「授權」所組成，其中包含了 NAS 可能提供給使用者 (例如 PPP 或 telnet) 的服務類型。</span><span class="sxs-lookup"><span data-stu-id="61cdd-120">This configuration information is composed of "authorizations" and contains, among others, the type of service NAS may provide to the User (for example, PPP, or telnet).</span></span>

<span data-ttu-id="61cdd-121">當 RADIUS 伺服器正在處理驗證要求時，它可以執行授權功能，例如驗證使用者的電話號碼，以及檢查使用者是否已經有進行中的會話。</span><span class="sxs-lookup"><span data-stu-id="61cdd-121">While the RADIUS server is processing the authentication request, it can perform authorization functions such as verifying the user's telephone number and checking whether the user already has a session in progress.</span></span> <span data-ttu-id="61cdd-122">RADIUS 伺服器可以藉由聯絡狀態伺服器，判斷使用者是否已經有進行中的會話。</span><span class="sxs-lookup"><span data-stu-id="61cdd-122">The RADIUS server can determine whether the user already has a session in progress by contacting a state server.</span></span>

<span data-ttu-id="61cdd-123">如需 RADIUS 驗證和授權的詳細資訊，請參閱 [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt)。</span><span class="sxs-lookup"><span data-stu-id="61cdd-123">For more information on RADIUS authentication and authorization, see [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).</span></span>

## <a name="radius-accounting"></a><span data-ttu-id="61cdd-124">RADIUS 帳戶處理</span><span class="sxs-lookup"><span data-stu-id="61cdd-124">RADIUS Accounting</span></span>

<span data-ttu-id="61cdd-125">RADIUS 伺服器也會收集 NAS 所傳送的各種資訊，這些資訊可用於帳戶處理和報告網路活動。</span><span class="sxs-lookup"><span data-stu-id="61cdd-125">The RADIUS server also collects a variety of information sent by the NAS that can be used for accounting and for reporting on network activity.</span></span> <span data-ttu-id="61cdd-126">當使用者登入和登出時，RADIUS 用戶端會將資訊傳送給指定的 RADIUS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="61cdd-126">The RADIUS client sends information to designated RADIUS servers when the User logs on and logs off.</span></span> <span data-ttu-id="61cdd-127">RADIUS 用戶端可能會在會話進行時定期傳送額外的使用量資訊。</span><span class="sxs-lookup"><span data-stu-id="61cdd-127">The RADIUS client may send additional usage information on a periodic basis while the session is in progress.</span></span> <span data-ttu-id="61cdd-128">用戶端傳送到伺服器以記錄登入/登出和使用資訊的要求通常稱為「會計要求」。</span><span class="sxs-lookup"><span data-stu-id="61cdd-128">The requests sent by the client to the server to record logon/logoff and usage information are generally called "accounting requests."</span></span>

<span data-ttu-id="61cdd-129">如需 RADIUS 帳戶處理的詳細資訊，請參閱 [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)。</span><span class="sxs-lookup"><span data-stu-id="61cdd-129">For more information on RADIUS accounting, see [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

## <a name="radius-proxy"></a><span data-ttu-id="61cdd-130">RADIUS Proxy</span><span class="sxs-lookup"><span data-stu-id="61cdd-130">RADIUS Proxy</span></span>

<span data-ttu-id="61cdd-131">RADIUS 伺服器可作為其他 RADIUS 伺服器的 proxy 用戶端。</span><span class="sxs-lookup"><span data-stu-id="61cdd-131">A RADIUS server can act as a proxy client to other RADIUS servers.</span></span> <span data-ttu-id="61cdd-132">在這些情況下，NAS 所聯繫的 RADIUS 伺服器會將驗證或帳戶處理要求傳遞至另一個實際執行驗證或帳戶處理工作的 RADIUS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="61cdd-132">In these cases, the RADIUS server contacted by the NAS passes the authentication or accounting request to another RADIUS server that actually performs the authentication or the accounting task.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61cdd-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="61cdd-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61cdd-134">網際網路驗證服務和網路原則伺服器</span><span class="sxs-lookup"><span data-stu-id="61cdd-134">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="61cdd-135">RADIUS 帳戶處理封包</span><span class="sxs-lookup"><span data-stu-id="61cdd-135">RADIUS Accounting Packets</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="61cdd-136">使用狀態伺服器</span><span class="sxs-lookup"><span data-stu-id="61cdd-136">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

 
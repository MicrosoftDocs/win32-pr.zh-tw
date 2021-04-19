---
description: 對等名稱解析通訊協定會使用對等名稱解析通訊協定 (PNRP) 、對等身分識別管理員以及對等群組基礎結構。
ms.assetid: b0d78b17-6f48-4294-b8a2-8fcc1a7f8ef1
title: 對等名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18774939d5e0e9bad208999fbc6ca1e5f624300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000123"
---
# <a name="peer-names"></a><span data-ttu-id="cd86e-103">對等名稱</span><span class="sxs-lookup"><span data-stu-id="cd86e-103">Peer Names</span></span>

<span data-ttu-id="cd86e-104">對等名稱解析通訊協定會使用對等名稱解析通訊協定 (PNRP) 、對等身分識別管理員以及對等群組基礎結構。</span><span class="sxs-lookup"><span data-stu-id="cd86e-104">Peer names are used by Peer Name Resolution Protocol (PNRP), the Peer Identity Manager, and the Peer Grouping Infrastructure.</span></span> <span data-ttu-id="cd86e-105">對等名稱是資源的穩定名稱，例如電腦、使用者、群組或服務。</span><span class="sxs-lookup"><span data-stu-id="cd86e-105">Peer names are stable names for resources such as computers, users, groups, or services.</span></span> <span data-ttu-id="cd86e-106">PNRP 會使用對等名稱來識別對等網路中的節點。</span><span class="sxs-lookup"><span data-stu-id="cd86e-106">PNRP uses peer names to identify nodes in a peer network.</span></span>

> [!Note]  
> <span data-ttu-id="cd86e-107">對等基礎結構所使用的端點實際上是包含 IPv4 或 IPv6 位址、埠和通訊協定 (TCP 或 UDP) 的元組。</span><span class="sxs-lookup"><span data-stu-id="cd86e-107">An endpoint that the Peer Infrastructure uses is actually a tuple that consists of an IPv4 or IPv6 address, port, and protocol (either TCP or UDP).</span></span> <span data-ttu-id="cd86e-108">一個對等名稱可以有一個以上的元組。</span><span class="sxs-lookup"><span data-stu-id="cd86e-108">One peer name can have more than one tuple.</span></span>

 

<span data-ttu-id="cd86e-109">對等名稱是具有下列格式的文字字串：</span><span class="sxs-lookup"><span data-stu-id="cd86e-109">A peer name is a text string that has the following format:</span></span>

-   <span data-ttu-id="cd86e-110">「授權單位。分類器」</span><span class="sxs-lookup"><span data-stu-id="cd86e-110">"Authority.Classifier"</span></span>

<span data-ttu-id="cd86e-111">授權單位的值取決於名稱是安全的還是不安全的。</span><span class="sxs-lookup"><span data-stu-id="cd86e-111">The value of an Authority depends on whether the name is secure or unsecured.</span></span> <span data-ttu-id="cd86e-112">對等名稱的分類器是字串。</span><span class="sxs-lookup"><span data-stu-id="cd86e-112">The Classifier of a peer name is a string.</span></span> <span data-ttu-id="cd86e-113">分類器可以是包含150或更少 UNICODE 字元的任何名稱。</span><span class="sxs-lookup"><span data-stu-id="cd86e-113">A Classifier can be any name that contains 150 or less UNICODE characters.</span></span> <span data-ttu-id="cd86e-114">對等名稱會區分大小寫，而且可以註冊為安全或不安全的。</span><span class="sxs-lookup"><span data-stu-id="cd86e-114">Peer names are case-sensitive and can be registered as secured or unsecured.</span></span> <span data-ttu-id="cd86e-115">下列清單會識別對等名稱的一些範例：</span><span class="sxs-lookup"><span data-stu-id="cd86e-115">The following list identifies some examples of peer names:</span></span>

-   <span data-ttu-id="cd86e-116">"0. MyUnsecuredPeerName"</span><span class="sxs-lookup"><span data-stu-id="cd86e-116">"0.MyUnsecuredPeerName"</span></span>
-   <span data-ttu-id="cd86e-117">"0. JohnDoe"</span><span class="sxs-lookup"><span data-stu-id="cd86e-117">"0.JohnDoe.Games"</span></span>
-   <span data-ttu-id="cd86e-118">"6520c005f63fc1864b7d8f3cabebd4916ae7f33d.JohnDoe</span><span class="sxs-lookup"><span data-stu-id="cd86e-118">"6520c005f63fc1864b7d8f3cabebd4916ae7f33d.JohnDoe"</span></span>

## <a name="secure-peer-names"></a><span data-ttu-id="cd86e-119">安全對等名稱</span><span class="sxs-lookup"><span data-stu-id="cd86e-119">Secure Peer Names</span></span>

<span data-ttu-id="cd86e-120">若為安全名稱，授權單位為安全雜湊演算法 (SHA) 對等名稱公開金鑰的雜湊，並產生40個字元的十六進位字串。</span><span class="sxs-lookup"><span data-stu-id="cd86e-120">For a secure name, the Authority is the Secure Hash Algorithm (SHA) hash of the public key of the peer name, and results in a 40 character hexadecimal string.</span></span> <span data-ttu-id="cd86e-121">安全的對等名稱只能透過對等名稱擁有者的擁有者或委派向 PNRP 註冊。</span><span class="sxs-lookup"><span data-stu-id="cd86e-121">A secure peer name can only be registered with PNRP by the owner or delegate of the peer name owner.</span></span> <span data-ttu-id="cd86e-122">您必須藉由呼叫 [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)來建立安全的對等名稱。</span><span class="sxs-lookup"><span data-stu-id="cd86e-122">A secured peer name must be created by calling [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).</span></span>

## <a name="unsecured-peer-names"></a><span data-ttu-id="cd86e-123">不安全的對等名稱</span><span class="sxs-lookup"><span data-stu-id="cd86e-123">Unsecured Peer Names</span></span>

<span data-ttu-id="cd86e-124">若為不安全的名稱，授權單位為零 (0) ，而且分類器是對等名稱的唯一重要部分，這會在沒有相關聯的身分 [識別](identity-manager-api.md)的情況下建立不安全的對等名稱。</span><span class="sxs-lookup"><span data-stu-id="cd86e-124">For an unsecured name, the Authority is zero (0), and the Classifier is the only significant part of the peer name, which creates an unsecured peer name without an associated [identity](identity-manager-api.md).</span></span> <span data-ttu-id="cd86e-125">不安全的對等名稱是在 PNRP 名稱註冊和解析中使用。</span><span class="sxs-lookup"><span data-stu-id="cd86e-125">Unsecured peer names are used in PNRP name registration and resolution.</span></span> <span data-ttu-id="cd86e-126">不安全的對等名稱提供了一種實用的方法，可用來註冊及解析不需要安全名稱解析的資源。</span><span class="sxs-lookup"><span data-stu-id="cd86e-126">Unsecured peer names provide a useful way to register and resolve resources that do not require secure name resolution.</span></span> <span data-ttu-id="cd86e-127">不過，任何節點都可以發佈任何不安全的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd86e-127">However, any node can publish any unsecured name.</span></span> <span data-ttu-id="cd86e-128">關心安全性的應用程式必須確保它們在取用不安全的對等名稱時是穩固且安全的。</span><span class="sxs-lookup"><span data-stu-id="cd86e-128">Applications concerned with security must ensure that they are robust and secure in their consumption of unsecured peer names.</span></span>

> [!Note]  
> <span data-ttu-id="cd86e-129">任何人都可以使用 PNRP 註冊不安全的對等名稱。</span><span class="sxs-lookup"><span data-stu-id="cd86e-129">Anyone can register an unsecured peer name with PNRP.</span></span>

 

## <a name="pnrp-and-the-nearest-peer-name-instance"></a><span data-ttu-id="cd86e-130">PNRP 和最接近的對等名稱實例</span><span class="sxs-lookup"><span data-stu-id="cd86e-130">PNRP and the Nearest Peer Name Instance</span></span>

<span data-ttu-id="cd86e-131">對等名稱可以有一個以上的實例。</span><span class="sxs-lookup"><span data-stu-id="cd86e-131">There can be more than one instance of a peer name.</span></span> <span data-ttu-id="cd86e-132">使用 [PNRP](pnrp-namespace-provider-api.md)解析對等名稱時，會有 **最接近** 的對等名稱實例的概念，表示名稱的服務位置最接近 [**PNRPINFO \_ V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)或 [**PNRPINFO \_ V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))中指定的 **saHint** 成員。</span><span class="sxs-lookup"><span data-stu-id="cd86e-132">When using [PNRP](pnrp-namespace-provider-api.md) to resolve a peer name, there is a concept of a **nearest** peer name instance, which means that the name has a service location closest to the **saHint** member specified in [**PNRPINFO\_V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) or [**PNRPINFO\_V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85)).</span></span> <span data-ttu-id="cd86e-133">如果未提供任何提示，則最接近其中一個本機 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="cd86e-133">If no hint is supplied, closest to one of the local IP addresses.</span></span>

 

 

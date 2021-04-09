---
description: 對等群組需要每個成員都有特定的憑證，稱為群組成員憑證 (GMC) 。
ms.assetid: 3966d4eb-4504-4b1e-9c9f-6eab7751d7ed
title: 群組安全性的運作方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d272e9a0567c6edc300a52cfa206305253ec5a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849309"
---
# <a name="how-group-security-works"></a><span data-ttu-id="7a53b-103">群組安全性的運作方式</span><span class="sxs-lookup"><span data-stu-id="7a53b-103">How Group Security Works</span></span>

<span data-ttu-id="7a53b-104">對等群組需要每個成員都有特定的憑證，稱為群組成員憑證 (GMC) 。</span><span class="sxs-lookup"><span data-stu-id="7a53b-104">Peer groups require that each member have a specific certificate, which is called a Group Member Certificate (GMC).</span></span> <span data-ttu-id="7a53b-105">GMC 憑證可確保對等之間交換的所有記錄都經過數位簽署。</span><span class="sxs-lookup"><span data-stu-id="7a53b-105">The GMC certificate ensures that all records exchanged between peers are digitally signed.</span></span> <span data-ttu-id="7a53b-106">對等的公開金鑰會包含在傳遞的結構中，這些結構會在對等之間進行通訊時傳遞，包括 [**對等 \_ 認證 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info)。</span><span class="sxs-lookup"><span data-stu-id="7a53b-106">The public key of a peer is contained in the structures that are passed as part of the communication between peers—including [**PEER\_CREDENTIAL\_INFO**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info).</span></span>

<span data-ttu-id="7a53b-107">GMC 可以在鏈中發出。</span><span class="sxs-lookup"><span data-stu-id="7a53b-107">A GMC can be issued in a chain.</span></span> <span data-ttu-id="7a53b-108">例如，建立者可以發出 GMC 給系統管理員 A，讓誰可以向系統管理員 B 發出 GMC，他們可以將 GMC 發給成員 M。產生的 GMC 鏈是： creator->A->B->M，其長度為4。</span><span class="sxs-lookup"><span data-stu-id="7a53b-108">For example, a creator can issue a GMC to administrator A, who can issue a GMC to administrator B, who can issue a GMC to member M. The resulting GMC chain is: creator->A->B->M, which has a length of 4.</span></span> <span data-ttu-id="7a53b-109">連鎖長度很重要，因為它的長度不能超過24。</span><span class="sxs-lookup"><span data-stu-id="7a53b-109">The chain length is important, because it cannot be longer than 24.</span></span> <span data-ttu-id="7a53b-110">如果鏈中的24日系統管理員嘗試將 GMC 發給成員， [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) 或 [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) 會傳回對等 \_ E \_ 鏈 \_ 太長的 \_ 時間。</span><span class="sxs-lookup"><span data-stu-id="7a53b-110">If the 24th administrator in a chain attempts to issue a GMC to a member, [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) or [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) returns PEER\_E\_CHAIN\_TOO\_LONG.</span></span>

<span data-ttu-id="7a53b-111">GMC 也可以藉由呼叫 [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)來發出。</span><span class="sxs-lookup"><span data-stu-id="7a53b-111">A GMC can also be issued by calling [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials).</span></span> <span data-ttu-id="7a53b-112">GMC 意指 GMC 發出的群組中的使用者成員資格，而且可以有有限或無限的存留期。</span><span class="sxs-lookup"><span data-stu-id="7a53b-112">A GMC implies user membership in the group that the GMC is issued for, and can have a finite or infinite lifetime.</span></span> <span data-ttu-id="7a53b-113">群組成員活動的長度不能超過 GMC 中指定的存留期。</span><span class="sxs-lookup"><span data-stu-id="7a53b-113">Group member activity cannot be longer than the lifetime specified in the GMC.</span></span>

> [!Note]  
> <span data-ttu-id="7a53b-114">無限 GMC 存留期目前設定為1000年。</span><span class="sxs-lookup"><span data-stu-id="7a53b-114">Infinite GMC lifetime is currently set at 1000 years.</span></span>

 

<span data-ttu-id="7a53b-115">群組成員活動會受限於 GMC 存留期，並包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="7a53b-115">Group member activity is limited by the GMC lifetime and includes the following:</span></span>

-   <span data-ttu-id="7a53b-116">**記錄作業** ：當群組成員資格到期之後，對等無法在群組中發行資訊，或發行存留期超過對等群組成員資格存留期的記錄。</span><span class="sxs-lookup"><span data-stu-id="7a53b-116">**Record operations** - A peer cannot publish information in a group after the group membership expires, or publish records that have a lifetime longer than the peer's group membership lifetime.</span></span>
-   <span data-ttu-id="7a53b-117">**成員資格作業** -群組系統管理員無法發行存留期超過群組管理員成員資格中指定之日期的成員資格。</span><span class="sxs-lookup"><span data-stu-id="7a53b-117">**Membership operations** - A group administrator cannot issue a membership that has a lifetime beyond the date specified in the group administrator membership.</span></span> <span data-ttu-id="7a53b-118">例如，如果系統管理員在其 GMC 存留期內剩餘500小時，則所有發行的成員資格都必須小於500小時。</span><span class="sxs-lookup"><span data-stu-id="7a53b-118">For example, if an administrator has 500 hours remaining on its GMC lifetime, all memberships issued must be less than 500 hours.</span></span>

<span data-ttu-id="7a53b-119">因為群組成員的存留期不能超過邀請該群組成員的系統管理員，建議您將系統管理員的 GMC 存留期設為無限期，或設定為很長的存留期。</span><span class="sxs-lookup"><span data-stu-id="7a53b-119">Because a group member cannot have a lifetime longer than the administrator who invites that group member, it is recommended that you set the GMC lifetime of an administrator as infinite, or for a very long lifetime.</span></span> <span data-ttu-id="7a53b-120">群組建立者預設為無限存留期。</span><span class="sxs-lookup"><span data-stu-id="7a53b-120">The group creator has an infinite lifetime by default.</span></span>

## <a name="renewing-group-membership"></a><span data-ttu-id="7a53b-121">更新群組成員資格</span><span class="sxs-lookup"><span data-stu-id="7a53b-121">Renewing Group Membership</span></span>

<span data-ttu-id="7a53b-122">若要更新 GMC 存留期已準備好到期的系統管理員或成員的認證，您有下列兩個選項：</span><span class="sxs-lookup"><span data-stu-id="7a53b-122">To renew the credentials of an administrator or member whose GMC lifetime is ready to expire, you have the following two options:</span></span>

-   <span data-ttu-id="7a53b-123">呼叫 [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) 並傳遞其存留期已準備好到期的成員身分識別。</span><span class="sxs-lookup"><span data-stu-id="7a53b-123">Call [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) and pass the identity of the member whose lifetime is ready to expire.</span></span> <span data-ttu-id="7a53b-124">如果認證已指定為 **Null** ，且對等的成員資格資訊可供群組使用，則會將更新時間設定為先前發佈的成員認證中所指定的相同持續時間。</span><span class="sxs-lookup"><span data-stu-id="7a53b-124">If the credentials are specified as **NULL** and the peer's membership information is available to the group, the renewal time is set to the same duration that is specified in the previously published member credentials.</span></span> <span data-ttu-id="7a53b-125">如果必須指定不同的持續期間，則必須提供新的 [**對等 \_ 認證 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) 結構，其中包含新的存留期持續時間，然後為該成員發行新的 GMC。</span><span class="sxs-lookup"><span data-stu-id="7a53b-125">If a different duration period must be specified, a new [**PEER\_CREDENTIAL\_INFO**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) structure must be provided that contains the new lifetime duration, and then a new GMC is published for the member.</span></span>

    <span data-ttu-id="7a53b-126">[**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)函式會選擇性地採用對等 \_ 群組 \_ 存放區 \_ 認證旗標，此旗標會自動發行群組資料庫中成員的新認證。</span><span class="sxs-lookup"><span data-stu-id="7a53b-126">The [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) function optionally takes the PEER\_GROUP\_STORE\_CREDENTIALS flag, which automatically publishes the new credentials of the member in the group database.</span></span> <span data-ttu-id="7a53b-127">當成員下次連接到群組時，在第一次或離線之後，成員會從資料庫取得更新的 GMC。</span><span class="sxs-lookup"><span data-stu-id="7a53b-127">When the member connects to the group the next time, for either the first time or after going offline, the member obtains the updated GMC from the database.</span></span>

-   <span data-ttu-id="7a53b-128">呼叫 [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) ，以傳遞 GMC 存留期已就緒即將到期之成員的身分識別。</span><span class="sxs-lookup"><span data-stu-id="7a53b-128">Call [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) to pass the identity of the member whose GMC lifetime is ready to expire.</span></span> <span data-ttu-id="7a53b-129">如果邀請中指定的到期日為 **Null**，則 GMC 的存留期間會與發出成員資格的系統管理員 GMC 相同。</span><span class="sxs-lookup"><span data-stu-id="7a53b-129">If the expiration specified in the invitation is **NULL**, the lifetime duration of the GMC is the same as the administrator GMC who issues membership.</span></span> <span data-ttu-id="7a53b-130">如果建立者將到期指定為 **Null**，則會發出無限存留期的 GMC。</span><span class="sxs-lookup"><span data-stu-id="7a53b-130">If the creator specifies the expiration as **NULL**, a GMC with an infinite lifetime is issued.</span></span>

    <span data-ttu-id="7a53b-131">如果對等發出的 GMC 是在存在存留期值之前過期，則對等體的位址就無法在由 [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)呼叫所起始的列舉中傳回的 [**對等 \_ 成員**](/windows/desktop/api/P2P/ns-p2p-peer_member)結構中使用。</span><span class="sxs-lookup"><span data-stu-id="7a53b-131">If a peer is issued a GMC that expires before the presence lifetime value, the addresses of the peer are not available in the [**PEER\_MEMBER**](/windows/desktop/api/P2P/ns-p2p-peer_member) structures returned in the enumeration initiated by a call to [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers).</span></span> <span data-ttu-id="7a53b-132">發生這種情況是因為在此情況下，即使未設定對等 \_ 停用狀態旗標，也不會發佈存在性資訊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7a53b-132">This happens because presence information is not published in this case, even if the PEER\_DISABLE\_PRESENCE flag is not set.</span></span>

 

 




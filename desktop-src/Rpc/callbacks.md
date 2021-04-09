---
title: '回呼 (RPC) '
description: 程式設計模型通常會透過遠端程序呼叫（ (RPC) ，或用戶端呼叫不受信任的伺服器，來要求用戶端的伺服器回呼。 這會帶來許多潛在的陷阱。
ms.assetid: a4f3ea26-ac4b-41e5-abde-96b4baedf2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6260e2cff2cbaff86f210764e89d55859c4d33af
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024501"
---
# <a name="callbacks-rpc"></a><span data-ttu-id="1d7ce-104">回呼 (RPC) </span><span class="sxs-lookup"><span data-stu-id="1d7ce-104">Callbacks (RPC)</span></span>

<span data-ttu-id="1d7ce-105">程式設計模型通常會透過遠端程序呼叫（ (RPC) ，或用戶端呼叫不受信任的伺服器，來要求用戶端的伺服器回呼。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-105">Often the programming model necessitates a server callback to a client through a remote procedure call (RPC), or client calls into an untrusted server.</span></span> <span data-ttu-id="1d7ce-106">這會帶來許多潛在的陷阱。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-106">This introduces many potential pitfalls.</span></span>

<span data-ttu-id="1d7ce-107">首先，用戶端的回呼必須有足夠的低模擬層級。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-107">First, callback to the client must be made with a sufficiently low impersonation level.</span></span> <span data-ttu-id="1d7ce-108">如果伺服器是具有高度許可權的系統服務，則以模擬層級或更高版本回呼本機用戶端，可讓用戶端有足夠的許可權可以接管系統。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-108">If the server is a highly privileged system service, calling back a local client with an impersonation level of impersonate or higher can provide the client with privileges sufficient to take over the system.</span></span> <span data-ttu-id="1d7ce-109">以比所需更高的模擬等級回呼遠端用戶端，也會導致非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-109">Calling back a remote client with higher impersonation level than necessary can also lead to undesirable consequences.</span></span>

<span data-ttu-id="1d7ce-110">其次，如果攻擊者引發您的服務來執行回呼，它可以啟動所謂的 *黑色漏洞*—阻絕服務攻擊。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-110">Second, if an attacker induces your service to perform a callback, it can launch what is called a *black hole*—denial of service attack.</span></span> <span data-ttu-id="1d7ce-111">這類攻擊並不是 RPC 特有的，在這些攻擊中，電腦會導致您將流量傳送給它，但不會回應您的要求。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-111">Such attacks are not specific to RPC; in these attacks, a machine induces you to send traffic to it, but it does not respond to your requests.</span></span> <span data-ttu-id="1d7ce-112">您可以接收更多和更多資源來呼叫黑色孔，但永遠不會回來。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-112">You sink more and more resources into calling the black hole, but they never come back.</span></span> <span data-ttu-id="1d7ce-113">這類攻擊的一個一般範例是 TCP 層級的攻擊，稱為 TCP/IP SYN 洪水攻擊。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-113">One generic example of such an attack is a TCP-level attack called a TCP/IP SYN flood attack.</span></span>

<span data-ttu-id="1d7ce-114">在 RPC 層級上，當攻擊者呼叫介面，並且要求伺服器回呼介面時，就會發生簡單的黑色漏洞攻擊。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-114">On the RPC level, a simple black-hole attack occurs when an attacker calls an interface, and requests the server to call the interface back.</span></span> <span data-ttu-id="1d7ce-115">介面符合，但是攻擊者永遠不會傳回呼叫：伺服器上的一個執行緒已系結。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-115">The interface complies, but the attacker never returns the call: one thread on the server is tied up.</span></span> <span data-ttu-id="1d7ce-116">攻擊者會執行此100次，並在伺服器上系結100執行緒。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-116">The attacker does this 100 times, tying 100 threads on the server.</span></span> <span data-ttu-id="1d7ce-117">伺服器最後會用盡記憶體。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-117">Eventually the server runs out of memory.</span></span> <span data-ttu-id="1d7ce-118">伺服器的偵錯工具可能會顯示黑洞呼叫端的身分識別，但通常伺服器不會在可疑粗鄙 play 的情況下重新開機，或可能沒有足夠的專業知識可判斷攻擊者。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-118">Debugging the server can potentially reveal the identity of the black-hole caller, but often the server will be restarted without suspecting foul play, or there may not be enough expertise available to determine the attacker.</span></span>

<span data-ttu-id="1d7ce-119">第三個缺陷是在用戶端上。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-119">The third pitfall is on the client.</span></span> <span data-ttu-id="1d7ce-120">用戶端通常會呼叫伺服器，告知伺服器如何呼叫它 (通常是字串系結) ，然後等候伺服器的呼叫抵達，以盲目地接受該端點上的任何呼叫，而該端點上的宣告來自伺服器。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-120">Often a client makes a call to the server informing the server how to call it back (usually a string binding), and then waits for a call from the server to arrive, blindly accepting any call on that endpoint that claims to come from the server.</span></span> <span data-ttu-id="1d7ce-121">從伺服器到用戶端的回呼通訊協定應該包含一些驗證機制，以確保當回呼進入用戶端時，它實際上是源自伺服器。</span><span class="sxs-lookup"><span data-stu-id="1d7ce-121">The callback protocol from the server to the client should include some verification mechanism to ensure that when the callback comes to the client, it actually originated on the server.</span></span>

 

 





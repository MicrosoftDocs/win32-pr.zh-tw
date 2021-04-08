---
title: 執行分散式系統
description: 在分散式系統中執行軟體的其中一種方式是使用原始網路支援。
ms.assetid: 46abbbec-caa1-4fee-a713-4a4a2b462051
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab45f8175e82bdd1f5d6e49f3d94578473ed5c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839671"
---
# <a name="implementing-a-distributed-system"></a><span data-ttu-id="20514-103">執行分散式系統</span><span class="sxs-lookup"><span data-stu-id="20514-103">Implementing a Distributed System</span></span>

<span data-ttu-id="20514-104">在分散式系統中執行軟體的其中一種方式是使用原始網路支援。</span><span class="sxs-lookup"><span data-stu-id="20514-104">One way to implement software in a distributed system is to use raw networking support.</span></span> <span data-ttu-id="20514-105">這種方法包括通訊端、具名管道或 HTTP Post、取得等等。</span><span class="sxs-lookup"><span data-stu-id="20514-105">This approach includes sockets, named pipes, or HTTP POSTs, GETs, and so on.</span></span> <span data-ttu-id="20514-106">所有這些模型都強制開發人員以一種方式使用低層級的程式設計基本專案，以強制開發人員處理網路資料表示 (NDR) 、封裝資料、管理網路流量和失敗狀況、資料完整性保護和加密等等。</span><span class="sxs-lookup"><span data-stu-id="20514-106">All of these models force the developer to use low-level programming primitives, in one way or another, which force the developer to deal with network data representation (NDR), packaging data, managing network traffic and failure conditions, data integrity protection and encryption, and so on.</span></span>

<span data-ttu-id="20514-107">RPC 提供了一種程式設計模型，讓開發人員可以透過豐富的 API，在用戶端與伺服器之間保有網路互動的細微控制，同時又能節省開發人員從分散式系統引進的詳細資料和負擔。</span><span class="sxs-lookup"><span data-stu-id="20514-107">RPC offers a programming model where the developer retains granular control of the network interaction between the client and server through a rich API, while saving developers from the details and burdens that a distributed system tends to introduce.</span></span>

<span data-ttu-id="20514-108">例如，請考慮與各種方法相關聯的負擔，以保護分散式系統中訊息交換的完整性和隱私權。</span><span class="sxs-lookup"><span data-stu-id="20514-108">For example, consider the burden associated with various approaches to protecting the integrity and privacy of message exchanges in a distributed system.</span></span> <span data-ttu-id="20514-109">當考慮網路安全性以進行封包交換時，有些保護措施較弱，有些則較強。</span><span class="sxs-lookup"><span data-stu-id="20514-109">When considering network security for packet exchanges, some protections are weaker, some stronger.</span></span> <span data-ttu-id="20514-110">沒有真正的網路安全性，只是各種以封包為基礎的安全性機制。識別 (呼叫端的安全性通常也很弱，因為封包內容通常可以在傳輸中變更) 、保護封包完整性的安全性，而不需要保護其隱私權 (各種簽章和雜湊) ，以及保護訊息交換的隱私權 (各種加密機制) 的安全性。</span><span class="sxs-lookup"><span data-stu-id="20514-110">There is no true network security, only various packet-based security mechanisms; security identifying the caller (which tends to be weak as well, since packet contents can often be changed in transit), security protecting the integrity of the packet without protecting its privacy (various signatures and hashes), and security protecting the privacy of the message exchange (various encryption mechanisms).</span></span>

<span data-ttu-id="20514-111">實行安全的分散式系統的另一個負擔，就是執行安全性基本專案所需的演算法，例如加密、簽署、驗證等等。</span><span class="sxs-lookup"><span data-stu-id="20514-111">Another burden of implementing a secure distributed system is the algorithms necessary to implement security primitives such as encryption, signing, authentication, and so on.</span></span> <span data-ttu-id="20514-112">開發人員可以實行這些演算法，但是這樣做很困難、容易出錯，甚至有風險，因為產生的演算法通常會有微妙的安全性缺陷。</span><span class="sxs-lookup"><span data-stu-id="20514-112">A developer can implement those algorithms, but doing so is difficult, error-prone, and even risky, since the resulting algorithms often have subtle security flaws.</span></span> <span data-ttu-id="20514-113">或者，開發人員可以使用可用的安全性提供者，為分散式系統內的網路互動執行保護。</span><span class="sxs-lookup"><span data-stu-id="20514-113">Alternatively, a developer can use an available security provider to implement protection for the network interactions within a distributed system.</span></span>

<span data-ttu-id="20514-114">使用 RPC 時，這兩個負擔很容易解決。</span><span class="sxs-lookup"><span data-stu-id="20514-114">Using RPC, both of these burdens are resolved very easily.</span></span> <span data-ttu-id="20514-115">開發人員只需要告訴 RPC 要使用哪一個安全性封裝，以及應該將哪些安全性保護套用至訊息交換 (的驗證、加密、相互驗證、呼叫端身分識別追蹤等) 。</span><span class="sxs-lookup"><span data-stu-id="20514-115">A developer simply needs to tell RPC which security package to use, and which security protection should be applied to the message exchange (in terms of authentication, encryption, mutual authentication, caller-identity tracking, and so on).</span></span> <span data-ttu-id="20514-116">RPC 會以有效率的方式處理幕後的所有詳細資料，但可讓開發人員完全掌控資料的保護方式。</span><span class="sxs-lookup"><span data-stu-id="20514-116">RPC takes care of all the details behind the scenes in an efficient manner, yet provides the developer with full control over precisely how the data will be protected.</span></span>

 

 





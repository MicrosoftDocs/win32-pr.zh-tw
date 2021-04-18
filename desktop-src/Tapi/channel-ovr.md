---
description: 每一行都有一或多個通道。 服務提供者通常會處理通道如何公開為應用程式的位址，而終端使用者或伺服器不需要特定的通道知識。
ms.assetid: 8c7d38e0-1863-461f-9225-7a0b419532a3
title: '通道 (電話語音 API) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b793a23c945cad79c9e2401ab6944302e908fd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512152"
---
# <a name="channel-telephony-api"></a><span data-ttu-id="f24cc-104">通道 (電話語音 API) </span><span class="sxs-lookup"><span data-stu-id="f24cc-104">Channel (Telephony API)</span></span>

<span data-ttu-id="f24cc-105">每一行都有一或多個通道。</span><span class="sxs-lookup"><span data-stu-id="f24cc-105">Each line has one or more channels.</span></span> <span data-ttu-id="f24cc-106">服務提供者通常會處理通道如何公開為應用程式的位址，而終端使用者或伺服器不需要特定的通道知識。</span><span class="sxs-lookup"><span data-stu-id="f24cc-106">The service providers normally handle how channels are exposed as addresses to an application, and the end user or server does not require specific knowledge of channels.</span></span>

<span data-ttu-id="f24cc-107">通道完全相同，因此可互換。</span><span class="sxs-lookup"><span data-stu-id="f24cc-107">Channels are identical and therefore interchangeable.</span></span> <span data-ttu-id="f24cc-108">在 POTS (單純的舊電話語音) 中，一行剛好有一個通道，而通道是專門用於語音。</span><span class="sxs-lookup"><span data-stu-id="f24cc-108">In POTS (Plain Old Telephone Service), exactly one channel exists on a line, and the channel is used exclusively for voice.</span></span> <span data-ttu-id="f24cc-109">使用 ISDN 時，至少有三個 (，且最多可有30個以上的) 通道同時存在於一行上。</span><span class="sxs-lookup"><span data-stu-id="f24cc-109">With ISDN, at least three (and as many as 30 or more) channels can exist on a line simultaneously.</span></span>

<span data-ttu-id="f24cc-110">每個通道都可以有自己的位址，這表示一行可以有多個位址，因為它具有通道。</span><span class="sxs-lookup"><span data-stu-id="f24cc-110">Each channel can have its own address, which means a line could have as many addresses as it has channels.</span></span> <span data-ttu-id="f24cc-111">公開給應用程式的通道和位址之間的精確關聯性，取決於服務提供者的實作為。</span><span class="sxs-lookup"><span data-stu-id="f24cc-111">The precise relationship between channels and addresses exposed to an application is dependent on a service provider's implementation.</span></span>

<span data-ttu-id="f24cc-112">某些服務提供者支援將一個以上的位址指派給單一通道。</span><span class="sxs-lookup"><span data-stu-id="f24cc-112">Some service providers support the assignment of more than one address to a single channel.</span></span> <span data-ttu-id="f24cc-113">在 POTS 程式列上，各種系統都能提供多個位址，例如直接撥入撥號 () 或特殊的鈴聲，也就是電話公司提供的額外費用服務。</span><span class="sxs-lookup"><span data-stu-id="f24cc-113">On POTS lines, multiple addresses are made possible by various systems, such as direct inward dialing (DID) or distinctive ringing, which are extra-fee services that the telephone company provides.</span></span>

<span data-ttu-id="f24cc-114">許多大型公司都使用撥入電話。</span><span class="sxs-lookup"><span data-stu-id="f24cc-114">Many large corporations use DID for incoming calls.</span></span> <span data-ttu-id="f24cc-115">連接電話之前，會將其目的地延伸模組的信號告知 PBX，這會導致延伸模組環形而非操作員的電話。</span><span class="sxs-lookup"><span data-stu-id="f24cc-115">Before a call is connected, its destination extension number is signaled to the PBX, which causes the extension to ring instead of the operator's phone.</span></span> <span data-ttu-id="f24cc-116">私人家庭中的相異響鈴範例有可能是家長使用一個位址、子女另一個位址，以及第三個位址。</span><span class="sxs-lookup"><span data-stu-id="f24cc-116">An example of distinctive ringing in a private home would be if the parents used one address, the children another, and a fax machine a third.</span></span> <span data-ttu-id="f24cc-117">由於只有一行連接到電話網絡，因此當來電出現時，所有電話響鈴，但環形模式會根據呼叫端合作物件撥打的號碼而有所不同。</span><span class="sxs-lookup"><span data-stu-id="f24cc-117">Because only one line connects the house to the telephone network, all phones ring when a call appears, but the ring pattern is different depending on the number that the calling party dialed.</span></span> <span data-ttu-id="f24cc-118">透過獨特的響鈴，人們知道來電的物件，而傳真電腦藉由辨識自己的響鈴樣式來回答通話。</span><span class="sxs-lookup"><span data-stu-id="f24cc-118">With distinctive ringing, the people know who the incoming call is for, and the fax machine answers its calls by recognizing its own ringing style.</span></span>

<span data-ttu-id="f24cc-119">在 ISDN 中，各種 B 通道可能沒有不同的位址。</span><span class="sxs-lookup"><span data-stu-id="f24cc-119">In ISDN, the various B channels might not have separate addresses.</span></span> <span data-ttu-id="f24cc-120">因為這些 B 通道可能位於相同的位址，所以它是服務提供者 (而非應用程式或已撥) 的人，會將呼叫指派給這些通道。</span><span class="sxs-lookup"><span data-stu-id="f24cc-120">Because these B channels might be on the same address, it is the service provider (and not the application or a person who has dialed the number) that assigns calls to these channels.</span></span>

 

 




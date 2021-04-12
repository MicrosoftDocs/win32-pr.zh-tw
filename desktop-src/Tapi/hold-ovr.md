---
description: 保存作業可讓單一位址處理多個通訊會話。
ms.assetid: 65e22e4e-e346-41c2-929a-ba0d1f7f1732
title: Hold
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df54b246c5bde5914a14b53dd56b71688d92a5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848347"
---
# <a name="hold"></a><span data-ttu-id="e6318-103">Hold</span><span class="sxs-lookup"><span data-stu-id="e6318-103">Hold</span></span>

<span data-ttu-id="e6318-104">保存作業可讓單一位址處理多個通訊會話。</span><span class="sxs-lookup"><span data-stu-id="e6318-104">The hold operation allows a single address to handle multiple communications sessions.</span></span> <span data-ttu-id="e6318-105">將會話放在硬性保存後，就可以釋出使用者的線路/位址來進行其他呼叫。</span><span class="sxs-lookup"><span data-stu-id="e6318-105">Placing a session on a hard hold frees the user's line/address to make other calls.</span></span> <span data-ttu-id="e6318-106">通話通常無法轉移或包含在會議電話中，但諮詢電話可以。</span><span class="sxs-lookup"><span data-stu-id="e6318-106">A call on hard hold typically cannot be transferred or included in a conference call, but a consultation call can.</span></span> <span data-ttu-id="e6318-107">諮詢電話是使用 [會議](conference-ovr.md) 或 [轉移](transfer-ovr.md) 作業起始的。</span><span class="sxs-lookup"><span data-stu-id="e6318-107">Consultation calls are initiated using [conference](conference-ovr.md) or [transfer](transfer-ovr.md) operations.</span></span>

<span data-ttu-id="e6318-108">在呼叫成功放置之後，撥號狀態通常會轉換成舉 servicerequeststatusenum.onhold 狀態。</span><span class="sxs-lookup"><span data-stu-id="e6318-108">After a call has been successfully placed on hold, the call state typically transitions to the onhold state.</span></span> <span data-ttu-id="e6318-109">當呼叫保留時，應用程式可以接收有關已保存撥號狀態變更的訊息。</span><span class="sxs-lookup"><span data-stu-id="e6318-109">While a call is on hold, the application can receive messages about state changes of the held call.</span></span> <span data-ttu-id="e6318-110">例如，如果持有的合作物件停止回應，則撥號狀態可以轉換為已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="e6318-110">For example, if the held party hangs up, the call state can transition to disconnected.</span></span>

<span data-ttu-id="e6318-111">在橋接的情況下，保留作業可能不會實際將通話放置在待命狀態。</span><span class="sxs-lookup"><span data-stu-id="e6318-111">In a bridged situation, the hold operation may not actually place the call on hold.</span></span> <span data-ttu-id="e6318-112">呼叫中其他工作站的狀態可以管理 (例如，無法在其他工作站參與時嘗試「保留」呼叫，) ;相反地，呼叫可以直接變更為非作用中狀態，同時維持在其他工作站的連線。</span><span class="sxs-lookup"><span data-stu-id="e6318-112">The status of other stations on the call can govern (for example, attempting to "hold" a call when other stations are participating is not possible); instead, the call can simply be changed to the inactive state while it remains connected at other stations.</span></span>

<span data-ttu-id="e6318-113">並非所有服務提供者都支援使用這項作業。</span><span class="sxs-lookup"><span data-stu-id="e6318-113">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="e6318-114">**TAPI 2.x：** 請參閱 [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold)、 [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold)。</span><span class="sxs-lookup"><span data-stu-id="e6318-114">**TAPI 2.x:** See [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).</span></span>

<span data-ttu-id="e6318-115">**TAPI 3.x：** 請參閱 [**ITBasicCallControl：： Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold)。</span><span class="sxs-lookup"><span data-stu-id="e6318-115">**TAPI 3.x:** See [**ITBasicCallControl::Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).</span></span>

 

 

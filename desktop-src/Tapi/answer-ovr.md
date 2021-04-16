---
description: 回應作業是應用程式對提供之通訊會話的典型回應。 如果成功，此作業會導致會話轉換為線上狀態。
ms.assetid: 34ac0b34-1d1b-4657-a737-27a4ed9326af
title: 回答
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e08081b32b7ba3a3a24cde3ec37c1a6118582cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513476"
---
# <a name="answer"></a><span data-ttu-id="a3180-104">回答</span><span class="sxs-lookup"><span data-stu-id="a3180-104">Answer</span></span>

<span data-ttu-id="a3180-105">回應作業是應用程式對提供之通訊會話的典型回應。</span><span class="sxs-lookup"><span data-stu-id="a3180-105">The answer operation is an application's typical response to an offered communications session.</span></span> <span data-ttu-id="a3180-106">如果成功，此作業會導致會話轉換為線上狀態。</span><span class="sxs-lookup"><span data-stu-id="a3180-106">If successful, this operation causes a session to transition into the connected state.</span></span>

<span data-ttu-id="a3180-107">在某些電話語音環境中 (像是 ISDN) ，其中使用者警示與電話供應專案不同，因此應用程式可以選擇在接聽或 [拒絕 (卸載](drop-ovr.md)) 或重新 [導向](redirect-ovr.md)供應 *專案呼叫之前*[接受](accept-ovr.md)呼叫。</span><span class="sxs-lookup"><span data-stu-id="a3180-107">In some telephony environments (like ISDN), where user alerting is separate from call offering, the application has the option to [accept](accept-ovr.md) a call prior to answering or to reject ([drop](drop-ovr.md)) or [redirect](redirect-ovr.md) the *offering* call.</span></span>

<span data-ttu-id="a3180-108">如果會話已在使用中時，針對新的會話執行回應作業，則對現有作用中會話的影響會視服務提供者的功能而定。</span><span class="sxs-lookup"><span data-stu-id="a3180-108">If an answer operation is performed for a new session when a session is already active, the effect this has on the existing active session depends on the service provider's capabilities.</span></span> <span data-ttu-id="a3180-109">第一個呼叫可能不受影響，它可以自動卸載，也可以自動放置在保存上。</span><span class="sxs-lookup"><span data-stu-id="a3180-109">The first call can be unaffected, it can automatically be dropped, or it can automatically be placed on hold.</span></span> <span data-ttu-id="a3180-110">TAPI 會傳送關於這兩個呼叫的適當事件通知。</span><span class="sxs-lookup"><span data-stu-id="a3180-110">TAPI will send the appropriate event notifications concerning both calls.</span></span>

<span data-ttu-id="a3180-111">在橋接的情況下，如果呼叫已連線但處於作用中狀態，則可以使用「回應」操作來聯結。</span><span class="sxs-lookup"><span data-stu-id="a3180-111">In a bridged situation, if a call is connected but in the active state, it can be joined using the answer operation.</span></span>

<span data-ttu-id="a3180-112">如果服務提供者支援，則應用程式可以選擇在解答時傳送使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="a3180-112">The application has the option to send user-user information at the time of the answer, if the service provider supports it.</span></span>

<span data-ttu-id="a3180-113">**TAPI 2.x：** 請參閱 [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer)。</span><span class="sxs-lookup"><span data-stu-id="a3180-113">**TAPI 2.x:** See [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).</span></span>

<span data-ttu-id="a3180-114">**TAPI 3.x：** 請參閱 [**ITBasicCallControl：：解答**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer)。</span><span class="sxs-lookup"><span data-stu-id="a3180-114">**TAPI 3.x:** See [**ITBasicCallControl::Answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).</span></span>

 

 

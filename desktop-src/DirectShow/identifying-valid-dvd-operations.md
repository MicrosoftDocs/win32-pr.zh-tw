---
description: 識別有效的 DVD 作業
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: 識別有效的 DVD 作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444595e402dc73a3468946b820f031dabaecc2f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385779"
---
# <a name="identifying-valid-dvd-operations"></a><span data-ttu-id="0afa4-103">識別有效的 DVD 作業</span><span class="sxs-lookup"><span data-stu-id="0afa4-103">Identifying Valid DVD Operations</span></span>

<span data-ttu-id="0afa4-104">有幾個因素會決定您是否可以執行指定的 DVD 操作：</span><span class="sxs-lookup"><span data-stu-id="0afa4-104">Several factors determine whether you can perform a given DVD operation:</span></span>

-   <span data-ttu-id="0afa4-105">目前的網域。</span><span class="sxs-lookup"><span data-stu-id="0afa4-105">The current domain.</span></span> <span data-ttu-id="0afa4-106">某些命令只有在某些網域中才有效。</span><span class="sxs-lookup"><span data-stu-id="0afa4-106">Some commands are only valid in certain domains.</span></span> <span data-ttu-id="0afa4-107">當網域變更時，瀏覽器會傳送 EC \_ DVD \_ 網域 \_ 變更事件。</span><span class="sxs-lookup"><span data-stu-id="0afa4-107">When the domain changes, the navigator sends an EC\_DVD\_DOMAIN\_CHANGE event.</span></span> <span data-ttu-id="0afa4-108">您也可以呼叫 [**IDvdInfo2：： GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) 來取得目前的網域。</span><span class="sxs-lookup"><span data-stu-id="0afa4-108">You can also call [**IDvdInfo2::GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) to get the current domain.</span></span>
-   <span data-ttu-id="0afa4-109">UOPS 旗標。</span><span class="sxs-lookup"><span data-stu-id="0afa4-109">UOPS flags.</span></span> <span data-ttu-id="0afa4-110">這些是寫入光碟上的旗標，表示允許的作業。</span><span class="sxs-lookup"><span data-stu-id="0afa4-110">These are flags written onto the disc that indicate which operations are permitted.</span></span> <span data-ttu-id="0afa4-111">每當旗標變更時，導覽器就會 \_ \_ \_ \_ 以新的旗標傳送 EC DVD 有效 UOPS 變更事件。</span><span class="sxs-lookup"><span data-stu-id="0afa4-111">Whenever the flags change, the navigator sends a EC\_DVD\_VALID\_UOPS\_CHANGE event with the new flags.</span></span> <span data-ttu-id="0afa4-112">您也可以呼叫 [**IDvdInfo2：： GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) 來取得目前的 UOPS 旗標。</span><span class="sxs-lookup"><span data-stu-id="0afa4-112">You can also call [**IDvdInfo2::GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) to get the current UOPS flags.</span></span>
-   <span data-ttu-id="0afa4-113">DVD 內容。</span><span class="sxs-lookup"><span data-stu-id="0afa4-113">DVD content.</span></span> <span data-ttu-id="0afa4-114">某些命令可能不會根據 DVD 的內容而相關。</span><span class="sxs-lookup"><span data-stu-id="0afa4-114">Some commands may not be relevant based on the content of the DVD.</span></span> <span data-ttu-id="0afa4-115">例如，可能會根據目前的網域和 UOPS 旗標來允許 [**IDvdControl2：： SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) 方法，但影片可能只有一個角度。</span><span class="sxs-lookup"><span data-stu-id="0afa4-115">For example, the [**IDvdControl2::SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) method might be permitted according to the current domain and UOPS flags, yet the video might have only one angle.</span></span> <span data-ttu-id="0afa4-116">在此情況下，允許 **SelectAngle** 呼叫但不是有意義的選項。</span><span class="sxs-lookup"><span data-stu-id="0afa4-116">In that case, the **SelectAngle** call is permitted but is not a meaningful option.</span></span>

<span data-ttu-id="0afa4-117">若有疑問，請允許動作。</span><span class="sxs-lookup"><span data-stu-id="0afa4-117">When in doubt, permit an action.</span></span> <span data-ttu-id="0afa4-118">在最糟的情況下， [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 方法將會失敗，而且您可以將意見反應提供給使用者。</span><span class="sxs-lookup"><span data-stu-id="0afa4-118">At worst, the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method will fail and you can give feedback to the user.</span></span> <span data-ttu-id="0afa4-119">意見反應應該相當不顯眼。</span><span class="sxs-lookup"><span data-stu-id="0afa4-119">The feedback should be relatively unobtrusive.</span></span> <span data-ttu-id="0afa4-120">例如，您可能會快閃一個小的紅色 X 來警示使用者。</span><span class="sxs-lookup"><span data-stu-id="0afa4-120">For example, you might flash a small red X to alert the user.</span></span> <span data-ttu-id="0afa4-121">\_當網域禁止操作時，DVD 導覽器會傳回 VFW e \_ dvd \_ INVALIDDOMAIN，而 \_ \_ \_ \_ UOPS 旗標禁止操作時，會禁止 VFW E dvd 操作</span><span class="sxs-lookup"><span data-stu-id="0afa4-121">The DVD Navigator returns VFW\_E\_DVD\_INVALIDDOMAIN when the domain prohibits an operation, and VFW\_E\_DVD\_OPERATION\_INHIBITED when the UOPS flags prohibit an operation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0afa4-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="0afa4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0afa4-123">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="0afa4-123">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 




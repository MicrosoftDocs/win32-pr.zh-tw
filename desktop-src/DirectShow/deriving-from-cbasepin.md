---
description: 衍生自 CBasePin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: 衍生自 CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ab56da3ae326be175c9519b5248e53fa02b82f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970517"
---
# <a name="deriving-from-cbasepin"></a><span data-ttu-id="e72f4-103">衍生自 CBasePin</span><span class="sxs-lookup"><span data-stu-id="e72f4-103">Deriving from CBasePin</span></span>

<span data-ttu-id="e72f4-104">若要使用 [**CBasePin**](cbasepin.md)來執行 pin，您必須從基類衍生新的類別，並覆寫數個方法。</span><span class="sxs-lookup"><span data-stu-id="e72f4-104">To implement a pin using [**CBasePin**](cbasepin.md), you must derive a new class from the base class and override several of its methods.</span></span> <span data-ttu-id="e72f4-105">您必須覆寫下列方法：</span><span class="sxs-lookup"><span data-stu-id="e72f4-105">You must override the following methods:</span></span>

-   [<span data-ttu-id="e72f4-106">**CBasePin::CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="e72f4-106">**CBasePin::CheckMediaType**</span></span>](cbasepin-checkmediatype.md)
-   [<span data-ttu-id="e72f4-107">**CBasePin::GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="e72f4-107">**CBasePin::GetMediaType**</span></span>](cbasepin-getmediatype.md)

<span data-ttu-id="e72f4-108">您可能需要覆寫這些額外的方法：</span><span class="sxs-lookup"><span data-stu-id="e72f4-108">You will probably need to override these additional methods:</span></span>

-   [<span data-ttu-id="e72f4-109">**CBasePin：： Active**</span><span class="sxs-lookup"><span data-stu-id="e72f4-109">**CBasePin::Active**</span></span>](cbasepin-active.md)
-   [<span data-ttu-id="e72f4-110">**CBasePin::BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="e72f4-110">**CBasePin::BreakConnect**</span></span>](cbasepin-breakconnect.md)
-   [<span data-ttu-id="e72f4-111">**CBasePin::CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="e72f4-111">**CBasePin::CheckConnect**</span></span>](cbasepin-checkconnect.md)
-   [<span data-ttu-id="e72f4-112">**CBasePin::CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="e72f4-112">**CBasePin::CompleteConnect**</span></span>](cbasepin-completeconnect.md)
-   [<span data-ttu-id="e72f4-113">**CBasePin::EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="e72f4-113">**CBasePin::EndOfStream**</span></span>](cbasepin-endofstream.md)
-   [<span data-ttu-id="e72f4-114">**CBasePin：：非使用中**</span><span class="sxs-lookup"><span data-stu-id="e72f4-114">**CBasePin::Inactive**</span></span>](cbasepin-inactive.md)
-   [<span data-ttu-id="e72f4-115">**CBasePin：： Notify**</span><span class="sxs-lookup"><span data-stu-id="e72f4-115">**CBasePin::Notify**</span></span>](cbasepin-notify.md)
-   [<span data-ttu-id="e72f4-116">**CBasePin：： Run**</span><span class="sxs-lookup"><span data-stu-id="e72f4-116">**CBasePin::Run**</span></span>](cbasepin-run.md)

<span data-ttu-id="e72f4-117">最後，您必須執行 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 和 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="e72f4-117">Finally, you must must implement the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods.</span></span>

<span data-ttu-id="e72f4-118">其中某些方法會在衍生自 **CBasePin** 的基類中執行，例如 [**CBaseInputPin**](cbaseinputpin.md) 和 [**CBaseOutputPin**](cbaseoutputpin.md)。</span><span class="sxs-lookup"><span data-stu-id="e72f4-118">Some of these methods are implemented in base classes that derive from **CBasePin**, such as [**CBaseInputPin**](cbaseinputpin.md) and [**CBaseOutputPin**](cbaseoutputpin.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e72f4-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="e72f4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e72f4-120">**CBasePin**</span><span class="sxs-lookup"><span data-stu-id="e72f4-120">**CBasePin**</span></span>](cbasepin.md)
</dt> </dl>

 

 




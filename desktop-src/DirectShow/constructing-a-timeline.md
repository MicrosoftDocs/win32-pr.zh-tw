---
description: 建立時間軸
ms.assetid: 4909f797-d296-4c9f-83fb-543e48bbe75d
title: 建立時間軸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c16b1134eb92b3e3ac5a0f1919d7c4a2736b206
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385756"
---
# <a name="constructing-a-timeline"></a><span data-ttu-id="76361-103">建立時間軸</span><span class="sxs-lookup"><span data-stu-id="76361-103">Constructing a Timeline</span></span>

<span data-ttu-id="76361-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="76361-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="76361-105">本文說明如何在 (DES) 的 [DirectShow 編輯服務](directshow-editing-services.md) 中建立時間軸。</span><span class="sxs-lookup"><span data-stu-id="76361-105">This article describes how to construct a timeline in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="76361-106">它會提供範例主控台應用程式，以建立時間軸並加以呈現。</span><span class="sxs-lookup"><span data-stu-id="76361-106">It presents an example console application that creates a timeline and renders it.</span></span> <span data-ttu-id="76361-107">時間軸是最基本的，包含具有一個來源剪輯的單一影片群組，但它會示範建立更複雜的時間軸所需的大部分概念。</span><span class="sxs-lookup"><span data-stu-id="76361-107">The timeline is minimal, consisting of a single video group with one source clip, but it demonstrates most of the concepts needed to create more complex timelines.</span></span>

<span data-ttu-id="76361-108">本文包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="76361-108">This article contains the following topics.</span></span>

-   [<span data-ttu-id="76361-109">建立時間軸物件</span><span class="sxs-lookup"><span data-stu-id="76361-109">Creating Timeline Objects</span></span>](creating-timeline-objects.md)
-   [<span data-ttu-id="76361-110">建立群組、撰寫和追蹤</span><span class="sxs-lookup"><span data-stu-id="76361-110">Creating Groups, Compositions, and Tracks</span></span>](creating-groups-compositions-and-tracks.md)
-   [<span data-ttu-id="76361-111">設定群組媒體類型</span><span class="sxs-lookup"><span data-stu-id="76361-111">Setting the Group Media Type</span></span>](setting-the-group-media-type.md)
-   [<span data-ttu-id="76361-112">新增來源</span><span class="sxs-lookup"><span data-stu-id="76361-112">Adding a Source</span></span>](adding-a-source.md)
-   [<span data-ttu-id="76361-113">建立時間軸：範例程式碼</span><span class="sxs-lookup"><span data-stu-id="76361-113">Creating a Timeline: Example Code</span></span>](creating-a-timeline--example-code.md)

## <a name="related-topics"></a><span data-ttu-id="76361-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="76361-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76361-115">使用 DirectShow 編輯服務</span><span class="sxs-lookup"><span data-stu-id="76361-115">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 




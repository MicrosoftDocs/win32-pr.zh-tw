---
description: 範圍前置詞是將文字標籤預先附加至 schema 關鍵字，以提供內容約制，包括作業、檔和頁面。
ms.assetid: 4bad85d7-a933-43fe-9d79-4835d92c82d6
title: 範圍前置詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c027de94fda403eb58905e536d8c6256cb2d6c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404901"
---
# <a name="scoping-prefix"></a><span data-ttu-id="6ab70-103">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="6ab70-103">Scoping Prefix</span></span>

<span data-ttu-id="6ab70-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="6ab70-104">This topic is not current.</span></span> <span data-ttu-id="6ab70-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="6ab70-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6ab70-106">範圍前置詞是一種文字標籤，預先附加至 schema 關鍵字以提供內容相關的範圍。</span><span class="sxs-lookup"><span data-stu-id="6ab70-106">A scope prefix is a textual label pre-appended to a schema keyword to provide a contextual scope.</span></span> <span data-ttu-id="6ab70-107">這可讓您以預先定義的方式將特定且易懂的內容 ascribing 至關鍵字。</span><span class="sxs-lookup"><span data-stu-id="6ab70-107">This allows ascribing a specific and well-understood context to keywords in a predefined manner.</span></span> <span data-ttu-id="6ab70-108">Print Schema Feature、ParameterDef、ParameterInit 和 ParameterRef 和根層級屬性關鍵字元素必須有下列其中一個範圍前置詞：「作業」、「檔」或「頁面」。</span><span class="sxs-lookup"><span data-stu-id="6ab70-108">Print Schema Feature, ParameterDef, ParameterInit, and ParameterRef and root-level Property keyword Elements MUST have one of the following scope prefixes: "Job", "Document", or "Page".</span></span>

## <a name="interpretation-of-the-scoping-prefix-with-printticket-content"></a><span data-ttu-id="6ab70-109">使用 PrintTicket 內容進行範圍前置詞的解讀</span><span class="sxs-lookup"><span data-stu-id="6ab70-109">Interpretation of the Scoping Prefix with PrintTicket Content</span></span>

<span data-ttu-id="6ab70-110">PrintTicket 可以細分為三個代表高階工作的內容層級、作業中的檔，以及每份檔中的頁面。</span><span class="sxs-lookup"><span data-stu-id="6ab70-110">The PrintTicket can be broken down into three content levels representing the high level job, the documents in the job, and the pages in each document.</span></span> <span data-ttu-id="6ab70-111">這些層級會根據明確程度進行排名;作業層級最普遍，而檔層級和頁面層級是最特定的。</span><span class="sxs-lookup"><span data-stu-id="6ab70-111">These levels are ranked according to specificity; the Job Level is most general, then the Document Level and then the Page Level is most specific.</span></span> <span data-ttu-id="6ab70-112">作業包含一或多個檔，而檔是由一或多個頁面所組成。</span><span class="sxs-lookup"><span data-stu-id="6ab70-112">A job consists of one or more documents and a document consists of one or more pages.</span></span>

## <a name="job-level-prefix"></a><span data-ttu-id="6ab70-113">作業層級前置詞</span><span class="sxs-lookup"><span data-stu-id="6ab70-113">Job level Prefix</span></span>

<span data-ttu-id="6ab70-114">作業層級票證包含所有預定要套用至整個作業的工作格式設定。</span><span class="sxs-lookup"><span data-stu-id="6ab70-114">A Job Level ticket contains all job formatting settings intended to apply to an entire job.</span></span> <span data-ttu-id="6ab70-115">作業層級票證中允許任何具有「作業」、「檔」或「頁面」範圍前置詞的元素。</span><span class="sxs-lookup"><span data-stu-id="6ab70-115">Any Elements with scope prefixes of "Job", "Document" or "Page" are permitted in a Job Level ticket.</span></span>

<span data-ttu-id="6ab70-116">作業層級票證中指定的「檔」和「頁面」前置設定，會自動套用至檔和頁面層級的票證。</span><span class="sxs-lookup"><span data-stu-id="6ab70-116">The "Document" and "Page" prefixed settings specified in a Job Level ticket will be automatically applied to the Document and Page Level tickets.</span></span>

## <a name="document-level-prefix"></a><span data-ttu-id="6ab70-117">檔層級前置詞</span><span class="sxs-lookup"><span data-stu-id="6ab70-117">Document level Prefix</span></span>

<span data-ttu-id="6ab70-118">檔層級票證包含任何預定要套用至工作中一或多個檔的工作格式設定。</span><span class="sxs-lookup"><span data-stu-id="6ab70-118">The Document Level ticket incorporates any job formatting settings intended to apply to one or more documents in a job.</span></span> <span data-ttu-id="6ab70-119">這些可能包括先前在作業層級票證中指定的設定。</span><span class="sxs-lookup"><span data-stu-id="6ab70-119">These may include settings previously specified in the Job Level ticket.</span></span> <span data-ttu-id="6ab70-120">檔層級票證中只允許範圍前置詞為 "Document" 或 "Page" 的元素。</span><span class="sxs-lookup"><span data-stu-id="6ab70-120">Only Elements with scope prefixes of "Document" or "Page" are allowed in a Document Level ticket.</span></span>

<span data-ttu-id="6ab70-121">檔層級票證可能包含先前由作業層級票證指定的檔前置詞設定。</span><span class="sxs-lookup"><span data-stu-id="6ab70-121">A Document Level Ticket may contain Document-prefixed settings previously specified by the Job level Ticket.</span></span>

## <a name="page-level-prefix"></a><span data-ttu-id="6ab70-122">頁面層級前置詞</span><span class="sxs-lookup"><span data-stu-id="6ab70-122">Page level Prefix</span></span>

<span data-ttu-id="6ab70-123">頁面層級票證包含任何要套用至一或多個頁面的工作格式設定， (不限於單一檔) 。</span><span class="sxs-lookup"><span data-stu-id="6ab70-123">The Page Level ticket incorporates any job formatting settings intended to apply to one or more pages a job (not limited to a single document).</span></span> <span data-ttu-id="6ab70-124">這些可能包括先前在作業或檔層級票證中指定的設定。</span><span class="sxs-lookup"><span data-stu-id="6ab70-124">These may include settings previously specified in the Job or Document Level ticket.</span></span> <span data-ttu-id="6ab70-125">頁面層級票證中只允許範圍前置詞為 "Page" 的元素。</span><span class="sxs-lookup"><span data-stu-id="6ab70-125">Only Elements with scope prefixes of "Page" are allowed in a Page Level ticket.</span></span>

<span data-ttu-id="6ab70-126">頁面層級票證可能包含先前由作業層級票證和/或檔層級票證所指定的「頁面」前置詞設定。</span><span class="sxs-lookup"><span data-stu-id="6ab70-126">A Page Level Ticket may contain "Page" prefixed settings previously specified by the Job Level Ticket and/or the Document level ticket.</span></span>

## <a name="prefix-usage-within-a-printticket-or-print-capabilities-document"></a><span data-ttu-id="6ab70-127">在 PrintTicket 或列印功能檔中使用前置詞</span><span class="sxs-lookup"><span data-stu-id="6ab70-127">Prefix Usage within a PrintTicket or Print Capabilities Document</span></span>

<span data-ttu-id="6ab70-128">PrintTicket 和 PrintCapabilities 檔不能包含多個關鍵字，這些關鍵字只會在範圍前置詞中不同。</span><span class="sxs-lookup"><span data-stu-id="6ab70-128">PrintTicket and PrintCapabilities documents MUST NOT contain multiple keywords that differ only in the scoping prefix.?</span></span> <span data-ttu-id="6ab70-129">例如，PrintCapabilities 檔不能同時指定 JobInputBin 和 PageInputBin。</span><span class="sxs-lookup"><span data-stu-id="6ab70-129">For example, a PrintCapabilities document MUST NOT have both JobInputBin and PageInputBin specified.?</span></span> <span data-ttu-id="6ab70-130">不過，列印功能檔可能會同時指定 JobDuplexAllDocumentsContiguously 和 DocumentDuplex，因為這些會被視為不同的功能，因為它們表現不同的行為。</span><span class="sxs-lookup"><span data-stu-id="6ab70-130">However, a Print Capabilities document MAY have both JobDuplexAllDocumentsContiguously and DocumentDuplex specified because these are considered different features, as they exhibit differing behavior.?</span></span> <span data-ttu-id="6ab70-131">此範例也適用于單一 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="6ab70-131">This example is also true for a single PrintTicket.</span></span>

## <a name="prefix-conflict-management"></a><span data-ttu-id="6ab70-132">前置詞衝突管理</span><span class="sxs-lookup"><span data-stu-id="6ab70-132">Prefix Conflict Management</span></span>

<span data-ttu-id="6ab70-133">設定之間的關鍵字衝突定義為，以 XML 屬性 "name" 表示的相同根層級列印架構元素，出現在多個層級票證中。</span><span class="sxs-lookup"><span data-stu-id="6ab70-133">A keyword conflict between settings is defined as, the same root level Print Schema Element denoted by the XML Attribute "name", appearing in multiple Level tickets.</span></span> <span data-ttu-id="6ab70-134">如果沒有衝突，前置詞範圍專案可能會從更一般的票證向下推送或繼承至更特定的票證。</span><span class="sxs-lookup"><span data-stu-id="6ab70-134">If there is no conflict, a prefix scoped Element may be pushed down, or inherited, from a more general ticket to a more specific ticket.</span></span> <span data-ttu-id="6ab70-135">如果發生衝突，則會優先使用最特定票證的設定。</span><span class="sxs-lookup"><span data-stu-id="6ab70-135">If there is a conflict, then the setting from the most specific ticket takes precedence.</span></span> <span data-ttu-id="6ab70-136">也就是說，頁面層級票證中的每個頁面設定會覆寫檔或作業層級票證中的每頁設定相同的設定。</span><span class="sxs-lookup"><span data-stu-id="6ab70-136">That is, per page settings in a Page Level ticket override the identical per page settings in a Document or Job Level ticket.</span></span> <span data-ttu-id="6ab70-137">同樣地，檔層級票證中的檔設定會優先于作業層級票證中的檔設定。</span><span class="sxs-lookup"><span data-stu-id="6ab70-137">Similarly, document settings in the Document Level ticket take precedence over document settings in the Job Level ticket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ab70-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="6ab70-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ab70-139">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="6ab70-139">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




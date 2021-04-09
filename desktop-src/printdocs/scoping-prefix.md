---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 4bad85d7-a933-43fe-9d79-4835d92c82d6
title: 範圍前置詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef74be192671124872e19e87973a266da4a09226
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103853508"
---
# <a name="scoping-prefix"></a><span data-ttu-id="bbb87-104">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="bbb87-104">Scoping Prefix</span></span>

<span data-ttu-id="bbb87-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="bbb87-105">This topic is not current.</span></span> <span data-ttu-id="bbb87-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="bbb87-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bbb87-107">範圍前置詞是一種文字標籤，預先附加至 schema 關鍵字以提供內容相關的範圍。</span><span class="sxs-lookup"><span data-stu-id="bbb87-107">A scope prefix is a textual label pre-appended to a schema keyword to provide a contextual scope.</span></span> <span data-ttu-id="bbb87-108">這可讓您以預先定義的方式將特定且易懂的內容 ascribing 至關鍵字。</span><span class="sxs-lookup"><span data-stu-id="bbb87-108">This allows ascribing a specific and well-understood context to keywords in a predefined manner.</span></span> <span data-ttu-id="bbb87-109">Print Schema Feature、ParameterDef、ParameterInit 和 ParameterRef 和根層級屬性關鍵字元素必須有下列其中一個範圍前置詞：「作業」、「檔」或「頁面」。</span><span class="sxs-lookup"><span data-stu-id="bbb87-109">Print Schema Feature, ParameterDef, ParameterInit, and ParameterRef and root-level Property keyword Elements MUST have one of the following scope prefixes: "Job", "Document", or "Page".</span></span>

## <a name="interpretation-of-the-scoping-prefix-with-printticket-content"></a><span data-ttu-id="bbb87-110">使用 PrintTicket 內容進行範圍前置詞的解讀</span><span class="sxs-lookup"><span data-stu-id="bbb87-110">Interpretation of the Scoping Prefix with PrintTicket Content</span></span>

<span data-ttu-id="bbb87-111">PrintTicket 可以細分為三個代表高階工作的內容層級、作業中的檔，以及每份檔中的頁面。</span><span class="sxs-lookup"><span data-stu-id="bbb87-111">The PrintTicket can be broken down into three content levels representing the high level job, the documents in the job, and the pages in each document.</span></span> <span data-ttu-id="bbb87-112">這些層級會根據明確程度進行排名;作業層級最普遍，而檔層級和頁面層級是最特定的。</span><span class="sxs-lookup"><span data-stu-id="bbb87-112">These levels are ranked according to specificity; the Job Level is most general, then the Document Level and then the Page Level is most specific.</span></span> <span data-ttu-id="bbb87-113">作業包含一或多個檔，而檔是由一或多個頁面所組成。</span><span class="sxs-lookup"><span data-stu-id="bbb87-113">A job consists of one or more documents and a document consists of one or more pages.</span></span>

## <a name="job-level-prefix"></a><span data-ttu-id="bbb87-114">作業層級前置詞</span><span class="sxs-lookup"><span data-stu-id="bbb87-114">Job level Prefix</span></span>

<span data-ttu-id="bbb87-115">作業層級票證包含所有預定要套用至整個作業的工作格式設定。</span><span class="sxs-lookup"><span data-stu-id="bbb87-115">A Job Level ticket contains all job formatting settings intended to apply to an entire job.</span></span> <span data-ttu-id="bbb87-116">作業層級票證中允許任何具有「作業」、「檔」或「頁面」範圍前置詞的元素。</span><span class="sxs-lookup"><span data-stu-id="bbb87-116">Any Elements with scope prefixes of "Job", "Document" or "Page" are permitted in a Job Level ticket.</span></span>

<span data-ttu-id="bbb87-117">作業層級票證中指定的「檔」和「頁面」前置設定，會自動套用至檔和頁面層級的票證。</span><span class="sxs-lookup"><span data-stu-id="bbb87-117">The "Document" and "Page" prefixed settings specified in a Job Level ticket will be automatically applied to the Document and Page Level tickets.</span></span>

## <a name="document-level-prefix"></a><span data-ttu-id="bbb87-118">檔層級前置詞</span><span class="sxs-lookup"><span data-stu-id="bbb87-118">Document level Prefix</span></span>

<span data-ttu-id="bbb87-119">檔層級票證包含任何預定要套用至工作中一或多個檔的工作格式設定。</span><span class="sxs-lookup"><span data-stu-id="bbb87-119">The Document Level ticket incorporates any job formatting settings intended to apply to one or more documents in a job.</span></span> <span data-ttu-id="bbb87-120">這些可能包括先前在作業層級票證中指定的設定。</span><span class="sxs-lookup"><span data-stu-id="bbb87-120">These may include settings previously specified in the Job Level ticket.</span></span> <span data-ttu-id="bbb87-121">檔層級票證中只允許範圍前置詞為 "Document" 或 "Page" 的元素。</span><span class="sxs-lookup"><span data-stu-id="bbb87-121">Only Elements with scope prefixes of "Document" or "Page" are allowed in a Document Level ticket.</span></span>

<span data-ttu-id="bbb87-122">檔層級票證可能包含先前由作業層級票證指定的檔前置詞設定。</span><span class="sxs-lookup"><span data-stu-id="bbb87-122">A Document Level Ticket may contain Document-prefixed settings previously specified by the Job level Ticket.</span></span>

## <a name="page-level-prefix"></a><span data-ttu-id="bbb87-123">頁面層級前置詞</span><span class="sxs-lookup"><span data-stu-id="bbb87-123">Page level Prefix</span></span>

<span data-ttu-id="bbb87-124">頁面層級票證包含任何要套用至一或多個頁面的工作格式設定， (不限於單一檔) 。</span><span class="sxs-lookup"><span data-stu-id="bbb87-124">The Page Level ticket incorporates any job formatting settings intended to apply to one or more pages a job (not limited to a single document).</span></span> <span data-ttu-id="bbb87-125">這些可能包括先前在作業或檔層級票證中指定的設定。</span><span class="sxs-lookup"><span data-stu-id="bbb87-125">These may include settings previously specified in the Job or Document Level ticket.</span></span> <span data-ttu-id="bbb87-126">頁面層級票證中只允許範圍前置詞為 "Page" 的元素。</span><span class="sxs-lookup"><span data-stu-id="bbb87-126">Only Elements with scope prefixes of "Page" are allowed in a Page Level ticket.</span></span>

<span data-ttu-id="bbb87-127">頁面層級票證可能包含先前由作業層級票證和/或檔層級票證所指定的「頁面」前置詞設定。</span><span class="sxs-lookup"><span data-stu-id="bbb87-127">A Page Level Ticket may contain "Page" prefixed settings previously specified by the Job Level Ticket and/or the Document level ticket.</span></span>

## <a name="prefix-usage-within-a-printticket-or-print-capabilities-document"></a><span data-ttu-id="bbb87-128">在 PrintTicket 或列印功能檔中使用前置詞</span><span class="sxs-lookup"><span data-stu-id="bbb87-128">Prefix Usage within a PrintTicket or Print Capabilities Document</span></span>

<span data-ttu-id="bbb87-129">PrintTicket 和 PrintCapabilities 檔不能包含多個關鍵字，這些關鍵字只會在範圍前置詞中不同。</span><span class="sxs-lookup"><span data-stu-id="bbb87-129">PrintTicket and PrintCapabilities documents MUST NOT contain multiple keywords that differ only in the scoping prefix.?</span></span> <span data-ttu-id="bbb87-130">例如，PrintCapabilities 檔不能同時指定 JobInputBin 和 PageInputBin。</span><span class="sxs-lookup"><span data-stu-id="bbb87-130">For example, a PrintCapabilities document MUST NOT have both JobInputBin and PageInputBin specified.?</span></span> <span data-ttu-id="bbb87-131">不過，列印功能檔可能會同時指定 JobDuplexAllDocumentsContiguously 和 DocumentDuplex，因為這些會被視為不同的功能，因為它們表現不同的行為。</span><span class="sxs-lookup"><span data-stu-id="bbb87-131">However, a Print Capabilities document MAY have both JobDuplexAllDocumentsContiguously and DocumentDuplex specified because these are considered different features, as they exhibit differing behavior.?</span></span> <span data-ttu-id="bbb87-132">此範例也適用于單一 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="bbb87-132">This example is also true for a single PrintTicket.</span></span>

## <a name="prefix-conflict-management"></a><span data-ttu-id="bbb87-133">前置詞衝突管理</span><span class="sxs-lookup"><span data-stu-id="bbb87-133">Prefix Conflict Management</span></span>

<span data-ttu-id="bbb87-134">設定之間的關鍵字衝突定義為，以 XML 屬性 "name" 表示的相同根層級列印架構元素，出現在多個層級票證中。</span><span class="sxs-lookup"><span data-stu-id="bbb87-134">A keyword conflict between settings is defined as, the same root level Print Schema Element denoted by the XML Attribute "name", appearing in multiple Level tickets.</span></span> <span data-ttu-id="bbb87-135">如果沒有衝突，前置詞範圍專案可能會從更一般的票證向下推送或繼承至更特定的票證。</span><span class="sxs-lookup"><span data-stu-id="bbb87-135">If there is no conflict, a prefix scoped Element may be pushed down, or inherited, from a more general ticket to a more specific ticket.</span></span> <span data-ttu-id="bbb87-136">如果發生衝突，則會優先使用最特定票證的設定。</span><span class="sxs-lookup"><span data-stu-id="bbb87-136">If there is a conflict, then the setting from the most specific ticket takes precedence.</span></span> <span data-ttu-id="bbb87-137">也就是說，頁面層級票證中的每個頁面設定會覆寫檔或作業層級票證中的每頁設定相同的設定。</span><span class="sxs-lookup"><span data-stu-id="bbb87-137">That is, per page settings in a Page Level ticket override the identical per page settings in a Document or Job Level ticket.</span></span> <span data-ttu-id="bbb87-138">同樣地，檔層級票證中的檔設定會優先于作業層級票證中的檔設定。</span><span class="sxs-lookup"><span data-stu-id="bbb87-138">Similarly, document settings in the Document Level ticket take precedence over document settings in the Job Level ticket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbb87-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="bbb87-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbb87-140">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="bbb87-140">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




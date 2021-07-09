---
description: 瞭解如何支援 PrintTicket 差異。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: 支援 PrintTicket 差異
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f72f82875d0207ed232f4db897c78295ce2ee0
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548776"
---
# <a name="supporting-printticket-deltas"></a><span data-ttu-id="45309-105">支援 PrintTicket 差異</span><span class="sxs-lookup"><span data-stu-id="45309-105">Supporting PrintTicket Deltas</span></span>

<span data-ttu-id="45309-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="45309-106">This topic is not current.</span></span> <span data-ttu-id="45309-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="45309-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="45309-108">PrintTicket 提供者介面具有可用來對現有的 PrintTicket 進行累加式變更的方法。</span><span class="sxs-lookup"><span data-stu-id="45309-108">The PrintTicket Provider Interface has methods that can be used to make incremental changes to an existing PrintTicket.</span></span> <span data-ttu-id="45309-109">增量的 PrintTicket 變更可以在稱為 PrintTicket delta 的部分 PrintTicket 中指定。</span><span class="sxs-lookup"><span data-stu-id="45309-109">The incremental PrintTicket changes can be specified in a partial PrintTicket that is known as a PrintTicket delta.</span></span> <span data-ttu-id="45309-110">修改過的 PrintTicket 是藉由合併 PrintTicket delta 與現有的 PrintTicket 來建立。</span><span class="sxs-lookup"><span data-stu-id="45309-110">A revised PrintTicket is created by merging a PrintTicket delta with an existing PrintTicket.</span></span> <span data-ttu-id="45309-111">如需有關具有 PrintTicket 差異之方法的詳細資訊，請參閱即將推出的 PrintTicket 提供者介面檔。</span><span class="sxs-lookup"><span data-stu-id="45309-111">See the forthcoming PrintTicket Provider Interface document for more information about methods involving PrintTicket deltas.</span></span>

<span data-ttu-id="45309-112">處理 PrintTicket 差異時，必須執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="45309-112">When a PrintTicket delta is processed, the following steps must be performed.</span></span>

1.  <span data-ttu-id="45309-113">識別現有的 PrintTicket (目標 PrintTicket) 和 PrintTicket 差異通用的功能或 ParameterInit 實例。</span><span class="sxs-lookup"><span data-stu-id="45309-113">Identify Feature or ParameterInit instances that are common to both the existing PrintTicket (the target PrintTicket) and the PrintTicket delta.</span></span>

    -   <span data-ttu-id="45309-114">針對目標 PrintTicket 和 PrintTicket 差異通用的每個功能，以 PrintTicket 差異中的對應功能取代目標 PrintTicket 中的功能。</span><span class="sxs-lookup"><span data-stu-id="45309-114">For each Feature common to both the target PrintTicket and the PrintTicket delta, replace the Feature in the target PrintTicket by the corresponding Feature in the PrintTicket delta.</span></span>

    -   <span data-ttu-id="45309-115">針對目標 PrintTicket 和 PrintTicket 差異通用的每個 ParameterInit，將目標 PrintTicket 中的 ParameterInit 取代為 PrintTicket delta 中對應的 ParameterInit。</span><span class="sxs-lookup"><span data-stu-id="45309-115">For each ParameterInit common to both the target PrintTicket and the PrintTicket delta, replace the ParameterInit in the target PrintTicket by the corresponding ParameterInit in the PrintTicket delta.</span></span>

2.  <span data-ttu-id="45309-116">將 PrintTicket delta 中所有剩餘的功能和 ParameterInit 實例複製到目標 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="45309-116">Copy all remaining Feature and ParameterInit instances in the PrintTicket delta to the target PrintTicket.</span></span>

3.  <span data-ttu-id="45309-117">如果您的衝突解決演算法允許在 PrintTicket 本身指定優先權，您可以選擇提高在 PrintTicket delta 中命名的功能和 ParameterInit 實例的優先順序。</span><span class="sxs-lookup"><span data-stu-id="45309-117">If your conflict resolution algorithm allows priorities to be specified in the PrintTicket itself, you may choose to elevate the priorities of the Feature and ParameterInit instances named in the PrintTicket delta.</span></span>

4.  <span data-ttu-id="45309-118">執行 printticket 驗證，如 [Printticket 驗證檢查清單](printticket-validation-checklist.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="45309-118">Perform PrintTicket validation as described in [PrintTicket Validation Checklist](printticket-validation-checklist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="45309-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="45309-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45309-120">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="45309-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




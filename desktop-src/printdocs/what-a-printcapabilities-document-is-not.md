---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: PrintCapabilities 檔不是什麼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6e18082a5e551f3997dad8b9688d84ff2f824a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106992656"
---
# <a name="what-a-printcapabilities-document-is-not"></a><span data-ttu-id="07a73-104">PrintCapabilities 檔不是什麼</span><span class="sxs-lookup"><span data-stu-id="07a73-104">What a PrintCapabilities Document Is Not</span></span>

<span data-ttu-id="07a73-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="07a73-105">This topic is not current.</span></span> <span data-ttu-id="07a73-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="07a73-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="07a73-107">您可以列出 PrintCapabilities 檔不打算提供的部分功能和資訊。</span><span class="sxs-lookup"><span data-stu-id="07a73-107">It is worthwhile to list some of the functionality and information the PrintCapabilities document is not intended to provide.</span></span>

<span data-ttu-id="07a73-108">PrintCapabilities 檔：</span><span class="sxs-lookup"><span data-stu-id="07a73-108">A PrintCapabilities document:</span></span>

-   <span data-ttu-id="07a73-109">不代表 (設定相依) 資料的多重值。</span><span class="sxs-lookup"><span data-stu-id="07a73-109">Does not represent multivalued (configuration-dependent) data.</span></span>

    <span data-ttu-id="07a73-110">每個 PrintCapabilities 檔都是針對特定設定所建立。</span><span class="sxs-lookup"><span data-stu-id="07a73-110">Each PrintCapabilities document is constructed for a specific configuration.</span></span> <span data-ttu-id="07a73-111">檔中沒有任何屬性或 ScoredProperty 可以有相依于特定設定的值。</span><span class="sxs-lookup"><span data-stu-id="07a73-111">No Property or ScoredProperty in the document can have a Value that depends on the particular configuration.</span></span> <span data-ttu-id="07a73-112">在初始架構版本中，PrintCapabilities 提供者必須處理輸入 PrintTicket，然後建立 PrintCapabilities 檔，其中包含適用于 PrintTicket 中所指定設定的屬性值。</span><span class="sxs-lookup"><span data-stu-id="07a73-112">In the initial schema version, the PrintCapabilities provider must process the input PrintTicket and create a PrintCapabilities document that contains Property values appropriate for the configuration specified in the PrintTicket.</span></span>

-   <span data-ttu-id="07a73-113">不包含條件約束資訊。</span><span class="sxs-lookup"><span data-stu-id="07a73-113">Does not contain constraint information.</span></span>

    <span data-ttu-id="07a73-114">PrintCapabilities 檔不會指出允許哪些設定，哪些是不允許的設定。</span><span class="sxs-lookup"><span data-stu-id="07a73-114">The PrintCapabilities document does not indicate which configurations are allowed and which are not allowed.</span></span> <span data-ttu-id="07a73-115">在初始架構版本中，PrintCapabilities 提供者必須儲存驗證設定所需的任何資訊、提供驗證輸入 PrintTicket 的方法，並在指定的 PrintTicket 違反一或多個條件約束的情況下傳回更正的 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="07a73-115">In the initial schema version, the PrintCapabilities provider must store any information needed to validate configurations, supply a method that validates the input PrintTicket, and return a corrected PrintTicket in the event that the specified PrintTicket violates one or more constraints.</span></span>

-   <span data-ttu-id="07a73-116">不包含動態裝置資訊。</span><span class="sxs-lookup"><span data-stu-id="07a73-116">Does not contain dynamic device information.</span></span>

    <span data-ttu-id="07a73-117">建立 PrintCapabilities 檔時，需要太多額外負荷來保存快速變更的狀態資訊，例如筆墨層級、每個紙匣剩餘的紙張，或是紙匣狀態。</span><span class="sxs-lookup"><span data-stu-id="07a73-117">There is too much overhead involved in constructing the PrintCapabilities document for it to be used to hold rapidly changing status information, such as ink levels, paper remaining in each tray, or paper jam status.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07a73-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="07a73-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07a73-119">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="07a73-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




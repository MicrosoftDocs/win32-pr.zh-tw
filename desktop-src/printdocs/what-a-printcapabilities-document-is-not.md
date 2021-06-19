---
description: 瞭解 PrintCapabilities 檔不打算提供的部分功能和資訊。
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: PrintCapabilities 檔不是什麼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcd5dbedf6ee3a7e2713bd3591b182c606cfb0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409891"
---
# <a name="what-a-printcapabilities-document-is-not"></a><span data-ttu-id="be835-103">PrintCapabilities 檔不是什麼</span><span class="sxs-lookup"><span data-stu-id="be835-103">What a PrintCapabilities Document Is Not</span></span>

<span data-ttu-id="be835-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="be835-104">This topic is not current.</span></span> <span data-ttu-id="be835-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="be835-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="be835-106">您可以列出 PrintCapabilities 檔不打算提供的部分功能和資訊。</span><span class="sxs-lookup"><span data-stu-id="be835-106">It is worthwhile to list some of the functionality and information the PrintCapabilities document is not intended to provide.</span></span>

<span data-ttu-id="be835-107">PrintCapabilities 檔：</span><span class="sxs-lookup"><span data-stu-id="be835-107">A PrintCapabilities document:</span></span>

-   <span data-ttu-id="be835-108">不代表 (設定相依) 資料的多重值。</span><span class="sxs-lookup"><span data-stu-id="be835-108">Does not represent multivalued (configuration-dependent) data.</span></span>

    <span data-ttu-id="be835-109">每個 PrintCapabilities 檔都是針對特定設定所建立。</span><span class="sxs-lookup"><span data-stu-id="be835-109">Each PrintCapabilities document is constructed for a specific configuration.</span></span> <span data-ttu-id="be835-110">檔中沒有任何屬性或 ScoredProperty 可以有相依于特定設定的值。</span><span class="sxs-lookup"><span data-stu-id="be835-110">No Property or ScoredProperty in the document can have a Value that depends on the particular configuration.</span></span> <span data-ttu-id="be835-111">在初始架構版本中，PrintCapabilities 提供者必須處理輸入 PrintTicket，然後建立 PrintCapabilities 檔，其中包含適用于 PrintTicket 中所指定設定的屬性值。</span><span class="sxs-lookup"><span data-stu-id="be835-111">In the initial schema version, the PrintCapabilities provider must process the input PrintTicket and create a PrintCapabilities document that contains Property values appropriate for the configuration specified in the PrintTicket.</span></span>

-   <span data-ttu-id="be835-112">不包含條件約束資訊。</span><span class="sxs-lookup"><span data-stu-id="be835-112">Does not contain constraint information.</span></span>

    <span data-ttu-id="be835-113">PrintCapabilities 檔不會指出允許哪些設定，哪些是不允許的設定。</span><span class="sxs-lookup"><span data-stu-id="be835-113">The PrintCapabilities document does not indicate which configurations are allowed and which are not allowed.</span></span> <span data-ttu-id="be835-114">在初始架構版本中，PrintCapabilities 提供者必須儲存驗證設定所需的任何資訊、提供驗證輸入 PrintTicket 的方法，並在指定的 PrintTicket 違反一或多個條件約束的情況下傳回更正的 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="be835-114">In the initial schema version, the PrintCapabilities provider must store any information needed to validate configurations, supply a method that validates the input PrintTicket, and return a corrected PrintTicket in the event that the specified PrintTicket violates one or more constraints.</span></span>

-   <span data-ttu-id="be835-115">不包含動態裝置資訊。</span><span class="sxs-lookup"><span data-stu-id="be835-115">Does not contain dynamic device information.</span></span>

    <span data-ttu-id="be835-116">建立 PrintCapabilities 檔時，需要太多額外負荷來保存快速變更的狀態資訊，例如筆墨層級、每個紙匣剩餘的紙張，或是紙匣狀態。</span><span class="sxs-lookup"><span data-stu-id="be835-116">There is too much overhead involved in constructing the PrintCapabilities document for it to be used to hold rapidly changing status information, such as ink levels, paper remaining in each tray, or paper jam status.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be835-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="be835-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be835-118">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="be835-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




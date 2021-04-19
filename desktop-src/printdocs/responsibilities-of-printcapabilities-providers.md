---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: PrintCapabilities 提供者的責任
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bbf355f7b62f8f9c8b3f3b0c59714cdd6ade5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106974776"
---
# <a name="responsibilities-of-printcapabilities-providers"></a><span data-ttu-id="968d6-104">PrintCapabilities 提供者的責任</span><span class="sxs-lookup"><span data-stu-id="968d6-104">Responsibilities of PrintCapabilities Providers</span></span>

<span data-ttu-id="968d6-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="968d6-105">This topic is not current.</span></span> <span data-ttu-id="968d6-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="968d6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="968d6-107">PrintCapabilities 提供者必須支援 PrintTicket/PrintCapabilities 提供者介面所隱含的最小一組功能。</span><span class="sxs-lookup"><span data-stu-id="968d6-107">PrintCapabilities providers must support a minimum set of capabilities, which are implied by the PrintTicket/PrintCapabilities Provider Interface.</span></span> <span data-ttu-id="968d6-108">這裡列出這些功能。</span><span class="sxs-lookup"><span data-stu-id="968d6-108">These capabilities are listed here.</span></span>

-   <span data-ttu-id="968d6-109">它們必須遵循傳播的方向嗎？XML 屬性（當它出現在適當的內容中，並且包含該內容的有效值時）。</span><span class="sxs-lookup"><span data-stu-id="968d6-109">They must follow the direction of the propagate??XML attribute, when it appears in the appropriate context and contains a valid value for that context.</span></span>

-   <span data-ttu-id="968d6-110">它們必須產生符合 PrintCapabilities 架構的 PrintCapabilities 檔，並滿足列印架構中所指定的需求。</span><span class="sxs-lookup"><span data-stu-id="968d6-110">They must generate a PrintCapabilities document that conforms to the PrintCapabilities Schema and satisfies the requirements specified in the Print Schema.</span></span>

-   <span data-ttu-id="968d6-111">他們必須能夠辨識有效的 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="968d6-111">They must be able to recognize a valid PrintTicket.</span></span>

-   <span data-ttu-id="968d6-112">他們必須能夠解讀 PrintTicket，並瞭解它所代表的特定設定。</span><span class="sxs-lookup"><span data-stu-id="968d6-112">They must be able to interpret a PrintTicket and understand the specific configuration it represents.</span></span>

-   <span data-ttu-id="968d6-113">他們必須能夠判斷該設定是否包含條件約束衝突。</span><span class="sxs-lookup"><span data-stu-id="968d6-113">They must be able to determine whether that configuration contains constraint conflicts.</span></span>

-   <span data-ttu-id="968d6-114">它們必須能夠修改無效或衝突的 PrintTicket，方法是進行必要的最少重大變更，使其有效且不會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="968d6-114">They must be able to modify an invalid or conflicting PrintTicket by making the least significant change necessary to make it both valid and without conflicts.</span></span>

-   <span data-ttu-id="968d6-115">他們必須能夠產生特定裝置設定的 PrintCapabilities 檔。</span><span class="sxs-lookup"><span data-stu-id="968d6-115">They must be able to generate a PrintCapabilities document for a particular device configuration.</span></span>

-   <span data-ttu-id="968d6-116">他們必須能夠產生預設設定或 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="968d6-116">They must be able to generate a default configuration or PrintTicket.</span></span>

-   <span data-ttu-id="968d6-117">他們必須能夠產生對應至預設設定的 PrintCapabilities 檔。</span><span class="sxs-lookup"><span data-stu-id="968d6-117">They must be able to generate a PrintCapabilities document that corresponds to the default configuration.</span></span>

-   <span data-ttu-id="968d6-118">他們必須實行設備磁碟機所定義的選項評分程式，能夠判斷屬於相同功能的兩個選項實例之間的相符接近程度。</span><span class="sxs-lookup"><span data-stu-id="968d6-118">They must implement an Option-scoring process defined by the device driver capable of determining the closeness of match between two Option instances that belong to the same Feature.</span></span> <span data-ttu-id="968d6-119">此演算法用於 PrintTicket 驗證程式。</span><span class="sxs-lookup"><span data-stu-id="968d6-119">This algorithm is used in the PrintTicket validation process.</span></span>

<span data-ttu-id="968d6-120">除了上述需求以外，PrintCapabilities 檔必須針對每個 XML 屬性包含有效且正確的值 (例如，每個選項的限制) 。</span><span class="sxs-lookup"><span data-stu-id="968d6-120">In addition to the foregoing requirements, the PrintCapabilities document must contain valid and correct values for each XML attribute (for example, constrained) of each Option.</span></span>

## <a name="related-topics"></a><span data-ttu-id="968d6-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="968d6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="968d6-122">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="968d6-122">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: 列印架構公用關鍵字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3e8fb9a46bbed2b135f4e81456dd65e79be830
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106986684"
---
# <a name="print-schema-public-keywords"></a><span data-ttu-id="7bf5a-104">列印架構公用關鍵字</span><span class="sxs-lookup"><span data-stu-id="7bf5a-104">Print Schema Public Keywords</span></span>

<span data-ttu-id="7bf5a-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="7bf5a-105">This topic is not current.</span></span> <span data-ttu-id="7bf5a-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="7bf5a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7bf5a-107">下一節指定針對列印架構定義的公用關鍵字。</span><span class="sxs-lookup"><span data-stu-id="7bf5a-107">The following section specifies the public keywords which are defined for the Print Schema.</span></span>

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a><span data-ttu-id="7bf5a-108">列印功能的列印架構公用關鍵字用法</span><span class="sxs-lookup"><span data-stu-id="7bf5a-108">Print Schema Public Keywords Usage for Print Capabilities</span></span>

<span data-ttu-id="7bf5a-109">在 PrintCapabilities Public 關鍵字下指定的關鍵字可能會顯示在列印功能檔中。</span><span class="sxs-lookup"><span data-stu-id="7bf5a-109">Keywords specified under PrintCapabilities Public Keywords MAY appear in a Print Capabilities document.</span></span> <span data-ttu-id="7bf5a-110">如需這些關鍵字如何與 PrintCapabilities 技術互動的詳細資訊，請參閱 [PrintCapabilities](overview-of-the-printcapabilities.md) 一節的總覽。</span><span class="sxs-lookup"><span data-stu-id="7bf5a-110">For more information on how these keywords interact with PrintCapabilities technology, please refer to [Overview of the PrintCapabilities](overview-of-the-printcapabilities.md) section.</span></span>

<span data-ttu-id="7bf5a-111">PrintTicket 專屬的公用關鍵字不應該出現在 PrintCapabilities 檔中。</span><span class="sxs-lookup"><span data-stu-id="7bf5a-111">Public keywords specific to PrintTicket SHOULD NOT appear in a PrintCapabilities document.</span></span>

## <a name="print-schema-public-keywords-usage-for-printticket"></a><span data-ttu-id="7bf5a-112">列印 PrintTicket 的架構公用關鍵字用法</span><span class="sxs-lookup"><span data-stu-id="7bf5a-112">Print Schema Public Keywords Usage for PrintTicket</span></span>

<span data-ttu-id="7bf5a-113">在 PrintTicket Public 關鍵字下指定的關鍵字可能會出現在 PrintTicket 中。</span><span class="sxs-lookup"><span data-stu-id="7bf5a-113">Keywords specified under PrintTicket Public Keywords MAY appear in a PrintTicket.</span></span> <span data-ttu-id="7bf5a-114">PrintTicket 關鍵字會實作為屬性元素類型。</span><span class="sxs-lookup"><span data-stu-id="7bf5a-114">PrintTicket keywords are implemented as a Property element type.</span></span> <span data-ttu-id="7bf5a-115">如需這些關鍵字如何與 PrintTicket 技術互動的詳細資訊，請參閱與 PrintCapabilities 無關的設定 [資訊](configuration-information-not-related-to-printcapabilities.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="7bf5a-115">For more information on how these keywords interact with PrintTicket technology, please refer to [Configuration Information Not Related to PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) section.</span></span>

<span data-ttu-id="7bf5a-116">在 PrintCapabilities Public 關鍵字下指定的關鍵字，可能會根據應用程式和（或）驅動程式中的 PrintTicket 執行而出現在 PrintTicket 中。</span><span class="sxs-lookup"><span data-stu-id="7bf5a-116">Keywords specified under PrintCapabilities Public Keywords MAY appear in a PrintTicket depending on the implementation of the PrintTicket in an application and/or driver.</span></span> <span data-ttu-id="7bf5a-117">這會針對 PrintCapabilities 檔中定義的裝置屬性提供選取專案。</span><span class="sxs-lookup"><span data-stu-id="7bf5a-117">This provides selections for device attributes defined in the PrintCapabilities document.</span></span> <span data-ttu-id="7bf5a-118">如需 PrintCapabilities 關鍵字與 PrintTicket 之間互動的詳細資訊，請參閱 PrintTicket 區段的 [用途](purpose-of-the-printticket.md) 。</span><span class="sxs-lookup"><span data-stu-id="7bf5a-118">For more information on the interaction between PrintCapabilities keywords and the PrintTicket, please refer to [Purpose of the PrintTicket](purpose-of-the-printticket.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bf5a-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="7bf5a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bf5a-120">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="7bf5a-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




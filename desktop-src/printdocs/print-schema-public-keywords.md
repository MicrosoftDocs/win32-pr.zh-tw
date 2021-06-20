---
description: 本文指定針對列印架構定義的公用關鍵字，以及其 PrintCapabilities 和 PrintTicket 的使用方式。
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: 列印架構公用關鍵字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0878ced6b011393479657a4fcdd4b7b7f9a2b62a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407141"
---
# <a name="print-schema-public-keywords"></a><span data-ttu-id="da57d-103">列印架構公用關鍵字</span><span class="sxs-lookup"><span data-stu-id="da57d-103">Print Schema Public Keywords</span></span>

<span data-ttu-id="da57d-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="da57d-104">This topic is not current.</span></span> <span data-ttu-id="da57d-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="da57d-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="da57d-106">下一節指定針對列印架構定義的公用關鍵字。</span><span class="sxs-lookup"><span data-stu-id="da57d-106">The following section specifies the public keywords which are defined for the Print Schema.</span></span>

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a><span data-ttu-id="da57d-107">列印功能的列印架構公用關鍵字用法</span><span class="sxs-lookup"><span data-stu-id="da57d-107">Print Schema Public Keywords Usage for Print Capabilities</span></span>

<span data-ttu-id="da57d-108">在 PrintCapabilities Public 關鍵字下指定的關鍵字可能會顯示在列印功能檔中。</span><span class="sxs-lookup"><span data-stu-id="da57d-108">Keywords specified under PrintCapabilities Public Keywords MAY appear in a Print Capabilities document.</span></span> <span data-ttu-id="da57d-109">如需這些關鍵字如何與 PrintCapabilities 技術互動的詳細資訊，請參閱 [PrintCapabilities](overview-of-the-printcapabilities.md) 一節的總覽。</span><span class="sxs-lookup"><span data-stu-id="da57d-109">For more information on how these keywords interact with PrintCapabilities technology, please refer to [Overview of the PrintCapabilities](overview-of-the-printcapabilities.md) section.</span></span>

<span data-ttu-id="da57d-110">PrintTicket 專屬的公用關鍵字不應該出現在 PrintCapabilities 檔中。</span><span class="sxs-lookup"><span data-stu-id="da57d-110">Public keywords specific to PrintTicket SHOULD NOT appear in a PrintCapabilities document.</span></span>

## <a name="print-schema-public-keywords-usage-for-printticket"></a><span data-ttu-id="da57d-111">列印 PrintTicket 的架構公用關鍵字用法</span><span class="sxs-lookup"><span data-stu-id="da57d-111">Print Schema Public Keywords Usage for PrintTicket</span></span>

<span data-ttu-id="da57d-112">在 PrintTicket Public 關鍵字下指定的關鍵字可能會出現在 PrintTicket 中。</span><span class="sxs-lookup"><span data-stu-id="da57d-112">Keywords specified under PrintTicket Public Keywords MAY appear in a PrintTicket.</span></span> <span data-ttu-id="da57d-113">PrintTicket 關鍵字會實作為屬性元素類型。</span><span class="sxs-lookup"><span data-stu-id="da57d-113">PrintTicket keywords are implemented as a Property element type.</span></span> <span data-ttu-id="da57d-114">如需這些關鍵字如何與 PrintTicket 技術互動的詳細資訊，請參閱與 PrintCapabilities 無關的設定 [資訊](configuration-information-not-related-to-printcapabilities.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="da57d-114">For more information on how these keywords interact with PrintTicket technology, please refer to [Configuration Information Not Related to PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) section.</span></span>

<span data-ttu-id="da57d-115">在 PrintCapabilities Public 關鍵字下指定的關鍵字，可能會根據應用程式和（或）驅動程式中的 PrintTicket 執行而出現在 PrintTicket 中。</span><span class="sxs-lookup"><span data-stu-id="da57d-115">Keywords specified under PrintCapabilities Public Keywords MAY appear in a PrintTicket depending on the implementation of the PrintTicket in an application and/or driver.</span></span> <span data-ttu-id="da57d-116">這會針對 PrintCapabilities 檔中定義的裝置屬性提供選取專案。</span><span class="sxs-lookup"><span data-stu-id="da57d-116">This provides selections for device attributes defined in the PrintCapabilities document.</span></span> <span data-ttu-id="da57d-117">如需 PrintCapabilities 關鍵字與 PrintTicket 之間互動的詳細資訊，請參閱 PrintTicket 區段的 [用途](purpose-of-the-printticket.md) 。</span><span class="sxs-lookup"><span data-stu-id="da57d-117">For more information on the interaction between PrintCapabilities keywords and the PrintTicket, please refer to [Purpose of the PrintTicket](purpose-of-the-printticket.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da57d-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="da57d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da57d-119">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="da57d-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




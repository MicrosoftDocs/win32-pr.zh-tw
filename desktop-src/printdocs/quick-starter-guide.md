---
description: 本文可讓您快速開始為應用程式或設備磁碟機實行 PrintTicket 和 PrintCapabilities。
ms.assetid: 2c1d912e-464e-48d2-ba4f-c0b9a811b25e
title: 快速入門手冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6060de551d3fb663e148cf80f661c4d517a51b93
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405311"
---
# <a name="quick-starter-guide"></a><span data-ttu-id="1dbfd-103">快速入門手冊</span><span class="sxs-lookup"><span data-stu-id="1dbfd-103">Quick Starter Guide</span></span>

<span data-ttu-id="1dbfd-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="1dbfd-104">This topic is not current.</span></span> <span data-ttu-id="1dbfd-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="1dbfd-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1dbfd-106">此頁面的設計目的是讓您快速開始為應用程式或設備磁碟機實行 PrintTicket 和 PrintCapabilities。</span><span class="sxs-lookup"><span data-stu-id="1dbfd-106">This page is designed to give you a quick start to implement PrintTicket and PrintCapabilities for your application or device driver.</span></span> <span data-ttu-id="1dbfd-107">雖然我們建議您完整閱讀列印架構規格，但此頁面可協助您快速開始使用您應該注意的重要區域。</span><span class="sxs-lookup"><span data-stu-id="1dbfd-107">Although we encourage that you read the Print Schema specification in full, this page will help give you a jump start in key areas you should pay attention to.</span></span>

1) <span data-ttu-id="1dbfd-108">閱讀 [列印 Schema-Related 技術](print-schema-related-technologies.md) ，以概述您的 PrintTicket 和列印功能技術</span><span class="sxs-lookup"><span data-stu-id="1dbfd-108">Read the [Print Schema-Related Technologies](print-schema-related-technologies.md) to give you an overview of PrintTicket and Print Capabilities technologies</span></span>

2) <span data-ttu-id="1dbfd-109">確定您已掌握用來表示列印架構相關技術的 [元素類型摘要](summary-of-element-types.md) 。</span><span class="sxs-lookup"><span data-stu-id="1dbfd-109">Ensure that you have a grasp on the [Summary of Element Types](summary-of-element-types.md) which are used to express Print Schema related technologies.</span></span>

3) <span data-ttu-id="1dbfd-110">PrintCapabilities 檔和 PrintTickets 定義在三個 [範圍的前置](scoping-prefix.md) 詞層級、作業、檔和頁面上。</span><span class="sxs-lookup"><span data-stu-id="1dbfd-110">PrintCapabilities documents and PrintTickets are defined at three [Scoping Prefix](scoping-prefix.md) levels, Job, Document and Page.</span></span>

4) <span data-ttu-id="1dbfd-111">讀取不同的 [XML 屬性](xml-attributes.md) ，這些屬性會用於不同的列印架構元素類型中</span><span class="sxs-lookup"><span data-stu-id="1dbfd-111">Read over the different [XML Attributes](xml-attributes.md) which are used within different Print Schema element types</span></span>

5) <span data-ttu-id="1dbfd-112">複習 [PrintCapabilities 檔結構檢查清單](printcapabilities-document-construction-checklist.md) ，以及所提供的 [PrintCapabilities 檔範例](printcapabilities-document-example.md)</span><span class="sxs-lookup"><span data-stu-id="1dbfd-112">Review the [PrintCapabilities Document Construction Checklist](printcapabilities-document-construction-checklist.md) and also the provided [PrintCapabilities Document Example](printcapabilities-document-example.md)</span></span>

6) <span data-ttu-id="1dbfd-113">查看 [Printticket 結構檢查](printticket-construction-checklists.md) 清單，以及所提供的 [printticket 範例](printticket-example.md)</span><span class="sxs-lookup"><span data-stu-id="1dbfd-113">Review the [PrintTicket Construction Checklists](printticket-construction-checklists.md) and also the provided [PrintTicket Example](printticket-example.md)</span></span>

7) <span data-ttu-id="1dbfd-114">PrintTicket 提供者也應查看 [Printticket 驗證檢查清單](printticket-validation-checklist.md) ，以確保符合 PrintSchema 規格</span><span class="sxs-lookup"><span data-stu-id="1dbfd-114">PrintTicket providers should also review the [PrintTicket Validation Checklist](printticket-validation-checklist.md) to ensure conformance with the PrintSchema specification</span></span>

8) <span data-ttu-id="1dbfd-115">檢查可在 PrintCapabilities 檔中顯示的 [使用者可設定元素](user-configurable-elements.md) 和 [參數定義](parameter-definitions.md) 公用列印架構關鍵字</span><span class="sxs-lookup"><span data-stu-id="1dbfd-115">Review both [User Configurable Elements](user-configurable-elements.md) and [Parameter Definitions](parameter-definitions.md) public Print Schema keywords which may appear in a PrintCapabilities document</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dbfd-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="1dbfd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dbfd-117">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="1dbfd-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




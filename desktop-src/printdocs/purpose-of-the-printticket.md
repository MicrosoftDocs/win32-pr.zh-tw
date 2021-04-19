---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 8a7dd185-0324-44a0-8405-59a2fdc1efcb
title: PrintTicket 的用途
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a191f341504a92fbb5f4cd00abd2a4357bbecf21
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106993800"
---
# <a name="purpose-of-the-printticket"></a><span data-ttu-id="83ddc-104">PrintTicket 的用途</span><span class="sxs-lookup"><span data-stu-id="83ddc-104">Purpose of the PrintTicket</span></span>

<span data-ttu-id="83ddc-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="83ddc-105">This topic is not current.</span></span> <span data-ttu-id="83ddc-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="83ddc-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="83ddc-107">PrintTicket 的主要目的是要表示裝置設定。</span><span class="sxs-lookup"><span data-stu-id="83ddc-107">The primary purpose of the PrintTicket is to express device configurations.</span></span> <span data-ttu-id="83ddc-108">相較于 PrintCapabilities 檔，它會定義裝置可採用 (裝置設定空間) 的所有可能設定，而 PrintTicket 的目的是要定義套用至工作物件的單一特定設定，在此案例中是要處理的頁面)  (。</span><span class="sxs-lookup"><span data-stu-id="83ddc-108">In contrast to the PrintCapabilities document, which defines all possible configurations the device can assume (the device's configuration space), the PrintTicket's purpose is to define a single specific configuration that is applied to the job object (in this case the page) that is being processed.</span></span> <span data-ttu-id="83ddc-109">為了提升設定的可攜性和一致性，PrintCapabilities 和 PrintTicket 技術會使用列印架構關鍵字區段中所呈現的特定關鍵字和階層。</span><span class="sxs-lookup"><span data-stu-id="83ddc-109">To promote portability and consistency of configurations, the specific keywords and hierarchy presented in the Print Schema Keywords section are used by both the PrintCapabilities and the PrintTicket technologies.</span></span> <span data-ttu-id="83ddc-110">此外， [Print Schema Framework](print-schema-framework.md) 也定義了這兩種技術的基本結構，以促進明確、開放且可延伸的作業格式和 PrintCapabilities 通訊。</span><span class="sxs-lookup"><span data-stu-id="83ddc-110">In addition, the [Print Schema Framework](print-schema-framework.md) defines the basic constructs of both technologies, to promote unambiguous, open, and extensible communication of job formatting and PrintCapabilities.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83ddc-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="83ddc-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83ddc-112">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="83ddc-112">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




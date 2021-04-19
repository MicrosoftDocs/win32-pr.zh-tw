---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: PrintTicket 結構檢查清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e742bcd3b94c5016fda6f97e2fb5e20a2cf70f73
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106981751"
---
# <a name="printticket-construction-checklists"></a><span data-ttu-id="b8e63-104">PrintTicket 結構檢查清單</span><span class="sxs-lookup"><span data-stu-id="b8e63-104">PrintTicket Construction Checklists</span></span>

<span data-ttu-id="b8e63-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="b8e63-105">This topic is not current.</span></span> <span data-ttu-id="b8e63-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="b8e63-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b8e63-107">本節將示範 PrintTicket 用戶端的作者如何使用在 Print Schema Framework 中定義的元素類型，來建立可描述裝置意圖的 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="b8e63-107">This section demonstrates how the author of a PrintTicket client can use the element types defined in the Print Schema Framework to create a PrintTicket that describes intents for a device.</span></span> <span data-ttu-id="b8e63-108">PrintTicket 可以是泛型 (未系結至特定裝置) ，也可以是裝置特定的。</span><span class="sxs-lookup"><span data-stu-id="b8e63-108">The PrintTicket can be generic (not tied to a specific device), or it can be device-specific.</span></span> <span data-ttu-id="b8e63-109">會更詳細地呈現 PrintTicket 的語法。</span><span class="sxs-lookup"><span data-stu-id="b8e63-109">The semantics of the PrintTicket are presented in greater detail.</span></span> <span data-ttu-id="b8e63-110">此外，本節還包含一些概念和術語的總覽，這些概念和術語在後續章節中有更深入的討論。</span><span class="sxs-lookup"><span data-stu-id="b8e63-110">In addition, this section contains an overview of concepts and terminology that are covered in more depth in subsequent sections.</span></span>

<span data-ttu-id="b8e63-111">有兩種本質上不同的方法可以用來建立 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="b8e63-111">There are two fundamentally different approaches to constructing a PrintTicket.</span></span> <span data-ttu-id="b8e63-112">這兩種方法都可以使用。</span><span class="sxs-lookup"><span data-stu-id="b8e63-112">Either approach can be used.</span></span>

-   <span data-ttu-id="b8e63-113">藉由 [建立一般的 printticket](creating-a-generic-printticket.md)，將 PrintTicket 的目標設為未知或一般裝置。</span><span class="sxs-lookup"><span data-stu-id="b8e63-113">Target the PrintTicket to an unknown or generic device by [Creating a Generic PrintTicket](creating-a-generic-printticket.md).</span></span>

    <span data-ttu-id="b8e63-114">如果您的主要目標是要保留使用者的意圖，您可能會想要採用這種方法，方法是使用檔來建立和儲存未經驗證一般 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="b8e63-114">If your primary objective is to preserve the end user's intent, you might want to take this approach, by constructing and storing an unvalidated generic PrintTicket with the document.</span></span>

-   <span data-ttu-id="b8e63-115">藉由 [建立 Device-Specific 的 printticket](creating-a-device-specific-printticket.md)，將 printticket 的目標設為特定裝置。</span><span class="sxs-lookup"><span data-stu-id="b8e63-115">Target the PrintTicket to a specific device, by [Creating a Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span></span>

    <span data-ttu-id="b8e63-116">如果您想要充分利用特定裝置所提供的所有功能，您可能會想要採用這種方法，方法是針對特定裝置建立 PrintTicket，並將驗證的 PrintTicket 與檔一起儲存。</span><span class="sxs-lookup"><span data-stu-id="b8e63-116">If you are more interested in taking advantage of all of the features offered by a particular device, you might want to take this approach, by constructing a PrintTicket for the specific device and storing the validated PrintTicket with the document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8e63-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8e63-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8e63-118">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="b8e63-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




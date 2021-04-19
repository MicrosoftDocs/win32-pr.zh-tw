---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: PrintCapabilities 檔的取用者責任
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b74cfc1885ecc5599365bc6eadcef30ef4c4ae3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106997602"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a><span data-ttu-id="19b97-104">PrintCapabilities 檔的取用者責任</span><span class="sxs-lookup"><span data-stu-id="19b97-104">Responsibilities of Consumers of the PrintCapabilities Document</span></span>

<span data-ttu-id="19b97-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="19b97-105">This topic is not current.</span></span> <span data-ttu-id="19b97-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="19b97-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="19b97-107">PrintCapabilities 檔的取用者必須先遵守某些義務，才能使用 PrintCapabilities 檔。</span><span class="sxs-lookup"><span data-stu-id="19b97-107">Consumers of PrintCapabilities documents have certain obligations they must uphold before they can use a PrintCapabilities document.</span></span> <span data-ttu-id="19b97-108">下列需求適用于 PrintCapabilities 檔的用戶端。</span><span class="sxs-lookup"><span data-stu-id="19b97-108">The following requirements apply to clients of a PrintCapabilities document.</span></span>

-   <span data-ttu-id="19b97-109">它們不得拒絕或無法處理任何語法有效的 PrintCapabilities;也就是符合 PrintCapabilities 架構的任何 PrintCapabilities 檔。</span><span class="sxs-lookup"><span data-stu-id="19b97-109">They must not reject or fail to process any syntactically valid PrintCapabilities; that is, any PrintCapabilities document that conforms to the PrintCapabilities Schema.</span></span>

-   <span data-ttu-id="19b97-110">他們必須能夠解決非預期的私用內容存在或不存在的情況。</span><span class="sxs-lookup"><span data-stu-id="19b97-110">They must be able to work around the unexpected presence or absence of privately-defined content.</span></span> <span data-ttu-id="19b97-111">這包括私用定義的內容，它會出現在 Print Schema 定義專案的實例內。</span><span class="sxs-lookup"><span data-stu-id="19b97-111">This includes privately-defined content that appears within instances of Print Schema-defined elements.</span></span>

-   <span data-ttu-id="19b97-112">他們必須能夠解決未存在的選擇性列印架構內容。</span><span class="sxs-lookup"><span data-stu-id="19b97-112">They must be able to work around optional Print Schema content that is absent.</span></span>

-   <span data-ttu-id="19b97-113">他們必須留意何時要求新檔。</span><span class="sxs-lookup"><span data-stu-id="19b97-113">They must be aware of when to request a new document.</span></span>

    -   <span data-ttu-id="19b97-114">屬性實例的值與設定相依 (因此，與快照集相依的) 。</span><span class="sxs-lookup"><span data-stu-id="19b97-114">Values of Property instances are configuration-dependent (hence, snapshot-dependent).</span></span> <span data-ttu-id="19b97-115">當您存取屬性實例時，必須更新快照集。</span><span class="sxs-lookup"><span data-stu-id="19b97-115">You must update the snapshot when you access a Property instance.</span></span>

    -   <span data-ttu-id="19b97-116">要複製到 PrintTicket 的功能、選項和 ScoredProperty 實例是以靜態定義為依據。</span><span class="sxs-lookup"><span data-stu-id="19b97-116">Feature, Option and ScoredProperty instances that are to be copied to a PrintTicket are by definition static.</span></span> <span data-ttu-id="19b97-117">也就是說，它們不 (，且不能) 依存于裝置設定。</span><span class="sxs-lookup"><span data-stu-id="19b97-117">That is, they are not (and must not be) dependent on the device configuration.</span></span> <span data-ttu-id="19b97-118">如果您存取這些類型的任何實例，當設定變更時，就不需要取得新的 PrintCapabilities 檔。</span><span class="sxs-lookup"><span data-stu-id="19b97-118">If you access any instances of these types, you do not need to obtain a new PrintCapabilities document when the configuration changes.</span></span>

-   <span data-ttu-id="19b97-119"> (UI) 用戶端使用者介面的 PrintCapabilities 取用者必須能夠使用 PrintCapabilities 檔中的資訊來建立使用者介面，並從使用者選取專案中建立有效的 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="19b97-119">Consumers of PrintCapabilities that are user interface (UI) clients must be able to use information in a PrintCapabilities document to construct a user interface and to construct a valid PrintTicket from the user selections.</span></span> <span data-ttu-id="19b97-120">這包括知道必須指定哪些 ParameterInit 實例，以及驗證所指定的實例。</span><span class="sxs-lookup"><span data-stu-id="19b97-120">This includes knowing which ParameterInit instances must be specified, and validating those instances that are specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19b97-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="19b97-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19b97-122">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="19b97-122">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




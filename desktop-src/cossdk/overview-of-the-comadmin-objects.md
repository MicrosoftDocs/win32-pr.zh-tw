---
description: COMAdmin 物件提供簡單的物件模型，可讓您存取 COM + 類別目錄。
ms.assetid: 84cee7a7-f7a6-41a0-afd5-fae56365612e
title: COMAdmin 物件的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22837cbe0548b623463234d1a03d17288eba2149
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111673"
---
# <a name="overview-of-the-comadmin-objects"></a><span data-ttu-id="b1636-103">COMAdmin 物件的總覽</span><span class="sxs-lookup"><span data-stu-id="b1636-103">Overview of the COMAdmin Objects</span></span>

<span data-ttu-id="b1636-104">COMAdmin 物件提供簡單的物件模型，可讓您存取 COM + 類別目錄。</span><span class="sxs-lookup"><span data-stu-id="b1636-104">The COMAdmin objects offer a simple object model that provides you with access to the COM+ catalog.</span></span> <span data-ttu-id="b1636-105">如此一來，他們就可以建立「元件服務」系統管理工具所提供的所有功能的模型。</span><span class="sxs-lookup"><span data-stu-id="b1636-105">In doing so, they serve to model all the functionality provided by the Component Services administrative tool.</span></span> <span data-ttu-id="b1636-106">每當您進行任何類型的 COM + 管理時，您都會與 COM + 類別目錄互動。</span><span class="sxs-lookup"><span data-stu-id="b1636-106">Whenever you do any kind of COM+ administration, you are interacting with the COM+ catalog.</span></span> <span data-ttu-id="b1636-107">如需目錄的描述，請參閱 [存取 COM + 類別目錄](accessing-the-com--catalog.md)。</span><span class="sxs-lookup"><span data-stu-id="b1636-107">For a description of the catalog, see [Accessing the COM+ Catalog](accessing-the-com--catalog.md).</span></span>

<span data-ttu-id="b1636-108">您從 [元件服務] 系統管理工具或使用 COMAdmin 物件取得的資訊結構類似，而且您在其中一個內容中執行的動作也類似。</span><span class="sxs-lookup"><span data-stu-id="b1636-108">The information you obtain either from the Component Services administrative tool or by using the COMAdmin objects is structured similarly, and the actions you perform in either context are analogous.</span></span> <span data-ttu-id="b1636-109">使用 [元件服務] 嵌入式管理單元和以程式設計方式管理的基本關聯性，是嵌入式管理單元的主控台樹中的資料夾，會對應至 COM + 目錄中的集合。</span><span class="sxs-lookup"><span data-stu-id="b1636-109">The basic correlation between using the Component Services snap-in and programmatic administration is that folders in the console tree of the snap-in correspond to collections in the COM+ catalog.</span></span> <span data-ttu-id="b1636-110">也就是說，就像嵌入式管理單元中的每個資料夾都包含各種專案，例如， **com + 應用程式** 會保存已安裝的 com + 應用程式，com + 目錄中的每個集合都會保存統一種類的專案。</span><span class="sxs-lookup"><span data-stu-id="b1636-110">That is, just as each folder in the snap-in contains items all of a kind; for example, **COM+ Applications** holds installed COM+ applications—each collection in the COM+ catalog holds items of a uniform kind.</span></span> <span data-ttu-id="b1636-111">此外，如同資料夾中的每個專案都有可在屬性工作表上設定的屬性，集合中的每個專案都會公開您可以設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="b1636-111">Further, just as each item in a folder has properties that you can set on a property sheet, each item in a collection exposes properties that you can set.</span></span>

<span data-ttu-id="b1636-112">為了讓您能夠設定此結構內的物件，COMAdmin 物件會提供您執行下列動作的方法：</span><span class="sxs-lookup"><span data-stu-id="b1636-112">To enable you to configure objects within this structure, the COMAdmin objects provide you with the means to do the following:</span></span>

-   <span data-ttu-id="b1636-113">存取 COM + 類別目錄</span><span class="sxs-lookup"><span data-stu-id="b1636-113">Access the COM+ catalog</span></span>
-   <span data-ttu-id="b1636-114">存取目錄中的集合</span><span class="sxs-lookup"><span data-stu-id="b1636-114">Access collections in the catalog</span></span>
-   <span data-ttu-id="b1636-115">存取集合中的專案</span><span class="sxs-lookup"><span data-stu-id="b1636-115">Access items in collections</span></span>
-   <span data-ttu-id="b1636-116">存取集合中專案的屬性</span><span class="sxs-lookup"><span data-stu-id="b1636-116">Access properties on the items in the collections</span></span>

<span data-ttu-id="b1636-117">為了支援這些動作，COMAdmin 程式庫提供下列三個類別：</span><span class="sxs-lookup"><span data-stu-id="b1636-117">To support these actions, the COMAdmin Library provides the following three classes:</span></span>

-   <span data-ttu-id="b1636-118">[**COMAdminCatalog**](comadmincatalog.md)，代表目錄本身。</span><span class="sxs-lookup"><span data-stu-id="b1636-118">[**COMAdminCatalog**](comadmincatalog.md), which represents the catalog itself.</span></span>
-   <span data-ttu-id="b1636-119">[**COMAdminCatalogCollection**](comadmincatalogcollection.md)，表示任何集合。</span><span class="sxs-lookup"><span data-stu-id="b1636-119">[**COMAdminCatalogCollection**](comadmincatalogcollection.md), which represents any collection.</span></span>
-   <span data-ttu-id="b1636-120">[**COMAdminCatalogObject**](comadmincatalogobject.md)，代表集合中的任何專案。</span><span class="sxs-lookup"><span data-stu-id="b1636-120">[**COMAdminCatalogObject**](comadmincatalogobject.md), which represents any item in a collection.</span></span>

<span data-ttu-id="b1636-121">如需這些類別的完整說明，請參閱本節中 [COMAdmin 類別的摘要描述](summary-description-of-the-comadmin-classes.md) 。</span><span class="sxs-lookup"><span data-stu-id="b1636-121">For fuller descriptions of these classes, see [Summary Description of the COMAdmin Classes](summary-description-of-the-comadmin-classes.md) in this section.</span></span>

<span data-ttu-id="b1636-122">若要快速瞭解您在程式設計管理中執行的一般動作，請參閱 [使用 COM + 系統管理目錄的簡介範例](introductory-example-using-the-com--administration-catalog.md)。</span><span class="sxs-lookup"><span data-stu-id="b1636-122">To get a quick idea of typical actions you perform in programmatic administration, see [Introductory Example Using the COM+ Administration Catalog](introductory-example-using-the-com--administration-catalog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1636-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="b1636-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1636-124">交易內的 COM + 管理作業</span><span class="sxs-lookup"><span data-stu-id="b1636-124">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="b1636-125">處理 COM + 管理錯誤</span><span class="sxs-lookup"><span data-stu-id="b1636-125">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="b1636-126">使用 COM + 系統管理目錄的簡介範例</span><span class="sxs-lookup"><span data-stu-id="b1636-126">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="b1636-127">在 COM + 類別目錄上取出集合</span><span class="sxs-lookup"><span data-stu-id="b1636-127">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="b1636-128">設定屬性並將變更儲存至 COM + 類別目錄</span><span class="sxs-lookup"><span data-stu-id="b1636-128">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 




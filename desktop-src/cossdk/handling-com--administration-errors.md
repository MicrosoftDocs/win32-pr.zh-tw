---
description: 處理 COM + 管理錯誤
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: 處理 COM + 管理錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e5838d7fee7616a23f5e361df1aef65421492
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973392"
---
# <a name="handling-com-administration-errors"></a><span data-ttu-id="19d05-103">處理 COM + 管理錯誤</span><span class="sxs-lookup"><span data-stu-id="19d05-103">Handling COM+ Administration Errors</span></span>

<span data-ttu-id="19d05-104">使用 COMAdmin 物件時所產生的錯誤會以兩種方式報告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="19d05-104">Errors that are generated when using the COMAdmin objects are reported in two ways, as follows:</span></span>

-   <span data-ttu-id="19d05-105">使用 COMAdmin 程式庫特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="19d05-105">Using error codes specific to the COMAdmin library.</span></span>
-   <span data-ttu-id="19d05-106">使用特殊 [**ErrorInfo**](errorinfo.md) 集合中可用的擴充錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="19d05-106">Using extended error information available in a special [**ErrorInfo**](errorinfo.md) collection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="19d05-107">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="19d05-107">Error Codes</span></span>

<span data-ttu-id="19d05-108">您可以處理管理錯誤碼，就像任何 COM 錯誤訊息一樣。</span><span class="sxs-lookup"><span data-stu-id="19d05-108">You handle administration error codes as you would any COM error message.</span></span> <span data-ttu-id="19d05-109">在 Microsoft Visual C++ 中，這些代碼會以 **HRESULT** 值的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="19d05-109">In Microsoft Visual C++, these codes are returned as **HRESULT** values.</span></span> <span data-ttu-id="19d05-110">在 Microsoft Visual Basic 中，它們會被視為您可以攔截的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="19d05-110">In Microsoft Visual Basic, they are thrown as exceptions that you can catch.</span></span> <span data-ttu-id="19d05-111">針對 c + + 程式設計人員，COM + 系統管理錯誤碼定義于 Winerror.h 中。</span><span class="sxs-lookup"><span data-stu-id="19d05-111">For C++ programmers, the COM+ administration error codes are defined in Winerror.h.</span></span> <span data-ttu-id="19d05-112">針對 Visual Basic 程式設計人員，可以透過 Visual Basic IDE 取得。</span><span class="sxs-lookup"><span data-stu-id="19d05-112">For Visual Basic programmers, they are available through the Visual Basic IDE.</span></span>

## <a name="errorinfo-collection"></a><span data-ttu-id="19d05-113">ErrorInfo 集合</span><span class="sxs-lookup"><span data-stu-id="19d05-113">ErrorInfo Collection</span></span>

<span data-ttu-id="19d05-114">發生錯誤時，會有某種失敗代碼的信號，視錯誤的性質而定，可能會提供更詳細的資訊。</span><span class="sxs-lookup"><span data-stu-id="19d05-114">When an error occurs, signaled by some kind of failure code, more detailed information may be available, depending on the nature of the error.</span></span> <span data-ttu-id="19d05-115">COMAdmin 物件提供延伸的資訊，在不需要詳細的報表（例如，有多個讀取和寫入作業）的情況下，可能會難以判斷失敗的確切原因。</span><span class="sxs-lookup"><span data-stu-id="19d05-115">The COMAdmin objects provide extended information in circumstances where the precise cause of the failure is difficult to determine without a detailed report, such as with multiple read and write operations.</span></span>

<span data-ttu-id="19d05-116">例如，當您在 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件上使用 [**填入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate)和 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)之類的方法時，您可以針對集合中的每個專案讀取或寫入資料。</span><span class="sxs-lookup"><span data-stu-id="19d05-116">For example, when you use methods such as [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on a [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, you can be reading or writing data for every item in the collection.</span></span> <span data-ttu-id="19d05-117">可能會發生複雜的錯誤，而且可能很難根據單一數值錯誤碼進行診斷。</span><span class="sxs-lookup"><span data-stu-id="19d05-117">Complicated errors can occur, and they can be difficult to diagnose based on a single numeric error code.</span></span> <span data-ttu-id="19d05-118">因此，COMAdmin 程式庫會透過特殊的集合來提供延伸的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="19d05-118">Therefore, the COMAdmin Library makes extended error information through a special collection.</span></span>

<span data-ttu-id="19d05-119">當有擴充的錯誤資訊可用時，它會放在與發生錯誤的原創組合相關的 [**ErrorInfo**](errorinfo.md) 集合中。</span><span class="sxs-lookup"><span data-stu-id="19d05-119">When extended error information is available, it is placed in the [**ErrorInfo**](errorinfo.md) collection that is related to the original collection that had the error.</span></span> <span data-ttu-id="19d05-120">若要取得錯誤報表，請取得與原創組合相關的 **ErrorInfo** 集合，並檢查它包含的專案。</span><span class="sxs-lookup"><span data-stu-id="19d05-120">To retrieve the error report, get the **ErrorInfo** collection that is related to the original collection and examine the items it contains.</span></span> <span data-ttu-id="19d05-121">您可以在 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)上使用 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection)來取出 **ErrorInfo** 集合，將第二個參數保留空白，您通常會在此指定父專案的索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="19d05-121">You can retrieve the **ErrorInfo** collection by using [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) on [**COMAdminCatalogCollection**](comadmincatalogcollection.md), leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

<span data-ttu-id="19d05-122">當您收到錯誤時，您必須立即取得並填入失敗之集合的 [**ErrorInfo**](errorinfo.md) 集合，而不會對該集合執行任何其他作業。</span><span class="sxs-lookup"><span data-stu-id="19d05-122">When you get an error, you must immediately get and populate the [**ErrorInfo**](errorinfo.md) collection for the collection that failed, without performing any other operations on that collection.</span></span> <span data-ttu-id="19d05-123">否則，會重設 **ErrorInfo** 集合，且不會詳細說明該失敗。</span><span class="sxs-lookup"><span data-stu-id="19d05-123">Otherwise, the **ErrorInfo** collection is reset and does not detail that failure.</span></span>

<span data-ttu-id="19d05-124">[**ErrorInfo**](errorinfo.md)集合中的專案會公開特殊的錯誤報表屬性 MajorRef 和 MinorRef，以詳細說明錯誤的特定原因。</span><span class="sxs-lookup"><span data-stu-id="19d05-124">The items in the [**ErrorInfo**](errorinfo.md) collection expose the special error-reporting properties MajorRef and MinorRef, which detail the particular cause of the error.</span></span> <span data-ttu-id="19d05-125">如需詳細資訊，請參閱 **ErrorInfo**。</span><span class="sxs-lookup"><span data-stu-id="19d05-125">For more information, see **ErrorInfo**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19d05-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="19d05-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19d05-127">交易內的 COM + 管理作業</span><span class="sxs-lookup"><span data-stu-id="19d05-127">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="19d05-128">使用 COM + 系統管理目錄的簡介範例</span><span class="sxs-lookup"><span data-stu-id="19d05-128">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="19d05-129">COMAdmin 物件的總覽</span><span class="sxs-lookup"><span data-stu-id="19d05-129">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="19d05-130">在 COM + 類別目錄上取出集合</span><span class="sxs-lookup"><span data-stu-id="19d05-130">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="19d05-131">設定屬性並將變更儲存至 COM + 類別目錄</span><span class="sxs-lookup"><span data-stu-id="19d05-131">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 




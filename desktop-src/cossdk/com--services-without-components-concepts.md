---
description: COM + 1.5 引進了在沒有元件的情況下使用 COM + 服務的能力。
ms.assetid: da93d164-234a-4d1e-b82c-f3f904bb8cb6
title: 沒有元件概念的 COM + 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d692657d33143b9437a9c8134260a8c32431cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847509"
---
# <a name="com-services-without-components-concepts"></a><span data-ttu-id="1dc37-103">沒有元件概念的 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="1dc37-103">COM+ Services Without Components Concepts</span></span>

<span data-ttu-id="1dc37-104">COM + 1.5 引進了在沒有元件的情況下使用 COM + 服務的能力。</span><span class="sxs-lookup"><span data-stu-id="1dc37-104">COM+ 1.5 introduces the ability to use COM+ services without components.</span></span> <span data-ttu-id="1dc37-105">這可大幅降低從未使用元件的環境使用 COM + 服務時所產生的效能成本，也可以消除使用這些服務的複雜度。</span><span class="sxs-lookup"><span data-stu-id="1dc37-105">This significantly reduces the performance costs when using COM+ services from an environment that doesn't use components, and it also eliminates the complexity of using these services.</span></span> <span data-ttu-id="1dc37-106">從 IIS 6.0 開始，IIS 和 ASP 利用沒有元件的 COM + 服務。</span><span class="sxs-lookup"><span data-stu-id="1dc37-106">Beginning with IIS 6.0, IIS and ASP take advantage of using COM+ services without components.</span></span>

<span data-ttu-id="1dc37-107">COM + 服務原本是設計來搭配 COM + 元件使用。</span><span class="sxs-lookup"><span data-stu-id="1dc37-107">COM+ services were originally designed to be used with COM+ components.</span></span> <span data-ttu-id="1dc37-108">不過，某些程式設計環境不是以元件為基礎，因此需要使用 COM + 服務的大量額外負荷。</span><span class="sxs-lookup"><span data-stu-id="1dc37-108">However, some programming environments are not component-based and therefore required substantial overhead to use COM+ services.</span></span> <span data-ttu-id="1dc37-109">例如，在 COM + 1.5 發行之前，IIS 必須單獨建立填充碼物件，才能在 ASP 頁面中使用 COM + 交易服務。</span><span class="sxs-lookup"><span data-stu-id="1dc37-109">For example, before the release of COM+ 1.5, IIS had to create shim objects solely to be able to use COM+ transaction services in ASP pages.</span></span> <span data-ttu-id="1dc37-110">建立這些物件的效能成本包括將設定資料儲存在 IIS 的中繼資料和 COM + 註冊資料庫中 (RegDB) 以及 IIS 中繼資料與 COM + + RegDB 之間的額外通訊，以有效管理設定資料。</span><span class="sxs-lookup"><span data-stu-id="1dc37-110">The performance costs that come from creating those objects include storing the configuration data in both the IIS metabase and the COM+ registration database (RegDB) as well as the extra communication between the IIS metabase and the COM+ RegDB that is needed to effectively manage the configuration data.</span></span>

<span data-ttu-id="1dc37-111">如果 IIS 需要使用第二個 COM + 服務，例如同步處理，則必須建立完全不同的填充碼物件來執行此作業。</span><span class="sxs-lookup"><span data-stu-id="1dc37-111">If IIS needed to use a second COM+ service, such as synchronization, it had to create a completely different shim object to do so.</span></span> <span data-ttu-id="1dc37-112">若要同時使用 COM + 交易與同步處理，則需要第三種類型的填充碼物件。</span><span class="sxs-lookup"><span data-stu-id="1dc37-112">To use both COM+ transactions and synchronization, a third type of shim object would be needed.</span></span> <span data-ttu-id="1dc37-113">這種方法的複雜度會隨著 O (n2) ，使新服務的執行極為困難。</span><span class="sxs-lookup"><span data-stu-id="1dc37-113">The complexity of this approach scales as O(n2), making the implementation of new services extremely difficult.</span></span>

<span data-ttu-id="1dc37-114">由於引進的 COM + 服務沒有元件，所需的服務是透過從類別具現化的物件來設定。</span><span class="sxs-lookup"><span data-stu-id="1dc37-114">With the introduction of COM+ services without components, the services that are needed are configured through an object instantiated from the class.</span></span> <span data-ttu-id="1dc37-115">[**CServiceConfig**](cserviceconfig.md)類別會執行設定不同服務所需的介面，同時提供同時支援多個服務的彈性，以及未來支援新服務的能力。</span><span class="sxs-lookup"><span data-stu-id="1dc37-115">The [**CServiceConfig**](cserviceconfig.md) class implements the interfaces needed to configure the different services while providing the flexibility to support multiple services at the same time and the ability to support new services in the future.</span></span>

<span data-ttu-id="1dc37-116">接著，您可以透過兩種不同的機制來使用設定的服務：它們可透過 [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) 函式使用，這會將服務套用至透過函式所建立之活動提交的所有工作，而且也可以藉由在 [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) 和 [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) 函數的呼叫之間內嵌使用服務的工作來使用。</span><span class="sxs-lookup"><span data-stu-id="1dc37-116">The configured services can then be used through two different mechanisms: They can be used through the [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) function, which applies the services to all of the work submitted via the activity that is created by the function, and they can also be used by embedding the work that uses the services between calls to the [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) and [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) functions.</span></span> <span data-ttu-id="1dc37-117">這些函式都不需要建立任何新元件，就能使用 COM + 服務;只需要 [**CServiceConfig**](cserviceconfig.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="1dc37-117">None of these functions requires the creation of any new components to be able to use the COM+ services; only the [**CServiceConfig**](cserviceconfig.md) object is needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dc37-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="1dc37-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dc37-119">沒有元件工作的 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="1dc37-119">COM+ Services Without Components Tasks</span></span>](com--services-without-components-tasks.md)
</dt> </dl>

 

 




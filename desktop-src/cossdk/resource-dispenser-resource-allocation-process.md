---
description: 資源配置器資源配置進程
ms.assetid: 695d08f4-ba5c-4a5f-a2ad-481a8ede49ab
title: 資源配置器資源配置進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a12cb22abd6d4d825f1ca048495b032a77fe216
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187709"
---
# <a name="resource-dispenser-resource-allocation-process"></a><span data-ttu-id="975cb-103">資源配置器資源配置進程</span><span class="sxs-lookup"><span data-stu-id="975cb-103">Resource Dispenser Resource Allocation Process</span></span>

<span data-ttu-id="975cb-104">每次資源配置器從其持有者配置資源時，就會發生下列情況：</span><span class="sxs-lookup"><span data-stu-id="975cb-104">Each time a resource dispenser allocates a resource from its holder, the following occurs:</span></span>

1.  <span data-ttu-id="975cb-105">資源配置器會宣告 (**RESTYPID**) 的資源類型識別碼，描述所需的資源類型。</span><span class="sxs-lookup"><span data-stu-id="975cb-105">The resource dispenser declares a resource type identifier (**RESTYPID**), which describes the type of resource required.</span></span>

2.  <span data-ttu-id="975cb-106">資源配置器會呼叫持有者的 [**IHolder：： AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) 方法，並傳遞此 **RESTYPID**。</span><span class="sxs-lookup"><span data-stu-id="975cb-106">The resource dispenser calls the holder's [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) method, passing this **RESTYPID**.</span></span>

3.  <span data-ttu-id="975cb-107">持有者會從可用的資源產生候選清單。</span><span class="sxs-lookup"><span data-stu-id="975cb-107">The holder generates a candidate list from the available resources.</span></span> <span data-ttu-id="975cb-108">候選項目是指未在交易中登記，或已在呼叫物件的交易中登記的資源。</span><span class="sxs-lookup"><span data-stu-id="975cb-108">Candidates are resources that are either not enlisted in a transaction or already enlisted in the calling object's transaction.</span></span>

4.  <span data-ttu-id="975cb-109">這些候選項目會個別傳遞至 [**IDispenserDriver：： RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) 方法，在此方法中，會根據候選資源與所需的 **RESTYPID** 有多好，以0到) 100 的級別 (。</span><span class="sxs-lookup"><span data-stu-id="975cb-109">These candidates are individually passed to the [**IDispenserDriver::RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) method where they are rated (on a scale of 0 to 100) by how well the candidate resource matches the desired **RESTYPID**.</span></span>

5.  <span data-ttu-id="975cb-110">持有者會選擇資源配置者費率最高的資源。</span><span class="sxs-lookup"><span data-stu-id="975cb-110">The holder chooses the resource that the resource dispenser rates as highest.</span></span>

6.  <span data-ttu-id="975cb-111">資源配置器可以提早終止評等迴圈，方法是將候選資源分級為 100 (完美符合) 。</span><span class="sxs-lookup"><span data-stu-id="975cb-111">The resource dispenser can terminate the rating loop early by assigning the candidate a resource rating of 100 (a perfect fit).</span></span> <span data-ttu-id="975cb-112">通常會針對已正確登記的候選資源保留100的評等，除非資源配置程式最後會將登記視為便宜的作業。</span><span class="sxs-lookup"><span data-stu-id="975cb-112">A rating of 100 would normally be reserved for candidate resources that are already properly enlisted, unless the resource dispenser concludes that enlistment is an inexpensive operation.</span></span> <span data-ttu-id="975cb-113">如果所有的候選資源 (如果有任何) 分級為 0 (無法使用) ，則會藉由呼叫 [**IDispenserDriver：： CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource)來建立新的資源。</span><span class="sxs-lookup"><span data-stu-id="975cb-113">If all candidate resources (if any) are rated 0 (unusable), a new resource is created by calling [**IDispenserDriver::CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).</span></span>

7.  <span data-ttu-id="975cb-114">如果先前選擇的資源尚未登記在呼叫物件的交易中，則會呼叫資源配置程式的 [**IDispenserDriver：： EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) 方法。</span><span class="sxs-lookup"><span data-stu-id="975cb-114">If the resource chosen previously is not already enlisted in the calling object's transaction, the resource dispenser's [**IDispenserDriver::EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) method is called.</span></span>

8.  <span data-ttu-id="975cb-115">[**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource)方法呼叫會傳回具有已登錄資源的資源配置器。</span><span class="sxs-lookup"><span data-stu-id="975cb-115">The [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) method call returns to the resource dispenser with the enlisted resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="975cb-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="975cb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="975cb-117">COM + 資源配置器概念</span><span class="sxs-lookup"><span data-stu-id="975cb-117">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="975cb-118">在交易中登記資源</span><span class="sxs-lookup"><span data-stu-id="975cb-118">Enlisting a Resource in a Transaction</span></span>](enlisting-a-resource-in-a-transaction.md)
</dt> <dt>

[<span data-ttu-id="975cb-119">追蹤未配置的資源</span><span class="sxs-lookup"><span data-stu-id="975cb-119">Tracking Non-Allocated Resources</span></span>](tracking-non-allocated-resources.md)
</dt> </dl>

 

 




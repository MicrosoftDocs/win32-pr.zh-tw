---
description: COM + 資源配置器介面中使用的類型
ms.assetid: f4b3a828-3d66-455c-9b0c-30086f3ffe23
title: COM + 資源配置器介面中使用的類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c4d0f62ec7c61a9bc0f189c1ee02d1868a3242
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688999"
---
# <a name="types-used-in-com-resource-dispenser-interfaces"></a><span data-ttu-id="2e06a-103">COM + 資源配置器介面中使用的類型</span><span class="sxs-lookup"><span data-stu-id="2e06a-103">Types Used in COM+ Resource Dispenser Interfaces</span></span>

<span data-ttu-id="2e06a-104">以下是在資源配置器介面中使用的類型。</span><span class="sxs-lookup"><span data-stu-id="2e06a-104">The following types are used in the resource dispenser interfaces.</span></span>



| <span data-ttu-id="2e06a-105">類型</span><span class="sxs-lookup"><span data-stu-id="2e06a-105">Type</span></span>           | <span data-ttu-id="2e06a-106">Description</span><span class="sxs-lookup"><span data-stu-id="2e06a-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e06a-107">**RESTYPID**</span><span class="sxs-lookup"><span data-stu-id="2e06a-107">**RESTYPID**</span></span>   | <span data-ttu-id="2e06a-108">**DWORD** ，識別資源的類型，而不是特定的資源。</span><span class="sxs-lookup"><span data-stu-id="2e06a-108">A **DWORD** that identifies a type of resource, not a particular resource.</span></span> <span data-ttu-id="2e06a-109">**RESTYPID** 通常是在配置器記憶體中描述資源類型之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2e06a-109">A **RESTYPID** is usually a pointer to a structure in the dispenser's memory that describes the resource type.</span></span> <span data-ttu-id="2e06a-110">分配器管理員不了解 (，也不需要瞭解資源配置器記憶體中) 此結構。</span><span class="sxs-lookup"><span data-stu-id="2e06a-110">The dispenser manager does not understand (and does not need to understand) this structure within the resource dispenser's memory.</span></span> <span data-ttu-id="2e06a-111">分配器管理員只使用 **RESTYPID** 來參考資源配置器內的資源類型。</span><span class="sxs-lookup"><span data-stu-id="2e06a-111">The dispenser manager uses **RESTYPID** only to refer to a resource type within a resource dispenser.</span></span>                                                                                                                                   |
| <span data-ttu-id="2e06a-112">**渣 油**</span><span class="sxs-lookup"><span data-stu-id="2e06a-112">**RESID**</span></span>      | <span data-ttu-id="2e06a-113">識別特定資源的 **DWORD** ，而不是資源的類型。</span><span class="sxs-lookup"><span data-stu-id="2e06a-113">A **DWORD** that identifies a particular resource, as opposed to a type of resource.</span></span> <span data-ttu-id="2e06a-114">**RESID** 通常是 (**void \* *_) ，指向資源配置器記憶體中代表資源的結構。在資源配置器的記憶體中，分配者管理員不需要瞭解此結構。分配器管理員會使用 _* RESID** 來參考資源配置器內的特定資源。</span><span class="sxs-lookup"><span data-stu-id="2e06a-114">A **RESID** is usually a (**void \**_) that points to a structure in the resource dispenser's memory that represents the resource. The dispenser manager does not need to understand this structure within the resource dispenser's memory. The dispenser manager uses _\* RESID*\* to refer to a particular resource within a resource dispenser.</span></span>                                                                                                                                 |
| <span data-ttu-id="2e06a-115">**SRESID**</span><span class="sxs-lookup"><span data-stu-id="2e06a-115">**SRESID**</span></span>     | <span data-ttu-id="2e06a-116">**RESID** 的 Unicode 字串版本，用於 [**IHolder：： TrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-trackresources)和 [**IHolder：： UntrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-untrackresources)方法。</span><span class="sxs-lookup"><span data-stu-id="2e06a-116">A Unicode string version of **RESID**, used in the [**IHolder::TrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-trackresources) and [**IHolder::UntrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-untrackresources) methods.</span></span> <span data-ttu-id="2e06a-117">當您只需要記錄資源的少量資訊，而且該資源的整個描述可以包含在 **SRESID** 中時，字串有時很有用。</span><span class="sxs-lookup"><span data-stu-id="2e06a-117">Strings are sometimes useful when only a small amount of information needs to be recorded about a resource and the entire description of the resource can be contained in the **SRESID**.</span></span> <span data-ttu-id="2e06a-118">尤其是，使用 **SRESID** 可能會在資源代表兩個 (或更多) 專案之間的關聯性時，消除資源配置器中的對應需求。</span><span class="sxs-lookup"><span data-stu-id="2e06a-118">In particular, using the **SRESID** can sometimes eliminate the need for a map in the resource dispenser when the resource represents a relationship between two (or more) things.</span></span> |
| <span data-ttu-id="2e06a-119">**TRANSID**</span><span class="sxs-lookup"><span data-stu-id="2e06a-119">**TRANSID**</span></span>    | <span data-ttu-id="2e06a-120">識別交易。</span><span class="sxs-lookup"><span data-stu-id="2e06a-120">Identifies a transaction.</span></span> <span data-ttu-id="2e06a-121">此類型可以轉換成 **ITransaction** 介面。</span><span class="sxs-lookup"><span data-stu-id="2e06a-121">This type may be cast to the **ITransaction** interface.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="2e06a-122">**TIMEINSECS**</span><span class="sxs-lookup"><span data-stu-id="2e06a-122">**TIMEINSECS**</span></span> | <span data-ttu-id="2e06a-123">表示資源在損毀之前可以處於非使用中狀態的時間長度。</span><span class="sxs-lookup"><span data-stu-id="2e06a-123">Indicates how long a resource can be inactive before it is destroyed.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="2e06a-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="2e06a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e06a-125">COM + 資源配置器概念</span><span class="sxs-lookup"><span data-stu-id="2e06a-125">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="2e06a-126">COM + 資源配置器介面</span><span class="sxs-lookup"><span data-stu-id="2e06a-126">COM+ Resource Dispenser Interfaces</span></span>](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 




---
description: 適用于 COM + 資源配置器的共用資源狀態
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: 適用于 COM + 資源配置器的共用資源狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0bc59dcc2b7e95e060c0d6e96a5880d09d26e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468301"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a><span data-ttu-id="1a0ab-103">適用于 COM + 資源配置器的共用資源狀態</span><span class="sxs-lookup"><span data-stu-id="1a0ab-103">Pooled Resource States Available to COM+ Resource Dispenser</span></span>

<span data-ttu-id="1a0ab-104">在任何一次，資源正在使用中或不在使用中，而且已登錄或未登錄在交易中。</span><span class="sxs-lookup"><span data-stu-id="1a0ab-104">At any one time, a resource is either in use or not in use and is either enlisted or not enlisted in a transaction.</span></span> <span data-ttu-id="1a0ab-105">這會產生四個可能的資源狀態，如下所示：</span><span class="sxs-lookup"><span data-stu-id="1a0ab-105">This yields four possible resource states, as follows:</span></span>

-   <span data-ttu-id="1a0ab-106">**取消登錄清查中的資源。**</span><span class="sxs-lookup"><span data-stu-id="1a0ab-106">**Resources in unenlisted inventory.**</span></span> <span data-ttu-id="1a0ab-107">未由物件使用且未在交易中登記的資源，正在取消登錄清查。</span><span class="sxs-lookup"><span data-stu-id="1a0ab-107">A resource that is not in use by an object and not enlisted in a transaction is in unenlisted inventory.</span></span> <span data-ttu-id="1a0ab-108">一般清查中的資源可供指派。</span><span class="sxs-lookup"><span data-stu-id="1a0ab-108">A resource in general inventory is available for assignment.</span></span>

-   <span data-ttu-id="1a0ab-109">**已登記清查中的資源。**</span><span class="sxs-lookup"><span data-stu-id="1a0ab-109">**Resources in enlisted inventory.**</span></span> <span data-ttu-id="1a0ab-110">未由物件使用但已在交易中登記的資源正在登錄清查中。</span><span class="sxs-lookup"><span data-stu-id="1a0ab-110">A resource that is not in use by an object but is enlisted in a transaction is in enlisted inventory.</span></span> <span data-ttu-id="1a0ab-111">這類資源僅可指派給在相同交易中執行的物件。</span><span class="sxs-lookup"><span data-stu-id="1a0ab-111">Such a resource is available for assignment only to objects running in the same transaction.</span></span> <span data-ttu-id="1a0ab-112">當 COM + 通知分配者管理員交易已完成時，資源會從已登記的清查移至取消登錄的清查。</span><span class="sxs-lookup"><span data-stu-id="1a0ab-112">A resource moves from enlisted inventory to unenlisted inventory when COM+ notifies the dispenser manager that the transaction is complete.</span></span>

-   <span data-ttu-id="1a0ab-113">**已取消登錄的資源使用。**</span><span class="sxs-lookup"><span data-stu-id="1a0ab-113">**Resources in unenlisted use.**</span></span> <span data-ttu-id="1a0ab-114">如果資源已指派給物件，且該實例未在交易中執行，或資源配置器已將資源識別為非交易式，則會在取消登錄的情況下使用此資源。</span><span class="sxs-lookup"><span data-stu-id="1a0ab-114">If a resource is assigned to an object and the instance is not running in a transaction or the resource dispenser has identified the resource as non-transactional, this resource is in unenlisted use.</span></span>

-   <span data-ttu-id="1a0ab-115">**已登記使用中的資源。**</span><span class="sxs-lookup"><span data-stu-id="1a0ab-115">**Resources in enlisted use.**</span></span> <span data-ttu-id="1a0ab-116">如果資源已指派給物件，則實例會在交易中執行，而且資源配置器已成功將資源登記在交易中，此資源就會在已登記的情況下使用。</span><span class="sxs-lookup"><span data-stu-id="1a0ab-116">If a resource is assigned to an object, the instance is running in a transaction, and the resource dispenser has successfully enlisted the resource in the transaction, this resource is in enlisted use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a0ab-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="1a0ab-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a0ab-118">COM + 資源配置器概念</span><span class="sxs-lookup"><span data-stu-id="1a0ab-118">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="1a0ab-119">在交易中登記資源</span><span class="sxs-lookup"><span data-stu-id="1a0ab-119">Enlisting a Resource in a Transaction</span></span>](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 




---
description: 您可以設定其他屬性（例如交易式需求）和及時 (JIT) 啟用，以自動決定或限制同步處理值。
ms.assetid: 16771121-cb10-42b4-babc-59270188495a
title: 同步處理相依性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c139d0d6e78288b25e42bd0a84b29432cebb44ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847216"
---
# <a name="synchronization-dependencies"></a><span data-ttu-id="1d719-103">同步處理相依性</span><span class="sxs-lookup"><span data-stu-id="1d719-103">Synchronization Dependencies</span></span>

<span data-ttu-id="1d719-104">您可以設定其他屬性（例如交易式需求）和及時 (JIT) 啟用，以自動決定或限制同步處理值。</span><span class="sxs-lookup"><span data-stu-id="1d719-104">Synchronization values can be automatically determined or constrained by the configuration of other properties, such as transactional requirements and just-in-time (JIT) activation.</span></span> <span data-ttu-id="1d719-105">例如，COM + 會針對交易式和 JIT 啟用的元件強制執行同步處理。</span><span class="sxs-lookup"><span data-stu-id="1d719-105">For example, COM+ enforces synchronization both for transactional and for JIT-activated components.</span></span>

<span data-ttu-id="1d719-106">這些相依性存在的原因是，JIT 啟動或參與交易的元件必須具有適當的隔離和並行行為。</span><span class="sxs-lookup"><span data-stu-id="1d719-106">These dependencies exist because components that are JIT-activated or participating in transactions must have proper isolation and concurrency behavior.</span></span> <span data-ttu-id="1d719-107">因此，COM + 需要藉由強制執行同步處理來序列化這些元件的存取權。</span><span class="sxs-lookup"><span data-stu-id="1d719-107">Therefore, COM+ requires that access to these components be serialized by enforcing synchronization.</span></span> <span data-ttu-id="1d719-108"> (如需這些相依性的詳細資訊，請參閱 [Com + 即時啟用](com--just-in-time-activation.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="1d719-108">(For details on these dependencies, see [COM+ Just-in-Time Activation](com--just-in-time-activation.md).)</span></span>

<span data-ttu-id="1d719-109">下表顯示 COM + 同步處理屬性值的特性。</span><span class="sxs-lookup"><span data-stu-id="1d719-109">The following tables show the characteristics of the COM+ synchronization attribute values.</span></span>

### <a name="transactional-requirement"></a><span data-ttu-id="1d719-110">交易式需求</span><span class="sxs-lookup"><span data-stu-id="1d719-110">Transactional requirement</span></span>



| <span data-ttu-id="1d719-111">當交易設定為時</span><span class="sxs-lookup"><span data-stu-id="1d719-111">When transactions are set to</span></span> | <span data-ttu-id="1d719-112">同步處理可以設定為</span><span class="sxs-lookup"><span data-stu-id="1d719-112">Synchronization can be set to</span></span>                    |
|------------------------------|--------------------------------------------------|
| <span data-ttu-id="1d719-113">Disabled</span><span class="sxs-lookup"><span data-stu-id="1d719-113">Disabled</span></span><br/>          | <span data-ttu-id="1d719-114">任何事項，視 JIT 啟用而定</span><span class="sxs-lookup"><span data-stu-id="1d719-114">Anything, depending on JIT activation</span></span><br/> |
| <span data-ttu-id="1d719-115">不支援</span><span class="sxs-lookup"><span data-stu-id="1d719-115">Not Supported</span></span><br/>     | <span data-ttu-id="1d719-116">任何事項，視 JIT 啟用而定</span><span class="sxs-lookup"><span data-stu-id="1d719-116">Anything, depending on JIT activation</span></span><br/> |
| <span data-ttu-id="1d719-117">支援</span><span class="sxs-lookup"><span data-stu-id="1d719-117">Supported</span></span><br/>         | <span data-ttu-id="1d719-118">必要</span><span class="sxs-lookup"><span data-stu-id="1d719-118">Required</span></span><br/>                              |
| <span data-ttu-id="1d719-119">必要</span><span class="sxs-lookup"><span data-stu-id="1d719-119">Required</span></span><br/>          | <span data-ttu-id="1d719-120">必要</span><span class="sxs-lookup"><span data-stu-id="1d719-120">Required</span></span><br/>                              |
| <span data-ttu-id="1d719-121">必須是新交易</span><span class="sxs-lookup"><span data-stu-id="1d719-121">Requires New</span></span><br/>      | <span data-ttu-id="1d719-122">必要或需要新的</span><span class="sxs-lookup"><span data-stu-id="1d719-122">Required or Requires New</span></span><br/>              |



 

### <a name="jit-activation"></a><span data-ttu-id="1d719-123">JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="1d719-123">JIT Activation</span></span>



| <span data-ttu-id="1d719-124">當 JIT 啟用設定為時</span><span class="sxs-lookup"><span data-stu-id="1d719-124">When JIT Activation is set to</span></span> | <span data-ttu-id="1d719-125">同步處理可以設定為</span><span class="sxs-lookup"><span data-stu-id="1d719-125">Synchronization can be set to</span></span>       |
|-------------------------------|-------------------------------------|
| <span data-ttu-id="1d719-126">已啟用</span><span class="sxs-lookup"><span data-stu-id="1d719-126">Enabled</span></span><br/>            | <span data-ttu-id="1d719-127">必要或需要新的</span><span class="sxs-lookup"><span data-stu-id="1d719-127">Required or Requires New</span></span><br/> |
| <span data-ttu-id="1d719-128">Disabled</span><span class="sxs-lookup"><span data-stu-id="1d719-128">Disabled</span></span><br/>           | <span data-ttu-id="1d719-129">什麼</span><span class="sxs-lookup"><span data-stu-id="1d719-129">Anything</span></span><br/>                 |



 

<span data-ttu-id="1d719-130">如需交易、JIT 啟動和同步處理屬性如何一起運作的詳細資訊，請參閱設定 [交易](configuring-transactions.md)。</span><span class="sxs-lookup"><span data-stu-id="1d719-130">For more detail about how transaction, JIT Activation, and Synchronization attributes behave together, see [Configuring Transactions](configuring-transactions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d719-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d719-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d719-132">設定同步處理屬性</span><span class="sxs-lookup"><span data-stu-id="1d719-132">Setting the Synchronization Attribute</span></span>](setting-the-synchronization-attribute.md)
</dt> <dt>

[<span data-ttu-id="1d719-133">同步處理屬性值</span><span class="sxs-lookup"><span data-stu-id="1d719-133">Synchronization Attribute Values</span></span>](synchronization-attribute-values.md)
</dt> </dl>

 

 





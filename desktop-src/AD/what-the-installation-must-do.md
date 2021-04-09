---
title: 安裝必須做什麼
description: 在步驟3中參考的新屬性必須由其 OID 參考，因為新的屬性名稱在架構快取中不存在於此位置。
ms.assetid: 57da8740-7646-4ca9-ba8d-832e4f520b13
ms.tgt_platform: multiple
keywords:
- 安裝必須進行的 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5724a7acbb4d0bf8ef3008fa48e2f10fcc04a324
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931869"
---
# <a name="what-the-installation-must-do"></a><span data-ttu-id="ed194-104">安裝必須做什麼</span><span class="sxs-lookup"><span data-stu-id="ed194-104">What the Installation Must Do</span></span>

<span data-ttu-id="ed194-105">延伸架構的應用程式必須套用更新，如下列程式所述。</span><span class="sxs-lookup"><span data-stu-id="ed194-105">Applications that extend the schema, must apply updates as described in the following procedure.</span></span>

<span data-ttu-id="ed194-106">**若要在擴充架構時套用更新**</span><span class="sxs-lookup"><span data-stu-id="ed194-106">**To apply updates when extending the schema**</span></span>

1.  <span data-ttu-id="ed194-107">加入新的屬性。</span><span class="sxs-lookup"><span data-stu-id="ed194-107">Add the new attributes.</span></span>
2.  <span data-ttu-id="ed194-108">加入新的類別。</span><span class="sxs-lookup"><span data-stu-id="ed194-108">Add the new classes.</span></span>
3.  <span data-ttu-id="ed194-109">將新屬性加入至類別。</span><span class="sxs-lookup"><span data-stu-id="ed194-109">Add the new attributes to classes.</span></span>
4.  <span data-ttu-id="ed194-110">觸發快取重載。</span><span class="sxs-lookup"><span data-stu-id="ed194-110">Trigger a cache reload.</span></span>

<span data-ttu-id="ed194-111">在步驟3中參考的新屬性必須由其 OID 參考，因為新的屬性名稱在架構快取中不存在於此位置。</span><span class="sxs-lookup"><span data-stu-id="ed194-111">New attributes referenced in Step 3 must be referred to by its OID because the new attribute name is not present in the schema cache at this point.</span></span>

<span data-ttu-id="ed194-112">如果不會立即使用延伸模組，則不需要步驟 4;視系統負載而定，擴充功能將會在架構快取中出現大約5分鐘。</span><span class="sxs-lookup"><span data-stu-id="ed194-112">Step 4 is unnecessary if the extensions will not be used immediately; the extensions will appear in the schema cache in approximately 5 minutes, depending on system load.</span></span> <span data-ttu-id="ed194-113">如需架構快取的詳細資訊，以及如何觸發快取重載，請參閱 [更新架構](updating-the-schema-cache.md)快取。</span><span class="sxs-lookup"><span data-stu-id="ed194-113">For more information about the schema cache and how to trigger a cache reload, see [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>

 

 





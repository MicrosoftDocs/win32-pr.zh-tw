---
title: MIB 名稱樹狀結構
description: MIB 物件識別碼的命名空間為階層式。 它是結構化的，因此可以將全域唯一名稱指派給每個可管理的物件。
ms.assetid: eb3c855c-b36b-4675-8df4-e11c128b2b34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d77b0cb4c64d9645f54ec7416c45ba1a4620ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021776"
---
# <a name="mib-name-tree"></a><span data-ttu-id="a7494-104">MIB 名稱樹狀結構</span><span class="sxs-lookup"><span data-stu-id="a7494-104">MIB Name Tree</span></span>

<span data-ttu-id="a7494-105">MIB 物件識別碼的命名空間為階層式。</span><span class="sxs-lookup"><span data-stu-id="a7494-105">The name space for MIB object identifiers is hierarchical.</span></span> <span data-ttu-id="a7494-106">它是結構化的，因此可以將全域唯一名稱指派給每個可管理的物件。</span><span class="sxs-lookup"><span data-stu-id="a7494-106">It is structured so that each manageable object can be assigned a globally unique name.</span></span>

<span data-ttu-id="a7494-107">命名空間部分的授權單位會指派給個別組織。</span><span class="sxs-lookup"><span data-stu-id="a7494-107">Authority for parts of the name space is assigned to individual organizations.</span></span> <span data-ttu-id="a7494-108">這可讓組織指派名稱，而不需為每個指派的網際網路授權單位進行參考。</span><span class="sxs-lookup"><span data-stu-id="a7494-108">This allows organizations to assign names without consulting an Internet authority for each assignment.</span></span> <span data-ttu-id="a7494-109">例如，指派給 Microsoft 的命名空間是 1.3.6.1.4.1.311.，在 MSFT 中定義。Mib。</span><span class="sxs-lookup"><span data-stu-id="a7494-109">For example, the name space assigned to Microsoft is 1.3.6.1.4.1.311, which is defined in MSFT.MIB.</span></span> <span data-ttu-id="a7494-110">Microsoft 有權將名稱指派給該命名空間下任何位置的物件。</span><span class="sxs-lookup"><span data-stu-id="a7494-110">Microsoft has the authority to assign names to objects anywhere below that name space.</span></span>

<span data-ttu-id="a7494-111">階層中的物件識別碼會以從根目錄開始的 subidentifiers 序列撰寫，並在物件結尾。</span><span class="sxs-lookup"><span data-stu-id="a7494-111">The object identifier in the hierarchy is written as a sequence of subidentifiers beginning at the root and ending at the object.</span></span> <span data-ttu-id="a7494-112">Subidentifiers 會以句號分隔。</span><span class="sxs-lookup"><span data-stu-id="a7494-112">Subidentifiers are separated with a period.</span></span>

 

 





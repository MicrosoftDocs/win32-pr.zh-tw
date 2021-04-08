---
title: 架構延伸的限制
description: 為了減少某個應用程式中斷其他應用程式的架構變更的可能性，以及維持架構一致性，Active Directory Domain Services 對允許應用程式或使用者進行的架構變更類型強制執行限制。
ms.assetid: 26254eb9-5dd9-414b-a398-be2a7f3b0279
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c97ab3d9f6406a89b24c772e7df8254095f1286
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671244"
---
# <a name="restrictions-on-schema-extension"></a><span data-ttu-id="5a348-103">架構延伸的限制</span><span class="sxs-lookup"><span data-stu-id="5a348-103">Restrictions on Schema Extension</span></span>

<span data-ttu-id="5a348-104">為了減少某個應用程式中斷其他應用程式的架構變更的可能性，以及維持架構一致性，Active Directory Domain Services 對允許應用程式或使用者進行的架構變更類型強制執行限制。</span><span class="sxs-lookup"><span data-stu-id="5a348-104">In order to reduce the possibility of schema changes by one application breaking other applications and to maintain schema consistency, Active Directory Domain Services enforce restrictions on the type of schema changes that an application or user is allowed to make.</span></span>

<span data-ttu-id="5a348-105">只有在修改現有的架構物件時，才會加諸限制。</span><span class="sxs-lookup"><span data-stu-id="5a348-105">The restrictions are imposed only on modification of existing schema objects.</span></span> <span data-ttu-id="5a348-106">架構分為兩個類別。</span><span class="sxs-lookup"><span data-stu-id="5a348-106">The schema is categorized into two categories.</span></span> <span data-ttu-id="5a348-107">基底架構中 Windows 2000 隨附的架構物件屬於類別1。</span><span class="sxs-lookup"><span data-stu-id="5a348-107">The schema objects that ship with Windows 2000 in the base schema belong to Category 1.</span></span> <span data-ttu-id="5a348-108">其他應用程式或使用者稍後透過動態架構延伸新增的任何架構物件都屬於類別2。</span><span class="sxs-lookup"><span data-stu-id="5a348-108">Any schema objects added later by other applications or users through dynamic schema extension belong to Category 2.</span></span> <span data-ttu-id="5a348-109">架構物件的類別可以由 **classSchema** 物件上 **systemFlags** 屬性中所設定的0x10 位來決定。</span><span class="sxs-lookup"><span data-stu-id="5a348-109">The category of a schema object can be determined by the 0x10 bit set in the **systemFlags** attribute on the **classSchema** object.</span></span> <span data-ttu-id="5a348-110">這個位只會在類別1物件上設定，且無法變更，也不能在任何類別2物件上設定。</span><span class="sxs-lookup"><span data-stu-id="5a348-110">This bit is only set on Category 1 objects, and cannot be altered, nor can it be set on any Category 2 object.</span></span>

<span data-ttu-id="5a348-111">**SystemFlags** 屬性是由 Active Directory Domain Services 在內部使用，以識別基底架構中「基礎結構」物件的特殊特性。</span><span class="sxs-lookup"><span data-stu-id="5a348-111">The **systemFlags** attribute is used internally by Active Directory Domain Services to identify special characteristics of "infrastructure" objects in the base schema.</span></span> <span data-ttu-id="5a348-112">除了識別類別1物件之外， **systemFlags** 還會控制是否可以移動、刪除或重新命名物件。</span><span class="sxs-lookup"><span data-stu-id="5a348-112">In addition to identifying Category 1 objects, **systemFlags** controls whether an object can be moved, deleted, or renamed.</span></span> <span data-ttu-id="5a348-113">Windows 2000 相依的物件無法執行這些作業。</span><span class="sxs-lookup"><span data-stu-id="5a348-113">These operations are prevented for objects that Windows 2000 depends on to run.</span></span>

<span data-ttu-id="5a348-114">在任何架構物件（類別1或2）上，Active Directory Domain Services 會強制執行下列限制：</span><span class="sxs-lookup"><span data-stu-id="5a348-114">On any schema objects, Category 1 or 2, Active Directory Domain Services impose the following restrictions:</span></span>

-   <span data-ttu-id="5a348-115">您無法將新的 **mustContain** 加入至類別 (直接或透過繼承加入) 的輔助類別。</span><span class="sxs-lookup"><span data-stu-id="5a348-115">You cannot add a new **mustContain** to a class (directly or through inheritance by adding an auxiliary class).</span></span>
-   <span data-ttu-id="5a348-116">您無法直接或透過繼承) 來刪除類別 (的任何 **mustContain** 。</span><span class="sxs-lookup"><span data-stu-id="5a348-116">You cannot delete any **mustContain** of the class (directly or through inheritance).</span></span>

<span data-ttu-id="5a348-117">此外，還會在類別1架構物件上加上下列額外的限制：</span><span class="sxs-lookup"><span data-stu-id="5a348-117">In addition, the following additional restrictions are imposed on Category 1 schema objects:</span></span>

-   <span data-ttu-id="5a348-118">您無法變更類別1屬性的下列屬性：</span><span class="sxs-lookup"><span data-stu-id="5a348-118">You cannot change the following attributes of a Category 1 attribute:</span></span>

    -   <span data-ttu-id="5a348-119">**rangeLower** 和 **rangeUpper** (值範圍) 。</span><span class="sxs-lookup"><span data-stu-id="5a348-119">**rangeLower** and **rangeUpper** (value range).</span></span>
    -   <span data-ttu-id="5a348-120">如果有任何) ， **attributeSecurityGuid** (會決定屬性所屬的屬性集。</span><span class="sxs-lookup"><span data-stu-id="5a348-120">**attributeSecurityGuid** (determines which property set the attribute belongs in, if any).</span></span>

-   <span data-ttu-id="5a348-121">您無法變更類別1類別的 **defaultObjectCategory** 。</span><span class="sxs-lookup"><span data-stu-id="5a348-121">You cannot change the **defaultObjectCategory** of a Category 1 class.</span></span>
-   <span data-ttu-id="5a348-122">您無法變更類別1類別的任何實例的 **objectCategory** 。</span><span class="sxs-lookup"><span data-stu-id="5a348-122">You cannot change the **objectCategory** of any instance of a Category 1 class.</span></span>
-   <span data-ttu-id="5a348-123">您無法讓類別目錄1類別或屬性無用。</span><span class="sxs-lookup"><span data-stu-id="5a348-123">You cannot make a Category 1 class or attribute defunct.</span></span>
-   <span data-ttu-id="5a348-124">您無法變更類別1類別或屬性的 **lDAPDisplayName** 。</span><span class="sxs-lookup"><span data-stu-id="5a348-124">You cannot change the **lDAPDisplayName** of a Category 1 class or attribute.</span></span>
-   <span data-ttu-id="5a348-125">您無法重新命名類別1類別或屬性。</span><span class="sxs-lookup"><span data-stu-id="5a348-125">You cannot rename a Category 1 class or attribute.</span></span>

 

 





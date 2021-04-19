---
description: 限定詞類別提供有關辨識符號的詳細資訊，例如衍生類別或實例是否可以覆寫限定詞的原始值。
ms.assetid: 6a0769ac-e16c-45e1-92b6-26e4969bf23d
ms.tgt_platform: multiple
title: 限定詞類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8ddf6c2daea59931e533174c532e3d07b147a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991931"
---
# <a name="qualifier-flavors"></a><span data-ttu-id="b714e-103">限定詞類別</span><span class="sxs-lookup"><span data-stu-id="b714e-103">Qualifier Flavors</span></span>

<span data-ttu-id="b714e-104">限定詞類別提供有關辨識符號的詳細資訊，例如衍生類別或實例是否可以覆寫辨識符號的原始值。</span><span class="sxs-lookup"><span data-stu-id="b714e-104">Qualifier flavors provide more information about a qualifier, such as whether a derived class or instance can override the qualifier's original value.</span></span>

<span data-ttu-id="b714e-105">您可以使用下列語法，將限定詞類別新增至 MOF 檔案的頂端，使其可在整個定義中套用。</span><span class="sxs-lookup"><span data-stu-id="b714e-105">Qualifier flavors may be added to the top of the MOF file, using the following syntax, causing them to be applied throughout the definition.</span></span> <span data-ttu-id="b714e-106">例如：</span><span class="sxs-lookup"><span data-stu-id="b714e-106">For example:</span></span>

``` syntax
Qualifier Description : ToSubClass Amended;
```

<span data-ttu-id="b714e-107">**ToSubClass** 和 **修訂** 的類別適用于 MOF 中的所有 **描述** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="b714e-107">The **ToSubClass** and **Amended** flavors applies to all the **Description** qualifiers in the MOF.</span></span>

<span data-ttu-id="b714e-108">下表列出辨識符號的類別。</span><span class="sxs-lookup"><span data-stu-id="b714e-108">The following table lists the qualifier flavors.</span></span>



| <span data-ttu-id="b714e-109">限定詞類別</span><span class="sxs-lookup"><span data-stu-id="b714e-109">Qualifier Flavor</span></span>    | <span data-ttu-id="b714e-110">意義</span><span class="sxs-lookup"><span data-stu-id="b714e-110">Meaning</span></span>                                                                                                                                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b714e-111">**修訂**</span><span class="sxs-lookup"><span data-stu-id="b714e-111">**Amended**</span></span>         | <span data-ttu-id="b714e-112">基本類別定義中不需要限定詞，且可以移動到要進行當地語系化的增修條款。</span><span class="sxs-lookup"><span data-stu-id="b714e-112">The qualifier is not required in the basic class definition and can be moved to the amendment to be localized.</span></span>                                                                                                                                  |
| <span data-ttu-id="b714e-113">**DisableOverride**</span><span class="sxs-lookup"><span data-stu-id="b714e-113">**DisableOverride**</span></span> | <span data-ttu-id="b714e-114">無法在衍生類別或執行個體中覆寫限定詞。</span><span class="sxs-lookup"><span data-stu-id="b714e-114">The qualifier cannot be overridden in a derived class or instance.</span></span> <span data-ttu-id="b714e-115">請注意，預設可覆寫傳播的限定詞。</span><span class="sxs-lookup"><span data-stu-id="b714e-115">Note that being able to override a propagated qualifier is the default.</span></span>                                                                                                      |
| <span data-ttu-id="b714e-116">**EnableOverride**</span><span class="sxs-lookup"><span data-stu-id="b714e-116">**EnableOverride**</span></span>  | <span data-ttu-id="b714e-117">傳播至衍生類別或實例時，限定詞的值可以覆寫。</span><span class="sxs-lookup"><span data-stu-id="b714e-117">When propagated to a derived class or instance, the value of the qualifier can be overridden.</span></span> <span data-ttu-id="b714e-118">設定 **EnableOverride** 是選擇性的，因為能夠覆寫辨識符號值是傳播限定詞的預設功能。</span><span class="sxs-lookup"><span data-stu-id="b714e-118">Setting **EnableOverride** is optional because being able to override the qualifier value is the default functionality for propagated qualifiers.</span></span> |
| <span data-ttu-id="b714e-119">**NotToInstance**</span><span class="sxs-lookup"><span data-stu-id="b714e-119">**NotToInstance**</span></span>   | <span data-ttu-id="b714e-120">限定詞不會傳播至類別實例。</span><span class="sxs-lookup"><span data-stu-id="b714e-120">The qualifier is not propagated to class instances.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="b714e-121">**NotToSubClass**</span><span class="sxs-lookup"><span data-stu-id="b714e-121">**NotToSubClass**</span></span>   | <span data-ttu-id="b714e-122">限定詞不會傳播到衍生類別。</span><span class="sxs-lookup"><span data-stu-id="b714e-122">The qualifier is not propagated to derived classes.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="b714e-123">**Restricted**</span><span class="sxs-lookup"><span data-stu-id="b714e-123">**Restricted**</span></span>      | <span data-ttu-id="b714e-124">限定詞不會傳播至實例或衍生類別。</span><span class="sxs-lookup"><span data-stu-id="b714e-124">The qualifier is not propagated to instances or derived classes.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="b714e-125">**ToInstance**</span><span class="sxs-lookup"><span data-stu-id="b714e-125">**ToInstance**</span></span>      | <span data-ttu-id="b714e-126">限定詞會傳播到執行個體。</span><span class="sxs-lookup"><span data-stu-id="b714e-126">The qualifier is propagated to instances.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="b714e-127">**ToSubClass**</span><span class="sxs-lookup"><span data-stu-id="b714e-127">**ToSubClass**</span></span>      | <span data-ttu-id="b714e-128">限定詞會傳播到衍生類別。</span><span class="sxs-lookup"><span data-stu-id="b714e-128">The qualifier is propagated to derived classes.</span></span> <span data-ttu-id="b714e-129">此類別僅適用于為類別定義的限定詞，無法附加至描述類別實例的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="b714e-129">This flavor is only appropriate for qualifiers defined for a class and cannot be attached to a qualifier describing a class instance.</span></span>                                                           |



 

 

 




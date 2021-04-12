---
description: WMI 有數種類型的類別和屬性限定詞。 限定詞也可以有修改的類別。
ms.assetid: b889df69-327b-40d0-bbd7-a33d7924f3e1
ms.tgt_platform: multiple
title: WMI 限定詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b14dc8f1f73571fc2c449e55c30034f86c2453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192049"
---
# <a name="wmi-qualifiers"></a><span data-ttu-id="3b185-104">WMI 限定詞</span><span class="sxs-lookup"><span data-stu-id="3b185-104">WMI Qualifiers</span></span>

<span data-ttu-id="3b185-105">WMI 有數種類型的類別和屬性 [*限定詞*](gloss-q.md)。</span><span class="sxs-lookup"><span data-stu-id="3b185-105">WMI has several types of class and property [*qualifiers*](gloss-q.md).</span></span> <span data-ttu-id="3b185-106">限定詞也可以 [*有修改的*](gloss-f.md)類別。</span><span class="sxs-lookup"><span data-stu-id="3b185-106">Qualifiers can also have modifying [*flavors*](gloss-f.md).</span></span> <span data-ttu-id="3b185-107">以下是在 WMI 中使用的限定詞和類別類型。</span><span class="sxs-lookup"><span data-stu-id="3b185-107">The following types of qualifiers and flavors are used in WMI.</span></span>

<span data-ttu-id="3b185-108">每個辨識符號的名稱都會顯示其資料類型，以及是否可以將限定詞套用至類別、實例、屬性或方法的指標。</span><span class="sxs-lookup"><span data-stu-id="3b185-108">The name of each qualifier appears with its data type and an indicator of whether the qualifier can be applied to a class, instance, property, or method.</span></span> <span data-ttu-id="3b185-109">針對在 [中繼限定詞](meta-qualifiers.md)) 下討論的 **關聯** (，有一個隱含的使用規則，也就是 meta 限定詞也必須存在。</span><span class="sxs-lookup"><span data-stu-id="3b185-109">For qualifiers such as **Association** (discussed under [Meta Qualifiers](meta-qualifiers.md)), there is an implied usage rule that the meta qualifier must also be present.</span></span> <span data-ttu-id="3b185-110">例如， **匯總** 限定詞的隱含使用規則是， **關聯** 限定詞也必須存在。</span><span class="sxs-lookup"><span data-stu-id="3b185-110">For example, the implicit usage rule for the **Aggregation** qualifiers is that the **Association** qualifier must also be present.</span></span>



| <span data-ttu-id="3b185-111">限定詞類型</span><span class="sxs-lookup"><span data-stu-id="3b185-111">Qualifier type</span></span>                              | <span data-ttu-id="3b185-112">Description</span><span class="sxs-lookup"><span data-stu-id="3b185-112">Description</span></span>                                                                                                                           |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b185-113">元</span><span class="sxs-lookup"><span data-stu-id="3b185-113">Meta</span></span>](meta-qualifiers.md)                 | <span data-ttu-id="3b185-114">藉由闡明類別或屬性宣告的實際使用方式，來改善中繼結構的定義。</span><span class="sxs-lookup"><span data-stu-id="3b185-114">Refines the definition of meta-constructs by clarifying the actual usage of a class or property declaration.</span></span>                          |
| [<span data-ttu-id="3b185-115">選擇性</span><span class="sxs-lookup"><span data-stu-id="3b185-115">Optional</span></span>](optional-qualifiers.md)         | <span data-ttu-id="3b185-116">解決所有符合 CIM 規範的情況下不常見的情況。</span><span class="sxs-lookup"><span data-stu-id="3b185-116">Addresses situations not common to all CIM-compliant implementations.</span></span>                                                                 |
| [<span data-ttu-id="3b185-117">限定詞類別</span><span class="sxs-lookup"><span data-stu-id="3b185-117">Qualifier Flavors</span></span>](qualifier-flavors.md)  | <span data-ttu-id="3b185-118">提供限定詞的詳細資訊，例如衍生類別或實例是否可以覆寫辨識符號的原始值。</span><span class="sxs-lookup"><span data-stu-id="3b185-118">Provides more information about a qualifier, such as whether a derived class or instance can override the qualifier's original value.</span></span> |
| [<span data-ttu-id="3b185-119">標準</span><span class="sxs-lookup"><span data-stu-id="3b185-119">Standard</span></span>](standard-qualifiers.md)         | <span data-ttu-id="3b185-120">支援所有 CIM 相容的實作為必須處理的描述。</span><span class="sxs-lookup"><span data-stu-id="3b185-120">Supports the descriptions that all CIM-compliant implementations must handle.</span></span>                                                         |
| [<span data-ttu-id="3b185-121">WMI 特定</span><span class="sxs-lookup"><span data-stu-id="3b185-121">WMI-specific</span></span>](wmi-specific-qualifiers.md) | <span data-ttu-id="3b185-122">描述 WMI 特定的限定詞，例如效能計數器類別限定詞。</span><span class="sxs-lookup"><span data-stu-id="3b185-122">Describes qualifiers specific to WMI, such as performance counter class qualifiers.</span></span>                                                   |



 

<span data-ttu-id="3b185-123">如需將限定詞套用至 WMI 類別的詳細資訊，請參閱 [新增限定詞](adding-a-qualifier.md)。</span><span class="sxs-lookup"><span data-stu-id="3b185-123">For more information on applying qualifiers to your WMI classes, see [Adding a Qualifier](adding-a-qualifier.md).</span></span> <span data-ttu-id="3b185-124">若要瞭解如何檢查現有 WMI 類別的限定詞，請參閱下列範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="3b185-124">To see how to examine qualifiers on existing WMI classes, see the example code below.</span></span>

## <a name="example"></a><span data-ttu-id="3b185-125">範例</span><span class="sxs-lookup"><span data-stu-id="3b185-125">Example</span></span>

<span data-ttu-id="3b185-126">下列來自 [TechNet 資源庫](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7)的 PowerShell 程式碼說明如何從 WMI 類別取出限定詞。</span><span class="sxs-lookup"><span data-stu-id="3b185-126">The following PowerShell code, taken from the [TechNet gallery](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7), describes how to retrieve qualifiers from a WMI class.</span></span>


```PowerShell
Function Get-WMIClassesWithQualifiers 
{ 
 Param([string]$qualifier = "dynamic", 
  [string]$namespace = "root\cimv2") 
 $classes = Gwmi -list -namespace $namespace 
 foreach($class in $classes) 
 { 
  $query = "select * from meta_class where __this isa ""$($class.name)"" " 
  $a = gwmi -Query $query -Namespace $namespace |  
  select -Property __class, qualifiers 
   if($a.qualifiers | % { $_ | ? { $_.name -match "$qualifier" }}) 
    { $a.__class } 
  } #end foreach $class 
} 
```



 

 




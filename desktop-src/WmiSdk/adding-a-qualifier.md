---
description: 辨識符號是提供類別、實例、屬性、方法或參數之詳細資訊的資料字串。
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: 新增限定詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a6f18f2b79bcd25b2b4ca75811157c9091e6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975565"
---
# <a name="adding-a-qualifier"></a><span data-ttu-id="0e77a-103">新增限定詞</span><span class="sxs-lookup"><span data-stu-id="0e77a-103">Adding a Qualifier</span></span>

<span data-ttu-id="0e77a-104">辨識符號是提供類別、實例、屬性、方法或參數之詳細資訊的資料字串。</span><span class="sxs-lookup"><span data-stu-id="0e77a-104">A qualifier is a data string that provides more information about a class, instance, property, method, or parameter.</span></span>

<span data-ttu-id="0e77a-105">下列類別定義是具有類別限定詞的衍生類別範例。</span><span class="sxs-lookup"><span data-stu-id="0e77a-105">The following class definition is an example of a derived class that has class qualifiers.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")] 
class MyDerivedClass : MyClass
{
    [key] string sKey;
    [Implemented] sint32 ValueMethod();
    [Implemented] sint32 MyMethod ([in, Id(0)] sint32 Param);
};
```

<span data-ttu-id="0e77a-106">限定詞可以分成標準限定詞、CIM 限定詞和唯一的限定詞，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0e77a-106">Qualifiers can be divided into standard qualifiers, CIM qualifiers, and unique qualifiers include the following:</span></span>

-   <span data-ttu-id="0e77a-107">標準辨識符號</span><span class="sxs-lookup"><span data-stu-id="0e77a-107">Standard qualifier</span></span>

    <span data-ttu-id="0e77a-108">標準限定詞是 WMI 所定義的辨識符號，通常用於 MOF 程式碼中。</span><span class="sxs-lookup"><span data-stu-id="0e77a-108">A standard qualifier is a qualifier defined by WMI and commonly used in MOF code.</span></span> <span data-ttu-id="0e77a-109">例如， [**動態**](dynamic-qualifier.md) 和 [**讀取**](standard-qualifiers.md) 限定詞都是標準限定詞。</span><span class="sxs-lookup"><span data-stu-id="0e77a-109">For example, the [**Dynamic**](dynamic-qualifier.md) and [**Read**](standard-qualifiers.md) qualifiers are both standard qualifiers.</span></span> <span data-ttu-id="0e77a-110">如需詳細資訊，請參閱 [WMI 限定詞](wmi-qualifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="0e77a-110">For more information, see [WMI Qualifiers](wmi-qualifiers.md).</span></span>

-   <span data-ttu-id="0e77a-111">CIM 辨識符號</span><span class="sxs-lookup"><span data-stu-id="0e77a-111">CIM qualifier</span></span>

    <span data-ttu-id="0e77a-112">CIM 辨識符號是 CIM 規格中包含的限定詞。</span><span class="sxs-lookup"><span data-stu-id="0e77a-112">A CIM qualifier is a qualifier included in the CIM specification.</span></span> <span data-ttu-id="0e77a-113">雖然在 MOF 程式碼中使用 CIM 辨識符號，但標準限定詞是特別針對 WMI 所設計。</span><span class="sxs-lookup"><span data-stu-id="0e77a-113">While use CIM qualifiers in MOF code, the standard qualifiers are designed specifically with WMI in mind.</span></span> <span data-ttu-id="0e77a-114">如需詳細資訊，請參閱「DMTF [CIM」規格](https://www.dmtf.org/spec/cims.html/)。</span><span class="sxs-lookup"><span data-stu-id="0e77a-114">For more information, see the DMTF [CIM Specification](https://www.dmtf.org/spec/cims.html/).</span></span>

-   <span data-ttu-id="0e77a-115">唯一限定詞</span><span class="sxs-lookup"><span data-stu-id="0e77a-115">Unique qualifier</span></span>

    <span data-ttu-id="0e77a-116">唯一限定詞是由類別提供者特別針對新類別所定義的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="0e77a-116">A unique qualifier is a qualifier defined specifically for a new class by a class provider.</span></span> <span data-ttu-id="0e77a-117">例如， [**單位**](standard-qualifiers.md) 限定詞是非標準的提供者特定限定詞。</span><span class="sxs-lookup"><span data-stu-id="0e77a-117">For example, the [**Units**](standard-qualifiers.md) qualifier is a nonstandard, provider-specific qualifier.</span></span> <span data-ttu-id="0e77a-118">您可以建立自己的限定詞來與提供者搭配使用。</span><span class="sxs-lookup"><span data-stu-id="0e77a-118">You can create your own qualifiers for use with your provider.</span></span> <span data-ttu-id="0e77a-119">如需建立提供者的詳細資訊，請參閱 [開發 WMI 提供者](developing-a-wmi-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="0e77a-119">For more information about creating a provider, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

<span data-ttu-id="0e77a-120">無論您的辨識符號有哪些，您執行的主要程式是在您的 MOF 程式碼中使用辨識符號。</span><span class="sxs-lookup"><span data-stu-id="0e77a-120">Whatever your qualifier does, the main process you perform is to use the qualifier in your MOF code.</span></span> <span data-ttu-id="0e77a-121">如需詳細資訊，請參閱套用 [限定詞](applying-a-qualifier.md)。</span><span class="sxs-lookup"><span data-stu-id="0e77a-121">For more information, see [Applying a Qualifier](applying-a-qualifier.md).</span></span> <span data-ttu-id="0e77a-122">您可以進一步描述限定詞類別的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="0e77a-122">You can further describe a qualifier with a qualifier flavor.</span></span> <span data-ttu-id="0e77a-123">限定詞類別包含有關提供者如何使用限定詞的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0e77a-123">A qualifier flavor contains more information regarding how a provider should use a qualifier.</span></span> <span data-ttu-id="0e77a-124">如需詳細資訊，請參閱描述限定詞類別的辨識 [符號](describing-a-qualifier-with-a-qualifier-flavor.md)。</span><span class="sxs-lookup"><span data-stu-id="0e77a-124">For more information, see [Describing a Qualifier with a Qualifier Flavor](describing-a-qualifier-with-a-qualifier-flavor.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e77a-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e77a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e77a-126">設計受控物件格式 (MOF) 類別</span><span class="sxs-lookup"><span data-stu-id="0e77a-126">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 




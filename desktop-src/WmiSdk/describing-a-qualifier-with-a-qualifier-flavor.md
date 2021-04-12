---
description: 限定詞類別是描述限定詞詳細資訊的旗標。
ms.assetid: a7d9d1c0-9386-4c90-9788-993b35ed12db
ms.tgt_platform: multiple
title: 描述限定詞類別的辨識符號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cfc2c590ec8916e2e9538b3e8224e97b3b5dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192199"
---
# <a name="describing-a-qualifier-with-a-qualifier-flavor"></a><span data-ttu-id="ef010-103">描述限定詞類別的辨識符號</span><span class="sxs-lookup"><span data-stu-id="ef010-103">Describing a Qualifier with a Qualifier Flavor</span></span>

<span data-ttu-id="ef010-104">[*限定詞*](gloss-q.md)類別是描述限定詞詳細資訊的旗標。</span><span class="sxs-lookup"><span data-stu-id="ef010-104">A [*qualifier flavor*](gloss-q.md) is a flag that describes more information about a qualifier.</span></span> <span data-ttu-id="ef010-105">例如，限制的辨識符號類別指出 WMI 不應將相關聯的辨識符號傳播至任何衍生的類別或實例。</span><span class="sxs-lookup"><span data-stu-id="ef010-105">For example, the Restricted qualifier flavor states that WMI should not propagate the associated qualifier to any derived classes or instances.</span></span> <span data-ttu-id="ef010-106">您可以使用 MOF 程式碼或以程式設計方式設定類別。</span><span class="sxs-lookup"><span data-stu-id="ef010-106">You can set flavors using either MOF code or programmatically.</span></span> <span data-ttu-id="ef010-107">雖然您可以使用各種不同的方式來描述各種效果，但類別旗標的主要目的是要定義 WMI 如何透過繼承來傳播限定詞。</span><span class="sxs-lookup"><span data-stu-id="ef010-107">While you can describe a variety of effects with flavors, the main purposes of flavor flags is to define how WMI propagates qualifiers through inheritance.</span></span>

<span data-ttu-id="ef010-108">WMI 會定義數個限定詞類別，您可以附加至任何辨識符號，而不論辨識符號的來源為何。</span><span class="sxs-lookup"><span data-stu-id="ef010-108">WMI defines several qualifier flavors that you can attach to any qualifier, regardless of the origin of the qualifier.</span></span> <span data-ttu-id="ef010-109">不過，有些類別並非適用于所有的辨識符號類型。</span><span class="sxs-lookup"><span data-stu-id="ef010-109">However, some flavors are not appropriate for all qualifier types.</span></span> <span data-ttu-id="ef010-110">例如， **ToSubClass** 類別僅適用于為類別定義的限定詞。</span><span class="sxs-lookup"><span data-stu-id="ef010-110">The **ToSubClass** flavor, for example, is appropriate only for qualifiers defined for a class.</span></span> <span data-ttu-id="ef010-111">您無法將 **ToSubClass** 附加至用來描述實例的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="ef010-111">You cannot attach **ToSubClass** to a qualifier used to describe an instance.</span></span>

<span data-ttu-id="ef010-112">您可以使用 [類別] 來描述辨識符號的各種不同效果。</span><span class="sxs-lookup"><span data-stu-id="ef010-112">You can use flavors to describe a variety of different effects for qualifiers.</span></span> <span data-ttu-id="ef010-113">例如，[類別] 可以指出是否可以當地語系化限定詞。</span><span class="sxs-lookup"><span data-stu-id="ef010-113">For example, flavor can indicate if a qualifier can be localized.</span></span> <span data-ttu-id="ef010-114">不過，限定詞類別的主要用途之一，就是描述父類別是否可以將限定詞傳遞給子類別或類別實例。</span><span class="sxs-lookup"><span data-stu-id="ef010-114">However, one of the main purposes of a qualifier flavor is to describe whether a parent class can pass qualifiers to a subclass or class instance.</span></span> <span data-ttu-id="ef010-115">您也可以使用「類別」（class）來判斷類別屬性（property）是否會將限定詞傳遞給實例屬性（property）。</span><span class="sxs-lookup"><span data-stu-id="ef010-115">You can also use flavors to determine if a class property passes a qualifier on to an instance property.</span></span> <span data-ttu-id="ef010-116">最後，使用 [類別] 來陳述子類別是否可以覆寫繼承的辨識符號的原始值。</span><span class="sxs-lookup"><span data-stu-id="ef010-116">Finally, use flavors to state whether a subclass can override the original value of an inherited qualifier.</span></span> <span data-ttu-id="ef010-117">不過，您為類別或實例宣告的限定詞不會傳播至該類別或實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="ef010-117">However, qualifiers that you declare for a class or instance do not propagate to the properties of that class or instance.</span></span> <span data-ttu-id="ef010-118">此外，建立覆寫許可權的類別只有在您同時設定 **ToInstance** 或 **ToSubClass** 類別時才有效。</span><span class="sxs-lookup"><span data-stu-id="ef010-118">Further, flavors that establish override permissions are valid only if you also set the **ToInstance** or **ToSubClass** flavors.</span></span>

<span data-ttu-id="ef010-119">您可以使用下列語法，將類別全域指派給整個 MOF 檔案的辨識符號，其中，當指定多個類別時，泛空白字元會作為分隔符號。</span><span class="sxs-lookup"><span data-stu-id="ef010-119">A flavor can be globally assigned to a qualifier for an entire MOF file using the following syntax in which white space acts as the delimiter when multiple flavors are specified.</span></span>

``` syntax
Qualifier QualifierName : flavor1 <flavor2...>;
```

<span data-ttu-id="ef010-120">全域類別適用于 MOF 檔案中所有後續的辨識符號用法。</span><span class="sxs-lookup"><span data-stu-id="ef010-120">Global flavors apply to all subsequent uses of the qualifier in the MOF file.</span></span> <span data-ttu-id="ef010-121">全域類別語句可能會發生在物件宣告區塊之外的檔案中的任何位置。</span><span class="sxs-lookup"><span data-stu-id="ef010-121">Global flavor statements may occur anywhere in the file outside of an object declaration block.</span></span> <span data-ttu-id="ef010-122">在類別、實例或屬性層級重新定義的類別，會覆寫該物件範圍的全域類別宣告。</span><span class="sxs-lookup"><span data-stu-id="ef010-122">Flavors redefined at the class, instance, or property level override the global flavor declarations for the scope of that object.</span></span>

<span data-ttu-id="ef010-123">您無法定義新的類別。</span><span class="sxs-lookup"><span data-stu-id="ef010-123">You cannot define a new flavor.</span></span> <span data-ttu-id="ef010-124">雖然您可以建立新的辨識符號，但只使用現有的 [限定詞](qualifier-flavors.md) 類別來描述新的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="ef010-124">Although you can create a new qualifier, use only existing [Qualifier Flavors](qualifier-flavors.md) to describe your new qualifier.</span></span>

<span data-ttu-id="ef010-125">**在 MOF 中定義限定詞類別**</span><span class="sxs-lookup"><span data-stu-id="ef010-125">**To define qualifier flavors in MOF**</span></span>

-   <span data-ttu-id="ef010-126">宣告用來描述限定詞名稱之後，限定詞括弧之間指定限定詞的類別。</span><span class="sxs-lookup"><span data-stu-id="ef010-126">Declare the flavors that describe a given qualifier after the qualifier name, between the qualifier brackets.</span></span> <span data-ttu-id="ef010-127">使用空白字元做為多個類別之間的分隔符號。</span><span class="sxs-lookup"><span data-stu-id="ef010-127">Use white space as the delimiter between multiple flavors.</span></span>

    <span data-ttu-id="ef010-128">下列範例顯示附加預先定義之限定詞的模式。</span><span class="sxs-lookup"><span data-stu-id="ef010-128">The following example shows the pattern for attaching predefined qualifiers.</span></span>

    ``` syntax
    [qualifier1 : flavor1 flavor2 flavor3, qualifier2 : flavor1]
    ```

<span data-ttu-id="ef010-129">您只能以程式設計的方式，在 c + + 中新增限定詞類別。</span><span class="sxs-lookup"><span data-stu-id="ef010-129">You can add qualifier flavors programmatically only in C++.</span></span> <span data-ttu-id="ef010-130">雖然您可以藉由呼叫 [**SWbemQualifierSet**](swbemqualifierset-add.md)加入新的辨識符號，但無法在適用于 [WMI 的腳本 API](scripting-api-for-wmi.md)中使用這項作業。</span><span class="sxs-lookup"><span data-stu-id="ef010-130">This operation is not available in the [Scripting API for WMI](scripting-api-for-wmi.md), although you can add a new qualifier by calling [**SWbemQualifierSet.Add**](swbemqualifierset-add.md).</span></span>

<span data-ttu-id="ef010-131">**使用 c + + 指派風格**</span><span class="sxs-lookup"><span data-stu-id="ef010-131">**To assign a flavor using C++**</span></span>

-   <span data-ttu-id="ef010-132">呼叫 [**IWbemQualifierSet：:P**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) lFlavor 參數，並將參數設定為針對方法定義的其中一個常數。</span><span class="sxs-lookup"><span data-stu-id="ef010-132">Call the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method with the *lFlavor* parameter set to one of the constants defined for the method.</span></span>

 

 




---
title: VARIANT 結構
description: 大部分的 Microsoft Active Accessibility 函數和 IAccessible 屬性和方法都採用 VARIANT 結構作為參數。 基本上，VARIANT 結構是大型聯集的容器，它會攜帶許多類型的資料。
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cafc63388de27ae01b3e1ca478add6802ac6b85c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092846"
---
# <a name="variant-structure"></a><span data-ttu-id="f271d-104">VARIANT 結構</span><span class="sxs-lookup"><span data-stu-id="f271d-104">VARIANT Structure</span></span>

<span data-ttu-id="f271d-105">大部分的 Microsoft Active Accessibility 函數和 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法都採用 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 結構作為參數。</span><span class="sxs-lookup"><span data-stu-id="f271d-105">Most of the Microsoft Active Accessibility functions and the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods take a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure as a parameter.</span></span> <span data-ttu-id="f271d-106">基本上， **VARIANT** 結構是大型聯集的容器，它會攜帶許多類型的資料。</span><span class="sxs-lookup"><span data-stu-id="f271d-106">Essentially, the **VARIANT** structure is a container for a large union that carries many types of data.</span></span>

<span data-ttu-id="f271d-107">結構中第一個成員的值（ **vt**）描述了哪些 union 成員是有效的。</span><span class="sxs-lookup"><span data-stu-id="f271d-107">The value in the first member of the structure, **vt**, describes which of the union members is valid.</span></span> <span data-ttu-id="f271d-108">雖然 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 結構支援許多不同的資料類型，但是 Microsoft Active Accessibility 只會使用下列類型。</span><span class="sxs-lookup"><span data-stu-id="f271d-108">Although the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure supports many different data types, Microsoft Active Accessibility uses only the following types.</span></span>



| <span data-ttu-id="f271d-109">vt 值</span><span class="sxs-lookup"><span data-stu-id="f271d-109">vt Value</span></span>     | <span data-ttu-id="f271d-110">對應的值成員名稱</span><span class="sxs-lookup"><span data-stu-id="f271d-110">Corresponding value member name</span></span> |
|--------------|---------------------------------|
| <span data-ttu-id="f271d-111">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f271d-111">VT\_I4</span></span>       | <span data-ttu-id="f271d-112">**lVal**</span><span class="sxs-lookup"><span data-stu-id="f271d-112">**lVal**</span></span>                        |
| <span data-ttu-id="f271d-113">VT \_ 分派</span><span class="sxs-lookup"><span data-stu-id="f271d-113">VT\_DISPATCH</span></span> | <span data-ttu-id="f271d-114">**pdispVal**</span><span class="sxs-lookup"><span data-stu-id="f271d-114">**pdispVal**</span></span>                    |
| <span data-ttu-id="f271d-115">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="f271d-115">VT\_BSTR</span></span>     | <span data-ttu-id="f271d-116">**bstrVal**</span><span class="sxs-lookup"><span data-stu-id="f271d-116">**bstrVal**</span></span>                     |
| <span data-ttu-id="f271d-117">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="f271d-117">VT\_EMPTY</span></span>    | <span data-ttu-id="f271d-118">無</span><span class="sxs-lookup"><span data-stu-id="f271d-118">none</span></span>                            |



 

<span data-ttu-id="f271d-119">當您在 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 結構中接收資訊時，請檢查 **vt** 成員以找出哪些成員包含有效的資料。</span><span class="sxs-lookup"><span data-stu-id="f271d-119">When you receive information in a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure, check the **vt** member to find out which member contains valid data.</span></span> <span data-ttu-id="f271d-120">同樣地，當您使用 **VARIANT** 結構傳送資訊時，請一律設定 **vt** 以反映包含資訊的聯集成員。</span><span class="sxs-lookup"><span data-stu-id="f271d-120">Similarly, when you send information using a **VARIANT** structure, always set **vt** to reflect the union member that contains the information.</span></span>

<span data-ttu-id="f271d-121">使用結構之前，請先呼叫 [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) 元件物件模型 (COM) 函數來將它初始化。</span><span class="sxs-lookup"><span data-stu-id="f271d-121">Before using the structure, initialize it by calling the [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model (COM) function.</span></span> <span data-ttu-id="f271d-122">完成結構之後，請先將它清除，然後再呼叫 [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)來釋放包含 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f271d-122">When finished with the structure, clear it before the memory that contains the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) is freed by calling [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).</span></span>

 

 
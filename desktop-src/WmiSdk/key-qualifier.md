---
description: 金鑰辨識符號會指出屬性是否為命名空間控制碼的一部分。
ms.assetid: 838d295f-e812-4e46-99a4-d2714a0ae8dc
ms.tgt_platform: multiple
title: 金鑰辨識符號
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Key
api_type:
- NA
api_location: ''
ms.openlocfilehash: affc9f4be594723700a65c9c92f8ae37ffead265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694191"
---
# <a name="key-qualifier"></a><span data-ttu-id="5e1df-103">金鑰辨識符號</span><span class="sxs-lookup"><span data-stu-id="5e1df-103">Key Qualifier</span></span>

<span data-ttu-id="5e1df-104">**金鑰** 辨識符號會指出屬性是否為命名空間控制碼的一部分。</span><span class="sxs-lookup"><span data-stu-id="5e1df-104">The **Key** qualifier indicates whether the property is part of the namespace handle.</span></span> <span data-ttu-id="5e1df-105">如果有一個以上的屬性具有索引 **鍵** 限定詞，則所有這類屬性統稱 (複合索引鍵) 。</span><span class="sxs-lookup"><span data-stu-id="5e1df-105">If more than one property has the **Key** qualifier, then all such properties collectively form the key (a compound key).</span></span> <span data-ttu-id="5e1df-106">在一起時，索引鍵屬性必須提供每個類別實例的唯一參考。</span><span class="sxs-lookup"><span data-stu-id="5e1df-106">When taken together, the key properties must supply a unique reference for each class instance.</span></span> <span data-ttu-id="5e1df-107">如果將這個限定詞放置在屬性上，則只允許值 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="5e1df-107">If this qualifier is placed on a property, only the value **TRUE** is allowed.</span></span>

<span data-ttu-id="5e1df-108">除了下列以外，您可以使用任何屬性類型：</span><span class="sxs-lookup"><span data-stu-id="5e1df-108">You can use any property type except for the following:</span></span>

-   <span data-ttu-id="5e1df-109">陣列</span><span class="sxs-lookup"><span data-stu-id="5e1df-109">Arrays</span></span>
-   <span data-ttu-id="5e1df-110">實數和浮點數</span><span class="sxs-lookup"><span data-stu-id="5e1df-110">Real and floating-point numbers</span></span>
-   <span data-ttu-id="5e1df-111">內嵌物件</span><span class="sxs-lookup"><span data-stu-id="5e1df-111">Embedded objects</span></span>
-   <span data-ttu-id="5e1df-112">低於 ASCII 32 的字元 (也就是空白字元) </span><span class="sxs-lookup"><span data-stu-id="5e1df-112">Characters lower than ASCII 32 (that is, white space characters)</span></span>
-   <span data-ttu-id="5e1df-113">**Char16** 類型的字元字串或定義為索引鍵的字元字串，必須包含大於 U + 0020 的值。</span><span class="sxs-lookup"><span data-stu-id="5e1df-113">Character strings of type **char16** or character strings that are defined as keys must contain values greater than U+0020.</span></span> <span data-ttu-id="5e1df-114">這是因為 WMI 會在物件路徑中使用索引鍵值，而您無法在物件路徑中使用非列印字元。</span><span class="sxs-lookup"><span data-stu-id="5e1df-114">This is because WMI uses key values in object paths, and you cannot use nonprinting characters in an object path.</span></span>

<span data-ttu-id="5e1df-115">當父類別指定索引鍵時，衍生自父類別的所有類別都會繼承該索引鍵。</span><span class="sxs-lookup"><span data-stu-id="5e1df-115">When a parent class specifies a key, all classes derived from the parent class inherit that key.</span></span> <span data-ttu-id="5e1df-116">衍生的類別無法改變繼承的索引鍵，或定義任何新的索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="5e1df-116">The derived classes cannot alter the inherited key or define any new key property.</span></span> <span data-ttu-id="5e1df-117">但是，當您從沒有索引鍵的抽象類別衍生子類別時，您可以在子類別中引入一個索引鍵。</span><span class="sxs-lookup"><span data-stu-id="5e1df-117">However, when you derive a subclass from an abstract class without a key, you can introduce a key in the subclass.</span></span>

<span data-ttu-id="5e1df-118">定義一個以上實例的所有類別都必須指定索引鍵。</span><span class="sxs-lookup"><span data-stu-id="5e1df-118">All classes that define more than one instance must specify a key.</span></span> <span data-ttu-id="5e1df-119">因為抽象類別不會定義任何實例，所以不需要指定索引鍵。</span><span class="sxs-lookup"><span data-stu-id="5e1df-119">Because abstract classes do not define any instances, they do not need to specify keys.</span></span> <span data-ttu-id="5e1df-120">因為 singleton 類別只會定義一個實例，所以無法指定索引鍵。</span><span class="sxs-lookup"><span data-stu-id="5e1df-120">Because singleton classes define only one instance, they cannot specify keys.</span></span>

<span data-ttu-id="5e1df-121">在物件具現化時，金鑰會寫入一次，且稍後不得修改。</span><span class="sxs-lookup"><span data-stu-id="5e1df-121">Keys are written one time at object instantiation and must not be modified later.</span></span> <span data-ttu-id="5e1df-122">將預設值套用至索引鍵限定屬性並不合理。</span><span class="sxs-lookup"><span data-stu-id="5e1df-122">It does not make sense to apply a default value to a key-qualified property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e1df-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e1df-123">Requirements</span></span>



| <span data-ttu-id="5e1df-124">需求</span><span class="sxs-lookup"><span data-stu-id="5e1df-124">Requirement</span></span> | <span data-ttu-id="5e1df-125">值</span><span class="sxs-lookup"><span data-stu-id="5e1df-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5e1df-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e1df-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5e1df-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e1df-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5e1df-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e1df-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5e1df-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e1df-129">Windows Server 2008</span></span><br/> |



 

 





---
description: 指定索引鍵以選取純量或資料表集合中的唯一資料列。
ms.assetid: 3c4edae0-55be-4804-b5fe-07458b918365
ms.tgt_platform: multiple
title: INDEX 子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 915cbe1c4bf1da5ccd7fbab881770722b70bc53c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115805"
---
# <a name="index-clause"></a><span data-ttu-id="b38ff-103">INDEX 子句</span><span class="sxs-lookup"><span data-stu-id="b38ff-103">INDEX Clause</span></span>

<span data-ttu-id="b38ff-104">INDEX 子句會指定索引鍵，以選取純量或資料表集合中的唯一資料列。</span><span class="sxs-lookup"><span data-stu-id="b38ff-104">The INDEX clause specifies a key to select a unique row in a scalar or table collection.</span></span> <span data-ttu-id="b38ff-105">SNMP 提供者會根據 SNMP 裝置使用的資料表類型，對應至不同類型的 CIM 類別。</span><span class="sxs-lookup"><span data-stu-id="b38ff-105">The SNMP Provider maps to a different type of CIM class depending on the type of table the SNMP device uses.</span></span> <span data-ttu-id="b38ff-106">因為索引鍵可以是一種以上的物件類型，所以提供者會根據索引鍵內的物件類型，使用不同的對應規則。</span><span class="sxs-lookup"><span data-stu-id="b38ff-106">Because a key can be more than one type of object, the provider uses different mapping rules depending on the type of object within the key.</span></span> <span data-ttu-id="b38ff-107">如需詳細資訊，請參閱 [索引子句資料類型](#index-clause-data-types)。</span><span class="sxs-lookup"><span data-stu-id="b38ff-107">For more information, see [INDEX Clause Data Types](#index-clause-data-types).</span></span>

> [!Note]  
> <span data-ttu-id="b38ff-108">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="b38ff-108">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="b38ff-109">純量集合會對應到 CIM singleton 類別：也就是只能有一個實例的類別。</span><span class="sxs-lookup"><span data-stu-id="b38ff-109">A scalar collection maps to a CIM singleton class: that is, a class that can have only one instance.</span></span> <span data-ttu-id="b38ff-110">因為不需要從另一個實例來唯一識別實例，所以單一類別不會將一或多個屬性指定為索引鍵。</span><span class="sxs-lookup"><span data-stu-id="b38ff-110">Because there is no need to uniquely identify one instance from another, a singleton class does not designate one or more properties as the key.</span></span> <span data-ttu-id="b38ff-111">從純量集合產生的類別：</span><span class="sxs-lookup"><span data-stu-id="b38ff-111">Classes generated from scalar collections:</span></span>

-   <span data-ttu-id="b38ff-112">請勿包含索引 **鍵** 屬性限定詞。</span><span class="sxs-lookup"><span data-stu-id="b38ff-112">Do not contain **Key** property qualifiers.</span></span>
-   <span data-ttu-id="b38ff-113">確實包含標準 CIM 類別辨識符號 **Singleton**，其為 **Bool** 類型。</span><span class="sxs-lookup"><span data-stu-id="b38ff-113">Do contain the standard CIM class qualifier **Singleton**, which is of type **Bool**.</span></span>

<span data-ttu-id="b38ff-114">資料表集合會對應到可以有一個以上實例的 CIM 類別。</span><span class="sxs-lookup"><span data-stu-id="b38ff-114">A table collection maps to a CIM class that can have more than one instance.</span></span> <span data-ttu-id="b38ff-115">因此，CIM 類別定義必須至少包含一個定義物件索引鍵的屬性;也就是可唯一識別類別實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="b38ff-115">As a result, the CIM class definition must contain at least one property that defines the object key; that is, a property that uniquely identifies an instance of the class.</span></span> <span data-ttu-id="b38ff-116">資料表集合的 [物件類型](object-type-macro.md) 宏的 INDEX 子句會指定集合的索引鍵屬性集。</span><span class="sxs-lookup"><span data-stu-id="b38ff-116">The INDEX clause of a table collection's [OBJECT-TYPE](object-type-macro.md) macro specifies the collection's set of key properties.</span></span> <span data-ttu-id="b38ff-117">下列對應規則適用：</span><span class="sxs-lookup"><span data-stu-id="b38ff-117">The following mapping rules apply:</span></span>

-   <span data-ttu-id="b38ff-118">CIM 辨識符號索引 **鍵**（type **Bool**）會定義索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="b38ff-118">The CIM qualifier **Key**, type **Bool**, defines a key property.</span></span>
-   <span data-ttu-id="b38ff-119">資料表集合內的索引資訊順序會定義 CIM 類別定義中索引鍵的順序。</span><span class="sxs-lookup"><span data-stu-id="b38ff-119">The ordering of the INDEX information within the table collection defines the ordering of the keys within the CIM class definition.</span></span>

    <span data-ttu-id="b38ff-120">CIM 辨識符號索引 **鍵 \_ 順序** 會定義索引鍵的順序。</span><span class="sxs-lookup"><span data-stu-id="b38ff-120">The CIM qualifier **Key\_Order** defines the ordering of the keys.</span></span> <span data-ttu-id="b38ff-121">此辨識符號是不帶正負號的32位整數值，基於 MOF 辨識符號語法的目的，必須使用2補數運算，將其轉換為帶正負號的32位整數值。</span><span class="sxs-lookup"><span data-stu-id="b38ff-121">This qualifier is an unsigned 32-bit integer value which, for the purposes of the MOF qualifier syntax, must be converted to a signed 32-bit integer value using the twos-complement operation.</span></span>

<span data-ttu-id="b38ff-122">目前，SNMPv2C INDEX 子句的對應不會處理 **隱含** 辨識符號的使用。</span><span class="sxs-lookup"><span data-stu-id="b38ff-122">Currently, the mapping of the SNMPv2C INDEX clause does not handle the use of the **IMPLIED** qualifier.</span></span> <span data-ttu-id="b38ff-123">在此情況下，不會產生 CIM 類別定義。</span><span class="sxs-lookup"><span data-stu-id="b38ff-123">A CIM class definition is not generated in this case.</span></span>

## <a name="index-clause-data-types"></a><span data-ttu-id="b38ff-124">INDEX 子句資料類型</span><span class="sxs-lookup"><span data-stu-id="b38ff-124">INDEX Clause Data Types</span></span>

<span data-ttu-id="b38ff-125">由於 [OBJECT TYPE](object-type-macro.md) 宏內的 INDEX 子句有彈性，因此索引鍵屬性的規格並不直接。</span><span class="sxs-lookup"><span data-stu-id="b38ff-125">Because of the flexibility of the INDEX clause within the [OBJECT-TYPE](object-type-macro.md) macro, the specification of keyed properties is not straightforward.</span></span> <span data-ttu-id="b38ff-126">相反地，您應該考慮 INDEX 子句可能包含下列一或多個資料類型的可能性：</span><span class="sxs-lookup"><span data-stu-id="b38ff-126">Instead, you should consider the possibilities that the INDEX clause may contain one or more of the following data types:</span></span>

-   <span data-ttu-id="b38ff-127">內部可存取的 **indexobject** 值</span><span class="sxs-lookup"><span data-stu-id="b38ff-127">Internally accessible **indexobject** value</span></span>

    <span data-ttu-id="b38ff-128">**Indexobject** 值是一個名為的值，它會參考出現在包含 INDEX 子句之相同資料表的概念資料列中的 MIB 物件定義。</span><span class="sxs-lookup"><span data-stu-id="b38ff-128">The **indexobject** value is a named value that refers to a MIB object definition appearing in the conceptual row of the same table that contains the INDEX clause.</span></span> <span data-ttu-id="b38ff-129">INDEX 子句中參考的 MIB 物件定義會對應到 CIM 類別定義的索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="b38ff-129">The MIB object definition referred to in the INDEX clause maps to a key property of the CIM class definition.</span></span>

-   <span data-ttu-id="b38ff-130">外部可存取的 **indexobject** 值</span><span class="sxs-lookup"><span data-stu-id="b38ff-130">Externally accessible **indexobject** value</span></span>

    <span data-ttu-id="b38ff-131">在此情況下， **indexobject** 是指在不同資料表的概念資料列中所顯示的 MIB 物件定義的命名值。</span><span class="sxs-lookup"><span data-stu-id="b38ff-131">In this case, **indexobject** is a named value that refers to a MIB object definition appearing in the conceptual row of a different table.</span></span>

-   <span data-ttu-id="b38ff-132">可存取的 **indextype** 值</span><span class="sxs-lookup"><span data-stu-id="b38ff-132">Accessible **indextype** value</span></span>

    <span data-ttu-id="b38ff-133">**Indextype** 值是參考下列其中一種資料類型的命名類型： **INTEGER**、**八進位字串**、**物件識別碼**、 **networkaddress.cache.ttl** 或 **IpAddress**。</span><span class="sxs-lookup"><span data-stu-id="b38ff-133">The **indextype** value is a named type that refers to one of the following data types: **INTEGER**, **OCTET STRING**, **OBJECT IDENTIFIER**, **NetworkAddress**, or **IpAddress**.</span></span> <span data-ttu-id="b38ff-134">如果 INDEX 子句包含 MIB 型別參考，則適用下列對應規則：</span><span class="sxs-lookup"><span data-stu-id="b38ff-134">If the INDEX clause contains an MIB-type reference, the following mapping rules apply:</span></span>

    -   <span data-ttu-id="b38ff-135">所參照的 MIB 物件會對應至 CIM 類別定義的索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="b38ff-135">The MIB object referred to maps to a key property of the CIM class definition.</span></span> <span data-ttu-id="b38ff-136">其型別語法是以指定的 **indextype** 值為基礎，這會使用標準 [語法子句](syntax-clause.md) 對應程式對應到 CIM 屬性限定詞。</span><span class="sxs-lookup"><span data-stu-id="b38ff-136">Its type syntax is based on the **indextype** value specified, which maps to CIM property qualifiers using the standard [SYNTAX clause](syntax-clause.md) mapping procedures.</span></span>
    -   <span data-ttu-id="b38ff-137">對應進程會串連 MIB 資料表物件描述元、底線 (\_) ，以及 INDEX 子句 **indextype** 值的次序順序，以產生唯一的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="b38ff-137">The mapping process generates a unique property name by concatenating the MIB table object descriptor, an underscore (\_), and the rank order of the INDEX clause **indextype** value.</span></span> <span data-ttu-id="b38ff-138">例如，MIB 資料表 **enterpriseIfTable** 的第三個元件 **indextype** 的屬性名稱是 **enterpriseIfTable \_ 3**。</span><span class="sxs-lookup"><span data-stu-id="b38ff-138">For example, the property name for the third component **indextype** of the MIB table **enterpriseIfTable** is **enterpriseIfTable\_3**.</span></span>
    -   <span data-ttu-id="b38ff-139">CIM 屬性會以 **虛擬 \_ 金鑰** 辨識符號進行批註。</span><span class="sxs-lookup"><span data-stu-id="b38ff-139">The CIM property is annotated with the **Virtual\_Key** qualifier.</span></span> <span data-ttu-id="b38ff-140">此辨識符號指定 SNMP 提供者應該根據與類別定義中所有可存取的 MIB 物件定義相關聯之實例資訊的超集合，來計算屬性的值。</span><span class="sxs-lookup"><span data-stu-id="b38ff-140">This qualifier specifies that the SNMP Provider should calculate the value of the property based on the superset of instance information associated with all of the accessible MIB object definitions in the class definition.</span></span>
    -   <span data-ttu-id="b38ff-141">CIM 類別定義必須至少包含一個沒有相關聯 **虛擬 \_ 金鑰** 辨識符號的屬性; 無法指定此屬性會讓類別定義失效。</span><span class="sxs-lookup"><span data-stu-id="b38ff-141">The CIM class definition must contain at least one property that does not have an associated **Virtual\_Key** qualifier; failure to specify this property invalidates the class definition.</span></span>

-   <span data-ttu-id="b38ff-142">固定長度的子類型</span><span class="sxs-lookup"><span data-stu-id="b38ff-142">Fixed-length subtype</span></span>

    <span data-ttu-id="b38ff-143">當 SNMP 資料表集合的 INDEX 子句包含 subtyped 為固定長度八位字串的 SNMP 支援型別時，必須使用 CIM 屬性辨識符號 **固定 \_ 長度** 來指定此值。</span><span class="sxs-lookup"><span data-stu-id="b38ff-143">When the INDEX clause of an SNMP table collection contains an SNMP-supported type that is subtyped as a fixed-length OCTET STRING, the CIM property qualifier **Fixed\_Length** must be used to specify this value.</span></span>

 

 




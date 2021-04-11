---
description: 物件類型宏包含必要的和選擇性子句，可描述 MIB 物件的基本特性。 SNMP 提供者會將 MIB 轉換成物件類型宏的對應部分。
ms.assetid: ad76a4fc-354e-4270-862c-062aa523bf7e
ms.tgt_platform: multiple
title: OBJECT 類型宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c605a414c402f2cf2d18be2d966db6408f23cdc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111961"
---
# <a name="object-type-macro"></a><span data-ttu-id="83fff-104">OBJECT 類型宏</span><span class="sxs-lookup"><span data-stu-id="83fff-104">OBJECT-TYPE Macro</span></span>

<span data-ttu-id="83fff-105">物件類型宏包含必要的和選擇性子句，可描述 MIB 物件的基本特性。</span><span class="sxs-lookup"><span data-stu-id="83fff-105">The OBJECT-TYPE macro contains mandatory and optional clauses that describe the basic characteristics of a MIB object.</span></span> <span data-ttu-id="83fff-106">SNMP 提供者會將 MIB 轉換成物件類型宏的對應部分。</span><span class="sxs-lookup"><span data-stu-id="83fff-106">The SNMP Provider converts an MIB to the corresponding parts of the OBJECT-TYPE macro.</span></span>

> [!Note]  
> <span data-ttu-id="83fff-107">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="83fff-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="components"></a><span data-ttu-id="83fff-108">單元</span><span class="sxs-lookup"><span data-stu-id="83fff-108">Components</span></span>

<dl> <dt>

<span data-ttu-id="83fff-109"><span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>MIB 物件</span><span class="sxs-lookup"><span data-stu-id="83fff-109"><span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>MIB object</span></span>
</dt> <dd>

<span data-ttu-id="83fff-110">物件，其中包含大部分有問題的資料。</span><span class="sxs-lookup"><span data-stu-id="83fff-110">Object that contains most of the data in question.</span></span>

</dd> <dt>

<span data-ttu-id="83fff-111"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>物件描述元</span><span class="sxs-lookup"><span data-stu-id="83fff-111"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Object descriptor</span></span>
</dt> <dd>

<span data-ttu-id="83fff-112">識別每個 MIB 物件的唯一名稱或物件描述元。</span><span class="sxs-lookup"><span data-stu-id="83fff-112">Unique name or object descriptor identifying each MIB object.</span></span> <span data-ttu-id="83fff-113">每個 MIB 物件描述項會完全對應至 CIM 屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="83fff-113">Each MIB object descriptor maps exactly to a CIM property name.</span></span> <span data-ttu-id="83fff-114">例如， **ifIndex** 會轉譯成 **ifIndex**。</span><span class="sxs-lookup"><span data-stu-id="83fff-114">For example, **ifIndex** translates to **ifIndex**.</span></span>

</dd> <dt>

<span data-ttu-id="83fff-115"><span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[語法子句](syntax-clause.md)</span><span class="sxs-lookup"><span data-stu-id="83fff-115"><span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[SYNTAX Clause](syntax-clause.md)</span></span>
</dt> <dd>

<span data-ttu-id="83fff-116">定義 MIB 物件的資料和類型。</span><span class="sxs-lookup"><span data-stu-id="83fff-116">Defines the data and type of an MIB object.</span></span>

</dd> <dt>

<span data-ttu-id="83fff-117"><span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[INDEX 子句](index-clause.md)</span><span class="sxs-lookup"><span data-stu-id="83fff-117"><span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[INDEX clause](index-clause.md)</span></span>
</dt> <dd>

<span data-ttu-id="83fff-118">定義用來選取唯一資料表資料列的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="83fff-118">Defines a key for selecting a unique table row.</span></span>

</dd> <dt>

<span data-ttu-id="83fff-119"><span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>增強子句</span><span class="sxs-lookup"><span data-stu-id="83fff-119"><span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>AUGMENTS clause</span></span>
</dt> <dd>

<span data-ttu-id="83fff-120">指出它所指定的資料表集合可以視為另一個資料表集合的延伸，並且可以取代 SNMPv2 中的 INDEX 子句。</span><span class="sxs-lookup"><span data-stu-id="83fff-120">Indicates that the table collection it specifies can be considered an extension of another table collection, and can replace the INDEX clause in SNMPv2.</span></span> <span data-ttu-id="83fff-121">增強型子句所參考的集合可以與其他資料表集合結合，以形成一個集合。</span><span class="sxs-lookup"><span data-stu-id="83fff-121">The collections referred to by the AUGMENTS clause can be combined with the other table collection to form one collection.</span></span> <span data-ttu-id="83fff-122">產生的集合會共用在鏈中最後一個資料表集合中指定的主要索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="83fff-122">The resulting collection shares the primary key properties specified in the last table collection in the chain.</span></span>

<span data-ttu-id="83fff-123">在此情況下，為 INDEX 子句指定的先前對應規則會套用至鏈中的最後一個資料表集合。</span><span class="sxs-lookup"><span data-stu-id="83fff-123">In this case, the previous mapping rules specified for the INDEX clause are applied to the last table collection in the chain.</span></span> <span data-ttu-id="83fff-124">接著，物件的集合會對應到一個 CIM 類別定義。</span><span class="sxs-lookup"><span data-stu-id="83fff-124">The collection of objects then maps to one CIM class definition.</span></span>

</dd> <dt>

<span data-ttu-id="83fff-125"><span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>物件識別碼子句</span><span class="sxs-lookup"><span data-stu-id="83fff-125"><span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>OBJECT-IDENTIFIER clause</span></span>
</dt> <dd>

<span data-ttu-id="83fff-126">包含 MIB 物件的唯一物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="83fff-126">Contains a unique object identifier for an MIB object.</span></span> <span data-ttu-id="83fff-127">此物件識別碼會對應至 CIM 屬性辨識符號 **物件 \_ 識別碼**。</span><span class="sxs-lookup"><span data-stu-id="83fff-127">This object identifier maps to the CIM property qualifier **object\_identifier**.</span></span>

</dd> <dt>

<span data-ttu-id="83fff-128"><span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[存取和最大存取權子句](access-and-max-access-clauses.md)</span><span class="sxs-lookup"><span data-stu-id="83fff-128"><span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[ACCESS and MAX-ACCESS Clauses](access-and-max-access-clauses.md)</span></span>
</dt> <dd>

<span data-ttu-id="83fff-129">定義 MIB 物件的存取權限。</span><span class="sxs-lookup"><span data-stu-id="83fff-129">Define the access rights to the MIB object.</span></span>

</dd> <dt>

<span data-ttu-id="83fff-130"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION 子句</span><span class="sxs-lookup"><span data-stu-id="83fff-130"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION clause</span></span>
</dt> <dd>

<span data-ttu-id="83fff-131">提供物件的文字描述，該物件會對應至 CIM 屬性辨識符號 **描述**。</span><span class="sxs-lookup"><span data-stu-id="83fff-131">Provides a text description of the object, which maps to the CIM property qualifier **Description**.</span></span> <span data-ttu-id="83fff-132">這個子句可能是空的。</span><span class="sxs-lookup"><span data-stu-id="83fff-132">This clause may be empty.</span></span>

<span data-ttu-id="83fff-133">SNMP 資料表定義中的每個 **資料表** 和 **專案** 物件也包含 DESCRIPTION 子句，也可能是空的。</span><span class="sxs-lookup"><span data-stu-id="83fff-133">Each **TABLE** and **ENTRY** object in an SNMP table definition also contains a DESCRIPTION clause, which also may be empty.</span></span> <span data-ttu-id="83fff-134">資料表和專案描述子句會串連在一起，且結果會對應至 CIM 類別限定詞 **描述**。</span><span class="sxs-lookup"><span data-stu-id="83fff-134">The TABLE and ENTRY DESCRIPTION clauses are concatenated and the result maps to the CIM class qualifier **Description**.</span></span>

</dd> <dt>

<span data-ttu-id="83fff-135"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS 子句</span><span class="sxs-lookup"><span data-stu-id="83fff-135"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS clause</span></span>
</dt> <dd>

<span data-ttu-id="83fff-136">指出是否必須支援此物件。</span><span class="sxs-lookup"><span data-stu-id="83fff-136">Indicates whether the object must be supported.</span></span> <span data-ttu-id="83fff-137">當 STATUS 子句的值 **過時** 時，提供者會從對應中捨棄 MIB 物件。</span><span class="sxs-lookup"><span data-stu-id="83fff-137">When the value of the STATUS clause is **obsolete**, the provider discards the MIB object from the mapping.</span></span> <span data-ttu-id="83fff-138">否則，STATUS 子句會對應到 CIM 屬性限定詞的 **狀態**。</span><span class="sxs-lookup"><span data-stu-id="83fff-138">Otherwise, the STATUS clause maps to the CIM property qualifier **Status**.</span></span>

<span data-ttu-id="83fff-139">針對 SNMPv1，[ **狀態** ] 的慣用值是 [ **強制** ] 或 [ **選擇性**]，但辨識符號可以包含其他一些值。</span><span class="sxs-lookup"><span data-stu-id="83fff-139">For SNMPv1, the preferred value of **Status** is either **mandatory** or **optional**, but the qualifier can contain some other value.</span></span> <span data-ttu-id="83fff-140">若為 SNMPv2C，則 [ **狀態** ] 的慣用值為 [ **目前** ] 或 [已 **淘汰**]，但辨識符號可以包含其他一些值。</span><span class="sxs-lookup"><span data-stu-id="83fff-140">For SNMPv2C, the preferred value of **Status** is either **current** or **deprecated**, but the qualifier can contain some other value.</span></span>

</dd> <dt>

<span data-ttu-id="83fff-141"><span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>DEFVAL 子句</span><span class="sxs-lookup"><span data-stu-id="83fff-141"><span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>DEFVAL clause</span></span>
</dt> <dd>

<span data-ttu-id="83fff-142">將預設值指派給邏輯資料表資料列中的變數，並對應至字串 CIM 屬性辨識符號 **Defval**。</span><span class="sxs-lookup"><span data-stu-id="83fff-142">Assigns a default value to a variable in a logical table row, and maps to the string CIM property qualifier **Defval**.</span></span>

</dd> <dt>

<span data-ttu-id="83fff-143"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE 子句</span><span class="sxs-lookup"><span data-stu-id="83fff-143"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE clause</span></span>
</dt> <dd>

<span data-ttu-id="83fff-144">指的是包含物件之詳細資訊的另一份檔。</span><span class="sxs-lookup"><span data-stu-id="83fff-144">Refers to another document that contains more information about the object.</span></span> <span data-ttu-id="83fff-145">這個子句會對應到 CIM 屬性辨識符號 **參考**，它是字串類型。</span><span class="sxs-lookup"><span data-stu-id="83fff-145">This clause maps to the CIM property qualifier **Reference**, which is of type string.</span></span>

</dd> <dt>

<span data-ttu-id="83fff-146"><span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>單位子句</span><span class="sxs-lookup"><span data-stu-id="83fff-146"><span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>UNITS clause</span></span>
</dt> <dd>

<span data-ttu-id="83fff-147">提供物件所代表內容的精確定義。</span><span class="sxs-lookup"><span data-stu-id="83fff-147">Provides a precise definition of what the object represents.</span></span> <span data-ttu-id="83fff-148">這個子句會對應到 CIM 屬性限定詞 **單位**，這是字串類型。</span><span class="sxs-lookup"><span data-stu-id="83fff-148">This clause maps to the CIM property qualifier **Units**, which is of type string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83fff-149">備註</span><span class="sxs-lookup"><span data-stu-id="83fff-149">Remarks</span></span>

<span data-ttu-id="83fff-150">物件類型宏描述個別 MIB 物件的基本特性。</span><span class="sxs-lookup"><span data-stu-id="83fff-150">The OBJECT-TYPE macro describes the basic characteristics of an individual MIB object.</span></span> <span data-ttu-id="83fff-151">一組物件類型宏可視為相關物件的群組。</span><span class="sxs-lookup"><span data-stu-id="83fff-151">A set of OBJECT-TYPE macros can be considered as a group of related objects.</span></span> <span data-ttu-id="83fff-152">在 SNMPv2C 中，使用物件群組宏將相關物件的集合正式分組到集合中。</span><span class="sxs-lookup"><span data-stu-id="83fff-152">In SNMPv2C, use the OBJECT-GROUP macro to formally group sets of related objects into a collection.</span></span> <span data-ttu-id="83fff-153">不過，在 SNMPv1 中建立集合沒有正式的機制。</span><span class="sxs-lookup"><span data-stu-id="83fff-153">However, there is no formal mechanism for creating collections in SNMPv1.</span></span> <span data-ttu-id="83fff-154">基於 SNMP 提供者的目的，會忽略物件群組宏，但您可以建立群組關聯性和製作集合。</span><span class="sxs-lookup"><span data-stu-id="83fff-154">For the purposes of the SNMP Provider, the OBJECT-GROUP macro is ignored, but you can invent grouping relationships and fabricate collections.</span></span>

 

 




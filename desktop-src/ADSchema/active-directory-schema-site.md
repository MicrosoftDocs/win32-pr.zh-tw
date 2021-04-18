---
title: Active Directory 架構術語
description: 下列詞彙通常是用來參考 Active Directory 架構。
ms.assetid: 22c5756f-d663-4cb7-aab0-956b22a01e9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efca7057a79d87c45cc3e3da4b604e842143fedd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "106968727"
---
# <a name="active-directory-schema-terminology"></a><span data-ttu-id="b1069-103">Active Directory 架構術語</span><span class="sxs-lookup"><span data-stu-id="b1069-103">Active Directory Schema Terminology</span></span>

<span data-ttu-id="b1069-104">下列詞彙通常是用來參考 Active Directory 架構。</span><span class="sxs-lookup"><span data-stu-id="b1069-104">The following terms are commonly used to refer to the Active Directory schema.</span></span>


<dl> <dt>

<span data-ttu-id="b1069-105"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="b1069-105"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="b1069-106">用來描述架構中所定義之類別所代表之物件的資料項目。</span><span class="sxs-lookup"><span data-stu-id="b1069-106">Data items used to describe the objects that are represented by the classes that are defined in the schema.</span></span> <span data-ttu-id="b1069-107">屬性是在架構中與類別分開定義;這可讓您將單一屬性定義套用至許多類別。</span><span class="sxs-lookup"><span data-stu-id="b1069-107">Attributes are defined in the schema separately from the classes; this allows a single attribute definition to be applied to many classes.</span></span> <span data-ttu-id="b1069-108">例如， [**Description**](a-description.md) 是可套用至架構中任何類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="b1069-108">For example, [**Description**](a-description.md) is an attribute that can be applied to any class in the schema.</span></span> <span data-ttu-id="b1069-109">**Description** 屬性會在架構中定義一次，以確保一致性，而不是對使用者的 **描述** 和印表機 **描述** 具有不同的定義。</span><span class="sxs-lookup"><span data-stu-id="b1069-109">The **Description** attribute is defined once in the schema, assuring consistency, rather than having a different definition for **Description** of a user and **Description** of a printer.</span></span>

> [!Note]  
> <span data-ttu-id="b1069-110">Term *屬性* 通常會與 term *屬性* 交換使用。</span><span class="sxs-lookup"><span data-stu-id="b1069-110">The term *property* is frequently used interchangeably with the term *attribute*.</span></span>

 

</dd> <dt>

<span data-ttu-id="b1069-111"><span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>屬性實例</span><span class="sxs-lookup"><span data-stu-id="b1069-111"><span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Attribute Instance</span></span>
</dt> <dd>

<span data-ttu-id="b1069-112">架構中所定義之屬性的出現位置。</span><span class="sxs-lookup"><span data-stu-id="b1069-112">An occurrence of an attribute that is defined in the schema.</span></span> <span data-ttu-id="b1069-113">這個詞彙是用來區別屬性的定義和屬性的離散出現。</span><span class="sxs-lookup"><span data-stu-id="b1069-113">This term is used to distinguish between the definition of an attribute and a discrete occurrence of the attribute.</span></span> <span data-ttu-id="b1069-114">例如，儲存 "Jeff Smith" 的使用者物件，並將 [**Common name**](a-cn.md) 屬性設定為 "jeff smith"，就會建立 [**共同名稱**](a-cn.md)的實例。</span><span class="sxs-lookup"><span data-stu-id="b1069-114">For example, storing a User object for "Jeff Smith" with the [**Common-Name**](a-cn.md) attribute set to "Jeff Smith" creates an instance of [**Common-Name**](a-cn.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1069-115"><span id="Class"></span><span id="class"></span><span id="CLASS"></span>類</span><span class="sxs-lookup"><span data-stu-id="b1069-115"><span id="Class"></span><span id="class"></span><span id="CLASS"></span>Class</span></span>
</dt> <dd>

<span data-ttu-id="b1069-116">目錄服務中所儲存之離散、可識別類型之物件的正式描述。</span><span class="sxs-lookup"><span data-stu-id="b1069-116">A formal description of a discrete, identifiable type of object stored in the directory service.</span></span> <span data-ttu-id="b1069-117">例如， [**使用者**](c-user.md)、 [**列印佇列**](c-printqueue.md)和 [**群組**](c-group.md) 都是類別。</span><span class="sxs-lookup"><span data-stu-id="b1069-117">For example, [**User**](c-user.md), [**Print-Queue**](c-printqueue.md), and [**Group**](c-group.md) are all classes.</span></span> <span data-ttu-id="b1069-118">此外，還有三個不同類別的類別： [結構化類別](classes-structural.md)、 [抽象類別](classes-abstract.md)和 [輔助類別](classes-auxiliary.md)。</span><span class="sxs-lookup"><span data-stu-id="b1069-118">Furthermore, there are 3 distinct categories of classes: [Structural Classes](classes-structural.md), [Abstract Classes](classes-abstract.md), and [Auxiliary Classes](classes-auxiliary.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1069-119"><span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>類別實例</span><span class="sxs-lookup"><span data-stu-id="b1069-119"><span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Class Instance</span></span>
</dt> <dd>

<span data-ttu-id="b1069-120">架構中所定義之類別的出現位置。</span><span class="sxs-lookup"><span data-stu-id="b1069-120">An occurrence of a class that is defined in the schema.</span></span> <span data-ttu-id="b1069-121">這個詞彙是用來區分類別的定義和個別出現的類別。</span><span class="sxs-lookup"><span data-stu-id="b1069-121">This term is used to distinguish between the definition of a class and a discrete occurrence of the class.</span></span> <span data-ttu-id="b1069-122">例如，在目錄服務中儲存 "Jeff Smith" 的 [**使用者**](c-user.md) 物件時，會建立 [**使用者**](c-user.md)的實例。</span><span class="sxs-lookup"><span data-stu-id="b1069-122">For example, storing a [**User**](c-user.md) object for "Jeff Smith" in the directory service creates an instance of [**User**](c-user.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1069-123"><span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>內容規則</span><span class="sxs-lookup"><span data-stu-id="b1069-123"><span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Content Rules</span></span>
</dt> <dd>

<span data-ttu-id="b1069-124">目錄服務中儲存之類別實例的可能內容定義。</span><span class="sxs-lookup"><span data-stu-id="b1069-124">The definition of the possible contents of the class instances that are stored in the directory service.</span></span> <span data-ttu-id="b1069-125">在 NT 目錄服務中 (NTDS) ，在 Active Directory 為基礎時，內容規則會以每個類別之架構定義的 [ [**必須包含**](a-mustcontain.md) ] 和 [ [**可能-包含**](a-maycontain.md) ] 屬性完全表示。</span><span class="sxs-lookup"><span data-stu-id="b1069-125">In NT Directory Services (NTDS), upon which Active Directory is based, the content rules are completely expressed by the [**Must-Contain**](a-mustcontain.md) and [**May-Contain**](a-maycontain.md) attributes of the schema definitions for each class.</span></span>

</dd> <dt>

<span data-ttu-id="b1069-126"><span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>推導</span><span class="sxs-lookup"><span data-stu-id="b1069-126"><span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Derivation</span></span>
</dt> <dd>

<span data-ttu-id="b1069-127">請參閱 *繼承*。</span><span class="sxs-lookup"><span data-stu-id="b1069-127">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="b1069-128"><span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>目錄資訊樹狀目錄</span><span class="sxs-lookup"><span data-stu-id="b1069-128"><span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Directory Information Tree</span></span>
</dt> <dd>

<span data-ttu-id="b1069-129">目錄本身，以樹狀結構表示，其中頂點是 (類別實例的目錄專案) ，而連接線則是專案之間的父子式關聯性。</span><span class="sxs-lookup"><span data-stu-id="b1069-129">The directory itself, represented as a tree structure in which the vertices are the directory entries (class instances) and the connecting lines the parent-child relationships between the entries.</span></span>

</dd> <dt>

<span data-ttu-id="b1069-130"><span id="DIT"></span><span id="dit"></span>DIT</span><span class="sxs-lookup"><span data-stu-id="b1069-130"><span id="DIT"></span><span id="dit"></span>DIT</span></span>
</dt> <dd>

<span data-ttu-id="b1069-131">請參閱 *目錄資訊樹狀目錄*。</span><span class="sxs-lookup"><span data-stu-id="b1069-131">See *Directory Information Tree*.</span></span>

</dd> <dt>

<span data-ttu-id="b1069-132"><span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>控制存取權限</span><span class="sxs-lookup"><span data-stu-id="b1069-132"><span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Control Access Rights</span></span>
</dt> <dd>

<span data-ttu-id="b1069-133">類別，描述未系結至資源但動作的存取權。</span><span class="sxs-lookup"><span data-stu-id="b1069-133">A class that describes an access right not tied to a resource, but an action.</span></span> <span data-ttu-id="b1069-134">例如，可以授與使用者建立相對識別碼值的許可權。</span><span class="sxs-lookup"><span data-stu-id="b1069-134">For example, a user can be granted the right to create relative ID values.</span></span>

</dd> <dt>

<span data-ttu-id="b1069-135"><span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>繼承</span><span class="sxs-lookup"><span data-stu-id="b1069-135"><span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Inheritance</span></span>
</dt> <dd>

<span data-ttu-id="b1069-136">能夠從現有的物件類別建立新的物件類別。</span><span class="sxs-lookup"><span data-stu-id="b1069-136">The ability to build new object classes from existing object classes.</span></span> <span data-ttu-id="b1069-137">新物件會定義為父物件的子 *類別* 。</span><span class="sxs-lookup"><span data-stu-id="b1069-137">The new object is defined as a *subclass* of the parent object.</span></span> <span data-ttu-id="b1069-138">父物件變成新物件的 *超級類別* 。</span><span class="sxs-lookup"><span data-stu-id="b1069-138">The parent object becomes a *superclass* of the new object.</span></span> <span data-ttu-id="b1069-139">子類別會繼承父系的屬性，包括結構規則和內容規則。</span><span class="sxs-lookup"><span data-stu-id="b1069-139">A subclass inherits the attributes of the parent, including structure rules and content rules.</span></span>

</dd> <dt>

<span data-ttu-id="b1069-140"><span id="LDAP"></span><span id="ldap"></span>Ldap</span><span class="sxs-lookup"><span data-stu-id="b1069-140"><span id="LDAP"></span><span id="ldap"></span>LDAP</span></span>
</dt> <dd>

<span data-ttu-id="b1069-141">請參閱 *輕量型目錄存取協定*。</span><span class="sxs-lookup"><span data-stu-id="b1069-141">See *Lightweight Directory Access Protocol*.</span></span>

</dd> <dt>

<span data-ttu-id="b1069-142"><span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>輕量型目錄存取協定</span><span class="sxs-lookup"><span data-stu-id="b1069-142"><span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Lightweight Directory Access Protocol</span></span>
</dt> <dd>

<span data-ttu-id="b1069-143">用來與 NTDS 通訊的標準網際網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b1069-143">A standard Internet communications protocol used to communicate with the NTDS.</span></span> <span data-ttu-id="b1069-144">支援 LDAP 第2版和第3版。</span><span class="sxs-lookup"><span data-stu-id="b1069-144">LDAP version 2 and version 3 are supported.</span></span>

</dd> <dt>

<span data-ttu-id="b1069-145"><span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>NT 安全描述項</span><span class="sxs-lookup"><span data-stu-id="b1069-145"><span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>NT Security Descriptor</span></span>
</dt> <dd>

<span data-ttu-id="b1069-146">請參閱 *安全描述項*。</span><span class="sxs-lookup"><span data-stu-id="b1069-146">See *Security Descriptor*.</span></span>

</dd> <dt>

<span data-ttu-id="b1069-147"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>物件</span><span class="sxs-lookup"><span data-stu-id="b1069-147"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Object</span></span>
</dt> <dd>

<span data-ttu-id="b1069-148">目錄服務中的資料儲存體單位。</span><span class="sxs-lookup"><span data-stu-id="b1069-148">A unit of data storage in the directory service.</span></span> <span data-ttu-id="b1069-149">目錄服務物件不會與 COM 物件或其他具有可執行元件和執行時間行為的物件導向系統物件混淆。</span><span class="sxs-lookup"><span data-stu-id="b1069-149">Directory service objects are not to be confused with COM objects or other object-oriented system objects, which have an executable component and run-time behavior.</span></span> <span data-ttu-id="b1069-150">目錄服務物件僅包含資料。</span><span class="sxs-lookup"><span data-stu-id="b1069-150">Directory service objects consist only of data.</span></span> <span data-ttu-id="b1069-151">目錄服務物件是由類別 [**架構**](c-classschema.md)物件和 [**類別架構**](c-classschema.md)物件所參考的一組 [**屬性架構**](c-attributeschema.md)物件所定義。</span><span class="sxs-lookup"><span data-stu-id="b1069-151">A directory service object is defined by a [**Class-Schema**](c-classschema.md) object and a group of [**Attribute-Schema**](c-attributeschema.md) objects referenced by the [**Class-Schema**](c-classschema.md) object.</span></span>

<span data-ttu-id="b1069-152">[**類別架構**](c-classschema.md) 和 [**屬性架構**](c-attributeschema.md) 物件本身是目錄服務物件，且架構中的定義與任何其他物件一樣。</span><span class="sxs-lookup"><span data-stu-id="b1069-152">[**Class-Schema**](c-classschema.md) and [**Attribute-Schema**](c-attributeschema.md) objects are themselves directory service objects, and have definitions in the schema like any other objects.</span></span> <span data-ttu-id="b1069-153">請參閱 *類別*。</span><span class="sxs-lookup"><span data-stu-id="b1069-153">See *Class*.</span></span>

</dd> <dt>

<span data-ttu-id="b1069-154"><span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>物件識別碼</span><span class="sxs-lookup"><span data-stu-id="b1069-154"><span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Object Identifier</span></span>
</dt> <dd>

<span data-ttu-id="b1069-155">由各種發行授權單位所發行的唯一數值，可唯一識別資料元素、語法，以及分散式應用程式的各種其他部分。</span><span class="sxs-lookup"><span data-stu-id="b1069-155">Unique numeric values, issued by various issuing authorities, to uniquely identify data elements, syntaxes, and various other parts of distributed applications.</span></span> <span data-ttu-id="b1069-156">在 OSI 應用程式、x.500 目錄、SNMP 和其他重要的應用程式中，都可以找到 (Oid) 的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1069-156">Object Identifiers (OIDs) are found in OSI applications, X.500 Directories, SNMP, and other applications where uniqueness is important.</span></span> <span data-ttu-id="b1069-157">Oid 是以樹狀結構為基礎，在此結構中，較高的發行授權單位（例如 ISO）會將樹狀結構的分支配置給子授權單位，進而配置子分支。</span><span class="sxs-lookup"><span data-stu-id="b1069-157">OIDs are based on a tree structure, in which a superior issuing authority, such as the ISO, allocates a branch of the tree to a sub-authority, which in turn can allocate sub-branches.</span></span>

<span data-ttu-id="b1069-158">NTDS 中的 Oid 包括由 ISO 針對 X. 500 類別和屬性簽發的部分，以及某些由 Microsoft 發出的 Oid。</span><span class="sxs-lookup"><span data-stu-id="b1069-158">OIDs in the NTDS include some issued by the ISO for X.500 classes and attributes, and some issued by Microsoft.</span></span> <span data-ttu-id="b1069-159">OID 標記法是數位的點字串，例如 "1.2.840.113556.1.5.4"，它會轉譯成下列清單所列的字串。</span><span class="sxs-lookup"><span data-stu-id="b1069-159">OID notation is a dotted string of numbers, for example "1.2.840.113556.1.5.4", which translates as listed in the following list.</span></span> 

| <span data-ttu-id="b1069-160">值</span><span class="sxs-lookup"><span data-stu-id="b1069-160">Value</span></span>  | <span data-ttu-id="b1069-161">描述</span><span class="sxs-lookup"><span data-stu-id="b1069-161">Description</span></span>                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1069-162">1</span><span class="sxs-lookup"><span data-stu-id="b1069-162">1</span></span>      | <span data-ttu-id="b1069-163">ISO-「根授權單位」，發行了 "1.2" 至 ANSI，後者接著 .。。</span><span class="sxs-lookup"><span data-stu-id="b1069-163">ISO - the "root authority", issued "1.2" to ANSI, which in turn...</span></span>                           |
| <span data-ttu-id="b1069-164">2</span><span class="sxs-lookup"><span data-stu-id="b1069-164">2</span></span>      | <span data-ttu-id="b1069-165">Ansi。。。發給美國的 "1.2.840"，也就是 .。。</span><span class="sxs-lookup"><span data-stu-id="b1069-165">ANSI ...issued "1.2.840" to USA, which in turn...</span></span>                                            |
| <span data-ttu-id="b1069-166">840</span><span class="sxs-lookup"><span data-stu-id="b1069-166">840</span></span>    | <span data-ttu-id="b1069-167">美國。。。已向 Microsoft 發出 "1.2.840.113556" .。。</span><span class="sxs-lookup"><span data-stu-id="b1069-167">USA ...issued "1.2.840.113556" to Microsoft...</span></span>                                               |
| <span data-ttu-id="b1069-168">113556</span><span class="sxs-lookup"><span data-stu-id="b1069-168">113556</span></span> | <span data-ttu-id="b1069-169">微軟。。。其中 Microsoft 會在 "1.2.840.113556" 下管理數個 OID 分支。</span><span class="sxs-lookup"><span data-stu-id="b1069-169">Microsoft ...where Microsoft internally manages several OID branches under "1.2.840.113556".</span></span> |
| <span data-ttu-id="b1069-170">1</span><span class="sxs-lookup"><span data-stu-id="b1069-170">1</span></span>      | <span data-ttu-id="b1069-171">Microsoft DS</span><span class="sxs-lookup"><span data-stu-id="b1069-171">Microsoft DS</span></span>                                                                                 |
| <span data-ttu-id="b1069-172">5</span><span class="sxs-lookup"><span data-stu-id="b1069-172">5</span></span>      | <span data-ttu-id="b1069-173">NTDS 類別</span><span class="sxs-lookup"><span data-stu-id="b1069-173">NTDS Classes</span></span>                                                                                 |
| <span data-ttu-id="b1069-174">4</span><span class="sxs-lookup"><span data-stu-id="b1069-174">4</span></span>      | <span data-ttu-id="b1069-175">Builtin-Domain</span><span class="sxs-lookup"><span data-stu-id="b1069-175">Builtin-Domain</span></span>                                                                               |



 

</dd> <dt>

<span data-ttu-id="b1069-176"><span id="OID"></span><span id="oid"></span>老</span><span class="sxs-lookup"><span data-stu-id="b1069-176"><span id="OID"></span><span id="oid"></span>OID</span></span>
</dt> <dd>

<span data-ttu-id="b1069-177">請參閱 *物件識別碼*。</span><span class="sxs-lookup"><span data-stu-id="b1069-177">See *Object Identifier*.</span></span>

</dd> <dt>

<span data-ttu-id="b1069-178"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>模式</span><span class="sxs-lookup"><span data-stu-id="b1069-178"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Schema</span></span>
</dt> <dd>

<span data-ttu-id="b1069-179">目錄服務內容和結構的正式定義。</span><span class="sxs-lookup"><span data-stu-id="b1069-179">A formal definition of the directory service contents and structure.</span></span> <span data-ttu-id="b1069-180">架構會定義所有的屬性和類別。</span><span class="sxs-lookup"><span data-stu-id="b1069-180">The schema defines all attributes and classes.</span></span> <span data-ttu-id="b1069-181">針對每個類別，會定義 [**Poss-Superiors**](a-posssuperiors.md)、 [**必須包含**](a-mustcontain.md)，而且 [**可能包含**](a-maycontain.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="b1069-181">For each class, the [**Poss-Superiors**](a-posssuperiors.md), [**Must-Contain**](a-mustcontain.md), and [**May-Contain**](a-maycontain.md) attributes are defined.</span></span> <span data-ttu-id="b1069-182">[**Poss-Superiors**](a-posssuperiors.md) 藉由指定哪些類別可以是任何指定類別的父系，來定義目錄服務的可能樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="b1069-182">[**Poss-Superiors**](a-posssuperiors.md) defines the possible tree structures for the directory service by specifying what classes can be the parent for any given class.</span></span> <span data-ttu-id="b1069-183">[**必須包含**](a-mustcontain.md) 且 [**可能包含**](a-maycontain.md) 類別的屬性，這些屬性必須存在才能儲存類別，以及選擇性的其他屬性可能會出現。</span><span class="sxs-lookup"><span data-stu-id="b1069-183">[**Must-Contain**](a-mustcontain.md) and [**May-Contain**](a-maycontain.md) list the attributes for a class that must be present to store the class and what additional attributes may optionally be present.</span></span>

</dd> <dt>

<span data-ttu-id="b1069-184"><span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>安全描述項</span><span class="sxs-lookup"><span data-stu-id="b1069-184"><span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Security Descriptor</span></span>
</dt> <dd>

<span data-ttu-id="b1069-185">物件擁有權的相關資訊，以及其他使用者對該物件的許可權。</span><span class="sxs-lookup"><span data-stu-id="b1069-185">Information about the ownership of an object and the permissions that other users have on that object.</span></span> <span data-ttu-id="b1069-186">架構專案的 [**NT-Security-描述**](a-ntsecuritydescriptor.md) 元屬性包含表示物件安全描述項的字串。</span><span class="sxs-lookup"><span data-stu-id="b1069-186">The [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md) property of a schema entry contains a string that represents the security descriptor of the object.</span></span> <span data-ttu-id="b1069-187">如需此欄位中資訊格式的詳細資訊，請參閱 [安全描述項字串格式](/windows/desktop/SecAuthZ/security-descriptor-string-format)。</span><span class="sxs-lookup"><span data-stu-id="b1069-187">For more information about the format of the information in this field, see [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span></span>

</dd> <dt>

<span data-ttu-id="b1069-188"><span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>結構規則</span><span class="sxs-lookup"><span data-stu-id="b1069-188"><span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Structure Rules</span></span>
</dt> <dd>

<span data-ttu-id="b1069-189">可能的樹狀結構或結構的定義。</span><span class="sxs-lookup"><span data-stu-id="b1069-189">The definition of the possible tree structure or structures.</span></span> <span data-ttu-id="b1069-190">在 NTDS 中，結構規則會以 Poss superiors 屬性（存在於每個 [**類別架構**](c-classschema.md) 物件上）完全表示。</span><span class="sxs-lookup"><span data-stu-id="b1069-190">In the NTDS, the structure rules are completely expressed by the Poss-superiors attribute present on each [**Class-Schema**](c-classschema.md) object.</span></span> <span data-ttu-id="b1069-191">請參閱 *架構*。</span><span class="sxs-lookup"><span data-stu-id="b1069-191">See *Schema*.</span></span>

</dd> <dt>

<span data-ttu-id="b1069-192"><span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>類</span><span class="sxs-lookup"><span data-stu-id="b1069-192"><span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Subclass</span></span>
</dt> <dd>

<span data-ttu-id="b1069-193">繼承自另一個 [**類別架構**](c-classschema.md)物件的 [**類別架構**](c-classschema.md)物件。</span><span class="sxs-lookup"><span data-stu-id="b1069-193">A [**Class-Schema**](c-classschema.md) object that inherits from another [**Class-Schema**](c-classschema.md) object.</span></span> <span data-ttu-id="b1069-194">請參閱 *繼承*。</span><span class="sxs-lookup"><span data-stu-id="b1069-194">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="b1069-195"><span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>超級</span><span class="sxs-lookup"><span data-stu-id="b1069-195"><span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Superclass</span></span>
</dt> <dd>

<span data-ttu-id="b1069-196">一個或多個其他 [**類別架構**](c-classschema.md)物件所繼承的 [**類別架構**](c-classschema.md)物件。</span><span class="sxs-lookup"><span data-stu-id="b1069-196">A [**Class-Schema**](c-classschema.md) object from which one or more other [**Class-Schema**](c-classschema.md) objects inherit.</span></span> <span data-ttu-id="b1069-197">請參閱 *繼承*。</span><span class="sxs-lookup"><span data-stu-id="b1069-197">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="b1069-198"><span id="Tree"></span><span id="tree"></span><span id="TREE"></span>樹</span><span class="sxs-lookup"><span data-stu-id="b1069-198"><span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Tree</span></span>
</dt> <dd>

<span data-ttu-id="b1069-199">請參閱 *目錄資訊樹狀目錄*。</span><span class="sxs-lookup"><span data-stu-id="b1069-199">See *Directory Information Tree*.</span></span>

</dd> <dt>

<span data-ttu-id="b1069-200"><span id="X.500"></span><span id="x.500"></span>X. 500</span><span class="sxs-lookup"><span data-stu-id="b1069-200"><span id="X.500"></span><span id="x.500"></span>X.500</span></span>
</dt> <dd>

<span data-ttu-id="b1069-201">由 ISO 和 ITU 共同開發的標準系列（先前稱為 CCITT），可指定目錄服務的命名、資料表示和通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b1069-201">A family of standards developed jointly by the ISO and ITU, formerly known as the CCITT, that specify the naming, data representation, and communications protocols for a directory service.</span></span>

</dd> </dl>

 

 
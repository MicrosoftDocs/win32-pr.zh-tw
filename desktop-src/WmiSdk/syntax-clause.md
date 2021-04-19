---
description: 包含定義 MIB 物件的資料和類型的語法子句。
ms.assetid: 24c483c8-db50-492f-9c2e-72620395331a
ms.tgt_platform: multiple
title: 語法子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d0bf25156ddda4bf71a7f40a8de1fede2a82d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989036"
---
# <a name="syntax-clause"></a><span data-ttu-id="83ff4-103">語法子句</span><span class="sxs-lookup"><span data-stu-id="83ff4-103">SYNTAX Clause</span></span>

<span data-ttu-id="83ff4-104">[物件類型](object-type-macro.md)宏包含語法子句，此子句會定義 MIB 物件的資料和類型。</span><span class="sxs-lookup"><span data-stu-id="83ff4-104">The [OBJECT-TYPE](object-type-macro.md) macro contains a SYNTAX clause that defines the data and type for the MIB object.</span></span> <span data-ttu-id="83ff4-105">雖然 SNMP 提供者會觀察對應語法子句的一般規則，但是提供者也會遵循數種資料類型的特定規則。</span><span class="sxs-lookup"><span data-stu-id="83ff4-105">While the SNMP Provider observes general rules for mapping SYNTAX clauses, the provider also follows rules specific to several data types.</span></span>

> [!Note]  
> <span data-ttu-id="83ff4-106">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="83ff4-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="83ff4-107">下列對應規則適用于下表所述的所有資料類型：</span><span class="sxs-lookup"><span data-stu-id="83ff4-107">The following mapping rules apply to all of the data types described in the table below:</span></span>

-   <span data-ttu-id="83ff4-108">語法子句的文字標記法會對應到 CIM 屬性辨識符號 **文字 \_ 慣例**。</span><span class="sxs-lookup"><span data-stu-id="83ff4-108">The textual representation of the SYNTAX clause maps to the CIM property qualifier **textual\_convention**.</span></span>
-   <span data-ttu-id="83ff4-109">語法子句中的指名型別定義會對應到 CIM 屬性限定詞 **物件 \_ 語法**。</span><span class="sxs-lookup"><span data-stu-id="83ff4-109">The named type definition in the SYNTAX clause maps to the CIM property qualifier **object\_syntax**.</span></span> <span data-ttu-id="83ff4-110">這個對應會根據資料類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="83ff4-110">This mapping differs depending on the data type.</span></span> <span data-ttu-id="83ff4-111">如需詳細資訊，請參閱對應描述。</span><span class="sxs-lookup"><span data-stu-id="83ff4-111">For more information, see the mapping descriptions.</span></span>
-   <span data-ttu-id="83ff4-112">將 SNMPv1 和 SNMPv2C 通訊協定框架編碼時，所使用的 SNMP 類型會對應至 CIM 屬性限定詞 **編碼**。</span><span class="sxs-lookup"><span data-stu-id="83ff4-112">The SNMP type used when encoding SNMPv1 and SNMPv2C protocol frames maps to the CIM property qualifier **encoding**.</span></span>
-   <span data-ttu-id="83ff4-113">CIM 屬性限定詞 **cimtype** 包含格式化基礎 CIM 通訊協定值的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="83ff4-113">The CIM property qualifier **cimtype** contains the textual representation that formats the underlying CIM protocol value.</span></span>

<span data-ttu-id="83ff4-114">下表列出具有管理提供者對應行為之特定規則的資料類型。</span><span class="sxs-lookup"><span data-stu-id="83ff4-114">The following table lists data types that have specific rules that govern the provider mapping behavior.</span></span>



| <span data-ttu-id="83ff4-115">SNMP 資料類型</span><span class="sxs-lookup"><span data-stu-id="83ff4-115">SNMP data type</span></span>                                     | <span data-ttu-id="83ff4-116">Description</span><span class="sxs-lookup"><span data-stu-id="83ff4-116">Description</span></span>                                                                                                                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83ff4-117">基本型別</span><span class="sxs-lookup"><span data-stu-id="83ff4-117">Primitive type</span></span>](#primitive-type)                  | <span data-ttu-id="83ff4-118">管理資訊的結構中定義的其中一個基本資料類型 (SMI-S) 檔 RFC 1213 和 RFC 1903。</span><span class="sxs-lookup"><span data-stu-id="83ff4-118">One of the basic data types defined in the Structure of Management Information (SMI) documents RFC 1213 and RFC 1903.</span></span>                                                                                                                            |
| [<span data-ttu-id="83ff4-119">文字慣例</span><span class="sxs-lookup"><span data-stu-id="83ff4-119">Textual convention</span></span>](textual-convention-macro.md) | <span data-ttu-id="83ff4-120">透過明確使用 SNMPv2C **文字慣例** 宏所產生的型別定義，或是透過使用命名的型別所產生的型別定義。</span><span class="sxs-lookup"><span data-stu-id="83ff4-120">Type definition generated through the explicit use of the SNMPv2C **TEXTUAL-CONVENTION** macro or generated through the use of a named type.</span></span> <span data-ttu-id="83ff4-121">文字慣例會指派名稱，而在某些情況下會將某個範圍的值指派給現有的資料類型。</span><span class="sxs-lookup"><span data-stu-id="83ff4-121">A textual convention assigns a name and, in some cases, a range of values to an existing data type.</span></span> |
| [<span data-ttu-id="83ff4-122">命名類型</span><span class="sxs-lookup"><span data-stu-id="83ff4-122">Named type</span></span>](#named-type)                          | <span data-ttu-id="83ff4-123">基本類型、文字慣例或受限型別的命名參考。</span><span class="sxs-lookup"><span data-stu-id="83ff4-123">Named reference to a primitive type, textual convention, or constrained type.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="83ff4-124">條件約束類型</span><span class="sxs-lookup"><span data-stu-id="83ff4-124">Constrained type</span></span>](#constrained-type)              | <span data-ttu-id="83ff4-125">已受限於 SMI-S 檔 RFC 1213 和 RFC 1903 中所定義之某些 subtyping 機制的基本類型、命名類型或文字慣例。</span><span class="sxs-lookup"><span data-stu-id="83ff4-125">Primitive type, named type, or textual convention that has been constrained by some subtyping mechanism defined in the SMI documents RFC 1213 and RFC 1903.</span></span>                                                                                      |



 

## <a name="primitive-type"></a><span data-ttu-id="83ff4-126">基本類型</span><span class="sxs-lookup"><span data-stu-id="83ff4-126">Primitive Type</span></span>

<span data-ttu-id="83ff4-127">基本型別是 (SMI-S) 檔 RFC 1213 和 RFC 1903 的管理資訊結構中所定義的其中一個基本資料類型。</span><span class="sxs-lookup"><span data-stu-id="83ff4-127">The primitive type is one of the basic data types defined in the Structure of Management Information (SMI) documents RFC 1213 and RFC 1903.</span></span> <span data-ttu-id="83ff4-128">SNMP 基本型別對應到 CIM 定義的類型。</span><span class="sxs-lookup"><span data-stu-id="83ff4-128">SNMP primitive types map to CIM-defined types.</span></span> <span data-ttu-id="83ff4-129">下表列出語法子句明確參考 SNMPv1 的基本類型時所發生的對應。</span><span class="sxs-lookup"><span data-stu-id="83ff4-129">The following table lists the mapping that occurs when the SYNTAX clause explicitly refers to a primitive type for SNMPv1.</span></span> <span data-ttu-id="83ff4-130">**文字 \_ 慣例**、**編碼方式** 和 **物件 \_ 語法** 辨識符號一律與 MIB 類型相同，且預設值一律為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="83ff4-130">The **textual\_convention**, **encoding**, and **object\_syntax** qualifiers are always the same as the MIB type and the default value is always **NULL**.</span></span>



| <span data-ttu-id="83ff4-131">MIB 類型</span><span class="sxs-lookup"><span data-stu-id="83ff4-131">MIB type</span></span>         | <span data-ttu-id="83ff4-132">CIM 變異類型</span><span class="sxs-lookup"><span data-stu-id="83ff4-132">CIM variant type</span></span> | <span data-ttu-id="83ff4-133">cimtype 值</span><span class="sxs-lookup"><span data-stu-id="83ff4-133">cimtype value</span></span> |
|------------------|------------------|---------------|
| <span data-ttu-id="83ff4-134">INTEGER</span><span class="sxs-lookup"><span data-stu-id="83ff4-134">INTEGER</span></span>          | <span data-ttu-id="83ff4-135">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="83ff4-135">VT\_I4</span></span>           | <span data-ttu-id="83ff4-136">**sint32**</span><span class="sxs-lookup"><span data-stu-id="83ff4-136">**sint32**</span></span>    |
| <span data-ttu-id="83ff4-137">OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="83ff4-137">OCTETSTRING</span></span>      | <span data-ttu-id="83ff4-138">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="83ff4-138">VT\_BSTR</span></span>         | <span data-ttu-id="83ff4-139">**string**</span><span class="sxs-lookup"><span data-stu-id="83ff4-139">**string**</span></span>    |
| <span data-ttu-id="83ff4-140">OBJECTIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="83ff4-140">OBJECTIDENTIFIER</span></span> | <span data-ttu-id="83ff4-141">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="83ff4-141">VT\_BSTR</span></span>         | <span data-ttu-id="83ff4-142">**string**</span><span class="sxs-lookup"><span data-stu-id="83ff4-142">**string**</span></span>    |
| <span data-ttu-id="83ff4-143">NULL</span><span class="sxs-lookup"><span data-stu-id="83ff4-143">NULL</span></span>             | <span data-ttu-id="83ff4-144">VT \_ Null</span><span class="sxs-lookup"><span data-stu-id="83ff4-144">VT\_NULL</span></span>         | <span data-ttu-id="83ff4-145">不支援</span><span class="sxs-lookup"><span data-stu-id="83ff4-145">Not supported</span></span> |
| <span data-ttu-id="83ff4-146">IpAddress</span><span class="sxs-lookup"><span data-stu-id="83ff4-146">IpAddress</span></span>        | <span data-ttu-id="83ff4-147">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="83ff4-147">VT\_BSTR</span></span>         | <span data-ttu-id="83ff4-148">**string**</span><span class="sxs-lookup"><span data-stu-id="83ff4-148">**string**</span></span>    |
| <span data-ttu-id="83ff4-149">計數器</span><span class="sxs-lookup"><span data-stu-id="83ff4-149">Counter</span></span>          | <span data-ttu-id="83ff4-150">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="83ff4-150">VT\_I4</span></span>           | <span data-ttu-id="83ff4-151">**uint32**</span><span class="sxs-lookup"><span data-stu-id="83ff4-151">**uint32**</span></span>    |
| <span data-ttu-id="83ff4-152">量測計</span><span class="sxs-lookup"><span data-stu-id="83ff4-152">Gauge</span></span>            | <span data-ttu-id="83ff4-153">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="83ff4-153">VT\_I4</span></span>           | <span data-ttu-id="83ff4-154">**uint32**</span><span class="sxs-lookup"><span data-stu-id="83ff4-154">**uint32**</span></span>    |
| <span data-ttu-id="83ff4-155">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="83ff4-155">TimeTicks</span></span>        | <span data-ttu-id="83ff4-156">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="83ff4-156">VT\_I4</span></span>           | <span data-ttu-id="83ff4-157">**uint32**</span><span class="sxs-lookup"><span data-stu-id="83ff4-157">**uint32**</span></span>    |
| <span data-ttu-id="83ff4-158">Opaque</span><span class="sxs-lookup"><span data-stu-id="83ff4-158">Opaque</span></span>           | <span data-ttu-id="83ff4-159">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="83ff4-159">VT\_BSTR</span></span>         | <span data-ttu-id="83ff4-160">**string**</span><span class="sxs-lookup"><span data-stu-id="83ff4-160">**string**</span></span>    |
| <span data-ttu-id="83ff4-161">Networkaddress.cache.ttl</span><span class="sxs-lookup"><span data-stu-id="83ff4-161">NetworkAddress</span></span>   | <span data-ttu-id="83ff4-162">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="83ff4-162">VT\_BSTR</span></span>         | <span data-ttu-id="83ff4-163">**string**</span><span class="sxs-lookup"><span data-stu-id="83ff4-163">**string**</span></span>    |



 

<span data-ttu-id="83ff4-164">當語法子句參考 **Null**（明確地或透過命名類型指派）時，提供者會忽略物件類型宏。</span><span class="sxs-lookup"><span data-stu-id="83ff4-164">The provider ignores the OBJECT-TYPE macro when the SYNTAX clause refers to **NULL**, either explicitly or through a named type assignment.</span></span> <span data-ttu-id="83ff4-165">下表列出語法子句明確參考 SNMPv2 的基本類型時所發生的對應。</span><span class="sxs-lookup"><span data-stu-id="83ff4-165">The following table lists the mapping that occurs when the SYNTAX clause explicitly refers to a primitive type for SNMPv2.</span></span> <span data-ttu-id="83ff4-166">**文字 \_ 慣例**、**編碼方式** 和 **物件 \_ 語法** 辨識符號一律與 MIB 類型相同，且預設值一律為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="83ff4-166">The **textual\_convention**, **encoding**, and **object\_syntax** qualifiers are always the same as the MIB type and the default value is always **NULL**.</span></span>



| <span data-ttu-id="83ff4-167">MIB 類型</span><span class="sxs-lookup"><span data-stu-id="83ff4-167">MIB type</span></span>          | <span data-ttu-id="83ff4-168">CIM 變異類型</span><span class="sxs-lookup"><span data-stu-id="83ff4-168">CIM variant type</span></span> | <span data-ttu-id="83ff4-169">cimtype 值</span><span class="sxs-lookup"><span data-stu-id="83ff4-169">cimtype value</span></span> |
|-------------------|------------------|---------------|
| <span data-ttu-id="83ff4-170">INTEGER</span><span class="sxs-lookup"><span data-stu-id="83ff4-170">INTEGER</span></span>           | <span data-ttu-id="83ff4-171">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="83ff4-171">VT\_I4</span></span>           | <span data-ttu-id="83ff4-172">**sint32**</span><span class="sxs-lookup"><span data-stu-id="83ff4-172">**sint32**</span></span>    |
| <span data-ttu-id="83ff4-173">八位字串</span><span class="sxs-lookup"><span data-stu-id="83ff4-173">OCTET STRING</span></span>      | <span data-ttu-id="83ff4-174">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="83ff4-174">VT\_BSTR</span></span>         | <span data-ttu-id="83ff4-175">**string**</span><span class="sxs-lookup"><span data-stu-id="83ff4-175">**string**</span></span>    |
| <span data-ttu-id="83ff4-176">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="83ff4-176">OBJECT IDENTIFIER</span></span> | <span data-ttu-id="83ff4-177">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="83ff4-177">VT\_BSTR</span></span>         | <span data-ttu-id="83ff4-178">**string**</span><span class="sxs-lookup"><span data-stu-id="83ff4-178">**string**</span></span>    |
| <span data-ttu-id="83ff4-179">IpAddress</span><span class="sxs-lookup"><span data-stu-id="83ff4-179">IpAddress</span></span>         | <span data-ttu-id="83ff4-180">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="83ff4-180">VT\_BSTR</span></span>         | <span data-ttu-id="83ff4-181">**string**</span><span class="sxs-lookup"><span data-stu-id="83ff4-181">**string**</span></span>    |
| <span data-ttu-id="83ff4-182">Counter32</span><span class="sxs-lookup"><span data-stu-id="83ff4-182">Counter32</span></span>         | <span data-ttu-id="83ff4-183">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="83ff4-183">VT\_I4</span></span>           | <span data-ttu-id="83ff4-184">**uint32**</span><span class="sxs-lookup"><span data-stu-id="83ff4-184">**uint32**</span></span>    |
| <span data-ttu-id="83ff4-185">Gauge32</span><span class="sxs-lookup"><span data-stu-id="83ff4-185">Gauge32</span></span>           | <span data-ttu-id="83ff4-186">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="83ff4-186">VT\_I4</span></span>           | <span data-ttu-id="83ff4-187">**uint32**</span><span class="sxs-lookup"><span data-stu-id="83ff4-187">**uint32**</span></span>    |
| <span data-ttu-id="83ff4-188">Unsigned32</span><span class="sxs-lookup"><span data-stu-id="83ff4-188">Unsigned32</span></span>        | <span data-ttu-id="83ff4-189">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="83ff4-189">VT\_I4</span></span>           | <span data-ttu-id="83ff4-190">**uint32**</span><span class="sxs-lookup"><span data-stu-id="83ff4-190">**uint32**</span></span>    |
| <span data-ttu-id="83ff4-191">Integer32</span><span class="sxs-lookup"><span data-stu-id="83ff4-191">Integer32</span></span>         | <span data-ttu-id="83ff4-192">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="83ff4-192">VT\_I4</span></span>           | <span data-ttu-id="83ff4-193">**sint32**</span><span class="sxs-lookup"><span data-stu-id="83ff4-193">**sint32**</span></span>    |
| <span data-ttu-id="83ff4-194">Counter64</span><span class="sxs-lookup"><span data-stu-id="83ff4-194">Counter64</span></span>         | <span data-ttu-id="83ff4-195">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="83ff4-195">VT\_BSTR</span></span>         | <span data-ttu-id="83ff4-196">**uint64**</span><span class="sxs-lookup"><span data-stu-id="83ff4-196">**uint64**</span></span>    |
| <span data-ttu-id="83ff4-197">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="83ff4-197">TimeTicks</span></span>         | <span data-ttu-id="83ff4-198">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="83ff4-198">VT\_I4</span></span>           | <span data-ttu-id="83ff4-199">**uint32**</span><span class="sxs-lookup"><span data-stu-id="83ff4-199">**uint32**</span></span>    |
| <span data-ttu-id="83ff4-200">Opaque</span><span class="sxs-lookup"><span data-stu-id="83ff4-200">Opaque</span></span>            | <span data-ttu-id="83ff4-201">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="83ff4-201">VT\_BSTR</span></span>         | <span data-ttu-id="83ff4-202">**string**</span><span class="sxs-lookup"><span data-stu-id="83ff4-202">**string**</span></span>    |



 

## <a name="named-type"></a><span data-ttu-id="83ff4-203">命名類型</span><span class="sxs-lookup"><span data-stu-id="83ff4-203">Named Type</span></span>

<span data-ttu-id="83ff4-204">SNMP 命名類型會對應至 CIM 定義類型。</span><span class="sxs-lookup"><span data-stu-id="83ff4-204">SNMP named types map to CIM-defined types.</span></span> <span data-ttu-id="83ff4-205">當語法子句透過型別指派衍生來參考基本型別、[文字慣例](textual-convention-macro.md)或[限制型](#constrained-type)別時，請使用[這些型別](#primitive-type)來判斷哪些對應程式適用。</span><span class="sxs-lookup"><span data-stu-id="83ff4-205">When the SYNTAX clause refers to a [primitive type](#primitive-type), [textual convention](textual-convention-macro.md), or [constrained type](#constrained-type) through a type assignment derivation, use the those types to determine which mapping procedures apply.</span></span>

-   <span data-ttu-id="83ff4-206">如果透過衍生類型指派規則，則會遇到限制型別定義：</span><span class="sxs-lookup"><span data-stu-id="83ff4-206">If, through derivation of the type assignment rules, you encounter a constrained type definition:</span></span>

    -   <span data-ttu-id="83ff4-207">此外，如果透過進一步的衍生，您就會遇到 [文字慣例宏](textual-convention-macro.md)中所列的其中一種文字慣例，然後套用適用于限制類型和文字慣例的對應規則。</span><span class="sxs-lookup"><span data-stu-id="83ff4-207">And if, through further derivation, you encounter one of the textual conventions listed in [TEXTUAL-CONVENTION Macro](textual-convention-macro.md), then apply the mapping rules for constrained types and textual conventions.</span></span>
    -   <span data-ttu-id="83ff4-208">否則，如果您遇到基本類型資料表中所列的其中一個基本類型，請套用基本型別和條件約束類型的對應規則。</span><span class="sxs-lookup"><span data-stu-id="83ff4-208">Otherwise, if you encounter one of the primitive types listed in either primitive type table, apply the mapping rules for primitive types and constrained types.</span></span>

-   <span data-ttu-id="83ff4-209">如果您遇到 [文字慣例 \_ 宏](textual-convention-macro.md)中所列的其中一個文字慣例，請套用文字慣例的對應規則。</span><span class="sxs-lookup"><span data-stu-id="83ff4-209">If you encounter one of the textual conventions listed in [TEXTUAL\_CONVENTION Macro](textual-convention-macro.md), apply the mapping rules for textual conventions.</span></span>
-   <span data-ttu-id="83ff4-210">如果您遇到任何一個基本類型資料表中所列的其中一個基本類型，請套用基本類型的對應規則。</span><span class="sxs-lookup"><span data-stu-id="83ff4-210">If you encounter one of the primitive types listed in either primitive type table, apply the mapping rules for primitive types.</span></span>

> [!Note]  
> <span data-ttu-id="83ff4-211">包含不符合上述對應之屬性類型的類別無效。</span><span class="sxs-lookup"><span data-stu-id="83ff4-211">Classes containing property types that do not conform to the mapping described above are not valid.</span></span> <span data-ttu-id="83ff4-212">在此情況下，當提供者在執行實例抓取函式時要求抓取類別定義時，提供者會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="83ff4-212">In this case, the provider returns an error if and when the provider requests the retrieval of a class definition while executing an instance retrieval function.</span></span>

 

## <a name="constrained-type"></a><span data-ttu-id="83ff4-213">條件約束類型</span><span class="sxs-lookup"><span data-stu-id="83ff4-213">Constrained Type</span></span>

<span data-ttu-id="83ff4-214">受限型別是一種基本類型、命名類型或文字慣例，受限於 SMI-S 檔 RFC 1213 和 RFC 1903 中所定義的部分 subtyping 機制。</span><span class="sxs-lookup"><span data-stu-id="83ff4-214">A constrained type is a primitive type, named type, or textual convention that has been constrained by some subtyping mechanism defined in the SMI documents RFC 1213 and RFC 1903.</span></span> <span data-ttu-id="83ff4-215">發生 subtyping 時，需要額外的 CIM 限定詞來指定子類型值。</span><span class="sxs-lookup"><span data-stu-id="83ff4-215">When subtyping occurs, additional CIM qualifiers are required to specify the subtype values.</span></span> <span data-ttu-id="83ff4-216">語法子句中的指名型別定義會逐字對應到 CIM 屬性限定詞 **物件 \_ 語法** （最多），但不包括子類型的條件約束。</span><span class="sxs-lookup"><span data-stu-id="83ff4-216">The named-type definition in the SYNTAX clause maps verbatim to the CIM property qualifier **object\_syntax** up to, but not including the constraints of the subtype.</span></span>

<span data-ttu-id="83ff4-217">子類型可以遵循下列任何格式：</span><span class="sxs-lookup"><span data-stu-id="83ff4-217">Subtypes may follow any of the following formats:</span></span>

-   <span data-ttu-id="83ff4-218">列舉整數</span><span class="sxs-lookup"><span data-stu-id="83ff4-218">Enumerated INTEGER</span></span>

    <span data-ttu-id="83ff4-219">CIM 屬性辨識符號 **列舉** 會指定列舉值。</span><span class="sxs-lookup"><span data-stu-id="83ff4-219">The CIM property qualifier **enumeration** specifies the enumerated values.</span></span> <span data-ttu-id="83ff4-220">此辨識符號會以字串表示，其中包含帶正負號的32位整數值清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="83ff4-220">This qualifier is represented as a string containing a comma-separated list of signed 32-bit integer values.</span></span> <span data-ttu-id="83ff4-221">下表列出對應類型。</span><span class="sxs-lookup"><span data-stu-id="83ff4-221">The following table lists the mapping types.</span></span> <span data-ttu-id="83ff4-222">預設值一律為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="83ff4-222">The default value is always **NULL**.</span></span>



| <span data-ttu-id="83ff4-223">受限的 MIB 類型</span><span class="sxs-lookup"><span data-stu-id="83ff4-223">Constrained MIB type</span></span> | <span data-ttu-id="83ff4-224">CIM 變異類型</span><span class="sxs-lookup"><span data-stu-id="83ff4-224">CIM variant type</span></span> | <span data-ttu-id="83ff4-225">CIM 限定詞</span><span class="sxs-lookup"><span data-stu-id="83ff4-225">CIM qualifiers</span></span>                                                                                                        |
|----------------------|------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83ff4-226">列舉整數</span><span class="sxs-lookup"><span data-stu-id="83ff4-226">Enumerated INTEGER</span></span>   | <span data-ttu-id="83ff4-227">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="83ff4-227">VT\_BSTR</span></span>         | <span data-ttu-id="83ff4-228">**文字 \_ 慣例**： enumeratedinteger</span><span class="sxs-lookup"><span data-stu-id="83ff4-228">**textual\_convention**: enumeratedinteger</span></span><br/> <span data-ttu-id="83ff4-229">**編碼**：整數</span><span class="sxs-lookup"><span data-stu-id="83ff4-229">**encoding**: INTEGER</span></span><br/> <span data-ttu-id="83ff4-230">**cimtype**：字串</span><span class="sxs-lookup"><span data-stu-id="83ff4-230">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="83ff4-231">BITS</span><span class="sxs-lookup"><span data-stu-id="83ff4-231">BITS</span></span>

    <span data-ttu-id="83ff4-232">CIM 屬性辨識符號 **位** 會指定列舉值。</span><span class="sxs-lookup"><span data-stu-id="83ff4-232">The CIM property qualifier **bits** specifies the enumerated values.</span></span> <span data-ttu-id="83ff4-233">此辨識符號會以字串表示，其中包含帶正負號的32位整數值清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="83ff4-233">This qualifier is represented as a string containing a comma-separated list of signed 32-bit integer values.</span></span> <span data-ttu-id="83ff4-234">下表列出對應類型。</span><span class="sxs-lookup"><span data-stu-id="83ff4-234">The following table lists the mapping types.</span></span> <span data-ttu-id="83ff4-235">預設值一律為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="83ff4-235">The default value is always **NULL**.</span></span>



| <span data-ttu-id="83ff4-236">受限的 MIB 類型</span><span class="sxs-lookup"><span data-stu-id="83ff4-236">Constrained MIB type</span></span> | <span data-ttu-id="83ff4-237">CIM 變異類型</span><span class="sxs-lookup"><span data-stu-id="83ff4-237">CIM variant type</span></span>      | <span data-ttu-id="83ff4-238">CIM 限定詞</span><span class="sxs-lookup"><span data-stu-id="83ff4-238">CIM qualifiers</span></span>                                                                                               |
|----------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83ff4-239">BITS</span><span class="sxs-lookup"><span data-stu-id="83ff4-239">BITS</span></span>                 | <span data-ttu-id="83ff4-240">VT \_ 陣列 \| VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="83ff4-240">VT\_ARRAY \| VT\_BSTR</span></span> | <span data-ttu-id="83ff4-241">**文字 \_ 慣例**：位</span><span class="sxs-lookup"><span data-stu-id="83ff4-241">**textual\_convention**: bits</span></span><br/> <span data-ttu-id="83ff4-242">**編碼**： OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="83ff4-242">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="83ff4-243">**cimtype**：字串</span><span class="sxs-lookup"><span data-stu-id="83ff4-243">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="83ff4-244">Variable-length</span><span class="sxs-lookup"><span data-stu-id="83ff4-244">Variable-length</span></span>

    <span data-ttu-id="83ff4-245">當語法子句參考 subtyped 為可變長度八進位字串或不透明的基本類型、命名類型或文字慣例時，CIM 屬性辨識符號的 **\_ 長度** 會指定與類型定義相關聯的最小值、最大值和固定長度值。</span><span class="sxs-lookup"><span data-stu-id="83ff4-245">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a variable-length OCTET STRING or Opaque, the CIM property qualifier **variable\_length** specifies the minimum, maximum, and fixed-length values associated with the type definition.</span></span> <span data-ttu-id="83ff4-246">此限定詞會實作為下列格式的字串，其中的可變長度值會以不帶正負號的32位整數表示。</span><span class="sxs-lookup"><span data-stu-id="83ff4-246">This qualifier is implemented as a string in the following format where the variable-length values are represented as unsigned 32-bit integers.</span></span>

    ``` syntax
    (((0.9) .. (0.9)) | (0.9))(, (((0.9) .. (0.9)) | (0.9)))*
    ```

-   <span data-ttu-id="83ff4-247">Fixed-length</span><span class="sxs-lookup"><span data-stu-id="83ff4-247">Fixed-length</span></span>

    <span data-ttu-id="83ff4-248">當語法子句參考 subtyped 為固定長度八進位字串或不透明的基本類型、命名類型或文字慣例時，CIM 屬性辨識符號 **固定 \_ 長度** 會指定固定長度的值。</span><span class="sxs-lookup"><span data-stu-id="83ff4-248">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a fixed-length OCTET STRING or Opaque, the CIM property qualifier **fixed\_length** specifies the fixed-length value.</span></span> <span data-ttu-id="83ff4-249">此辨識符號會表示為不帶正負號的32位整數值。</span><span class="sxs-lookup"><span data-stu-id="83ff4-249">This qualifier is represented as an unsigned 32-bit integer value.</span></span>

-   <span data-ttu-id="83ff4-250">範圍</span><span class="sxs-lookup"><span data-stu-id="83ff4-250">Range</span></span>

    <span data-ttu-id="83ff4-251">當語法子句參考 subtyped 為範圍值或固定值整數或量測計的基本類型、命名類型或文字慣例時，CIM 屬性辨識符號 **變數 \_ 值** 會指定與類型定義相關聯的範圍和固定值。</span><span class="sxs-lookup"><span data-stu-id="83ff4-251">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a ranged or fixed-value INTEGER or Gauge, the CIM property qualifier **variable\_value** specifies the ranged and fixed values associated with the type definition.</span></span> <span data-ttu-id="83ff4-252">此限定詞會實作為下列格式的字串，其中範圍和固定長度的值會以不帶正負號的32位整數表示。</span><span class="sxs-lookup"><span data-stu-id="83ff4-252">This qualifier is implemented as a string in the following format where the range and fixed-length values are represented as unsigned 32-bit integers.</span></span>

    ``` syntax
    (((0.9)..(0.9))|(0.9))(,(((0.9)..(0.9))|(0.9)))*
    ```

## <a name="example-code"></a><span data-ttu-id="83ff4-253">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="83ff4-253">Example Code</span></span>

<span data-ttu-id="83ff4-254">下列範例描述列舉整數子類型。</span><span class="sxs-lookup"><span data-stu-id="83ff4-254">The following example describes an enumerated INTEGER subtype.</span></span>

``` syntax
Status := INTEGER {
up(1),
down(2),
testing(3)
}
```

<span data-ttu-id="83ff4-255">此範例對應至：</span><span class="sxs-lookup"><span data-stu-id="83ff4-255">This example maps to:</span></span>

``` syntax
enumeration("up(1),down(2),testing(3)")
```

<span data-ttu-id="83ff4-256">下列程式碼範例描述位子類型。</span><span class="sxs-lookup"><span data-stu-id="83ff4-256">The following code example describes a BITS subtype.</span></span>

``` syntax
Status := BITS {
up(1),
down(2), 
testing(3)
}
```

<span data-ttu-id="83ff4-257">下列程式碼範例會對應至：</span><span class="sxs-lookup"><span data-stu-id="83ff4-257">The following code example maps to:</span></span>

``` syntax
bits("up(1),down(2),testing(3)")
```

<span data-ttu-id="83ff4-258">下列程式碼範例描述可變長度的子類型。</span><span class="sxs-lookup"><span data-stu-id="83ff4-258">The following code example describes a variable-length subtype.</span></span>

``` syntax
MySnmpOSIAddress ::=  TEXTUAL-CONVENTION

    DISPLAY-HINT    "*1x:/1x:"
    STATUS        current
    DESCRIPTION
            "Represents an OSI transport-address:

            octets    contents         encoding
              1        length of NSAP   'n' as an unsigned-integer
                                        (either 0 or from 3 to 20)
              2..(n+1)  NSAP          concrete binary representation
              (n+2)..m  TSEL             string of (up to 64) octets
            "
    SYNTAX         OCTET STRING (SIZE (1|4..85))
```

<span data-ttu-id="83ff4-259">此範例對應至：</span><span class="sxs-lookup"><span data-stu-id="83ff4-259">This example maps to:</span></span>

``` syntax
display_hint("*1x:/1x:"),
encoding("OCTETSTRING"),
textual_convention("OCTETSTRING"),
variable_length ("1,4..85")
```

<span data-ttu-id="83ff4-260">下列範例描述固定長度的子類型。</span><span class="sxs-lookup"><span data-stu-id="83ff4-260">The following example describes a fixed-length subtype.</span></span>

``` syntax
IPXADDRESS := OCTET STRING (SIZE (6))
```

<span data-ttu-id="83ff4-261">此範例對應至：</span><span class="sxs-lookup"><span data-stu-id="83ff4-261">This example maps to:</span></span>

``` syntax
fixed_length(6)
```

<span data-ttu-id="83ff4-262">下列範例說明範圍子類型。</span><span class="sxs-lookup"><span data-stu-id="83ff4-262">The following example describes a range subtype.</span></span>

``` syntax
Status := INTEGER (10..20|8)
```

<span data-ttu-id="83ff4-263">此範例對應至：</span><span class="sxs-lookup"><span data-stu-id="83ff4-263">This example maps to:</span></span>

``` syntax
variable_value("10..20,8")
```

 

 





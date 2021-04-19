---
description: SNMP 文字慣例會對應到 CIM 定義的類型。
ms.assetid: 73bb6c22-0a68-4a4b-8de2-8326ec67a059
ms.tgt_platform: multiple
title: 文字慣例宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329508ce3d124c0b3954675b3142aeb33c402923
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982335"
---
# <a name="textual-convention-macro"></a><span data-ttu-id="b0300-103">文字慣例宏</span><span class="sxs-lookup"><span data-stu-id="b0300-103">TEXTUAL-CONVENTION Macro</span></span>

<span data-ttu-id="b0300-104">SNMP 文字慣例會對應到 CIM 定義的類型。</span><span class="sxs-lookup"><span data-stu-id="b0300-104">SNMP textual conventions map to CIM-defined types.</span></span>

> [!Note]  
> <span data-ttu-id="b0300-105">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="b0300-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="b0300-106">下列對應規則適用于 SNMP 文字慣例：</span><span class="sxs-lookup"><span data-stu-id="b0300-106">The following mapping rules apply to SNMP textual conventions:</span></span>

-   <span data-ttu-id="b0300-107">語法子句中的指名型別定義會逐字地對應到 CIM 屬性限定詞 **物件 \_ 語法**。</span><span class="sxs-lookup"><span data-stu-id="b0300-107">The named type definition in the SYNTAX clause maps verbatim to the CIM property qualifier **object\_syntax**.</span></span>
-   <span data-ttu-id="b0300-108">當語法子句明確參考 SNMPv2C 文字慣例宏的文字慣例，或參考隱含的文字慣例時，請使用下表來對應文字慣例。</span><span class="sxs-lookup"><span data-stu-id="b0300-108">Use the following table to map textual conventions when the SYNTAX clause explicitly refers to a textual convention of a SNMPv2C TEXTUAL-CONVENTION macro, or refers to an implied textual convention.</span></span> <span data-ttu-id="b0300-109">預設值一律為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b0300-109">The default value is always **NULL**.</span></span>



| <span data-ttu-id="b0300-110">文字慣例</span><span class="sxs-lookup"><span data-stu-id="b0300-110">Textual convention</span></span> | <span data-ttu-id="b0300-111">CIM 變異類型</span><span class="sxs-lookup"><span data-stu-id="b0300-111">CIM variant type</span></span> | <span data-ttu-id="b0300-112">CIM 辨識符號</span><span class="sxs-lookup"><span data-stu-id="b0300-112">CIM qualifier</span></span>                                                                                                                                                        |
|--------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0300-113">DateAndTime</span><span class="sxs-lookup"><span data-stu-id="b0300-113">DateAndTime</span></span>        | <span data-ttu-id="b0300-114">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="b0300-114">**VT\_BSTR**</span></span>     | <span data-ttu-id="b0300-115">**文字 \_ 慣例**： >formatting.dateandtime.custom</span><span class="sxs-lookup"><span data-stu-id="b0300-115">**textual\_convention**: DateAndTime</span></span><br/> <span data-ttu-id="b0300-116">**編碼**： OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="b0300-116">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="b0300-117">**物件 \_ 語法**： >formatting.dateandtime.custom</span><span class="sxs-lookup"><span data-stu-id="b0300-117">**object\_syntax**: DateAndTime</span></span><br/> <span data-ttu-id="b0300-118">**cimtype**：字串</span><span class="sxs-lookup"><span data-stu-id="b0300-118">**cimtype**: string</span></span><br/>       |
| <span data-ttu-id="b0300-119">Displaystring</span><span class="sxs-lookup"><span data-stu-id="b0300-119">Displaystring</span></span>      | <span data-ttu-id="b0300-120">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="b0300-120">**VT\_BSTR**</span></span>     | <span data-ttu-id="b0300-121">**文字 \_ 慣例**： Displaystring</span><span class="sxs-lookup"><span data-stu-id="b0300-121">**textual\_convention**: Displaystring</span></span><br/> <span data-ttu-id="b0300-122">**編碼**： OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="b0300-122">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="b0300-123">**物件 \_ 語法**： Displaystring</span><span class="sxs-lookup"><span data-stu-id="b0300-123">**object\_syntax**: Displaystring</span></span><br/> <span data-ttu-id="b0300-124">**cimtype**：字串</span><span class="sxs-lookup"><span data-stu-id="b0300-124">**cimtype**: string</span></span><br/>   |
| <span data-ttu-id="b0300-125">MacAddress</span><span class="sxs-lookup"><span data-stu-id="b0300-125">MacAddress</span></span>         | <span data-ttu-id="b0300-126">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="b0300-126">**VT\_BSTR**</span></span>     | <span data-ttu-id="b0300-127">**文字 \_ 慣例**： MacAddress</span><span class="sxs-lookup"><span data-stu-id="b0300-127">**textual\_convention**: MacAddress</span></span><br/> <span data-ttu-id="b0300-128">**編碼**： OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="b0300-128">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="b0300-129">**物件 \_ 語法**： MacAddress</span><span class="sxs-lookup"><span data-stu-id="b0300-129">**object\_syntax**: MacAddress</span></span><br/> <span data-ttu-id="b0300-130">**cimtype**：字串</span><span class="sxs-lookup"><span data-stu-id="b0300-130">**cimtype**: string</span></span><br/>         |
| <span data-ttu-id="b0300-131">PhysAddress</span><span class="sxs-lookup"><span data-stu-id="b0300-131">PhysAddress</span></span>        | <span data-ttu-id="b0300-132">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="b0300-132">**VT\_BSTR**</span></span>     | <span data-ttu-id="b0300-133">**文字 \_ 慣例**： PhysAddress</span><span class="sxs-lookup"><span data-stu-id="b0300-133">**textual\_convention**: PhysAddress</span></span><br/> <span data-ttu-id="b0300-134">**編碼**： OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="b0300-134">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="b0300-135">**物件 \_ 語法**： PhysAddress</span><span class="sxs-lookup"><span data-stu-id="b0300-135">**object\_syntax**: PhysAddress</span></span><br/> <span data-ttu-id="b0300-136">**cimtype**：字串</span><span class="sxs-lookup"><span data-stu-id="b0300-136">**cimtype**: string</span></span><br/>       |
| <span data-ttu-id="b0300-137">SnmpUDPAddress</span><span class="sxs-lookup"><span data-stu-id="b0300-137">SnmpUDPAddress</span></span>     | <span data-ttu-id="b0300-138">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="b0300-138">**VT\_BSTR**</span></span>     | <span data-ttu-id="b0300-139">**文字 \_ 慣例**： SnmpUDPAddress</span><span class="sxs-lookup"><span data-stu-id="b0300-139">**textual\_convention**: SnmpUDPAddress</span></span><br/> <span data-ttu-id="b0300-140">**編碼**： OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="b0300-140">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="b0300-141">**物件 \_ 語法**： SnmpUDPAddress</span><span class="sxs-lookup"><span data-stu-id="b0300-141">**object\_syntax**: SnmpUDPAddress</span></span><br/> <span data-ttu-id="b0300-142">**cimtype**：字串</span><span class="sxs-lookup"><span data-stu-id="b0300-142">**cimtype**: string</span></span><br/> |
| <span data-ttu-id="b0300-143">SnmpOSIAddress</span><span class="sxs-lookup"><span data-stu-id="b0300-143">SnmpOSIAddress</span></span>     | <span data-ttu-id="b0300-144">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="b0300-144">**VT\_BSTR**</span></span>     | <span data-ttu-id="b0300-145">**文字 \_ 慣例**： SnmpOSIAddress</span><span class="sxs-lookup"><span data-stu-id="b0300-145">**textual\_convention**: SnmpOSIAddress</span></span><br/> <span data-ttu-id="b0300-146">**編碼**： OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="b0300-146">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="b0300-147">**物件 \_ 語法**： SnmpOSIAddress</span><span class="sxs-lookup"><span data-stu-id="b0300-147">**object\_syntax**: SnmpOSIAddress</span></span><br/> <span data-ttu-id="b0300-148">**cimtype**：字串</span><span class="sxs-lookup"><span data-stu-id="b0300-148">**cimtype**: string</span></span><br/> |
| <span data-ttu-id="b0300-149">SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="b0300-149">SnmpIPXAddress</span></span>     | <span data-ttu-id="b0300-150">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="b0300-150">**VT\_BSTR**</span></span>     | <span data-ttu-id="b0300-151">**文字 \_ 慣例**： SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="b0300-151">**textual\_convention**: SnmpIPXAddress</span></span><br/> <span data-ttu-id="b0300-152">**編碼**： OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="b0300-152">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="b0300-153">**物件 \_ 語法**： SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="b0300-153">**object\_syntax**: SnmpIPXAddress</span></span><br/> <span data-ttu-id="b0300-154">**cimtype**：字串</span><span class="sxs-lookup"><span data-stu-id="b0300-154">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="b0300-155">使用基礎基本類型的 CIM 定義變異類型和 CIM 屬性限定詞 **文字 \_ 慣例**、 **編碼**、 **物件 \_ 語法** 和 **cimtype** 對應。</span><span class="sxs-lookup"><span data-stu-id="b0300-155">The CIM-defined variant type and the CIM property qualifiers **textual\_convention**, **encoding**, **object\_syntax**, and **cimtype** map using the underlying primitive type.</span></span>
-   <span data-ttu-id="b0300-156">SNMPv2C 文字慣例宏的顯示提示子句會逐字對應到 CIM 屬性辨識符號 **顯示 \_ 提示**。</span><span class="sxs-lookup"><span data-stu-id="b0300-156">The DISPLAY-HINT clause of the SNMPv2C TEXTUAL-CONVENTION macro maps verbatim to the CIM property qualifier **display\_hint**.</span></span> <span data-ttu-id="b0300-157">如果沒有文字慣例宏，或宏未包含顯示提示子句，就不會產生這個限定詞。</span><span class="sxs-lookup"><span data-stu-id="b0300-157">This qualifier is not generated if there is no TEXTUAL-CONVENTION macro, or the macro does not contain a DISPLAY-HINT clause.</span></span>

## <a name="example-code"></a><span data-ttu-id="b0300-158">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="b0300-158">Example Code</span></span>

<span data-ttu-id="b0300-159">下列範例說明 SNMPv1 文字慣例。</span><span class="sxs-lookup"><span data-stu-id="b0300-159">The following example describes an SNMPv1 textual convention.</span></span>

``` syntax
myNamedType ::= DISPLAYSTRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myNamedType
ACCESS read-only
STATUS MANDATORY
DESCRIPTION ""
```

<span data-ttu-id="b0300-160">此範例會產生下列 CIM 限定詞。</span><span class="sxs-lookup"><span data-stu-id="b0300-160">This example generates the following CIM qualifiers.</span></span>

``` syntax
object_syntax("myNamedType"),
textual_convention("DISPLAYSTRING"),
encoding("OCTETSTRING"),
variable_length("0..127")
```

<span data-ttu-id="b0300-161">下列範例說明 SNMPv2 文字慣例。</span><span class="sxs-lookup"><span data-stu-id="b0300-161">The following example describes an SNMPv2 textual convention.</span></span>

``` syntax
myDisplaystring ::= TEXTUAL-CONVENTION
DISPLAY-HINT "255a"
STATUS current
DESCRIPTION "" 
SYNTAX OCTET STRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myDisplaystring
MAX-ACCESS read-only
STATUS current
DESCRIPTION ""
```

<span data-ttu-id="b0300-162">此範例會產生下列 CIM 限定詞。</span><span class="sxs-lookup"><span data-stu-id="b0300-162">This example generates the following CIM qualifiers.</span></span>

``` syntax
object_syntax("myDisplaystring"),
textual_convention("OCTETSTRING"),
encoding("OCTETSTRING"),
display_hint("255a"),
variable_length("0..127")
```

 

 





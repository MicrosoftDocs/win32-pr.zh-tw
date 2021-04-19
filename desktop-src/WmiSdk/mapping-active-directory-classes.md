---
description: 提供將 WMI 類別對應至 Active Directory 的規則。
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: 對應 Active Directory 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a606cfacc2e9d56ef07973df182f5ce1a65be35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987675"
---
# <a name="mapping-active-directory-classes"></a><span data-ttu-id="0f8e7-103">對應 Active Directory 類別</span><span class="sxs-lookup"><span data-stu-id="0f8e7-103">Mapping Active Directory Classes</span></span>

<span data-ttu-id="0f8e7-104">由於 Active Directory 有各種可能的物件，因此 WMI 無法建立直接的一對一對應。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-104">Because Active Directory has a wide variety of possible objects, WMI cannot create a direct one-to-one mapping.</span></span> <span data-ttu-id="0f8e7-105">相反地，目錄服務提供者會使用規則來對應兩個技術之間的類別。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-105">Instead, the Directory Services provider uses rules to map classes between the two technologies.</span></span>

<span data-ttu-id="0f8e7-106">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="0f8e7-106">This following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="0f8e7-107">對應類別</span><span class="sxs-lookup"><span data-stu-id="0f8e7-107">Mapping Classes</span></span>](#mapping-classes)
-   [<span data-ttu-id="0f8e7-108">對應屬性</span><span class="sxs-lookup"><span data-stu-id="0f8e7-108">Mapping Attributes</span></span>](#mapping-attributes)
-   [<span data-ttu-id="0f8e7-109">關聯類別</span><span class="sxs-lookup"><span data-stu-id="0f8e7-109">Association Classes</span></span>](#association-classes)

> [!Note]  
> <span data-ttu-id="0f8e7-110">如需有關在特定作業系統上支援和安裝此元件的詳細資訊，請參閱 [WMI 元件的作業系統可用性](operating-system-availability-of-wmi-components.md)。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

## <a name="mapping-classes"></a><span data-ttu-id="0f8e7-111">對應類別</span><span class="sxs-lookup"><span data-stu-id="0f8e7-111">Mapping Classes</span></span>

<span data-ttu-id="0f8e7-112">下列清單描述目錄服務提供者用來將 Active Directory 類別對應至 WMI 類別的指導方針：</span><span class="sxs-lookup"><span data-stu-id="0f8e7-112">The following list describes the guidelines that the Directory Services provider uses to map Active Directory classes to WMI classes:</span></span>

-   <span data-ttu-id="0f8e7-113">Active Directory 架構中的每個抽象類別都會對應至 WMI 架構中的一個抽象類別。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-113">Each abstract class in the Active Directory schema maps to one abstract class in the WMI schema.</span></span>

    <span data-ttu-id="0f8e7-114">在 WMI 架構中，每個抽象類別的前面都會加上 DS \_ 。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-114">In the WMI schema, each abstract class is prefixed with DS\_.</span></span> <span data-ttu-id="0f8e7-115">例如，Active Directory 架構中的 **person** 類別會對應到 **DS \_ person** WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-115">For example, the **person** class from the Active Directory schema maps to the **DS\_person** WMI class.</span></span>

-   <span data-ttu-id="0f8e7-116">Active Directory 架構中的每個非抽象類別別都會對應至 WMI 架構中的下列兩個類別：</span><span class="sxs-lookup"><span data-stu-id="0f8e7-116">Each nonabstract class from the Active Directory schema maps to the following two classes in the WMI schema:</span></span>

    -   <span data-ttu-id="0f8e7-117">第一個對應的類別前面會加上 ADS \_ 。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-117">The first mapped class is prefixed with ADS\_.</span></span> <span data-ttu-id="0f8e7-118">這些是抽象類別，根據下列規則進行對應。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-118">These are abstract classes, mapped according to the rules below.</span></span>
    -   <span data-ttu-id="0f8e7-119">第二個對應類別是具有 DS 名稱前置詞的非抽象類別別 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-119">The second mapped class is a nonabstract class with the DS\_ name prefix.</span></span> <span data-ttu-id="0f8e7-120">此類別衍生自 ADS \_ 抽象類別，並加入了 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 辨識符號。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-120">This class is derived from the ADS\_ abstract class, with the addition of the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span>

    <span data-ttu-id="0f8e7-121">例如，Active Directory 架構中的 **user** 類別會對應到兩個類別。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-121">For example, the **user** class from the Active Directory schema maps to two classes.</span></span> <span data-ttu-id="0f8e7-122">第一個類別是 **ADS \_ 使用者** 抽象類別，根據下列規則進行對應。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-122">The first class is the **ADS\_user** abstract class, mapped according to rules below.</span></span> <span data-ttu-id="0f8e7-123">第二個類別是 **DS \_ 使用者** 非抽象類別別。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-123">The second class is the **DS\_user** nonabstract class.</span></span> <span data-ttu-id="0f8e7-124">它衍生自 **ADS \_ 使用者** ，並具有新增的 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 辨識符號。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-124">It is derived from **ADS\_user** and has the added [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span>

-   <span data-ttu-id="0f8e7-125">除非另有指定，否則對應類別的名稱是 Active Directory 類別中 **LDAP 顯示名稱** 屬性的已損壞值。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-125">Unless specified otherwise, the name of a mapped class is the mangled value of the **LDAP-Display-Name** property in the Active Directory class.</span></span>
-   <span data-ttu-id="0f8e7-126">如果 Active Directory 類別上有 **子類別的** 屬性，則 WMI 對應的類別會衍生自指定的類別。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-126">If the **Sub-Class-Of** property is present on the Active Directory class, the WMI-mapped class is derived from the specified class.</span></span>

    <span data-ttu-id="0f8e7-127">如果不存在 **子類別的** 屬性，則 WMI 對應類別會衍生自「 **DS \_ LDAP \_ 根 \_ 類別** 」類別，如 MOF 檔案中所指定。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-127">If the **Sub-Class-Of** property is not present, the WMI-mapped class is derived from the **DS\_LDAP\_Root\_Class** class, as specified in the MOF file.</span></span>

    > [!Note]  
    > <span data-ttu-id="0f8e7-128">此類別具有 **ADSIPath** 索引鍵屬性，其類型為 **VT \_ BSTR**。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-128">This class has the **ADSIPath** key property, with a type **VT\_BSTR**.</span></span> <span data-ttu-id="0f8e7-129">這是識別此實例的唯一 ADSI 路徑。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-129">This is the unique ADSI path that identifies this instance.</span></span> <span data-ttu-id="0f8e7-130">Active Directory 僅支援單一繼承，因此可正常運作。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-130">Active Directory supports single-inheritance only, so this works.</span></span>

     

-   <span data-ttu-id="0f8e7-131">會為每個類別建立 **VT \_ BOOL** 類型的 **動態** 限定詞，並 `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` 設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-131">A **Dynamic** qualifier of type **VT\_BOOL**, and flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` set to **TRUE** is created for every class.</span></span> <span data-ttu-id="0f8e7-132">這是標準的 WMI 辨識符號，表示會動態提供這個類別的實例。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-132">This is a standard WMI qualifier that indicates that instances of this class are provided dynamically.</span></span>
-   <span data-ttu-id="0f8e7-133">如果類別不是抽象的，則提供者會為每個類別建立類型為 **VT \_ BSTR BOOL** 的 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider)辨識符號，以及 `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` 設定為 "DS Instance provider" 的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-133">If the class is not abstract, the provider creates a [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier of type **VT\_BSTR BOOL** and qualifier flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` set to "DS Instance Provider" for every class.</span></span> <span data-ttu-id="0f8e7-134">這是標準的 WMI 辨識符號，表示提供者的名稱會動態提供這個類別的實例。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-134">This is a standard WMI qualifier that indicates the name of the provider dynamically providing instances of this class.</span></span>

<span data-ttu-id="0f8e7-135">ADSI 屬性的其餘部分會根據下列資料表對應至類別限定詞和屬性。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-135">The rest of the ADSI properties map to class qualifiers and properties as per the following tables.</span></span> <span data-ttu-id="0f8e7-136">具有限定詞旗標值的所有限定詞對應 `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` 。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-136">All qualifiers map with a qualifier flag value of `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS`.</span></span>

<span data-ttu-id="0f8e7-137">以下列出 Active Directory 類別的對應資訊，其中顯示每個 Active Directory 屬性的 WMI 辨識符號和 WMI 辨識符號類型。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-137">The following lists mapping information for the Active Directory class, showing the WMI qualifier and WMI qualifier type for each Active Directory property.</span></span>

<dl> <dt>

<span data-ttu-id="0f8e7-138">**一般名稱**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-138">**Common-Name**</span></span>
</dt> <dd>

<span data-ttu-id="0f8e7-139">**CN** (**VT \_ BSTR**) </span><span class="sxs-lookup"><span data-stu-id="0f8e7-139">**CN** (**VT\_BSTR**)</span></span>

<span data-ttu-id="0f8e7-140">直接從字串值對應。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-140">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="0f8e7-141">**預設-物件-類別**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-141">**Default-Object-Category**</span></span>
</dt> <dd>

<span data-ttu-id="0f8e7-142">**DefaultObjectCategory** (**VT \_ BSTR**) </span><span class="sxs-lookup"><span data-stu-id="0f8e7-142">**DefaultObjectCategory** (**VT\_BSTR**)</span></span>

<span data-ttu-id="0f8e7-143">直接從字串值對應。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-143">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="0f8e7-144">**預設-安全性-描述元**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-144">**Default-Security-Descriptor**</span></span>
</dt> <dd>

<span data-ttu-id="0f8e7-145">**DefaultSecurityDescriptor** (**VT \_ BSTR**) </span><span class="sxs-lookup"><span data-stu-id="0f8e7-145">**DefaultSecurityDescriptor** (**VT\_BSTR**)</span></span>

<span data-ttu-id="0f8e7-146">直接從字串值對應。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-146">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="0f8e7-147">**控管-識別碼**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-147">**Governs-Id**</span></span>
</dt> <dd>

<span data-ttu-id="0f8e7-148">**GovernsId** (**VT \_ BSTR**) </span><span class="sxs-lookup"><span data-stu-id="0f8e7-148">**GovernsId** (**VT\_BSTR**)</span></span>

<span data-ttu-id="0f8e7-149">從 OID 的字串表示進行對應;例如，"{1 3 3 6}"。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-149">Mapped from the string representation of the OID; for example, "{ 1 3 3 6 }".</span></span>

</dd> <dt>

<span data-ttu-id="0f8e7-150">**物件類別**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-150">**Object-Class**</span></span>
</dt> <dd>

<span data-ttu-id="0f8e7-151">N/A</span><span class="sxs-lookup"><span data-stu-id="0f8e7-151">N/A</span></span>

<span data-ttu-id="0f8e7-152">未對應。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-152">Not mapped.</span></span>

</dd> <dt>

<span data-ttu-id="0f8e7-153">**物件類別-類別目錄**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-153">**Object-Class-Category**</span></span>
</dt> <dd>

<span data-ttu-id="0f8e7-154">**ObjectClassCategory** (**VT \_ I4**) </span><span class="sxs-lookup"><span data-stu-id="0f8e7-154">**ObjectClassCategory** (**VT\_I4**)</span></span>

<span data-ttu-id="0f8e7-155">直接從整數值對應。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-155">Mapped directly from the integer value.</span></span> <span data-ttu-id="0f8e7-156">此外，如果此值為 Abstract (2) ，則也會建立標準 **VT \_ BOOL** CIM 辨識符號（稱為「 **抽象** 」限定詞）。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-156">In addition, if the value is Abstract(2), then the standard **VT\_BOOL** CIM qualifier, called the **"Abstract"** qualifier, is also created.</span></span>

</dd> <dt>

<span data-ttu-id="0f8e7-157">**RDN-ATT-ID**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-157">**RDN-ATT-ID**</span></span>
</dt> <dd>

<span data-ttu-id="0f8e7-158">**RDNATTID** (**VT \_ BSTR**) </span><span class="sxs-lookup"><span data-stu-id="0f8e7-158">**RDNATTID** (**VT\_BSTR**)</span></span>

<span data-ttu-id="0f8e7-159">從 OID 值的字串標記法對應;例如，"{1 3 3 6}"。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-159">Mapped from the string representation of the OID value; for example, "{ 1 3 3 6 }".</span></span> <span data-ttu-id="0f8e7-160">此外，此處識別的屬性會標注標準的 **索引** CIM 辨識符號設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-160">In addition, the property identified here is annotated with the standard **Indexed** CIM qualifier set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="0f8e7-161">**僅限系統**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-161">**System-Only**</span></span>
</dt> <dd>

<span data-ttu-id="0f8e7-162">**SystemOnly** (**VT \_ BOOL**) </span><span class="sxs-lookup"><span data-stu-id="0f8e7-162">**SystemOnly** (**VT\_BOOL**)</span></span>

<span data-ttu-id="0f8e7-163">直接從布林值對應。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-163">Mapped directly from the Boolean value.</span></span>

</dd> </dl>

 

<span data-ttu-id="0f8e7-164">以下列出對應至 WMI 類別屬性的 Active Directory 類別屬性。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-164">The following lists the Active Directory class properties mapped to WMI class properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f8e7-165">**可能包含**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-165">**May-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="0f8e7-166">此清單中的每個屬性都會對應至 WMI 屬性。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-166">Each property in this list is mapped to a WMI property.</span></span>

</dd> <dt>

<span data-ttu-id="0f8e7-167">**必須包含**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-167">**Must-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="0f8e7-168">此清單中的每個屬性都會對應至 WMI 屬性。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-168">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="0f8e7-169">這每一個都是針對上述各項建立標準 **非 \_ Null** CIM 限定詞。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-169">The standard **Not\_Null** CIM qualifier is created for each of these.</span></span>

</dd> <dt>

<span data-ttu-id="0f8e7-170">**系統-可能包含**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-170">**System-May-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="0f8e7-171">此清單中的每個屬性都會對應至 WMI 屬性。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-171">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="0f8e7-172">此外，每個屬性都會以 **系統** 限定詞標注，設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-172">In addition, each property is annotated with a **System** qualifier, set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="0f8e7-173">**系統-必須包含**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-173">**System-Must-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="0f8e7-174">此清單中的每個屬性都會對應至 WMI 屬性。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-174">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="0f8e7-175">這每一個都是針對上述各項建立標準 **非 \_ Null** CIM 限定詞。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-175">The standard **Not\_Null** CIM qualifier is created for each of these.</span></span> <span data-ttu-id="0f8e7-176">此外，每個屬性都會以 **系統** 限定詞標注，設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-176">In addition, each property is annotated with a **System** qualifier, set to **TRUE**.</span></span>

</dd> </dl>

## <a name="mapping-attributes"></a><span data-ttu-id="0f8e7-177">對應屬性</span><span class="sxs-lookup"><span data-stu-id="0f8e7-177">Mapping Attributes</span></span>

<span data-ttu-id="0f8e7-178">目錄服務提供者會根據本節中的規則，將 Active Directory 類別的每個屬性對應到相對應 WMI 類別的一個屬性。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-178">The Directory Services provider maps each attribute of an Active Directory class to exactly one property of the corresponding WMI class according to the rules in this section.</span></span> <span data-ttu-id="0f8e7-179">一般情況下，目錄服務提供者會將 WMI 屬性命名為 Active Directory 屬性的 **LDAP 顯示名稱** 值的損壞版本。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-179">In general, the Directory Services Provider names the WMI property as the mangled version of the **LDAP-Display-Name** value of the Active Directory attribute.</span></span>

<span data-ttu-id="0f8e7-180">如果 Active Directory 屬性 **為-單一值** 為 **FALSE**，則此 WMI 屬性會與 OR 運算子結合 **CIM 旗標 \_ \_ 陣列**。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-180">If the Active Directory property **Is-Single-Valued** is **FALSE**, then this WMI property is combined with the OR operator with **CIM\_FLAG\_ARRAY**.</span></span> <span data-ttu-id="0f8e7-181">請注意，每個屬性都會以 **VT \_ BSTR** 辨識符號（ **ADSyntax**）標記。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-181">Note that each property is tagged with the **VT\_BSTR** qualifier, **ADSyntax**.</span></span> <span data-ttu-id="0f8e7-182">它代表基礎 Active Directory 語法。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-182">It represents the underlying Active Directory syntax.</span></span>

<span data-ttu-id="0f8e7-183">下表列出 Active Directory 語法與 WMI 屬性資料類型的對應。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-183">The following table lists the mapping of the Active Directory syntax to the WMI property data type.</span></span>



| <span data-ttu-id="0f8e7-184">Active Directory 元素</span><span class="sxs-lookup"><span data-stu-id="0f8e7-184">Active Directory element</span></span>                                      | <span data-ttu-id="0f8e7-185">WMI 資料類型</span><span class="sxs-lookup"><span data-stu-id="0f8e7-185">WMI data type</span></span>                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="0f8e7-186">**存取點**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-186">**Access-Point**</span></span>](/windows/desktop/ADSchema/s-object-access-point)            | <span data-ttu-id="0f8e7-187">**CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-187">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="0f8e7-188">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-188">**Boolean**</span></span>](/windows/desktop/ADSchema/s-boolean)                             | <span data-ttu-id="0f8e7-189">**CIM \_ 布林值**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-189">**CIM\_BOOLEAN**</span></span>                                                        |
| <span data-ttu-id="0f8e7-190">**不區分大小寫的字串**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-190">**Case Insensitive String**</span></span>                                   | <span data-ttu-id="0f8e7-191">**CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-191">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="0f8e7-192">**區分大小寫的字串**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-192">**Case Sensitive String**</span></span>](/windows/desktop/ADSchema/s-string-case-sensitive) | <span data-ttu-id="0f8e7-193">**CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-193">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="0f8e7-194">**辨別名稱**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-194">**Distinguished Name**</span></span>](/windows/desktop/ADSchema/s-object-ds-dn)             | <span data-ttu-id="0f8e7-195">**CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-195">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="0f8e7-196">**DN-二進位**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-196">**DN-Binary**</span></span>](/windows/desktop/ADSchema/s-object-dn-binary)                  | <span data-ttu-id="0f8e7-197">類別 DN 的內嵌 **物件 \_ ， \_** 定義如下的二進位檔。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-197">Embedded object of class **DN\_With\_Binary** defined below.</span></span><br/> |
| [<span data-ttu-id="0f8e7-198">**DN-字串**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-198">**DN-String**</span></span>](/windows/desktop/ADSchema/s-object-dn-string)                  | <span data-ttu-id="0f8e7-199">類別 DN 的內嵌 **物件 \_ ， \_ 具有** 以下定義的字串。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-199">Embedded object of class **DN\_With\_String** defined below.</span></span><br/> |
| [<span data-ttu-id="0f8e7-200">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-200">**Enumeration**</span></span>](/windows/desktop/ADSchema/s-enumeration)                     | <span data-ttu-id="0f8e7-201">**CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-201">**CIM\_SINT32**</span></span>                                                         |
| [<span data-ttu-id="0f8e7-202">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-202">**Enumeration**</span></span>](/windows/desktop/ADSchema/s-enumeration)                     | <span data-ttu-id="0f8e7-203">**CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-203">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="0f8e7-204">**整數**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-204">**Integer**</span></span>](/windows/desktop/ADSchema/s-integer)                             | <span data-ttu-id="0f8e7-205">**CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-205">**CIM\_SINT32**</span></span>                                                         |
| [<span data-ttu-id="0f8e7-206">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-206">**LargeInteger**</span></span>](/windows/desktop/ADSchema/s-largeinteger)                   | <span data-ttu-id="0f8e7-207">**CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-207">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="0f8e7-208">安全性描述元</span><span class="sxs-lookup"><span data-stu-id="0f8e7-208">Security Descriptor</span></span>                                           | <span data-ttu-id="0f8e7-209">以下定義之類別 **Uint8Array** 的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-209">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="0f8e7-210">數值字串</span><span class="sxs-lookup"><span data-stu-id="0f8e7-210">Numeric String</span></span>                                                | <span data-ttu-id="0f8e7-211">**CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-211">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="0f8e7-212">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="0f8e7-212">Object ID</span></span>                                                     | <span data-ttu-id="0f8e7-213">**CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-213">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="0f8e7-214">八位字串</span><span class="sxs-lookup"><span data-stu-id="0f8e7-214">Octet String</span></span>                                                  | <span data-ttu-id="0f8e7-215">以下定義之類別 **Uint8Array** 的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-215">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="0f8e7-216">或名稱</span><span class="sxs-lookup"><span data-stu-id="0f8e7-216">OR Name</span></span>                                                       | <span data-ttu-id="0f8e7-217">**CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-217">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="0f8e7-218">Presentation-Address</span><span class="sxs-lookup"><span data-stu-id="0f8e7-218">Presentation-Address</span></span>                                          | <span data-ttu-id="0f8e7-219">以下定義之類別 **Uint8Array** 的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-219">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="0f8e7-220">列印案例字串</span><span class="sxs-lookup"><span data-stu-id="0f8e7-220">Print Case String</span></span>                                             | <span data-ttu-id="0f8e7-221">**CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-221">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="0f8e7-222">複本連結</span><span class="sxs-lookup"><span data-stu-id="0f8e7-222">Replica Link</span></span>                                                  | <span data-ttu-id="0f8e7-223">以下定義之類別 **Uint8Array** 的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-223">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| [<span data-ttu-id="0f8e7-224">**(Sid) 的字串**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-224">**String(Sid)**</span></span>](/windows/desktop/ADSchema/s-string-sid)                      | <span data-ttu-id="0f8e7-225">以下定義之類別 **Uint8Array** 的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-225">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="0f8e7-226">Time</span><span class="sxs-lookup"><span data-stu-id="0f8e7-226">Time</span></span>                                                          | <span data-ttu-id="0f8e7-227">**CIM \_ DATETIME**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-227">**CIM\_DATETIME**</span></span>                                                       |
| <span data-ttu-id="0f8e7-228">UTC 編碼時間</span><span class="sxs-lookup"><span data-stu-id="0f8e7-228">UTC Coded Time</span></span>                                                | <span data-ttu-id="0f8e7-229">**CIM \_ DATETIME**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-229">**CIM\_DATETIME**</span></span>                                                       |
| <span data-ttu-id="0f8e7-230">Unicode 字串</span><span class="sxs-lookup"><span data-stu-id="0f8e7-230">Unicode String</span></span>                                                | <span data-ttu-id="0f8e7-231">**CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-231">**CIM\_STRING**</span></span>                                                         |



 

<span data-ttu-id="0f8e7-232">八位字串語法（參考 **uint8** 值的陣列）會在對應至 WMI 時呈現問題，因為 wmi 允許 **uint8** 類型的屬性和 **uint8** 的陣列，而 Active Directory 則允許類型為八進位字串的屬性，以及八位字串的陣列。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-232">The Octet String syntax, which refers to an array of **uint8** values, presents a problem when mapped to WMI because WMI allows properties of types **uint8** and arrays of **uint8**, whereas Active Directory allows properties of type Octet String as well as arrays of Octet String.</span></span>

<span data-ttu-id="0f8e7-233">下列範例顯示的目錄服務提供者類別，用來對應八位字串型別屬性的陣列。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-233">The following example shows the Directory Services Provider class that is used to map an array of Octet String type properties.</span></span>

``` syntax
Class Uint8Array 
{
    uint8 values[];
    uint32 numberOfValues;
};
```

<span data-ttu-id="0f8e7-234">WMI 會將所有的八位字串 Active Directory 屬性值對應至 **Uint8Array** 的內嵌實例。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-234">WMI maps all Octet String Active Directory property values to embedded instances of **Uint8Array**.</span></span> <span data-ttu-id="0f8e7-235">同樣地，WMI 會將八位字串的陣列對應至內嵌 **Uint8Array** 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-235">Similarly, WMI maps arrays of Octet String to arrays of embedded **Uint8Array** objects.</span></span>

<span data-ttu-id="0f8e7-236">下列範例顯示 WMI 對應的類別，以 DN-Binary 和 DN-String DS 屬性值。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-236">The following example shows the classes that are mapped by WMI to DN-Binary and DN-String DS property values.</span></span>

``` syntax
Class DN_With_String
{
    string dnString;
    string value;
};

Class DN_With_Binary
{
    string dnString;
    uint8 value[];
};
```

<span data-ttu-id="0f8e7-237">下表列出 WMI 如何將 Active Directory 屬性介面屬性的其餘部分對應至 WMI 屬性限定詞。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-237">The following table lists how WMI maps the rest of the Active Directory attribute interface properties to WMI property qualifiers.</span></span>



| <span data-ttu-id="0f8e7-238">Active Directory 屬性-屬性名稱</span><span class="sxs-lookup"><span data-stu-id="0f8e7-238">Active Directory attribute-property name</span></span> | <span data-ttu-id="0f8e7-239">WMI 辨識符號</span><span class="sxs-lookup"><span data-stu-id="0f8e7-239">WMI Qualifier</span></span>       | <span data-ttu-id="0f8e7-240">資料類型</span><span class="sxs-lookup"><span data-stu-id="0f8e7-240">Data type</span></span>    | <span data-ttu-id="0f8e7-241">對應資訊</span><span class="sxs-lookup"><span data-stu-id="0f8e7-241">Mapping information</span></span>                               |
|------------------------------------------|---------------------|--------------|---------------------------------------------------|
| <span data-ttu-id="0f8e7-242">**屬性語法**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-242">**Attribute-Syntax**</span></span>                     | <span data-ttu-id="0f8e7-243">**AttributeSyntax**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-243">**AttributeSyntax**</span></span> | <span data-ttu-id="0f8e7-244">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-244">**VT\_BSTR**</span></span> | <span data-ttu-id="0f8e7-245">從 OID 的字串表示進行對應。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-245">Mapped from the string representation of the OID.</span></span> |
| <span data-ttu-id="0f8e7-246">**一般名稱**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-246">**Common-Name**</span></span>                          | <span data-ttu-id="0f8e7-247">**快遞 之 家**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-247">**CN**</span></span>              | <span data-ttu-id="0f8e7-248">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-248">**VT\_BSTR**</span></span> | <span data-ttu-id="0f8e7-249">從字串值對應。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-249">Mapped from the string value.</span></span>                     |
| <span data-ttu-id="0f8e7-250">**僅限系統**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-250">**System-Only**</span></span>                          | <span data-ttu-id="0f8e7-251">**系統**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-251">**System**</span></span>          | <span data-ttu-id="0f8e7-252">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="0f8e7-252">**VT\_BOOL**</span></span> | <span data-ttu-id="0f8e7-253">從布林值對應。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-253">Mapped from the Boolean value.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="0f8e7-254">WMI 會將所有 Active Directory 限定詞對應到辨識符號的類別 `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` 。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-254">WMI maps all Active Directory qualifiers with the `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` qualifier flavors.</span></span>

 

## <a name="association-classes"></a><span data-ttu-id="0f8e7-255">關聯類別</span><span class="sxs-lookup"><span data-stu-id="0f8e7-255">Association Classes</span></span>

<span data-ttu-id="0f8e7-256">目錄服務基本上是物件的階層式存放區。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-256">The Directory Service is essentially a hierarchical store of objects.</span></span> <span data-ttu-id="0f8e7-257">這些物件可以出現在階層中的非分葉層級上，稱為「容器」。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-257">Those objects that can appear at a nonleaf level in the hierarchy are called "containers".</span></span> <span data-ttu-id="0f8e7-258">此階層的結構會進一步由架構中類別的 "Poss-Superiors" 和 "Poss-Superiors" 屬性控制。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-258">The structure of this hierarchy is further controlled by the "Poss-Superiors" and "System-Poss-Superiors" properties of a class in the schema.</span></span> <span data-ttu-id="0f8e7-259">這些會一起建立，並指定一組類別，其實例可以包含在容器類別的實例中。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-259">These, taken together, specify the set of classes whose instances can be contained within an instance of a container class.</span></span>

<span data-ttu-id="0f8e7-260">下列範例會將 CIM 關聯模型為靜態關聯類別的 [**DS \_ LDAP \_ 類別 \_**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment)內含專案的實例。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-260">The following example models a CIM association as instances of the static association class [**DS\_LDAP\_Class\_Containment**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).</span></span>

``` syntax
//  DS Class Associations Provider 

// Create a class of which instances are
// provided by this provider

[
  Association : ToInstance,
  dynamic,
  HasClassRefs,
  Provider("Microsoft|DSLDAPClassAssociationProvider|V1.0")
]
class DS_LDAP_Class_Containment
{
    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass]
    object Ref ChildClass;

    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass] 
    object Ref ParentClass; // The parent DS Class
};


// Create an instance of the provider class for registration
instance of __Win32Provider as $AssociationsProvider
{
    Name = "Microsoft|DSLDAPClassAssociationProvider|V1.0";
    Clsid = "{33831ED4-42B8-11d2-93AD-00805F853771}";
    ImpersonationLevel = 1;
};    

// Specification of the instances and operation
// provided by the provider
instance of __InstanceProviderRegistration
{
    Provider = $AssociationsProvider;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
    SupportsDelete = FALSE;
    SupportsEnumeration = TRUE;
};
```

<span data-ttu-id="0f8e7-261">Association 類別提供者支援 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 和 [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) 方法。</span><span class="sxs-lookup"><span data-stu-id="0f8e7-261">The association class provider supports the [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) and [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) methods.</span></span>

 


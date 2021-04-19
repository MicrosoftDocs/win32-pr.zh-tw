---
description: 以下列出 WMI 特定的標準限定詞。
ms.assetid: 63bdbafc-51f3-4714-8b7e-9d5a61cef45e
ms.tgt_platform: multiple
title: 標準 WMI 限定詞
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: e73b053354d86c4a56698a7a65c17e302425f56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001733"
---
# <a name="standard-wmi-qualifiers"></a><span data-ttu-id="5add4-103">標準 WMI 限定詞</span><span class="sxs-lookup"><span data-stu-id="5add4-103">Standard WMI Qualifiers</span></span>

<span data-ttu-id="5add4-104">以下列出 WMI 特定的標準限定詞。</span><span class="sxs-lookup"><span data-stu-id="5add4-104">The following lists standard qualifiers specific to WMI.</span></span>

<dt>

<span data-ttu-id="5add4-105"><span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**修訂**</span><span class="sxs-lookup"><span data-stu-id="5add4-105"><span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Amendment**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-106">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5add4-106">Data type: **boolean**</span></span>

<span data-ttu-id="5add4-107">適用于：類別</span><span class="sxs-lookup"><span data-stu-id="5add4-107">Applies to: classes</span></span>

<span data-ttu-id="5add4-108">指出類別包含已修改的修飾限定詞。</span><span class="sxs-lookup"><span data-stu-id="5add4-108">Indicates that a class contains amended qualifiers that are localized.</span></span> <span data-ttu-id="5add4-109">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="5add4-109">The default is **TRUE**.</span></span>

<span data-ttu-id="5add4-110">可以轉譯相關聯的類別。</span><span class="sxs-lookup"><span data-stu-id="5add4-110">The associated class can be translated.</span></span> <span data-ttu-id="5add4-111">若要存取翻譯的版本，請使用地區設定識別碼來建立命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="5add4-111">To access the translated version, use the locale identifier to construct a namespace name.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-112"><span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**略過 \_ GetObject**</span><span class="sxs-lookup"><span data-stu-id="5add4-112"><span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**Bypass\_GetObject**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5add4-113">Data type: **boolean**</span></span>

<span data-ttu-id="5add4-114">適用于：方法</span><span class="sxs-lookup"><span data-stu-id="5add4-114">Applies to: methods</span></span>

<span data-ttu-id="5add4-115">指出方法呼叫應該直接傳遞給提供者的 **ExecMethodAsync** 呼叫，而不是提供者先對 **GetObject** 進行呼叫，以驗證物件路徑。</span><span class="sxs-lookup"><span data-stu-id="5add4-115">Indicates that the method call should pass directly to the **ExecMethodAsync** call of the provider rather than the provider first making a call to **GetObject** to validate the object path.</span></span> <span data-ttu-id="5add4-116">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5add4-116">The default is **FALSE**.</span></span> <span data-ttu-id="5add4-117">使用 **略過 \_ GetObject** 可大幅提升效能。</span><span class="sxs-lookup"><span data-stu-id="5add4-117">Using **Bypass\_GetObject** can significantly improve performance.</span></span>

<span data-ttu-id="5add4-118">使用「 **略過 \_ GetObject**」之前，請確定不會採取下列動作：</span><span class="sxs-lookup"><span data-stu-id="5add4-118">Before using **Bypass\_GetObject**, ensure that neither of the following actions are taken:</span></span>

-   <span data-ttu-id="5add4-119">從您的類別衍生類別。</span><span class="sxs-lookup"><span data-stu-id="5add4-119">Derive a class from your class.</span></span>
-   <span data-ttu-id="5add4-120">覆寫具有 **略過 \_ GetObject** 辨識符號的方法。</span><span class="sxs-lookup"><span data-stu-id="5add4-120">Override the method that has the **Bypass\_GetObject** qualifier.</span></span>

<span data-ttu-id="5add4-121">若無法遵循這些預防措施，可能會導致叫用父類別的方法執行，而不是子類別。</span><span class="sxs-lookup"><span data-stu-id="5add4-121">Failure to follow these precautions can result in invoking the method implementation of the parent class instead of the child class.</span></span> <span data-ttu-id="5add4-122">如需詳細資訊，請參閱使用略過 \_ GetObject 限定詞。</span><span class="sxs-lookup"><span data-stu-id="5add4-122">For more information, see Using the Bypass\_GetObject Qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-123"><span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**CIM \_ 金鑰**</span><span class="sxs-lookup"><span data-stu-id="5add4-123"><span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**CIM\_Key**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-124">資料類型： **CIM \_ 布林值**</span><span class="sxs-lookup"><span data-stu-id="5add4-124">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="5add4-125">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="5add4-125">Applies to: properties</span></span>

<span data-ttu-id="5add4-126">指出相關聯的屬性是 CIM 中的索引鍵屬性，但不是 WMI 中的索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="5add4-126">Indicates that the associated property is a key property in CIM but not in WMI.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-127"><span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="5add4-127"><span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="5add4-128">資料類型： **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="5add4-128">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="5add4-129">適用物件：屬性、方法、參數</span><span class="sxs-lookup"><span data-stu-id="5add4-129">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="5add4-130">包含描述屬性類型的文字。</span><span class="sxs-lookup"><span data-stu-id="5add4-130">Contains text describing the type of a property.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-131"><span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassCoNtext**</span><span class="sxs-lookup"><span data-stu-id="5add4-131"><span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-132">資料類型： **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="5add4-132">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="5add4-133">適用于：類別</span><span class="sxs-lookup"><span data-stu-id="5add4-133">Applies to: classes</span></span>

<span data-ttu-id="5add4-134">指出類別具有與提供者動態提供的詳細資訊相關聯的實例。</span><span class="sxs-lookup"><span data-stu-id="5add4-134">Indicates that a class has instances associated with more information dynamically supplied by a provider.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-135"><span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**廢棄**</span><span class="sxs-lookup"><span data-stu-id="5add4-135"><span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**Deprecated**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-136">資料類型： **CIM \_ 布林值**</span><span class="sxs-lookup"><span data-stu-id="5add4-136">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="5add4-137">適用物件：屬性、類別</span><span class="sxs-lookup"><span data-stu-id="5add4-137">Applies to: properties, classes</span></span>

<span data-ttu-id="5add4-138">表示屬性已由另一個屬性取代。</span><span class="sxs-lookup"><span data-stu-id="5add4-138">Indicates the property has been superseded by another property.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-139"><span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**顯示**</span><span class="sxs-lookup"><span data-stu-id="5add4-139"><span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Display**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-140">適用于：類別、屬性</span><span class="sxs-lookup"><span data-stu-id="5add4-140">Applies to: classes, properties</span></span>

<span data-ttu-id="5add4-141">相關聯類別的 **UUID** 。</span><span class="sxs-lookup"><span data-stu-id="5add4-141">The **UUID** of the associated class.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-142"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**動態**](dynamic-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="5add4-142"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Dynamic**](dynamic-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="5add4-143">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5add4-143">Data type: **boolean**</span></span>

<span data-ttu-id="5add4-144">適用于：類別、屬性</span><span class="sxs-lookup"><span data-stu-id="5add4-144">Applies to: classes, properties</span></span>

<span data-ttu-id="5add4-145">表示以動態方式建立實例的類別。</span><span class="sxs-lookup"><span data-stu-id="5add4-145">Indicates a class whose instances are created dynamically.</span></span> <span data-ttu-id="5add4-146">此限定詞的值必須設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="5add4-146">The value of this qualifier must be set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-147"><span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**</span><span class="sxs-lookup"><span data-stu-id="5add4-147"><span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-148">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5add4-148">Data type: **boolean**</span></span>

<span data-ttu-id="5add4-149">適用于：類別、實例</span><span class="sxs-lookup"><span data-stu-id="5add4-149">Applies to: classes, instances</span></span>

<span data-ttu-id="5add4-150">指出實例包含動態屬性提供者所提供的值。</span><span class="sxs-lookup"><span data-stu-id="5add4-150">Indicates that an instance contains values provided by dynamic property providers.</span></span> <span data-ttu-id="5add4-151">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="5add4-151">The default is **TRUE**.</span></span>

<span data-ttu-id="5add4-152">您必須在這類實例上指定這個限定詞。</span><span class="sxs-lookup"><span data-stu-id="5add4-152">You must specify this qualifier on such an instance.</span></span> <span data-ttu-id="5add4-153">只允許值 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="5add4-153">Only the value **TRUE** is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-154"><span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**固定**</span><span class="sxs-lookup"><span data-stu-id="5add4-154"><span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Fixed**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-155">資料類型： **CIM \_ 布林值**</span><span class="sxs-lookup"><span data-stu-id="5add4-155">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="5add4-156">適用于：實例</span><span class="sxs-lookup"><span data-stu-id="5add4-156">Applies to: instances</span></span>

<span data-ttu-id="5add4-157">指出這個屬性的值在實例的存留期內無法變更。</span><span class="sxs-lookup"><span data-stu-id="5add4-157">Indicates that the value of this property cannot change during the lifetime of the instance.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-158"><span id="ID"></span><span id="id"></span>**Id**</span><span class="sxs-lookup"><span data-stu-id="5add4-158"><span id="ID"></span><span id="id"></span>**ID**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-159">資料類型： **VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="5add4-159">Data type: **VT\_I4**</span></span>

<span data-ttu-id="5add4-160">適用物件：屬性、參數</span><span class="sxs-lookup"><span data-stu-id="5add4-160">Applies to: properties, parameters</span></span>

<span data-ttu-id="5add4-161">當自動產生 MOF 語句時，可唯一識別和序列屬性或方法參數。</span><span class="sxs-lookup"><span data-stu-id="5add4-161">Uniquely identifies and sequences a property or method parameter when MOF statements are generated automatically.</span></span>

<span data-ttu-id="5add4-162">只有方法參數需要此限定詞。</span><span class="sxs-lookup"><span data-stu-id="5add4-162">This qualifier is required for method parameters only.</span></span> <span data-ttu-id="5add4-163">建立方法的參數時，類別設計工具的開頭應該是第一個參數的識別碼 (0) ，然後針對每個後續的參數使用每個後續的整數。</span><span class="sxs-lookup"><span data-stu-id="5add4-163">When creating parameters for a method, class designers should begin with Id(0) for the first parameter and use each successive integer for each successive parameter.</span></span> <span data-ttu-id="5add4-164">如果未小心省略 **識別碼** 限定詞，MOF 編譯器會自動產生 **識別碼** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="5add4-164">If the **ID** qualifiers are unintentionally omitted, the MOF compiler generates **ID** qualifiers automatically.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-165"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**實現**</span><span class="sxs-lookup"><span data-stu-id="5add4-165"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implemented**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-166">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5add4-166">Data type: **boolean**</span></span>

<span data-ttu-id="5add4-167">適用于：方法</span><span class="sxs-lookup"><span data-stu-id="5add4-167">Applies to: methods</span></span>

<span data-ttu-id="5add4-168">指出方法具有提供者所提供的實作為。</span><span class="sxs-lookup"><span data-stu-id="5add4-168">Indicates that a method has an implementation supplied by a provider.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-169"><span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceCoNtext**</span><span class="sxs-lookup"><span data-stu-id="5add4-169"><span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-170">資料類型： **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="5add4-170">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="5add4-171">適用于：實例</span><span class="sxs-lookup"><span data-stu-id="5add4-171">Applies to: instances</span></span>

<span data-ttu-id="5add4-172">指出實例包含動態屬性提供者所提供的值。</span><span class="sxs-lookup"><span data-stu-id="5add4-172">Indicates that an instance contains values provided by a dynamic property provider.</span></span>

<span data-ttu-id="5add4-173">值會傳遞給屬性提供者，做為 [**IWbemPropertyProvider：： GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) 方法的引數。</span><span class="sxs-lookup"><span data-stu-id="5add4-173">The value is passed to the property provider as an argument to the [**IWbemPropertyProvider::GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) method.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-174"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**現場**</span><span class="sxs-lookup"><span data-stu-id="5add4-174"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-175">資料類型： **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="5add4-175">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="5add4-176">適用于：類別或實例</span><span class="sxs-lookup"><span data-stu-id="5add4-176">Applies to: classes or instances</span></span>

<span data-ttu-id="5add4-177">指定類別或實例的原始語言。</span><span class="sxs-lookup"><span data-stu-id="5add4-177">Specifies the language of origin for a class or instance.</span></span> <span data-ttu-id="5add4-178">如需地區設定值的詳細資訊，請參閱 [地區設定代碼](#locale-codes)。</span><span class="sxs-lookup"><span data-stu-id="5add4-178">For more information about locale values, see [Locale Codes](#locale-codes).</span></span>

</dd> <dt>

<span data-ttu-id="5add4-179"><span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**</span><span class="sxs-lookup"><span data-stu-id="5add4-179"><span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-180">資料類型： **字串陣列**</span><span class="sxs-lookup"><span data-stu-id="5add4-180">Data type: **string array**</span></span>

<span data-ttu-id="5add4-181">適用于：命名空間實例</span><span class="sxs-lookup"><span data-stu-id="5add4-181">Applies to: namespace instances</span></span>

<span data-ttu-id="5add4-182">以 [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) 格式指定命名空間的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="5add4-182">Specifies a security descriptor for the namespace in [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) format.</span></span> <span data-ttu-id="5add4-183">如需詳細資訊，請參閱 [在建立命名空間時設定命名空間安全性](setting-namespace-security-when-the-namespace-is-created.md)。</span><span class="sxs-lookup"><span data-stu-id="5add4-183">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span> <span data-ttu-id="5add4-184">SDDL 字串是由 WMI 處理來建立命名空間安全性，但不會儲存為字串。</span><span class="sxs-lookup"><span data-stu-id="5add4-184">The SDDL string is processed by WMI to establish the namespace security but not stored as a string.</span></span> <span data-ttu-id="5add4-185">如果未指定任何安全描述項，則會使用預設安全性。</span><span class="sxs-lookup"><span data-stu-id="5add4-185">If no security descriptor is specified, the default security is used.</span></span> <span data-ttu-id="5add4-186">如需詳細資訊，請參閱 [設定命名空間安全描述項](setting-namespace-security-descriptors.md)。</span><span class="sxs-lookup"><span data-stu-id="5add4-186">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

</dd> <dt>

<span data-ttu-id="5add4-187"><span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**選**</span><span class="sxs-lookup"><span data-stu-id="5add4-187"><span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Optional**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-188">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5add4-188">Data type: **boolean**</span></span>

<span data-ttu-id="5add4-189">適用于：參數</span><span class="sxs-lookup"><span data-stu-id="5add4-189">Applies to: parameters</span></span>

<span data-ttu-id="5add4-190">表示不需要參數，且其具有行為良好的預設值。</span><span class="sxs-lookup"><span data-stu-id="5add4-190">Indicates that a parameter is not required, and that it has a well-behaved default value.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-191"><span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**特權**</span><span class="sxs-lookup"><span data-stu-id="5add4-191"><span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Privileges**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-192">資料類型： **字串陣列**</span><span class="sxs-lookup"><span data-stu-id="5add4-192">Data type: **string array**</span></span>

<span data-ttu-id="5add4-193">適用物件：屬性、方法</span><span class="sxs-lookup"><span data-stu-id="5add4-193">Applies to: properties, methods</span></span>

<span data-ttu-id="5add4-194">值的集合，用來通知用戶端建立實例、填入屬性或執行方法時需要哪些許可權。</span><span class="sxs-lookup"><span data-stu-id="5add4-194">Set of values used to inform the client which privileges are required to create instances, fill in properties, or perform methods.</span></span> <span data-ttu-id="5add4-195">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5add4-195">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-196"><span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyCoNtext**</span><span class="sxs-lookup"><span data-stu-id="5add4-196"><span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyContext**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-197">資料類型： **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="5add4-197">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="5add4-198">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="5add4-198">Applies to: properties</span></span>

<span data-ttu-id="5add4-199">指出實例屬性包含動態屬性提供者所提供的值。</span><span class="sxs-lookup"><span data-stu-id="5add4-199">Indicates that an instance property contains values provided by dynamic property providers.</span></span>

<span data-ttu-id="5add4-200">您必須在這類屬性上指定這個限定詞。</span><span class="sxs-lookup"><span data-stu-id="5add4-200">You must specify this qualifier on such a property.</span></span> <span data-ttu-id="5add4-201">值會以引數形式傳遞給屬性提供者，以作為 [**IWbemPropertyProvider：： GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty)的引數。</span><span class="sxs-lookup"><span data-stu-id="5add4-201">The value is passed to the property provider as an argument to [**IWbemPropertyProvider::GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty).</span></span>

</dd> <dt>

<span data-ttu-id="5add4-202"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**供應商**</span><span class="sxs-lookup"><span data-stu-id="5add4-202"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-203">資料類型： **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="5add4-203">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="5add4-204">適用于：類別</span><span class="sxs-lookup"><span data-stu-id="5add4-204">Applies to: classes</span></span>

<span data-ttu-id="5add4-205">此辨識符號的值是提供類別實例和重新整理實例資料的動態提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="5add4-205">The value of this qualifier is the name of the dynamic provider that provides class instances and refreshes instance data.</span></span> <span data-ttu-id="5add4-206">您必須使用包含此名稱的 **name** 屬性來建立 [**\_ \_ Win32Provider**](--win32provider.md)類別的實例，以向 WMI 註冊此名稱。</span><span class="sxs-lookup"><span data-stu-id="5add4-206">This name must be registered with WMI by creating an instance of the [**\_\_Win32Provider**](--win32provider.md) class with the **Name** property containing this name.</span></span> <span data-ttu-id="5add4-207">當此限定詞指定于動態提供其實例的類別上時，也必須指定 **動態** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="5add4-207">When this qualifier is specified on a class whose instances are provided dynamically, the **Dynamic** qualifier must also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-208"><span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**</span><span class="sxs-lookup"><span data-stu-id="5add4-208"><span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-209">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5add4-209">Data type: **boolean**</span></span>

<span data-ttu-id="5add4-210">適用于：命名空間實例</span><span class="sxs-lookup"><span data-stu-id="5add4-210">Applies to: namespace instances</span></span>

<span data-ttu-id="5add4-211">如果設定為 **TRUE**， **RequiresEncryption** 會標示命名空間，讓用戶端應用程式和腳本必須使用加密的驗證進行連接。</span><span class="sxs-lookup"><span data-stu-id="5add4-211">If set to **TRUE**, **RequiresEncryption** marks a namespace so that client applications and scripts must connect with encrypted authentication.</span></span> <span data-ttu-id="5add4-212">驗證層級必須設定為 c + + 中的 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 。</span><span class="sxs-lookup"><span data-stu-id="5add4-212">The authentication level must be set to **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** in C++.</span></span> <span data-ttu-id="5add4-213">在腳本或 Visual Basic 中，驗證層級必須設為 **WbemAuthenticationLevelPktPrivacy**。</span><span class="sxs-lookup"><span data-stu-id="5add4-213">In scripting or Visual Basic, authentication level must be set to **WbemAuthenticationLevelPktPrivacy**.</span></span> <span data-ttu-id="5add4-214">如需詳細資訊，請參閱 [設定命名空間安全描述項](setting-namespace-security-descriptors.md)。</span><span class="sxs-lookup"><span data-stu-id="5add4-214">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span> <span data-ttu-id="5add4-215">辨識符號是用於具有 pragma 命名空間預處理器命令的 [*MOF*](gloss-m.md) 中。</span><span class="sxs-lookup"><span data-stu-id="5add4-215">The qualifier is used in [*MOF*](gloss-m.md) with the pragma namespace preprocessor command.</span></span>

<span data-ttu-id="5add4-216">如需詳細資訊，請參閱 [使用 c + + 設定預設進程安全性等級](setting-the-default-process-security-level-using-c-.md) 或 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="5add4-216">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md) or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span> <span data-ttu-id="5add4-217">腳本驗證層級是在 [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)中定義。</span><span class="sxs-lookup"><span data-stu-id="5add4-217">Scripting authentication levels are defined in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span>

</dd> <dt>

<span data-ttu-id="5add4-218"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**單身 人士**</span><span class="sxs-lookup"><span data-stu-id="5add4-218"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-219">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5add4-219">Data type: **boolean**</span></span>

<span data-ttu-id="5add4-220">適用于：類別</span><span class="sxs-lookup"><span data-stu-id="5add4-220">Applies to: classes</span></span>

<span data-ttu-id="5add4-221">指定只能有一個實例而且不包含索引鍵屬性的類別。</span><span class="sxs-lookup"><span data-stu-id="5add4-221">Designates a class that can only have one instance and that does not contain key properties.</span></span>

<span data-ttu-id="5add4-222">只允許值 **TRUE** (預設) 。</span><span class="sxs-lookup"><span data-stu-id="5add4-222">Only the value **TRUE** (default) is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-223"><span id="Static"></span><span id="static"></span><span id="STATIC"></span>**靜態**</span><span class="sxs-lookup"><span data-stu-id="5add4-223"><span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Static**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-224">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5add4-224">Data type: **boolean**</span></span>

<span data-ttu-id="5add4-225">適用于：方法</span><span class="sxs-lookup"><span data-stu-id="5add4-225">Applies to: methods</span></span>

<span data-ttu-id="5add4-226">指出方法是否可以使用類別定義或其實例來呼叫。</span><span class="sxs-lookup"><span data-stu-id="5add4-226">Indicates whether a method can called by using the class definition or its instances.</span></span>

<span data-ttu-id="5add4-227">無法從實例叫用方法。</span><span class="sxs-lookup"><span data-stu-id="5add4-227">The method cannot be invoked from an instance.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-228"><span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**亞**</span><span class="sxs-lookup"><span data-stu-id="5add4-228"><span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**SubType**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-229">資料類型： **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="5add4-229">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="5add4-230">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="5add4-230">Applies to: properties</span></span>

<span data-ttu-id="5add4-231">指出 **CIM \_ DATETIME** 類型的屬性代表時間間隔，而不是特定時間。</span><span class="sxs-lookup"><span data-stu-id="5add4-231">Indicates that a property of type **CIM\_DATETIME** represents a time interval rather than a specific time.</span></span>

<span data-ttu-id="5add4-232">若要將屬性識別為間隔，此限定詞的值必須是 "interval"。</span><span class="sxs-lookup"><span data-stu-id="5add4-232">To identify the property as an interval, the value of this qualifier must be "interval".</span></span> <span data-ttu-id="5add4-233">此辨識符號的所有其他值都會保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="5add4-233">All other values for this qualifier are reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-234"><span id="UUID"></span><span id="uuid"></span>**Uuid**</span><span class="sxs-lookup"><span data-stu-id="5add4-234"><span id="UUID"></span><span id="uuid"></span>**UUID**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-235">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5add4-235">Data type: **string**</span></span>

<span data-ttu-id="5add4-236">適用于：類別</span><span class="sxs-lookup"><span data-stu-id="5add4-236">Applies to: classes</span></span>

<span data-ttu-id="5add4-237">套用至類別的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5add4-237">Universally unique identifier applied to the class.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-238"><span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**</span><span class="sxs-lookup"><span data-stu-id="5add4-238"><span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-239">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5add4-239">Data type: **string**</span></span>

<span data-ttu-id="5add4-240">適用于：類別</span><span class="sxs-lookup"><span data-stu-id="5add4-240">Applies to: classes</span></span>

<span data-ttu-id="5add4-241">類別物件的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="5add4-241">The version number of the class object.</span></span> <span data-ttu-id="5add4-242">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5add4-242">The default is **NULL**.</span></span> <span data-ttu-id="5add4-243">當對類別進行變更時，版本號碼會遞增。</span><span class="sxs-lookup"><span data-stu-id="5add4-243">The version number is incremented when changes are made to the class.</span></span>

</dd> <dt>

<span data-ttu-id="5add4-244"><span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**</span><span class="sxs-lookup"><span data-stu-id="5add4-244"><span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**</span></span>
</dt> <dd>

<span data-ttu-id="5add4-245">資料類型： **字串陣列**</span><span class="sxs-lookup"><span data-stu-id="5add4-245">Data type: **string array**</span></span>

<span data-ttu-id="5add4-246">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="5add4-246">Applies to: properties</span></span>

<span data-ttu-id="5add4-247">值的集合，指出哪些系統許可權必須可供使用且已啟用，以進行成功的寫入操作。</span><span class="sxs-lookup"><span data-stu-id="5add4-247">Set of values indicating which system privileges must be available and enabled for a successful write operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5add4-248">備註</span><span class="sxs-lookup"><span data-stu-id="5add4-248">Remarks</span></span>

### <a name="locale-codes"></a><span data-ttu-id="5add4-249">地區設定代碼</span><span class="sxs-lookup"><span data-stu-id="5add4-249">Locale Codes</span></span>

<span data-ttu-id="5add4-250">地區設定代碼的格式為 "MS \_ <Three Digit Language ID> "。</span><span class="sxs-lookup"><span data-stu-id="5add4-250">A locale code is of the form "MS\_<Three Digit Language ID>".</span></span> <span data-ttu-id="5add4-251">例如，英文地區設定為 MS \_ 409。</span><span class="sxs-lookup"><span data-stu-id="5add4-251">For example, English locale is MS\_409.</span></span> <span data-ttu-id="5add4-252">下表列出語言識別項。</span><span class="sxs-lookup"><span data-stu-id="5add4-252">The following table lists the language IDs.</span></span>



| <span data-ttu-id="5add4-253">語言</span><span class="sxs-lookup"><span data-stu-id="5add4-253">Language</span></span>              | <span data-ttu-id="5add4-254">語言識別項 (十六進位) </span><span class="sxs-lookup"><span data-stu-id="5add4-254">Language ID (hexadecimal)</span></span> |
|-----------------------|---------------------------|
| <span data-ttu-id="5add4-255">阿拉伯文</span><span class="sxs-lookup"><span data-stu-id="5add4-255">Arabic</span></span>                | <span data-ttu-id="5add4-256">401</span><span class="sxs-lookup"><span data-stu-id="5add4-256">401</span></span>                       |
| <span data-ttu-id="5add4-257">葡萄牙文 (巴西)</span><span class="sxs-lookup"><span data-stu-id="5add4-257">Portuguese (Brazil)</span></span>   | <span data-ttu-id="5add4-258">416</span><span class="sxs-lookup"><span data-stu-id="5add4-258">416</span></span>                       |
| <span data-ttu-id="5add4-259">簡體中文</span><span class="sxs-lookup"><span data-stu-id="5add4-259">Chinese (Simplified)</span></span>  | <span data-ttu-id="5add4-260">804</span><span class="sxs-lookup"><span data-stu-id="5add4-260">804</span></span>                       |
| <span data-ttu-id="5add4-261">繁體中文</span><span class="sxs-lookup"><span data-stu-id="5add4-261">Chinese (Traditional)</span></span> | <span data-ttu-id="5add4-262">404</span><span class="sxs-lookup"><span data-stu-id="5add4-262">404</span></span>                       |
| <span data-ttu-id="5add4-263">捷克文</span><span class="sxs-lookup"><span data-stu-id="5add4-263">Czech</span></span>                 | <span data-ttu-id="5add4-264">405</span><span class="sxs-lookup"><span data-stu-id="5add4-264">405</span></span>                       |
| <span data-ttu-id="5add4-265">丹麥文</span><span class="sxs-lookup"><span data-stu-id="5add4-265">Danish</span></span>                | <span data-ttu-id="5add4-266">406</span><span class="sxs-lookup"><span data-stu-id="5add4-266">406</span></span>                       |
| <span data-ttu-id="5add4-267">荷蘭文</span><span class="sxs-lookup"><span data-stu-id="5add4-267">Dutch</span></span>                 | <span data-ttu-id="5add4-268">413</span><span class="sxs-lookup"><span data-stu-id="5add4-268">413</span></span>                       |
| <span data-ttu-id="5add4-269">英文 (預設值)</span><span class="sxs-lookup"><span data-stu-id="5add4-269">English (default)</span></span>     | <span data-ttu-id="5add4-270">409</span><span class="sxs-lookup"><span data-stu-id="5add4-270">409</span></span>                       |
| <span data-ttu-id="5add4-271">芬蘭文</span><span class="sxs-lookup"><span data-stu-id="5add4-271">Finnish</span></span>               | <span data-ttu-id="5add4-272">40b</span><span class="sxs-lookup"><span data-stu-id="5add4-272">40b</span></span>                       |
| <span data-ttu-id="5add4-273">法文</span><span class="sxs-lookup"><span data-stu-id="5add4-273">French</span></span>                | <span data-ttu-id="5add4-274">40c</span><span class="sxs-lookup"><span data-stu-id="5add4-274">40c</span></span>                       |
| <span data-ttu-id="5add4-275">德文</span><span class="sxs-lookup"><span data-stu-id="5add4-275">German</span></span>                | <span data-ttu-id="5add4-276">407</span><span class="sxs-lookup"><span data-stu-id="5add4-276">407</span></span>                       |
| <span data-ttu-id="5add4-277">希臘文</span><span class="sxs-lookup"><span data-stu-id="5add4-277">Greek</span></span>                 | <span data-ttu-id="5add4-278">408</span><span class="sxs-lookup"><span data-stu-id="5add4-278">408</span></span>                       |
| <span data-ttu-id="5add4-279">Hebrew</span><span class="sxs-lookup"><span data-stu-id="5add4-279">Hebrew</span></span>                | <span data-ttu-id="5add4-280">40d</span><span class="sxs-lookup"><span data-stu-id="5add4-280">40d</span></span>                       |
| <span data-ttu-id="5add4-281">匈牙利文</span><span class="sxs-lookup"><span data-stu-id="5add4-281">Hungarian</span></span>             | <span data-ttu-id="5add4-282">40e</span><span class="sxs-lookup"><span data-stu-id="5add4-282">40e</span></span>                       |
| <span data-ttu-id="5add4-283">義大利文</span><span class="sxs-lookup"><span data-stu-id="5add4-283">Italian</span></span>               | <span data-ttu-id="5add4-284">410</span><span class="sxs-lookup"><span data-stu-id="5add4-284">410</span></span>                       |
| <span data-ttu-id="5add4-285">日文</span><span class="sxs-lookup"><span data-stu-id="5add4-285">Japanese</span></span>              | <span data-ttu-id="5add4-286">411</span><span class="sxs-lookup"><span data-stu-id="5add4-286">411</span></span>                       |
| <span data-ttu-id="5add4-287">韓文</span><span class="sxs-lookup"><span data-stu-id="5add4-287">Korean</span></span>                | <span data-ttu-id="5add4-288">412</span><span class="sxs-lookup"><span data-stu-id="5add4-288">412</span></span>                       |
| <span data-ttu-id="5add4-289">挪威文</span><span class="sxs-lookup"><span data-stu-id="5add4-289">Norwegian</span></span>             | <span data-ttu-id="5add4-290">414</span><span class="sxs-lookup"><span data-stu-id="5add4-290">414</span></span>                       |
| <span data-ttu-id="5add4-291">波蘭文</span><span class="sxs-lookup"><span data-stu-id="5add4-291">Polish</span></span>                | <span data-ttu-id="5add4-292">415</span><span class="sxs-lookup"><span data-stu-id="5add4-292">415</span></span>                       |
| <span data-ttu-id="5add4-293">葡萄牙文 (葡萄牙)</span><span class="sxs-lookup"><span data-stu-id="5add4-293">Portuguese (Portugal)</span></span> | <span data-ttu-id="5add4-294">816</span><span class="sxs-lookup"><span data-stu-id="5add4-294">816</span></span>                       |
| <span data-ttu-id="5add4-295">俄文</span><span class="sxs-lookup"><span data-stu-id="5add4-295">Russian</span></span>               | <span data-ttu-id="5add4-296">419</span><span class="sxs-lookup"><span data-stu-id="5add4-296">419</span></span>                       |
| <span data-ttu-id="5add4-297">西班牙文</span><span class="sxs-lookup"><span data-stu-id="5add4-297">Spanish</span></span>               | <span data-ttu-id="5add4-298">c0a</span><span class="sxs-lookup"><span data-stu-id="5add4-298">c0a</span></span>                       |
| <span data-ttu-id="5add4-299">瑞典文</span><span class="sxs-lookup"><span data-stu-id="5add4-299">Swedish</span></span>               | <span data-ttu-id="5add4-300">41D</span><span class="sxs-lookup"><span data-stu-id="5add4-300">41D</span></span>                       |
| <span data-ttu-id="5add4-301">土耳其文</span><span class="sxs-lookup"><span data-stu-id="5add4-301">Turkish</span></span>               | <span data-ttu-id="5add4-302">41f</span><span class="sxs-lookup"><span data-stu-id="5add4-302">41f</span></span>                       |



 

### <a name="using-the-bypass_getobject-qualifier"></a><span data-ttu-id="5add4-303">使用略過 \_ GetObject 辨識符號</span><span class="sxs-lookup"><span data-stu-id="5add4-303">Using the Bypass\_GetObject Qualifier</span></span>

<span data-ttu-id="5add4-304">在方法上使用 **略過 \_ GetObject** 限定詞可能會產生令人困惑的結果。</span><span class="sxs-lookup"><span data-stu-id="5add4-304">Using the **Bypass\_GetObject** qualifier on a method can produce confusing results.</span></span>

<span data-ttu-id="5add4-305">下列範例會定義 **圖形** 和 **圓形** 類別。</span><span class="sxs-lookup"><span data-stu-id="5add4-305">The following example defines the **Shape** and **Circle** classes.</span></span> <span data-ttu-id="5add4-306">請注意， **圓形** 類別衍生自 **Shape** 類別。</span><span class="sxs-lookup"><span data-stu-id="5add4-306">Note that the **Circle** class is derived from the **Shape** class.</span></span>


```VB
class Shape
{
   string Name;
   uint32 DrawIt();  // - draws an irregular geometric shape
};

class Circle : Shape
{
   uint32 DrawIt();  // - draws a circle
};
```



<span data-ttu-id="5add4-307">下列對 **ExecMethod** 的呼叫會使用名為 "MyCircle" 的 **圓形** 物件來繪製圓形。</span><span class="sxs-lookup"><span data-stu-id="5add4-307">The following call to **ExecMethod** uses a **Circle** object named "MyCircle" to draw a circle.</span></span>


```VB
ExecMethod("Shape.Name='MyCircle'","DrawIt");
```



<span data-ttu-id="5add4-308">在先前的案例中，WMI 會呼叫 **GetObject**;探索 "Shape. Name = ' MyCircle '" 是 **圓形**;並執行 **DrawIt** 的 **圓形** 實作為。</span><span class="sxs-lookup"><span data-stu-id="5add4-308">In the previous scenario, WMI calls **GetObject**; discovers that "Shape.Name='MyCircle'" is a **Circle**; and executes the **Circle** implementation of **DrawIt**.</span></span> <span data-ttu-id="5add4-309">但是，如果您在 **DrawIt** 上使用 [**略過 \_ getobject** 辨識符號]，WMI 不會呼叫 **GetObject**，而不會發現 "shape. Name = ' MyCircle '" 是 **圓形**，而是執行 **DrawIt** 的 **圖形** 實，而不是 **DrawIt** 的 **圓形** 實作為。</span><span class="sxs-lookup"><span data-stu-id="5add4-309">However, if you use the **Bypass\_GetObject** qualifier on **DrawIt**, WMI does not call **GetObject**, does not discover that "Shape.Name='MyCircle'" is a **Circle**, and executes the **Shape** implementation of **DrawIt** instead of the **Circle** implementation of **DrawIt**.</span></span>

<span data-ttu-id="5add4-310">下列 **ExecMethod** 呼叫一律會叫用正確的 **DrawIt** 執行。</span><span class="sxs-lookup"><span data-stu-id="5add4-310">The following call to **ExecMethod** always invokes the correct implementation of **DrawIt**.</span></span>


```VB
ExecMethod("Circle.Name='MyCircle'","DrawIt");
```



## <a name="requirements"></a><span data-ttu-id="5add4-311">規格需求</span><span class="sxs-lookup"><span data-stu-id="5add4-311">Requirements</span></span>



| <span data-ttu-id="5add4-312">需求</span><span class="sxs-lookup"><span data-stu-id="5add4-312">Requirement</span></span> | <span data-ttu-id="5add4-313">值</span><span class="sxs-lookup"><span data-stu-id="5add4-313">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5add4-314">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5add4-314">Minimum supported client</span></span><br/> | <span data-ttu-id="5add4-315">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5add4-315">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5add4-316">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5add4-316">Minimum supported server</span></span><br/> | <span data-ttu-id="5add4-317">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5add4-317">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5add4-318">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5add4-318">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5add4-319">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="5add4-319">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="5add4-320">WMI 限定詞</span><span class="sxs-lookup"><span data-stu-id="5add4-320">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="5add4-321">新增限定詞</span><span class="sxs-lookup"><span data-stu-id="5add4-321">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 


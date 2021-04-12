---
title: '得到 iadsclass 屬性方法 (Iads .h) '
description: 得到 iadsclass 介面的屬性方法會取得或設定下列屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 191f6873-c4bd-4e71-9d23-478454b7cec2
ms.tgt_platform: multiple
keywords:
- 得到 iadsclass 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsClass Property Methods
- IADsClass.Abstract
- IADsClass.get_Abstract
- IADsClass.put_Abstract
- IADsClass.AuxDerivedFrom
- IADsClass.get_AuxDerivedFrom
- IADsClass.put_AuxDerivedFrom
- IADsClass.Auxiliary
- IADsClass.get_Auxiliary
- IADsClass.put_Auxiliary
- IADsClass.CLSID
- IADsClass.get_CLSID
- IADsClass.put_CLSID
- IADsClass.Container
- IADsClass.get_Container
- IADsClass.put_Container
- IADsClass.Containment
- IADsClass.get_Containment
- IADsClass.put_Containment
- IADsClass.DerivedFrom
- IADsClass.get_DerivedFrom
- IADsClass.put_DerivedFrom
- IADsClass.HelpFileContext
- IADsClass.get_HelpFileContext
- IADsClass.put_HelpFileContext
- IADsClass.HelpFileName
- IADsClass.get_HelpFileName
- IADsClass.put_HelpFileName
- IADsClass.MandatoryProperties
- IADsClass.get_MandatoryProperties
- IADsClass.put_MandatoryProperties
- IADsClass.NamingProperties
- IADsClass.get_NamingProperties
- IADsClass.put_NamingProperties
- IADsClass.OID
- IADsClass.get_OID
- IADsClass.put_OID
- IADsClass.OptionalProperties
- IADsClass.get_OptionalProperties
- IADsClass.put_OptionalProperties
- IADsClass.PossibleSuperiors
- IADsClass.get_PossibleSuperiors
- IADsClass.put_PossibleSuperiors
- IADsClass.PrimaryInterface
- IADsClass.get_PrimaryInterface
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358bc33347f035af92303a4ce9879105cd247a3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105155"
---
# <a name="iadsclass-property-methods"></a><span data-ttu-id="fd34b-105">得到 iadsclass 屬性方法</span><span class="sxs-lookup"><span data-stu-id="fd34b-105">IADsClass Property Methods</span></span>

<span data-ttu-id="fd34b-106">[**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)介面的屬性方法會取得或設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="fd34b-106">The property methods of the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface get or set the following properties.</span></span> <span data-ttu-id="fd34b-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="fd34b-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="fd34b-108">屬性</span><span class="sxs-lookup"><span data-stu-id="fd34b-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="fd34b-109">**摘要**</span><span class="sxs-lookup"><span data-stu-id="fd34b-109">**Abstract**</span></span>
<span data-ttu-id="fd34b-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd34b-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd34b-111">指出此類別為抽象或非抽象的布林值。</span><span class="sxs-lookup"><span data-stu-id="fd34b-111">Boolean value that indicates if this class is Abstract or non-abstract.</span></span> <span data-ttu-id="fd34b-112">當 **為 TRUE** 時，這個類別是抽象類別，無法在目錄服務中直接具現化。</span><span class="sxs-lookup"><span data-stu-id="fd34b-112">When **TRUE**, this class is an Abstract class and cannot be directly instantiated in the directory service.</span></span> <span data-ttu-id="fd34b-113">抽象類別只能用來做為超級類別。</span><span class="sxs-lookup"><span data-stu-id="fd34b-113">Abstract classes can only be used as super classes.</span></span>

<dt>

<span data-ttu-id="fd34b-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd34b-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd34b-115">腳本資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fd34b-115">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Abstract(
  [out] BOOLEAN* pbAbstract
);
HRESULT put_Abstract(
  [in] BOOLEAN bAbstract
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd34b-116">**AuxDerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="fd34b-116">**AuxDerivedFrom**</span></span>
<span data-ttu-id="fd34b-117"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd34b-117"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd34b-118">ADsPath 字串的陣列，表示此類別衍生自的超級輔助類別。</span><span class="sxs-lookup"><span data-stu-id="fd34b-118">Array of ADsPath strings that indicate the super Auxiliary classes this class derives from.</span></span>

<dt>

<span data-ttu-id="fd34b-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd34b-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd34b-120">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="fd34b-120">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AuxDerivedFrom(
  [out] VARIANT* pvAuxDerivedFrom
);
HRESULT put_AuxDerivedFrom(
  [in] VARIANT vAuxDerivedFrom
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd34b-121">**輔助**</span><span class="sxs-lookup"><span data-stu-id="fd34b-121">**Auxiliary**</span></span>
<span data-ttu-id="fd34b-122"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd34b-122"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd34b-123">指出此類別是否為輔助的布林值。</span><span class="sxs-lookup"><span data-stu-id="fd34b-123">Boolean value that indicates whether or not this class is Auxiliary.</span></span> <span data-ttu-id="fd34b-124">當 **為 TRUE** 時，這個類別是輔助類別，無法在目錄服務中直接具現化。</span><span class="sxs-lookup"><span data-stu-id="fd34b-124">When **TRUE**, this class is an Auxiliary class and cannot be directly instantiated in the directory service.</span></span> <span data-ttu-id="fd34b-125">輔助類別只能用來做為其他輔助類別的超級類別，或是結構類別上其他屬性的來源。</span><span class="sxs-lookup"><span data-stu-id="fd34b-125">Auxiliary classes can only be used as super classes of other Auxiliary classes or as a source of additional properties on structural classes.</span></span>

<dt>

<span data-ttu-id="fd34b-126">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd34b-126">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd34b-127">腳本資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fd34b-127">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Auxiliary(
  [out] BOOLEAN* pbAuxiliary
);
HRESULT put_Auxiliary(
  [in] BOOLEAN bAuxiliary
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd34b-128">**Clsid**</span><span class="sxs-lookup"><span data-stu-id="fd34b-128">**CLSID**</span></span>
<span data-ttu-id="fd34b-129"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd34b-129"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd34b-130">選擇性的提供者特定 CLSID，識別可執行此類別的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="fd34b-130">Optional provider-specific CLSID identifying the COM object that implements this class.</span></span>

<dt>

<span data-ttu-id="fd34b-131">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd34b-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd34b-132">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="fd34b-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CLSID(
  [out] BSTR* pbstrCLSID
);
HRESULT put_CLSID(
  [in] BSTR bstrCLSID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd34b-133">**容器**</span><span class="sxs-lookup"><span data-stu-id="fd34b-133">**Container**</span></span>
<span data-ttu-id="fd34b-134"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd34b-134"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd34b-135">指出此類別是否可以是其他物件類別之容器的布林值。</span><span class="sxs-lookup"><span data-stu-id="fd34b-135">Boolean value that indicates if this class can be a container of other object classes.</span></span> <span data-ttu-id="fd34b-136">如果這個值為 **TRUE**，您可以呼叫 **get \_ 容器** 方法，以取得這個類別可包含的物件類別陣列。</span><span class="sxs-lookup"><span data-stu-id="fd34b-136">If this value is **TRUE**, you can call the **get\_Container** method to get an array of the object classes that this class can contain.</span></span>

<dt>

<span data-ttu-id="fd34b-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd34b-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd34b-138">腳本資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fd34b-138">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Container(
  [out] BOOLEAN* pbContainer
);
HRESULT put_Container(
  [in] BOOLEAN bContainer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd34b-139">**遏制**</span><span class="sxs-lookup"><span data-stu-id="fd34b-139">**Containment**</span></span>
<span data-ttu-id="fd34b-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd34b-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd34b-141">**BSTR** 陣列，其中每個元素都是這個類別可包含的物件類別名稱。</span><span class="sxs-lookup"><span data-stu-id="fd34b-141">A **BSTR** array in which each element is the name of an object class that this class can contain.</span></span>

<dt>

<span data-ttu-id="fd34b-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd34b-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd34b-143">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="fd34b-143">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Containment(
  [out] VARIANT* pvContainment
);
HRESULT put_Containment(
  [in] VARIANT vContainment
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd34b-144">**DerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="fd34b-144">**DerivedFrom**</span></span>
<span data-ttu-id="fd34b-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd34b-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd34b-146">ADsPath 字串的陣列，表示此類別衍生自哪些類別。</span><span class="sxs-lookup"><span data-stu-id="fd34b-146">Array of ADsPath strings that indicate which classes this class was derived from.</span></span>

<dt>

<span data-ttu-id="fd34b-147">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd34b-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd34b-148">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="fd34b-148">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DerivedFrom(
  [out] VARIANT* pvDerivedFrom
);
HRESULT put_DerivedFrom(
  [in] VARIANT vDerivedFrom
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd34b-149">**HelpFileCoNtext**</span><span class="sxs-lookup"><span data-stu-id="fd34b-149">**HelpFileContext**</span></span>
<span data-ttu-id="fd34b-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd34b-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd34b-151">**HelpFileName** 內的內容識別碼，可以找到這個類別的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="fd34b-151">Context ID inside **HelpFileName** where specific information for this class can be found.</span></span>

<dt>

<span data-ttu-id="fd34b-152">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd34b-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd34b-153">編寫資料類型的腳本： **long**</span><span class="sxs-lookup"><span data-stu-id="fd34b-153">Scripting data type: **long**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileContext(
  [out] long* plHelpContext
);
HRESULT put_HelpFileContext(
  [in] long lHelpContext
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd34b-154">**HelpFileName**</span><span class="sxs-lookup"><span data-stu-id="fd34b-154">**HelpFileName**</span></span>
<span data-ttu-id="fd34b-155"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd34b-155"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd34b-156">包含此類別物件之詳細資訊的說明檔名稱。</span><span class="sxs-lookup"><span data-stu-id="fd34b-156">Name of a help file that contains more information about objects of this class.</span></span>

<dt>

<span data-ttu-id="fd34b-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd34b-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd34b-158">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="fd34b-158">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileName(
  [out] BSTR* pbstrHelpFileName
);
HRESULT put_HelpFileName(
  [in] BSTR bstrHelpFileName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd34b-159">**MandatoryProperties**</span><span class="sxs-lookup"><span data-stu-id="fd34b-159">**MandatoryProperties**</span></span>
<span data-ttu-id="fd34b-160"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd34b-160"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd34b-161">**VARIANT** 的 **SAFEARRAY** ，其中列出必須設定才能將此類別寫入至儲存體的屬性。</span><span class="sxs-lookup"><span data-stu-id="fd34b-161">**SAFEARRAY** of **VARIANT** s that lists the properties that must be set for this class to be written to storage.</span></span> <span data-ttu-id="fd34b-162">如果類別只包含一個屬性，則 **get \_ MandatoryProperties** 會傳回 **BSTR**。</span><span class="sxs-lookup"><span data-stu-id="fd34b-162">If the class only contains one property, then **get\_MandatoryProperties** will return a **BSTR**.</span></span>

<dt>

<span data-ttu-id="fd34b-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd34b-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd34b-164">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="fd34b-164">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MandatoryProperties(
  [out] VARIANT* pvarMandatoryProperties
);
HRESULT put_MandatoryProperties(
  [in] VARIANT varMandatoryProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd34b-165">**NamingProperties**</span><span class="sxs-lookup"><span data-stu-id="fd34b-165">**NamingProperties**</span></span>
<span data-ttu-id="fd34b-166"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd34b-166"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd34b-167">**BSTR** 的 **SAFEARRAY** ，列出用來命名這個架構類別之屬性的屬性。</span><span class="sxs-lookup"><span data-stu-id="fd34b-167">**SAFEARRAY** of **BSTR** s that lists the properties used to name attributes of this schema class.</span></span>

<dt>

<span data-ttu-id="fd34b-168">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd34b-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd34b-169">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="fd34b-169">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamingProperties(
  [out] VARIANT* pvarNamingProperties
);
HRESULT put_NamingProperties(
  [in] VARIANT varNamingProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd34b-170">**老**</span><span class="sxs-lookup"><span data-stu-id="fd34b-170">**OID**</span></span>
<span data-ttu-id="fd34b-171"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd34b-171"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd34b-172">定義此類別的提供者特定物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="fd34b-172">Provider-specific Object Identifier that defines this class.</span></span> <span data-ttu-id="fd34b-173">這是為了在需要類別的提供者特定 Oid 的目錄服務中，使用 Active Directory 來允許架構延伸。</span><span class="sxs-lookup"><span data-stu-id="fd34b-173">This is provided to allow schema extension, using Active Directory, in directory services that require provider-specific OIDs for classes.</span></span>

<dt>

<span data-ttu-id="fd34b-174">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd34b-174">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd34b-175">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="fd34b-175">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* pbstrOID
);
HRESULT put_OID(
  [in] BSTR bstrOID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd34b-176">**OptionalProperties**</span><span class="sxs-lookup"><span data-stu-id="fd34b-176">**OptionalProperties**</span></span>
<span data-ttu-id="fd34b-177"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd34b-177"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd34b-178">**VARIANT** 的 **SAFEARRAY** ，列出此架構類別的選擇性屬性。</span><span class="sxs-lookup"><span data-stu-id="fd34b-178">**SAFEARRAY** of **VARIANT** s that lists the optional properties for this schema class.</span></span> <span data-ttu-id="fd34b-179">如果類別只包含一個屬性，則 **get \_ OptionalProperties** 會傳回 **BSTR**。</span><span class="sxs-lookup"><span data-stu-id="fd34b-179">If the class only contains one property, then **get\_OptionalProperties** will return a **BSTR**.</span></span>

<dt>

<span data-ttu-id="fd34b-180">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd34b-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd34b-181">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="fd34b-181">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OptionalProperties(
  [out] VARIANT* pvarOptionalProperties
);
HRESULT put_OptionalProperties(
  [in] VARIANT varOptionalProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd34b-182">**PossibleSuperiors**</span><span class="sxs-lookup"><span data-stu-id="fd34b-182">**PossibleSuperiors**</span></span>
<span data-ttu-id="fd34b-183"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd34b-183"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd34b-184">ADsPath 字串的陣列，表示可以包含這個類別之實例的架構類別。</span><span class="sxs-lookup"><span data-stu-id="fd34b-184">Array of ADsPath strings that indicate the schema classes that can contain instances of this class.</span></span>

<dt>

<span data-ttu-id="fd34b-185">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd34b-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd34b-186">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="fd34b-186">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PossibleSuperiors(
  [out] VARIANT* pvSuperiors
);
HRESULT put_PossibleSuperiors(
  [in] VARIANT vSuperiors
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd34b-187">**PrimaryInterface**</span><span class="sxs-lookup"><span data-stu-id="fd34b-187">**PrimaryInterface**</span></span>
<span data-ttu-id="fd34b-188"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd34b-188"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd34b-189">選擇性的提供者特定識別碼 GUID，可將介面與此架構類別的物件產生關聯。</span><span class="sxs-lookup"><span data-stu-id="fd34b-189">Optional provider-specific identifier GUID that associates an interface to objects of this schema class.</span></span> <span data-ttu-id="fd34b-190">例如，支援 [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) 和 **PrimaryInterface** 的 "User" 類別是由 **IID \_ IADsUser** 所識別。</span><span class="sxs-lookup"><span data-stu-id="fd34b-190">For example, the "User" class that supports [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) and **PrimaryInterface** is identified by **IID\_IADsUser**.</span></span> <span data-ttu-id="fd34b-191">這必須是由 COM 定義的 GUID 標準字串格式。</span><span class="sxs-lookup"><span data-stu-id="fd34b-191">This must be in the standard string format of a GUID, as defined by COM.</span></span> <span data-ttu-id="fd34b-192">此 GUID 是在這個類別的實例中，出現在 [**IADs：： get \_ GUID**](/windows/desktop/api/Iads/nn-iads-iads) 屬性中的值，可供執行這個屬性的提供者。</span><span class="sxs-lookup"><span data-stu-id="fd34b-192">This GUID is the value that appears in the [**IADs::get\_GUID**](/windows/desktop/api/Iads/nn-iads-iads) property in instances of this class for providers that implement this property.</span></span> <span data-ttu-id="fd34b-193">依類別程式碼主要介面的 IID 來識別架構類別，可讓您在執行時間使用 **QueryInterface** 來判斷物件是否為所需的類別。</span><span class="sxs-lookup"><span data-stu-id="fd34b-193">Identifying a schema class by IID of the class code's primary interface enables the use of **QueryInterface** at run time to determine whether an object is of the desired class.</span></span>

<dt>

<span data-ttu-id="fd34b-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fd34b-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd34b-195">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="fd34b-195">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryInterface(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="fd34b-196">範例</span><span class="sxs-lookup"><span data-stu-id="fd34b-196">Examples</span></span>

<span data-ttu-id="fd34b-197">下列程式碼範例示範如何使用 [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) 介面判斷物件是否可以是容器，如果是，則會列出任何包含物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd34b-197">The following code example shows how to use the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface to determine if an object can be a container and, if so, lists the names of any contained objects.</span></span>


```VB
Dim ads As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set ads = GetObject("WinNT://myComputer,computer")
Set cls = GetObject(ads.Schema)
if cls.Container = True Then
    MsgBox "This object contains the following children:"
    For Each o In cls.Containment
        MsgBox o
    Next
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ads = Nothing
    Set cls = Nothing
```



<span data-ttu-id="fd34b-198">下列程式碼範例示範如何使用 [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) 介面判斷物件是否可以是容器，如果是，則會列出任何包含物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd34b-198">The following code example shows how to use the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface to determine if an object can be a container and, if so, lists the names of any contained objects.</span></span>


```C++
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs = NULL;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) {goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) {goto Cleanup;}
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) {goto Cleanup;}
 
VariantInit(&var);
VARIANT_BOOL bCont;
pCls->get_Container(&bCont);
if(bCont != false) {
    VariantClear(&var);
    pCls->get_Containment(&var);
    hr = printVarArray(var);
}

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    SysFreeString(bstrSchema);
    CoUninitialize();
```



## <a name="requirements"></a><span data-ttu-id="fd34b-199">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd34b-199">Requirements</span></span>



| <span data-ttu-id="fd34b-200">需求</span><span class="sxs-lookup"><span data-stu-id="fd34b-200">Requirement</span></span> | <span data-ttu-id="fd34b-201">值</span><span class="sxs-lookup"><span data-stu-id="fd34b-201">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd34b-202">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd34b-202">Minimum supported client</span></span><br/> | <span data-ttu-id="fd34b-203">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd34b-203">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd34b-204">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd34b-204">Minimum supported server</span></span><br/> | <span data-ttu-id="fd34b-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd34b-205">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd34b-206">標頭</span><span class="sxs-lookup"><span data-stu-id="fd34b-206">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd34b-207"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd34b-207"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="fd34b-208">DLL</span><span class="sxs-lookup"><span data-stu-id="fd34b-208">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd34b-209"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd34b-209"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="fd34b-210">IID</span><span class="sxs-lookup"><span data-stu-id="fd34b-210">IID</span></span><br/>                      | <span data-ttu-id="fd34b-211">IID \_ 得到 iadsclass 定義為 C8F93DD0-4AE0-11CF-9E73-00AA004A5691</span><span class="sxs-lookup"><span data-stu-id="fd34b-211">IID\_IADsClass is defined as C8F93DD0-4AE0-11CF-9E73-00AA004A5691</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="fd34b-212">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd34b-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd34b-213">**得到 iadsclass**</span><span class="sxs-lookup"><span data-stu-id="fd34b-213">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="fd34b-214">**得到 iadsclass：：限定詞**</span><span class="sxs-lookup"><span data-stu-id="fd34b-214">**IADsClass::Qualifiers**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers)
</dt> </dl>

 

 






---
title: 'IADsOU 屬性方法 (Iads .h) '
description: IADsOU 介面的屬性方法會取得或設定下表所列的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 8cb84972-733b-47ca-8647-1b7a85c97021
ms.tgt_platform: multiple
keywords:
- IADsOU 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsOU Property Methods
- IADsOU.BusinessCategory
- IADsOU.get_BusinessCategory
- IADsOU.put_BusinessCategory
- IADsOU.Description
- IADsOU.get_Description
- IADsOU.put_Description
- IADsOU.FaxNumber
- IADsOU.get_FaxNumber
- IADsOU.put_FaxNumber
- IADsOU.LocalityName
- IADsOU.get_LocalityName
- IADsOU.put_LocalityName
- IADsOU.PostalAddress
- IADsOU.get_PostalAddress
- IADsOU.put_PostalAddress
- IADsOU.TelephoneNumber
- IADsOU.get_TelephoneNumber
- IADsOU.put_TelephoneNumber
- IADsOU.SeeAlso
- IADsOU.get_SeeAlso
- IADsOU.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0ce30fad6a690a26a8e16b817b77b129dee25f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001302"
---
# <a name="iadsou-property-methods"></a><span data-ttu-id="7a78d-105">IADsOU 屬性方法</span><span class="sxs-lookup"><span data-stu-id="7a78d-105">IADsOU Property Methods</span></span>

<span data-ttu-id="7a78d-106">[**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou)介面的屬性方法會取得或設定下表所列的屬性。</span><span class="sxs-lookup"><span data-stu-id="7a78d-106">The property methods of the [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou) interface get or set the properties listed in the following table.</span></span> <span data-ttu-id="7a78d-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="7a78d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="7a78d-108">屬性</span><span class="sxs-lookup"><span data-stu-id="7a78d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="7a78d-109">**BusinessCategory**</span><span class="sxs-lookup"><span data-stu-id="7a78d-109">**BusinessCategory**</span></span>
<span data-ttu-id="7a78d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7a78d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="7a78d-111">包含一般商務函式或組織單位所執行之函式的字串，例如「會計」。</span><span class="sxs-lookup"><span data-stu-id="7a78d-111">A string that contains the general business function or functions performed by the organizational unit, for example "Accounting".</span></span>

<dt>

<span data-ttu-id="7a78d-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7a78d-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7a78d-113">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7a78d-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BusinessCategory(
  [out] BSTR* pbstrBusinessCategory
);
HRESULT put_BusinessCategory(
  [in] BSTR bstrBusinessCategory
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a78d-114">**說明**</span><span class="sxs-lookup"><span data-stu-id="7a78d-114">**Description**</span></span>
<span data-ttu-id="7a78d-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7a78d-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="7a78d-116">字串，其中包含組織單位的文字描述。</span><span class="sxs-lookup"><span data-stu-id="7a78d-116">A string that contains a textual description of the organizational unit.</span></span>

<dt>

<span data-ttu-id="7a78d-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7a78d-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7a78d-118">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7a78d-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a78d-119">**FaxNumber**</span><span class="sxs-lookup"><span data-stu-id="7a78d-119">**FaxNumber**</span></span>
<span data-ttu-id="7a78d-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7a78d-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="7a78d-121">字串，其中包含組織單位的傳真號碼。</span><span class="sxs-lookup"><span data-stu-id="7a78d-121">A string that contains the facsimile number of the organizational unit.</span></span>

<dt>

<span data-ttu-id="7a78d-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7a78d-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7a78d-123">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7a78d-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_FaxNumber(
  [out] BSTR* pbstrFaxNumber
);
HRESULT put_FaxNumber(
  [in] BSTR bstrFaxNumber
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a78d-124">**LocalityName**</span><span class="sxs-lookup"><span data-stu-id="7a78d-124">**LocalityName**</span></span>
<span data-ttu-id="7a78d-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7a78d-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="7a78d-126">包含組織單位地理區功能變數名稱稱的字串。</span><span class="sxs-lookup"><span data-stu-id="7a78d-126">A string that contains the name of the geographic region of the organizational unit.</span></span>

<dt>

<span data-ttu-id="7a78d-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7a78d-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7a78d-128">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7a78d-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LocalityName(
  [out] BSTR* pbstrLocalityName
);
HRESULT put_LocalityName(
  [in] BSTR bstrLocalityName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a78d-129">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="7a78d-129">**PostalAddress**</span></span>
<span data-ttu-id="7a78d-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7a78d-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="7a78d-131">包含組織單位郵件標籤的字串。</span><span class="sxs-lookup"><span data-stu-id="7a78d-131">A string that contains the postal address of the organizational unit.</span></span>

<dt>

<span data-ttu-id="7a78d-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7a78d-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7a78d-133">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7a78d-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] BSTR* pbstrPostalAddress
);
HRESULT put_PostalAddress(
  [in] BSTR bstrPostalAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a78d-134">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="7a78d-134">**SeeAlso**</span></span>
<span data-ttu-id="7a78d-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7a78d-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="7a78d-136">字串陣列，其中包含可能與這個物件相關的其他目錄物件的辨別名稱。</span><span class="sxs-lookup"><span data-stu-id="7a78d-136">An array of strings that contains the distinguished names of other directory objects which may be relevant to this object.</span></span>

<dt>

<span data-ttu-id="7a78d-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7a78d-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7a78d-138">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="7a78d-138">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SeeAlso(
  [out] VARIANT* pvSeeAlso
);
HRESULT put_SeeAlso(
  [in] VARIANT vSeeAlso
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a78d-139">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="7a78d-139">**TelephoneNumber**</span></span>
<span data-ttu-id="7a78d-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7a78d-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="7a78d-141">字串，其中包含組織單位的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="7a78d-141">A string that contains the telephone number of the organizational unit.</span></span>

<dt>

<span data-ttu-id="7a78d-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7a78d-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7a78d-143">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7a78d-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* pbstrTelephoneNumber
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="7a78d-144">範例</span><span class="sxs-lookup"><span data-stu-id="7a78d-144">Examples</span></span>

<span data-ttu-id="7a78d-145">下列程式碼範例會顯示容器中所有組織單位的 **BusinessCategory** 和 **描述** 。</span><span class="sxs-lookup"><span data-stu-id="7a78d-145">The following code example displays the **BusinessCategory** and **Description** of all organization units in a container.</span></span> <span data-ttu-id="7a78d-146">它會假設基礎目錄服務支援依組織單位來分組目錄物件。</span><span class="sxs-lookup"><span data-stu-id="7a78d-146">It assumes that the underlying directory service supports grouping of directory objects by organization unit.</span></span>


```VB
Dim dom As IADsContainer
Dim ou As IADsOU

' Bind to the container.
Set dom = GetObject("LDAP://server1/domain1")

' Filter out all objects that are not of class "organizationalUnit".
dom.filter = Array("organizationalUnit")

' Enumerate the organizational units in the container and display  
' the BusinessCategory and Description properties of each OU.
For Each ou In dom
    MsgBox ou.BusinessCategory & ": " & ou.Description
Next
```



## <a name="requirements"></a><span data-ttu-id="7a78d-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a78d-147">Requirements</span></span>



| <span data-ttu-id="7a78d-148">需求</span><span class="sxs-lookup"><span data-stu-id="7a78d-148">Requirement</span></span> | <span data-ttu-id="7a78d-149">值</span><span class="sxs-lookup"><span data-stu-id="7a78d-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a78d-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a78d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="7a78d-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a78d-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a78d-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a78d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="7a78d-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a78d-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a78d-154">標頭</span><span class="sxs-lookup"><span data-stu-id="7a78d-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a78d-155"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="7a78d-155"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="7a78d-156">DLL</span><span class="sxs-lookup"><span data-stu-id="7a78d-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a78d-157"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a78d-157"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a78d-158">IID</span><span class="sxs-lookup"><span data-stu-id="7a78d-158">IID</span></span><br/>                      | <span data-ttu-id="7a78d-159">IID \_ IADsOU 定義為 A2F733B8-EFFE-11CF-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="7a78d-159">IID\_IADsOU is defined as A2F733B8-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="7a78d-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a78d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a78d-161">**IADsOU**</span><span class="sxs-lookup"><span data-stu-id="7a78d-161">**IADsOU**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsou)
</dt> <dt>

[<span data-ttu-id="7a78d-162">介面屬性方法</span><span class="sxs-lookup"><span data-stu-id="7a78d-162">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 






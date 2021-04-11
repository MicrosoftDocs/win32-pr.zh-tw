---
title: 'IADsO 屬性方法 (Iads .h) '
description: IADsO 介面的屬性方法會取得或設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: d4bc1d29-98de-462d-b59c-2bc2641c25a0
ms.tgt_platform: multiple
keywords:
- IADsO 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsO Property Methods
- IADsO.Description
- IADsO.get_Description
- IADsO.put_Description
- IADsO.FaxNumber
- IADsO.get_FaxNumber
- IADsO.put_FaxNumber
- IADsO.LocalityName
- IADsO.get_LocalityName
- IADsO.put_LocalityName
- IADsO.PostalAddress
- IADsO.get_PostalAddress
- IADsO.put_PostalAddress
- IADsO.TelephoneNumber
- IADsO.get_TelephoneNumber
- IADsO.put_TelephoneNumber
- IADsO.SeeAlso
- IADsO.get_SeeAlso
- IADsO.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09840cf62d6883eb4f5ca326998b697a34698c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686204"
---
# <a name="iadso-property-methods"></a><span data-ttu-id="416c6-105">IADsO 屬性方法</span><span class="sxs-lookup"><span data-stu-id="416c6-105">IADsO Property Methods</span></span>

<span data-ttu-id="416c6-106">[**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso)介面的屬性方法會取得或設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="416c6-106">The property methods of the [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="416c6-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="416c6-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="416c6-108">屬性</span><span class="sxs-lookup"><span data-stu-id="416c6-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="416c6-109">**說明**</span><span class="sxs-lookup"><span data-stu-id="416c6-109">**Description**</span></span>
<span data-ttu-id="416c6-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="416c6-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="416c6-111">組織的描述。</span><span class="sxs-lookup"><span data-stu-id="416c6-111">The description of the organization.</span></span>

<dt>

<span data-ttu-id="416c6-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="416c6-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="416c6-113">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="416c6-113">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="416c6-114">**FaxNumber**</span><span class="sxs-lookup"><span data-stu-id="416c6-114">**FaxNumber**</span></span>
<span data-ttu-id="416c6-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="416c6-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="416c6-116">傳真 (傳真) 號碼。</span><span class="sxs-lookup"><span data-stu-id="416c6-116">The facsimile (fax) number of the organization.</span></span>

<dt>

<span data-ttu-id="416c6-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="416c6-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="416c6-118">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="416c6-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="416c6-119">**LocalityName**</span><span class="sxs-lookup"><span data-stu-id="416c6-119">**LocalityName**</span></span>
<span data-ttu-id="416c6-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="416c6-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="416c6-121">組織所在的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="416c6-121">The name of the place in which the organization is located.</span></span>

<dt>

<span data-ttu-id="416c6-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="416c6-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="416c6-123">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="416c6-123">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="416c6-124">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="416c6-124">**PostalAddress**</span></span>
<span data-ttu-id="416c6-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="416c6-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="416c6-126">組織的郵政位址。</span><span class="sxs-lookup"><span data-stu-id="416c6-126">The postal address of the organization.</span></span>

<dt>

<span data-ttu-id="416c6-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="416c6-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="416c6-128">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="416c6-128">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="416c6-129">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="416c6-129">**SeeAlso**</span></span>
<span data-ttu-id="416c6-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="416c6-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="416c6-131">其他 ADSI 物件的 ADsPath 名稱陣列，這些物件可能與這個物件相關。</span><span class="sxs-lookup"><span data-stu-id="416c6-131">An array of ADsPath names of other ADSI objects which may be relevant to this object.</span></span>

<dt>

<span data-ttu-id="416c6-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="416c6-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="416c6-133">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="416c6-133">Scripting data type: **VARIANT**</span></span>
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

<span data-ttu-id="416c6-134">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="416c6-134">**TelephoneNumber**</span></span>
<span data-ttu-id="416c6-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="416c6-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="416c6-136">組織的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="416c6-136">The telephone number of the organization.</span></span>

<dt>

<span data-ttu-id="416c6-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="416c6-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="416c6-138">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="416c6-138">Scripting data type: **BSTR**</span></span>
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

 

## <a name="examples"></a><span data-ttu-id="416c6-139">範例</span><span class="sxs-lookup"><span data-stu-id="416c6-139">Examples</span></span>

<span data-ttu-id="416c6-140">下列程式碼範例會顯示指定組織的描述。</span><span class="sxs-lookup"><span data-stu-id="416c6-140">The following code example displays the description of a given organization.</span></span> <span data-ttu-id="416c6-141">它會假設基礎目錄服務支援依組織群組目錄物件。</span><span class="sxs-lookup"><span data-stu-id="416c6-141">It assumes the underlying directory service supports grouping directory objects by organization.</span></span>


```VB
Dim dom As IADsContainer
Dim dso As IADsOpenDSObject
Dim szUsername As String
Dim szPassword As String
On Error GoTo Cleanup

' Insert code to securely retrieve the user name and password
 
Set dso = GetObject("LDAP:")
Set dom = dso.OpenDSObject("LDAP://adsrv1/dc=Fabrikam, dc=Com", _
                           szUsername, szPassword,1)
dom.Filter = Array("organization")
For Each o In dom
    MsgBox "Fax number of " & o.Name & " : " & o.Description
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set dom = Nothing
    Set dso = Nothing
```



## <a name="requirements"></a><span data-ttu-id="416c6-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="416c6-142">Requirements</span></span>



| <span data-ttu-id="416c6-143">需求</span><span class="sxs-lookup"><span data-stu-id="416c6-143">Requirement</span></span> | <span data-ttu-id="416c6-144">值</span><span class="sxs-lookup"><span data-stu-id="416c6-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="416c6-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="416c6-145">Minimum supported client</span></span><br/> | <span data-ttu-id="416c6-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="416c6-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="416c6-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="416c6-147">Minimum supported server</span></span><br/> | <span data-ttu-id="416c6-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="416c6-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="416c6-149">標頭</span><span class="sxs-lookup"><span data-stu-id="416c6-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="416c6-150"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="416c6-150"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="416c6-151">DLL</span><span class="sxs-lookup"><span data-stu-id="416c6-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="416c6-152"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="416c6-152"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="416c6-153">IID</span><span class="sxs-lookup"><span data-stu-id="416c6-153">IID</span></span><br/>                      | <span data-ttu-id="416c6-154">IID \_ IADsO 定義為 A1CD2DC6-EFFE-11CF-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="416c6-154">IID\_IADsO is defined as A1CD2DC6-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="416c6-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="416c6-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="416c6-156">**IADsO**</span><span class="sxs-lookup"><span data-stu-id="416c6-156">**IADsO**</span></span>](/windows/desktop/api/Iads/nn-iads-iadso)
</dt> <dt>

[<span data-ttu-id="416c6-157">介面屬性方法</span><span class="sxs-lookup"><span data-stu-id="416c6-157">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 






---
title: 'IADsPropertyEntry 屬性方法 (Iads .h) '
description: 提供下列屬性的存取權。
ms.assetid: 73b0f6d4-55db-46cf-a781-e10bc4fcf2db
ms.tgt_platform: multiple
keywords:
- IADsPropertyEntry 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsPropertyEntry Property Methods
- IADsPropertyEntry.Name
- IADsPropertyEntry.get_Name
- IADsPropertyEntry.put_Name
- IADsPropertyEntry.ADsType
- IADsPropertyEntry.get_ADsType
- IADsPropertyEntry.put_ADsType
- IADsPropertyEntry.ControlCode
- IADsPropertyEntry.get_ControlCode
- IADsPropertyEntry.put_ControlCode
- IADsPropertyEntry.Values
- IADsPropertyEntry.get_Values
- IADsPropertyEntry.put_Values
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e82344b2b659395bb14c0500fde3214530e000
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844292"
---
# <a name="iadspropertyentry-property-methods"></a><span data-ttu-id="9d560-104">IADsPropertyEntry 屬性方法</span><span class="sxs-lookup"><span data-stu-id="9d560-104">IADsPropertyEntry Property Methods</span></span>

<span data-ttu-id="9d560-105">[**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)介面的屬性方法會提供下列屬性的存取權。</span><span class="sxs-lookup"><span data-stu-id="9d560-105">The property methods of the [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) interface provide access to the following properties.</span></span> <span data-ttu-id="9d560-106">如需屬性方法的詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="9d560-106">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="9d560-107">屬性</span><span class="sxs-lookup"><span data-stu-id="9d560-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="9d560-108">**ADsType**</span><span class="sxs-lookup"><span data-stu-id="9d560-108">**ADsType**</span></span>
<span data-ttu-id="9d560-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9d560-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="9d560-110">**Name** 屬性的資料類型。</span><span class="sxs-lookup"><span data-stu-id="9d560-110">The data type of the **Name** property.</span></span> <span data-ttu-id="9d560-111">資料類型的值定義于 [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) 列舉中。</span><span class="sxs-lookup"><span data-stu-id="9d560-111">The values of the data type is defined in the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) enumeration.</span></span>

<dt>

<span data-ttu-id="9d560-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9d560-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9d560-113">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="9d560-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsType(
  [out] LONG* plADsType
);
HRESULT put_ADsType(
  [in] LONG lADsType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="9d560-114">**ControlCode**</span><span class="sxs-lookup"><span data-stu-id="9d560-114">**ControlCode**</span></span>
<span data-ttu-id="9d560-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9d560-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="9d560-116">常數，指定要在已命名屬性上執行的作業。</span><span class="sxs-lookup"><span data-stu-id="9d560-116">A constant that specifies the operation to be performed on the named property.</span></span> <span data-ttu-id="9d560-117">此值定義于 [**ADS \_ 屬性 \_ 運算 \_**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) 列舉列舉中。</span><span class="sxs-lookup"><span data-stu-id="9d560-117">The value is defined in the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration.</span></span>

<dt>

<span data-ttu-id="9d560-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9d560-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9d560-119">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="9d560-119">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ControlCode(
  [out] LONG* pControlCode
);
HRESULT put_ControlCode(
  [in] LONG lnControlCode
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="9d560-120">**名稱**</span><span class="sxs-lookup"><span data-stu-id="9d560-120">**Name**</span></span>
<span data-ttu-id="9d560-121"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9d560-121"></dt> <dd> <dl></span></span>

<span data-ttu-id="9d560-122">屬性專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d560-122">Name of the property entry.</span></span> <span data-ttu-id="9d560-123">這個名稱應該與架構中定義的屬性名稱相對應。</span><span class="sxs-lookup"><span data-stu-id="9d560-123">This name should correspond to the name of an attribute as defined in the schema.</span></span>

<dt>

<span data-ttu-id="9d560-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9d560-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9d560-125">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9d560-125">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
HRESULT put_Name(
  [in] BSTR bstrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="9d560-126">**值**</span><span class="sxs-lookup"><span data-stu-id="9d560-126">**Values**</span></span>
<span data-ttu-id="9d560-127"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9d560-127"></dt> <dd> <dl></span></span>

<span data-ttu-id="9d560-128">**VARIANT** 陣列。</span><span class="sxs-lookup"><span data-stu-id="9d560-128">A **VARIANT** array.</span></span> <span data-ttu-id="9d560-129">這個陣列中的每個元素都代表一個命名屬性的值。</span><span class="sxs-lookup"><span data-stu-id="9d560-129">Each element in this array represents a value of the named property.</span></span> <span data-ttu-id="9d560-130">這類屬性值是由執行 [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) 和 [**IADSPROPERTYVALUE2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) 介面的 ADSI 物件表示。</span><span class="sxs-lookup"><span data-stu-id="9d560-130">Such property values are represented by ADSI objects implementing the [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) and [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) interfaces.</span></span> <span data-ttu-id="9d560-131">因此， **VARIANT** 陣列會在執行 **IADsPropertyValue** 和 **IADsPropertyValue2** 介面的 ADSI 物件上，保存 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="9d560-131">Therefore, the **VARIANT** array holds an array of pointers to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface on the ADSI objects implementing the **IADsPropertyValue** and **IADsPropertyValue2** interfaces.</span></span>

<dt>

<span data-ttu-id="9d560-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9d560-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9d560-133">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="9d560-133">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Values(
  [out] VARIANT* pvValues
);
HRESULT put_Values(
  [in] VARIANT vValues
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="9d560-134">備註</span><span class="sxs-lookup"><span data-stu-id="9d560-134">Remarks</span></span>

<span data-ttu-id="9d560-135">每個屬性方法都支援標準 **HRESULT** 傳回值，包括 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="9d560-135">Each property method supports the standard **HRESULT** return values, including S\_OK.</span></span> <span data-ttu-id="9d560-136">如需其他傳回值的詳細資訊，請參閱 [ADSI 錯誤碼](adsi-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="9d560-136">For more information about other return values, see [ADSI Error Codes](adsi-error-codes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9d560-137">範例</span><span class="sxs-lookup"><span data-stu-id="9d560-137">Examples</span></span>

<span data-ttu-id="9d560-138">下列程式碼範例示範如何從快取中取出指名的屬性，並建立新的屬性專案。</span><span class="sxs-lookup"><span data-stu-id="9d560-138">The following code example shows how to retrieve a named property from the cache and create a new property entry.</span></span>


```VB
 
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup

'------------------------------------------------------------
'----- Getting IADsPropertyEntry ----------------------------
'------------------------------------------------------------
 
' Create the property list object.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Get a named property entry object.
Set propEntry = propList.GetPropertyItem("dc", ADSTYPE_CASE_IGNORE_STRING)

' Insert code to do something with propEntry
Set propEntry = Nothing
 
'------------------------------------------------------------
'---- Setting IADsPropertyEntry -----------------------------
'------------------------------------------------------------
 
' Create a property value object.
Set propVal = New PropertyValue
 
'---- Property Value -----
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
 
'---- Create a new Property Entry ----
Set propEntry = New PropertyEntry
propEntry.Name = "adminDescription"
propEntry.Values = Array(propVal)
propEntry.ControlCode = ADS_PROPERTY_UPDATE
propEntry.ADsType = ADS_CASE_IGNORE_STRING
 
' ---- Put the newly created property entry to the cache ----
propList.PutPropertyItem (propEntry)
 
' Commit the entry to the directory store.
propList.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```



<span data-ttu-id="9d560-139">下列程式碼範例示範如何從快取取得命名屬性。</span><span class="sxs-lookup"><span data-stu-id="9d560-139">The following code example shows how to get a named property from a cache.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADs *pObj = NULL;
VARIANT var;
long valType = ADSTYPE_CASE_IGNORE_STRING;
 
VariantInit(&var);
 
// Bind to directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);
if(FAILED(hr)){return;}
 
// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
pObj->GetInfo();
pObj->Release();
 
// Get a property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), valType, &var);
pList->Release();
if(FAILED(hr)){goto Cleanup;}
hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
VariantClear(&var);
if(FAILED(hr)){goto Cleanup;}
 
// Get the name and the type of the property entry.
BSTR nm = NULL;
hr = pEntry->get_Name(&nm);
printf("Property name = %S\n",nm);
VariantClear(&var);
long at;
hr = pEntry->get_ADsType(&at);
printf("Property type = %d\n",a);

Cleanup:
    if(nm)
        SysFreeString(nm);

    if(pList)
        pList->Release();

    if(pEntry)
        pEntry->Release();

    if(pObj)
        pObj->Release();

    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="9d560-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d560-140">Requirements</span></span>



| <span data-ttu-id="9d560-141">需求</span><span class="sxs-lookup"><span data-stu-id="9d560-141">Requirement</span></span> | <span data-ttu-id="9d560-142">值</span><span class="sxs-lookup"><span data-stu-id="9d560-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d560-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d560-143">Minimum supported client</span></span><br/> | <span data-ttu-id="9d560-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d560-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9d560-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d560-145">Minimum supported server</span></span><br/> | <span data-ttu-id="9d560-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d560-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9d560-147">標頭</span><span class="sxs-lookup"><span data-stu-id="9d560-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d560-148"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="9d560-148"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="9d560-149">DLL</span><span class="sxs-lookup"><span data-stu-id="9d560-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d560-150"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d560-150"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="9d560-151">IID</span><span class="sxs-lookup"><span data-stu-id="9d560-151">IID</span></span><br/>                      | <span data-ttu-id="9d560-152">IID \_ IADsPropertyEntry 定義為05792C8E-941F-11D0-8529-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="9d560-152">IID\_IADsPropertyEntry is defined as 05792C8E-941F-11D0-8529-00C04FD8D503</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="9d560-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d560-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d560-154">**ADS \_ 屬性 \_ 運算 \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="9d560-154">**ADS\_PROPERTY\_OPERATION\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_property_operation_enum)
</dt> <dt>

[<span data-ttu-id="9d560-155">ADSI 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="9d560-155">ADSI Error Codes</span></span>](adsi-error-codes.md)
</dt> <dt>

[<span data-ttu-id="9d560-156">**ADSTYPEENUM**</span><span class="sxs-lookup"><span data-stu-id="9d560-156">**ADSTYPEENUM**</span></span>](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[<span data-ttu-id="9d560-157">**IADsPropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="9d560-157">**IADsPropertyEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[<span data-ttu-id="9d560-158">**IADsPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="9d560-158">**IADsPropertyValue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[<span data-ttu-id="9d560-159">**IADsPropertyValue2**</span><span class="sxs-lookup"><span data-stu-id="9d560-159">**IADsPropertyValue2**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[<span data-ttu-id="9d560-160">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="9d560-160">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 


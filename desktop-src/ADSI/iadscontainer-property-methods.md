---
title: 'IADsContainer 屬性方法 (Iads .h) '
description: IADsContainer 介面的屬性方法會取得或設定下表所述的屬性。 如需詳細資訊，以及有關屬性方法的一般討論，請參閱介面屬性方法。
ms.assetid: 74d348bf-7b7f-4971-ba03-f77940600674
ms.tgt_platform: multiple
keywords:
- IADsContainer 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsContainer Property Methods
- IADsContainer.Count
- IADsContainer.get_Count
- IADsContainer.Filter
- IADsContainer.get_Filter
- IADsContainer.put_Filter
- IADsContainer.Hints
- IADsContainer.get_Hints
- IADsContainer.put_Hints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5196addda0d9ff89f8a4976f3197bbeeae07044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105150"
---
# <a name="iadscontainer-property-methods"></a><span data-ttu-id="cccde-105">IADsContainer 屬性方法</span><span class="sxs-lookup"><span data-stu-id="cccde-105">IADsContainer Property Methods</span></span>

<span data-ttu-id="cccde-106">[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)介面的屬性方法會取得或設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="cccde-106">The property methods of the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="cccde-107">如需詳細資訊，以及有關屬性方法的一般討論，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="cccde-107">For more information, and a general discussion about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="cccde-108">屬性</span><span class="sxs-lookup"><span data-stu-id="cccde-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="cccde-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="cccde-109">**Count**</span></span>
<span data-ttu-id="cccde-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cccde-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="cccde-111">捕獲容器中的專案數。</span><span class="sxs-lookup"><span data-stu-id="cccde-111">Retrieves the number of items in the container.</span></span> <span data-ttu-id="cccde-112">當設定 **篩選準則** 時， **Count** 只會傳回篩選的專案數目。</span><span class="sxs-lookup"><span data-stu-id="cccde-112">When **Filter** is set, **Count** returns only the number of filtered items.</span></span>

<dt>

<span data-ttu-id="cccde-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cccde-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cccde-114">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="cccde-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cccde-115">**Filter**</span><span class="sxs-lookup"><span data-stu-id="cccde-115">**Filter**</span></span>
<span data-ttu-id="cccde-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cccde-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="cccde-117">抓取或設定篩選準則，用來選取指定列舉中的物件類別。</span><span class="sxs-lookup"><span data-stu-id="cccde-117">Retrieves or sets the filter used to select object classes in a given enumeration.</span></span> <span data-ttu-id="cccde-118">這是 variant 陣列，其中的每個元素都是架構類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="cccde-118">This is a variant array, each element of which is the name of a schema class.</span></span> <span data-ttu-id="cccde-119">如果 **篩選** 未設定或設為空白，則列舉值會抓取所有類別的所有物件。</span><span class="sxs-lookup"><span data-stu-id="cccde-119">If **Filter** is not set or set to empty, all objects of all classes are retrieved by the enumerator.</span></span>

<dt>

<span data-ttu-id="cccde-120">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cccde-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cccde-121">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="cccde-121">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cccde-122">**提示**</span><span class="sxs-lookup"><span data-stu-id="cccde-122">**Hints**</span></span>
<span data-ttu-id="cccde-123"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cccde-123"></dt> <dd> <dl></span></span>

<span data-ttu-id="cccde-124">**BSTR** 字串的 variant 陣列。</span><span class="sxs-lookup"><span data-stu-id="cccde-124">A variant array of **BSTR** strings.</span></span> <span data-ttu-id="cccde-125">每個元素都會識別在架構定義中找到的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="cccde-125">Each element identifies the name of a property found in the schema definition.</span></span> <span data-ttu-id="cccde-126">*VHints* 參數可讓用戶端指定要為每個列舉物件載入哪些屬性。</span><span class="sxs-lookup"><span data-stu-id="cccde-126">The *vHints* parameter enables the client to indicate which attributes to load for each enumerated object.</span></span> <span data-ttu-id="cccde-127">您可以使用這類資料來優化網路存取。</span><span class="sxs-lookup"><span data-stu-id="cccde-127">Such data may be used to optimize network access.</span></span> <span data-ttu-id="cccde-128">但是，確切的實作為提供者特有的，而且目前不是由 WinNT 提供者所使用。</span><span class="sxs-lookup"><span data-stu-id="cccde-128">The exact implementation, however, is provider-specific, and is currently not used by the WinNT provider.</span></span>

<dt>

<span data-ttu-id="cccde-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cccde-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cccde-130">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="cccde-130">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Hints(
  [out] VARIANT* pvHints
);
HRESULT put_Hints(
  [in] VARIANT vHints
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="cccde-131">備註</span><span class="sxs-lookup"><span data-stu-id="cccde-131">Remarks</span></span>

<span data-ttu-id="cccde-132">[**IADsContainer：： get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum)和 **IADsContainer：： get \_ Count** 下的列舉進程會針對快取中的包含物件執行。</span><span class="sxs-lookup"><span data-stu-id="cccde-132">The enumeration processes under [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) and **IADsContainer::get\_Count** are performed against the contained objects in the cache.</span></span> <span data-ttu-id="cccde-133">當容器包含大量物件時，效能可能會受到影響。</span><span class="sxs-lookup"><span data-stu-id="cccde-133">When a container contains a large number of objects, the performance may be affected.</span></span> <span data-ttu-id="cccde-134">若要增強效能，請關閉快取、設定適當的頁面大小，然後使用 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面。</span><span class="sxs-lookup"><span data-stu-id="cccde-134">To enhance performance, turn off the cache, set up an appropriate page size, and use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span> <span data-ttu-id="cccde-135">基於這個理由，Microsoft LDAP 提供者不支援 **get \_ Count** 屬性。</span><span class="sxs-lookup"><span data-stu-id="cccde-135">For this reason, the **get\_Count** property is not supported in the Microsoft LDAP provider.</span></span>

## <a name="examples"></a><span data-ttu-id="cccde-136">範例</span><span class="sxs-lookup"><span data-stu-id="cccde-136">Examples</span></span>

<span data-ttu-id="cccde-137">下列 Visual Basic 程式碼範例會示範如何使用 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 的屬性方法。</span><span class="sxs-lookup"><span data-stu-id="cccde-137">The following Visual Basic code example shows how property methods of [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) can be used.</span></span>


```VB
Dim cont As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup
 
Set cont = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
cont.Hints = Array("adminDescription") ' Load this attribute. Optional.
Debug.Print cont.Get("adminDescription")

' Filter users.
cont.Filter = Array("user")

For Each usr In cont
  Debug.Print usr.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set usr = Nothing
```



<span data-ttu-id="cccde-138">下列 c + + 程式碼範例會顯示如何使用 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 的屬性方法。</span><span class="sxs-lookup"><span data-stu-id="cccde-138">The following C++ code example shows how the property methods of [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) can be used.</span></span> <span data-ttu-id="cccde-139">為了簡潔起見，會忽略錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="cccde-139">For brevity, error checking is omitted.</span></span>


```C++
IADsContainer *pCont;
IADs *pChild;
IADs *pADs;
 
HRESULT hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=COM",
                          IID_IADsContainer, 
                          (void**)&pCont);

if(FAILED(hr)){goto Cleanup;}

LPWSTR pszArray[] = { L"adminDescription" };
DWORD dwNumber = sizeof(pszArray)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr( pszArray, dwNumber, &var);
if(FAILED(hr)){goto Cleanup;}

hr = pCont->put_Hints( var );
if(FAILED(hr)){goto Cleanup;}

VariantClear(&var);
 
hr = pCont->QueryInterface(IID_IADs, (void**)pADs);
if(FAILED(hr)){goto Cleanup;}
 
hr = pADs->Get(CComBSTR("adminDescription"), var);
 
LPWSTR pszUsers = {L"user"};
dwNumber = sizeof(pszUsers)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr(pszUsers, dwNumber, &var);
hr = pCont->put_Filter( var );
VariantClear(&var);
 
// Enumerate user objects in the container.
IEnumVARIANT *pEnum = NULL;
hr = ADsBuildEnumerator(pCont, &pEnum);
pCont->Release();    // Not required when users are enumerated.
 
ULONG lFetch;
VariantClear(&var);
while (SUCCEEDED(ADsEnumerateNext(pEnum, 1, &var, &lFetch)) && 
                      lFetch==1) {
    hr = V_DISPATCH(&var)->QueryInterface(IID_IADs, (void**)&pChild)
    if(SUCCEEDED(hr)) {
        BSTR bstrName;
        pChild->get_Name(&bstrName);
        printf("  %S\n", bstrName);
        SysFreeString(bstrName);
        pChild->Release();
    }
    VariantClear(&var);
}
Cleanup:
    if(pADs)
        pADs->Release();

    if(pCont)
        pCont->Release();

    if(pChild)
        pChild->Release();

    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="cccde-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="cccde-140">Requirements</span></span>



| <span data-ttu-id="cccde-141">需求</span><span class="sxs-lookup"><span data-stu-id="cccde-141">Requirement</span></span> | <span data-ttu-id="cccde-142">值</span><span class="sxs-lookup"><span data-stu-id="cccde-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cccde-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cccde-143">Minimum supported client</span></span><br/> | <span data-ttu-id="cccde-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cccde-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cccde-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cccde-145">Minimum supported server</span></span><br/> | <span data-ttu-id="cccde-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cccde-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cccde-147">標頭</span><span class="sxs-lookup"><span data-stu-id="cccde-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="cccde-148"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="cccde-148"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="cccde-149">DLL</span><span class="sxs-lookup"><span data-stu-id="cccde-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cccde-150"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cccde-150"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="cccde-151">IID</span><span class="sxs-lookup"><span data-stu-id="cccde-151">IID</span></span><br/>                      | <span data-ttu-id="cccde-152">IID \_ IADsContainer 定義為001677D0-FD16-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="cccde-152">IID\_IADsContainer is defined as 001677D0-FD16-11CE-ABC4-02608C9E7553</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="cccde-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cccde-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cccde-154">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="cccde-154">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[<span data-ttu-id="cccde-155">**>idirectorysearch**</span><span class="sxs-lookup"><span data-stu-id="cccde-155">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
</dt> </dl>

 

 






---
title: 'IADsAccessControlEntry 屬性方法 (Iads .h) '
description: IADsAccessControlEntry 介面的屬性方法會取得或設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: dce11723-0e30-4baa-8666-0a32f0968ebb
ms.tgt_platform: multiple
keywords:
- IADsAccessControlEntry 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsAccessControlEntry Property Methods
- IADsAccessControlEntry.AccessMask
- IADsAccessControlEntry.get_AccessMask
- IADsAccessControlEntry.put_AccessMask
- IADsAccessControlEntry.AceType
- IADsAccessControlEntry.get_AceType
- IADsAccessControlEntry.put_AceType
- IADsAccessControlEntry.AceFlags
- IADsAccessControlEntry.get_AceFlags
- IADsAccessControlEntry.put_AceFlags
- IADsAccessControlEntry.Flags
- IADsAccessControlEntry.get_Flags
- IADsAccessControlEntry.put_Flags
- IADsAccessControlEntry.ObjectType
- IADsAccessControlEntry.get_ObjectType
- IADsAccessControlEntry.put_ObjectType
- IADsAccessControlEntry.InheritedObjectType
- IADsAccessControlEntry.get_InheritedObjectType
- IADsAccessControlEntry.put_InheritedObjectType
- IADsAccessControlEntry.Trustee
- IADsAccessControlEntry.get_Trustee
- IADsAccessControlEntry.put_Trustee
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8539807f21944ab6f4b2c03f04b14a53dffdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685664"
---
# <a name="iadsaccesscontrolentry-property-methods"></a><span data-ttu-id="36612-105">IADsAccessControlEntry 屬性方法</span><span class="sxs-lookup"><span data-stu-id="36612-105">IADsAccessControlEntry Property Methods</span></span>

<span data-ttu-id="36612-106">[**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)介面的屬性方法會取得或設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="36612-106">The property methods of the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="36612-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="36612-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="36612-108">屬性</span><span class="sxs-lookup"><span data-stu-id="36612-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="36612-109">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="36612-109">**AccessMask**</span></span>
<span data-ttu-id="36612-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="36612-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="36612-111">包含一組指定物件存取權限的旗標。</span><span class="sxs-lookup"><span data-stu-id="36612-111">Contains a set of flags that specifies access privileges for the object.</span></span> <span data-ttu-id="36612-112">Active Directory 物件的有效值會定義于 [**ADS \_ 許可權 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_rights_enum) 列舉中。</span><span class="sxs-lookup"><span data-stu-id="36612-112">Valid values for Active Directory objects are defined in the [**ADS\_RIGHTS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum) enumeration.</span></span>

<span data-ttu-id="36612-113">如需詳細資訊以及檔案或檔案共用物件的可能值清單，請參閱檔案 [安全性和存取權限](/windows/desktop/FileIO/file-security-and-access-rights)。</span><span class="sxs-lookup"><span data-stu-id="36612-113">For more information and a list of possible values for file or file share objects, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights).</span></span>

<span data-ttu-id="36612-114">如需登錄物件的可能值清單以及登錄物件的可能值清單，請參閱登錄機 [碼安全性和存取權限](/windows/desktop/SysInfo/registry-key-security-and-access-rights)。</span><span class="sxs-lookup"><span data-stu-id="36612-114">For more information and a list of possible values for registry objects, see [Registry Key Security and Access Rights](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span></span>

<dt>

<span data-ttu-id="36612-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="36612-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="36612-116">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="36612-116">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AccessMask(
  [out] LONG* plnAccessMask
);
HRESULT put_AccessMask(
  [in] LONG lnAccessMask
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="36612-117">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="36612-117">**AceFlags**</span></span>
<span data-ttu-id="36612-118"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="36612-118"></dt> <dd> <dl></span></span>

<span data-ttu-id="36612-119">包含一組旗標，指定其他容器或物件是否可以繼承 ACE。</span><span class="sxs-lookup"><span data-stu-id="36612-119">Contains a set of flags that specifies if other containers or objects can inherit the ACE.</span></span> <span data-ttu-id="36612-120">Active Directory 物件的有效值會定義于 [**ADS \_ ACEFLAG \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum) 列舉中。</span><span class="sxs-lookup"><span data-stu-id="36612-120">Valid values for Active Directory object are defined in the [**ADS\_ACEFLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum) enumeration.</span></span>

<span data-ttu-id="36612-121">如需檔案、檔案共用和登錄物件的詳細資訊和可能的值，請參閱 [**ACE \_ 標頭**](/windows/desktop/api/winnt/ns-winnt-ace_header)結構的 **AceFlags** 成員。</span><span class="sxs-lookup"><span data-stu-id="36612-121">For more information and possible values for file, file share, and registry objects, see the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

<dt>

<span data-ttu-id="36612-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="36612-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="36612-123">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="36612-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceFlags(
  [out] LONG* plnAceFlags
);
HRESULT put_AceFlags(
  [in] LONG lnAceFlags
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="36612-124">**AceType**</span><span class="sxs-lookup"><span data-stu-id="36612-124">**AceType**</span></span>
<span data-ttu-id="36612-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="36612-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="36612-126">包含指出 ACE 類型的值。</span><span class="sxs-lookup"><span data-stu-id="36612-126">Contains a value that indicates the type of ACE.</span></span> <span data-ttu-id="36612-127">Active Directory 物件的有效值會定義于 [**ADS \_ ACETYPE \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_acetype_enum) 列舉中。</span><span class="sxs-lookup"><span data-stu-id="36612-127">Valid values for Active Directory objects are defined in the [**ADS\_ACETYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_acetype_enum) enumeration.</span></span>

<span data-ttu-id="36612-128">如需檔案、檔案共用和登錄物件的詳細資訊和可能的值，請參閱 [**ACE \_ 標頭**](/windows/desktop/api/winnt/ns-winnt-ace_header)結構的 **AceType** 成員。</span><span class="sxs-lookup"><span data-stu-id="36612-128">For more information and possible values for file, file share, and registry objects, see the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

<dt>

<span data-ttu-id="36612-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="36612-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="36612-130">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="36612-130">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceType(
  [out] LONG* plAceType
);
HRESULT put_AceType(
  [in] LONG lnAceType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="36612-131">**旗標**</span><span class="sxs-lookup"><span data-stu-id="36612-131">**Flags**</span></span>
<span data-ttu-id="36612-132"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="36612-132"></dt> <dd> <dl></span></span>

<span data-ttu-id="36612-133">旗標，指出 ACE 是否有物件類型或繼承的物件類型。</span><span class="sxs-lookup"><span data-stu-id="36612-133">A flag that indicates if the ACE has an object type or inherited object type.</span></span> <span data-ttu-id="36612-134">有效的旗標定義于 [**ADS \_ FLAGTYPE \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum) 列舉中。</span><span class="sxs-lookup"><span data-stu-id="36612-134">Valid flags are defined in the [**ADS\_FLAGTYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum) enumeration.</span></span>

<dt>

<span data-ttu-id="36612-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="36612-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="36612-136">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="36612-136">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Flags(
  [out] LONG* lnflags
);
HRESULT put_Flags(
  [in] LONG lnflags
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="36612-137">**InheritedObjectType**</span><span class="sxs-lookup"><span data-stu-id="36612-137">**InheritedObjectType**</span></span>
<span data-ttu-id="36612-138"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="36612-138"></dt> <dd> <dl></span></span>

<span data-ttu-id="36612-139">指出 ADSI 物件之子物件類型的旗標。</span><span class="sxs-lookup"><span data-stu-id="36612-139">A flag that indicates the type of a child object of an ADSI object.</span></span> <span data-ttu-id="36612-140">它的值是字串格式之物件的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="36612-140">Its value is a **GUID** to an object in string format.</span></span> <span data-ttu-id="36612-141">設定這類 **guid** 時，ACE 只會套用至 **GUID** 所參考的物件。</span><span class="sxs-lookup"><span data-stu-id="36612-141">When such a **GUID** is set, the ACE applies only to the object referred to by the **GUID**.</span></span>

<dt>

<span data-ttu-id="36612-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="36612-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="36612-143">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="36612-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_InheritedObjectType(
  [out] BSTR* bstrInheritedObjectType
);
HRESULT put_InheritedObjectType(
  [in] BSTR bstrInheritedObjectType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="36612-144">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="36612-144">**ObjectType**</span></span>
<span data-ttu-id="36612-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="36612-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="36612-146">指出 ADSI 物件類型的旗標。</span><span class="sxs-lookup"><span data-stu-id="36612-146">A flag that indicates the ADSI object type.</span></span> <span data-ttu-id="36612-147">它的值是屬性的 **GUID** 或字串格式的物件。</span><span class="sxs-lookup"><span data-stu-id="36612-147">Its value is a **GUID** to a property or an object in string format.</span></span> <span data-ttu-id="36612-148">當使用 **ads \_ right \_ ds \_ 讀取 \_** 屬性和 **ads \_ Right \_ ds \_ WRITE \_** 屬性存取遮罩時， **GUID** 會參考屬性。</span><span class="sxs-lookup"><span data-stu-id="36612-148">The **GUID** refers to a property when **ADS\_RIGHT\_DS\_READ\_PROP** and **ADS\_RIGHT\_DS\_WRITE\_PROP** access masks are used.</span></span> <span data-ttu-id="36612-149">**GUID** 會在 **廣告 \_ 正確的 \_ ds \_ 建立 \_ 子** 系，並 **使用 \_ 正確的 \_ ds \_ 刪除 \_ 子** 存取遮罩時指定物件。</span><span class="sxs-lookup"><span data-stu-id="36612-149">The **GUID** specifies an object when **ADS\_RIGHT\_DS\_CREATE\_CHILD** and **ADS\_RIGHT\_DS\_DELETE\_CHILD** access masks are used.</span></span>

<dt>

<span data-ttu-id="36612-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="36612-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="36612-151">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="36612-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectType(
  [out] BSTR* bstrObjectType
);
HRESULT put_ObjectType(
  [in] BSTR bstrObjectType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="36612-152">**受託 人**</span><span class="sxs-lookup"><span data-stu-id="36612-152">**Trustee**</span></span>
<span data-ttu-id="36612-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="36612-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="36612-154">包含套用 ACE 的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="36612-154">Contains the name of the account that the ACE applies to.</span></span>

<dt>

<span data-ttu-id="36612-155">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="36612-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="36612-156">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="36612-156">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Trustee(
  [out] BSTR* pbstrSecurityId
);
HRESULT put_Trustee(
  [in] BSTR bstrSecurityId
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="36612-157">範例</span><span class="sxs-lookup"><span data-stu-id="36612-157">Examples</span></span>

<span data-ttu-id="36612-158">下列程式碼範例示範如何使用 [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) 屬性方法，將專案加入至任意的 ACL。</span><span class="sxs-lookup"><span data-stu-id="36612-158">The following code example shows how to add entries to a discretionary ACL using the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) property methods.</span></span>


```VB
Dim x As IADs
Dim sd As IADsSecurityDescriptor
Dim ace As IADsAccessControlEntry
Dim Dacl As IADsAccessControlList
Dim Ace1 As New AccessControlEntry
Dim Ace2 As New AccessControlEntry

On Error GoTo Cleanup
 
Set x = GetObject("LDAP://OU=Sales, DC=Fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")
Set Dacl = sd.DiscretionaryAcl
 
' Show the existing ACEs.
For Each ace In Dacl
  Debug.Print ace.Trustee
Next
 
 
' Setup the first ACE.
Ace1.AccessMask = -1 'Full Permission (Allowed)
Ace1.AceType = ADS_ACETYPE_ACCESS_ALLOWED
Ace1.AceFlags = ADS_ACEFLAG_INHERIT_ACE
Ace1.Trustee = "ACTIVED\Administrator"
 
' Setup the 2nd ACE.
Ace2.AccessMask = -1 'Full Permission (Denied)
Ace2.AceType = ADS_ACETYPE_ACCESS_DENIED
Ace2.AceFlags = ADS_ACEFLAG_INHERIT_ACE
Ace2.Trustee = "ACTIVED\Andyhar"
 
' Add the ACEs to the Discretionary ACL.
Dacl.AddAce Ace1
Dacl.AddAce Ace2
 
sd.DiscretionaryAcl = Dacl
x.Put "ntSecurityDescriptor", Array(sd)
x.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set x = Nothing
    Set sd = Nothing
    Set ace = Nothing
    Set Dacl = Nothing
    Set Ace1 = Nothing
    Set Ace2 = Nothing
    Set obj = Nothing
    Set cls = Nothing
```



<span data-ttu-id="36612-159">下列程式碼範例會顯示存取控制專案。</span><span class="sxs-lookup"><span data-stu-id="36612-159">The following code example displays access-control entries.</span></span>


```C++
IADs *pADs = NULL;
IDispatch *pDisp = NULL;
IADsSecurityDescriptor *pSD = NULL;
VARIANT var;
HRESULT hr = S_OK;
 
VariantInit(&var);

hr = ADsOpenObject(L"LDAP://OU=Sales, DC=Fabrikam,DC=com",NULL,NULL,
                   ADS_SECURE_AUTHENTICATION, IID_IADs,(void**)&pADs);
if(FAILED(hr)) {goto Cleanup;}

hr = pADs->Get(CComBSTR("ntSecurityDescriptor"),&var);
if(FAILED(hr)) {goto Cleanup;}

pDisp = V_DISPATCH(&var);

hr = pDisp->QueryInterface(IID_IADsSecurityDescriptor,(void**)&pSD);
if(FAILED(hr)) {goto Cleanup;}
pDisp->Release();


pSD->get_DiscretionaryAcl(&pDisp);

hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
if(FAILED(hr)) {goto Cleanup;}

hr = DisplayAccessInfo(pSD);
if(FAILED(hr)) {goto Cleanup;}
VariantClear(&var);

Cleanup:
    if(pADs) pADs->Release();
    if(pDisp) pDisp->Release();
    if(pSD) pSD->Release();
    return hr;



HRESULT DisplayAccessInfo(IADsSecurityDescriptor *pSD)
{
    LPWSTR lpszFunction = L"DisplayAccessInfo";
    IDispatch *pDisp = NULL;
    IADsAccessControlList *pACL = NULL;
    IADsAccessControlEntry *pACE = NULL;
    IEnumVARIANT *pEnum = NULL;
    IUnknown *pUnk = NULL;
    HRESULT hr = S_OK;
    ULONG nFetch = 0;
    BSTR bstrValue = NULL;
    VARIANT var;
    LPWSTR lpszOutput = NULL;
    LPWSTR lpszMask = NULL;
    size_t nLength = 0;
    
    VariantInit(&var);
    
    hr = pSD->get_DiscretionaryAcl(&pDisp);
    if(FAILED(hr)){goto Cleanup;}
    hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pACL->get__NewEnum(&pUnk);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
    
    if(FAILED(hr)){goto Cleanup;}
    hr = pEnum->Next(1,&var,&nFetch);
    
    while(hr == S_OK)
    {
        if(nFetch==1)
        {
            if(VT_DISPATCH != V_VT(&var))
            {
                goto Cleanup;
            }
            
            pDisp = V_DISPATCH(&var);
            hr = pDisp->QueryInterface(IID_IADsAccessControlEntry,(void**)&pACE);
            
            if(SUCCEEDED(hr))
            {
                lpszMask = L"Trustee: %s";
                hr = pACE->get_Trustee(&bstrValue);
                nLength = wcslen(lpszMask) + wcslen(bstrValue) + 1;
                lpszOutput = new WCHAR[nLength];
                swprintf_s(lpszOutput,lpszMask,bstrValue);
                printf(lpszOutput);
                delete [] lpszOutput;
                SysFreeString(bstrValue);
                
                pACE->Release();
                pACE = NULL;
                pDisp->Release();
                pDisp = NULL;
            }       
            
            VariantClear(&var);
        }       
        hr = pEnum->Next(1,&var,&nFetch);
    }
    
Cleanup:
    if(pDisp) pDisp->Release();
    if(pACL) pACL->Release();
    if(pACE) pACE->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(szValue) SysFreeString(szValue);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="36612-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="36612-160">Requirements</span></span>



| <span data-ttu-id="36612-161">需求</span><span class="sxs-lookup"><span data-stu-id="36612-161">Requirement</span></span> | <span data-ttu-id="36612-162">值</span><span class="sxs-lookup"><span data-stu-id="36612-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="36612-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36612-163">Minimum supported client</span></span><br/> | <span data-ttu-id="36612-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36612-164">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="36612-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36612-165">Minimum supported server</span></span><br/> | <span data-ttu-id="36612-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36612-166">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="36612-167">標頭</span><span class="sxs-lookup"><span data-stu-id="36612-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="36612-168"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="36612-168"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="36612-169">DLL</span><span class="sxs-lookup"><span data-stu-id="36612-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36612-170"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36612-170"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="36612-171">IID</span><span class="sxs-lookup"><span data-stu-id="36612-171">IID</span></span><br/>                      | <span data-ttu-id="36612-172">IID \_ IADsAccessControlEntry 定義為 B4F3A14C-9BDD-11D0-852C-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="36612-172">IID\_IADsAccessControlEntry is defined as B4F3A14C-9BDD-11D0-852C-00C04FD8D503</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="36612-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36612-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36612-174">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="36612-174">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[<span data-ttu-id="36612-175">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="36612-175">**IADsAccessControlList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> <dt>

[<span data-ttu-id="36612-176">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="36612-176">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> </dl>

 


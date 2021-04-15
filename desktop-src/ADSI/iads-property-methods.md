---
title: 'IADs 屬性方法 (Iads .h) '
description: IADs 介面的屬性方法會取得或設定下表所述的屬性。 如需屬性方法的詳細資訊，請參閱介面屬性方法。
ms.assetid: d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12
ms.tgt_platform: multiple
keywords:
- IADs 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADs Property Methods
- IADs.ADsPath
- IADs.get_ADsPath
- IADs.Class
- IADs.get_Class
- IADs.GUID
- IADs.get_GUID
- IADs.Name
- IADs.get_Name
- IADs.Parent
- IADs.get_Parent
- IADs.Schema
- IADs.get_Schema
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1134260c780958bcdba8d1f14eac535ddbf4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508344"
---
# <a name="iads-property-methods"></a><span data-ttu-id="7fc3a-105">IADs 屬性方法</span><span class="sxs-lookup"><span data-stu-id="7fc3a-105">IADs Property Methods</span></span>

<span data-ttu-id="7fc3a-106">[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)介面的屬性方法會取得或設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-106">The property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="7fc3a-107">如需屬性方法的詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="7fc3a-108">屬性</span><span class="sxs-lookup"><span data-stu-id="7fc3a-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="7fc3a-109">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-109">**ADsPath**</span></span>
<span data-ttu-id="7fc3a-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7fc3a-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="7fc3a-111">這個物件的 ADsPath 字串。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-111">The ADsPath string of this object.</span></span> <span data-ttu-id="7fc3a-112">此字串可在網路環境中唯一識別此物件。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-112">The string uniquely identifies this object in a network environment.</span></span> <span data-ttu-id="7fc3a-113">您一律可以使用此路徑來抓取物件。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-113">The object can always be retrieved using this path.</span></span>

<dt>

<span data-ttu-id="7fc3a-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fc3a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fc3a-115">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-115">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsPath(
  [out] BSTR* pbstrADsPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fc3a-116">**類別**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-116">**Class**</span></span>
<span data-ttu-id="7fc3a-117"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7fc3a-117"></dt> <dd> <dl></span></span>

<span data-ttu-id="7fc3a-118">物件架構類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-118">The name of the object Schema class.</span></span>

<dt>

<span data-ttu-id="7fc3a-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fc3a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fc3a-120">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-120">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Class(
  [out] BSTR* pbstrClass
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fc3a-121">**GUID**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-121">**GUID**</span></span>
<span data-ttu-id="7fc3a-122"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7fc3a-122"></dt> <dd> <dl></span></span>

<span data-ttu-id="7fc3a-123">目錄物件的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-123">The globally unique identifier of the directory object.</span></span> <span data-ttu-id="7fc3a-124">[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)介面會將 **GUID** 從儲存在目錄伺服器上的八位字串轉換成字串格式。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-124">The [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface converts the **GUID** from an octet string, as stored on a directory server, into a string format.</span></span>

<dt>

<span data-ttu-id="7fc3a-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fc3a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fc3a-126">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-126">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GUID(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fc3a-127">**名稱**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-127">**Name**</span></span>
<span data-ttu-id="7fc3a-128"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7fc3a-128"></dt> <dd> <dl></span></span>

<span data-ttu-id="7fc3a-129">在基礎目錄服務中命名之物件的相對名稱。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-129">The relative name of the object as named within the underlying directory service.</span></span> <span data-ttu-id="7fc3a-130">此名稱會區分這個物件與其同級。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-130">This name distinguishes this object from its siblings.</span></span>

<dt>

<span data-ttu-id="7fc3a-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fc3a-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fc3a-132">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fc3a-133">**父系**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-133">**Parent**</span></span>
<span data-ttu-id="7fc3a-134"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7fc3a-134"></dt> <dd> <dl></span></span>

<span data-ttu-id="7fc3a-135">父容器的 ADsPath 字串。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-135">The ADsPath string of the parent container.</span></span> <span data-ttu-id="7fc3a-136">Active Directory 不允許藉由串連 **Parent** 和 **Name** 屬性來構成指定物件的 ADsPath。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-136">Active Directory does not permit the formation of the ADsPath of a given object by concatenating the **Parent** and **Name** properties.</span></span> <span data-ttu-id="7fc3a-137">雖然這項作業可能適用于某些提供者，但不保證適用于所有的執行。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-137">While this operation might work in some providers, it is not guaranteed to work for all implementations.</span></span> <span data-ttu-id="7fc3a-138">ADsPath 保證是有效的，而且應該一律用來取出物件的介面指標。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-138">The ADsPath is guaranteed to be valid and should always be used to retrieve an object's interface pointer.</span></span>

<dt>

<span data-ttu-id="7fc3a-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fc3a-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fc3a-140">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-140">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parent(
  [out] BSTR* pbstrParent
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fc3a-141">**結構描述**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-141">**Schema**</span></span>
<span data-ttu-id="7fc3a-142"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7fc3a-142"></dt> <dd> <dl></span></span>

<span data-ttu-id="7fc3a-143">這個物件的架構類別物件的 ADsPath 字串。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-143">The ADsPath string of the Schema class object of this object.</span></span>

<dt>

<span data-ttu-id="7fc3a-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fc3a-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fc3a-145">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-145">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Schema(
  [out] BSTR* pbstrSchema
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="7fc3a-146">備註</span><span class="sxs-lookup"><span data-stu-id="7fc3a-146">Remarks</span></span>

<span data-ttu-id="7fc3a-147">在 Active Directory 中，GUID 傳回的 **guid** 是 hexadecimals 的字串。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-147">In Active Directory, the **GUID** returned from GUID is a string of hexadecimals.</span></span> <span data-ttu-id="7fc3a-148">使用結果 **GUID** 直接系結至物件。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-148">Use the resultant **GUID** to bind to the object directly.</span></span>


```VB
Dim x As IADs
Set x = GetObject("LDAP://servername/<GUID=xxx>")
```



<span data-ttu-id="7fc3a-149">其中 xxx 是從 GUID 屬性傳回的值。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-149">where xxx is the value returned from the GUID property.</span></span> <span data-ttu-id="7fc3a-150">如需詳細資訊，請參閱 [使用 objectGUID 系結至物件](/windows/desktop/AD/using-objectguid-to-bind-to-an-object)。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-150">For more information, see [Using objectGUID to Bind to an Object](/windows/desktop/AD/using-objectguid-to-bind-to-an-object).</span></span> <span data-ttu-id="7fc3a-151">請注意，如果您使用 GUID 來系結至物件，則 **ADsPath** 屬性方法會傳回不同于一般值的值，如果您使用 (DN) 的分辨名稱來系結至相同物件，則會傳回這些值。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-151">Be aware that if you use a GUID to bind to an object, the **ADsPath** property method returns values that are different from the normal values that would be returned if you used a distinguished name (DN) to bind to the same object.</span></span> <span data-ttu-id="7fc3a-152">例如，下表列出使用兩個不同的系結方法系結至相同的使用者物件時，所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-152">For example, the following table lists the values returned when using the two different binding methods to bind to the same user object.</span></span>



|             | <span data-ttu-id="7fc3a-153">使用 DN 系結</span><span class="sxs-lookup"><span data-stu-id="7fc3a-153">Bind using DN</span></span>                                           | <span data-ttu-id="7fc3a-154">使用 GUID 系結</span><span class="sxs-lookup"><span data-stu-id="7fc3a-154">Bind using GUID</span></span>                                             |
|-------------|---------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7fc3a-155">**名稱**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-155">**Name**</span></span>    | <span data-ttu-id="7fc3a-156">CN = Jeff Smith</span><span class="sxs-lookup"><span data-stu-id="7fc3a-156">CN=Jeff Smith</span></span>                                           | <span data-ttu-id="7fc3a-157">CN = Jeff Smith</span><span class="sxs-lookup"><span data-stu-id="7fc3a-157">CN=Jeff Smith</span></span>                                               |
| <span data-ttu-id="7fc3a-158">**父系**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-158">**Parent**</span></span>  | <span data-ttu-id="7fc3a-159">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span><span class="sxs-lookup"><span data-stu-id="7fc3a-159">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span></span>               | <span data-ttu-id="7fc3a-160">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span><span class="sxs-lookup"><span data-stu-id="7fc3a-160">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span></span>                   |
| <span data-ttu-id="7fc3a-161">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-161">**ADsPath**</span></span> | <span data-ttu-id="7fc3a-162">LDAP://server/CN=Jeff Smith，CN = Users，DC = Fabrikam，DC = com</span><span class="sxs-lookup"><span data-stu-id="7fc3a-162">LDAP://server/CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=com</span></span> | <span data-ttu-id="7fc3a-163">LDAP://server/<GUID = c0f59dfcf507d311a99e0000f879f7c7></span><span class="sxs-lookup"><span data-stu-id="7fc3a-163">LDAP://server/<GUID=c0f59dfcf507d311a99e0000f879f7c7></span></span> |



 

> [!Note]  
> <span data-ttu-id="7fc3a-164">WinNT 提供者不支援使用物件 **GUID** 進行系結，並以稍微不同的字串格式傳回 **GUID** 屬性。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-164">The WinNT provider does not support binding using the object **GUID**, and returns the **GUID** property in a slightly different string format.</span></span>

 

## <a name="examples"></a><span data-ttu-id="7fc3a-165">範例</span><span class="sxs-lookup"><span data-stu-id="7fc3a-165">Examples</span></span>

<span data-ttu-id="7fc3a-166">下列程式碼範例示範如何使用 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面的屬性方法來取出物件資料。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-166">The following code example shows how to retrieve object data using property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```VB
Dim x As IADs
Dim parent As IADsContainer
Dim cls As IADsClass
Dim op As Variant

On Error GoTo Cleanup

Set x = GetObject("WinNT://Fabrikam/Administrator")
Debug.Print "Object Name: " & x.Name
Debug.Print "Object Path: " & x.ADsPath
Debug.Print "Object Class: " & x.Class
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Debug.Print "Class Name is: " & cls.Name
For Each op In cls.OptionalProperties
    Debug.Print "Optional Property: " & op
Next op

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
    Set parent = Nothing
    Set cls = Nothing
```



<span data-ttu-id="7fc3a-167">下列程式碼範例示範如何使用 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面的屬性方法來取出物件資料。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-167">The following code example shows how to retrieve object data using property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```VB
<HTML>
<head><title></title></head>

<body>
<%
Dim x 
On Error Resume Next
 
Set x = GetObject("WinNT://Fabrikam/Administrator")
Response.Write "Object Name: " & x.Name & "<br>"
Response.Write "Object Path: " & x.ADsPath & "<br>"
Response.Write "Object Class: " & x.Class & "<br>"
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Response.Write "Class Name is: " & cls.Name & "<br>"
For Each op In cls.OptionalProperties
    Response.Write "Optional Property: " & op & "<br>"
Next op
%>

</body>
</html>
```



<span data-ttu-id="7fc3a-168">下列程式碼範例顯示如何使用 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面的屬性方法。</span><span class="sxs-lookup"><span data-stu-id="7fc3a-168">The following code example shows how to work with the property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```C++
#include <stdio.h>
#include <activeds.h>
 
int main(int argc, char* argv[])
{
    IADs *pADs = NULL;
    IADsUser *pADsUser = NULL;
    IADsClass *pCls = NULL;
    CComBSTR sbstr;
 
    HRESULT hr = CoInitialize(NULL);
    if (hr != S_OK) { return 0; }
 
    hr=ADsGetObject(L"WinNT://Fabrikam/Administrator",
                IID_IADsUser,
                (void**) &pADsUser);
    if (hr != S_OK) { goto Cleanup; }
 
    hr = pADsUser->QueryInterface(IID_IADs, (void**) &pADs);
    if( hr !=S_OK) { goto Cleanup;}
 
    pADsUser->Release();
 
    if( S_OK == pADs->get_Name(&sbstr) ) {
        printf("Object Name: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_ADsPath(&sbstr) ) {
        printf("Object path: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_Class(&sbstr) ) {
        printf("Object class: %S\n",sbstr);
    }
 
    hr = pADs->get_Schema(&sbstr);
    if ( hr != S_OK) {goto Cleanup;}
 
    hr = ADsGetObject(sbstr,IID_IADsClass, (void**)&pCls);
    if ( hr != S_OK) {goto Cleanup;}
    if( S_OK == pCls->get_Name(&sbstr) ) {
        printf("Class name is %S\n", sbstr);
    }
 
 Cleanup:
    if(pADs)
        pADs->Release();

    if(pIADsUser)
        pADsUser->Release();

    if(IADsClass)
        pADsClass->Release();

    CoUninitialize();

    if(hr==S_OK)
    {
        return 1;
    }
    else
    {
        return 0;
    }
}
```



## <a name="requirements"></a><span data-ttu-id="7fc3a-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fc3a-169">Requirements</span></span>



| <span data-ttu-id="7fc3a-170">需求</span><span class="sxs-lookup"><span data-stu-id="7fc3a-170">Requirement</span></span> | <span data-ttu-id="7fc3a-171">值</span><span class="sxs-lookup"><span data-stu-id="7fc3a-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc3a-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7fc3a-172">Minimum supported client</span></span><br/> | <span data-ttu-id="7fc3a-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7fc3a-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7fc3a-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7fc3a-174">Minimum supported server</span></span><br/> | <span data-ttu-id="7fc3a-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fc3a-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7fc3a-176">標頭</span><span class="sxs-lookup"><span data-stu-id="7fc3a-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fc3a-177"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="7fc3a-177"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="7fc3a-178">DLL</span><span class="sxs-lookup"><span data-stu-id="7fc3a-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fc3a-179"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fc3a-179"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="7fc3a-180">IID</span><span class="sxs-lookup"><span data-stu-id="7fc3a-180">IID</span></span><br/>                      | <span data-ttu-id="7fc3a-181">IID \_ IADs 定義為 FD8256D0-FD15-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="7fc3a-181">IID\_IADs is defined as FD8256D0-FD15-11CE-ABC4-02608C9E7553</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="7fc3a-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fc3a-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fc3a-183">**IADs**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-183">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="7fc3a-184">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="7fc3a-184">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> </dl>

 


---
title: 'IADsResource 屬性方法 (Iads .h) '
description: IADsResource 介面的屬性方法會取得或設定下表所述的屬性。 如需屬性方法的一般討論，請參閱介面屬性方法。
ms.assetid: a2d6ed76-88e9-468f-928a-a038b73fb362
ms.tgt_platform: multiple
keywords:
- IADsResource 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsResource Property Methods
- IADsResource.LockCount
- IADsResource.get_LockCount
- IADsResource.Path
- IADsResource.get_Path
- IADsResource.User
- IADsResource.get_User
- IADsResource.UserPath
- IADsResource.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0f2ab2642dd8d03062a26d096190cf7615977a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968757"
---
# <a name="iadsresource-property-methods"></a><span data-ttu-id="67ecd-105">IADsResource 屬性方法</span><span class="sxs-lookup"><span data-stu-id="67ecd-105">IADsResource Property Methods</span></span>

<span data-ttu-id="67ecd-106">[**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource)介面的屬性方法會取得或設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="67ecd-106">The property methods of the [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="67ecd-107">如需屬性方法的一般討論，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="67ecd-107">For a general discussion of property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="67ecd-108">屬性</span><span class="sxs-lookup"><span data-stu-id="67ecd-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="67ecd-109">**LockCount**</span><span class="sxs-lookup"><span data-stu-id="67ecd-109">**LockCount**</span></span>
<span data-ttu-id="67ecd-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="67ecd-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="67ecd-111">資源上的鎖定數目。</span><span class="sxs-lookup"><span data-stu-id="67ecd-111">Number of locks on the resource.</span></span>

<dt>

<span data-ttu-id="67ecd-112">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ecd-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ecd-113">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="67ecd-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockCount(
  [out] LONG* plLockCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="67ecd-114">**路徑**</span><span class="sxs-lookup"><span data-stu-id="67ecd-114">**Path**</span></span>
<span data-ttu-id="67ecd-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="67ecd-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="67ecd-116">開啟之資源的檔案系統路徑。</span><span class="sxs-lookup"><span data-stu-id="67ecd-116">The file system path of the opened resource.</span></span>

<dt>

<span data-ttu-id="67ecd-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ecd-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ecd-118">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="67ecd-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="67ecd-119">**使用者**</span><span class="sxs-lookup"><span data-stu-id="67ecd-119">**User**</span></span>
<span data-ttu-id="67ecd-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="67ecd-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="67ecd-121">開啟資源之使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="67ecd-121">The name of the user who opened the resource.</span></span>

<dt>

<span data-ttu-id="67ecd-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ecd-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ecd-123">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="67ecd-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="67ecd-124">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="67ecd-124">**UserPath**</span></span>
<span data-ttu-id="67ecd-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="67ecd-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="67ecd-126">開啟資源之使用者的使用者物件 ADsPath。</span><span class="sxs-lookup"><span data-stu-id="67ecd-126">The ADsPath of the user object for the user who opened the resource.</span></span>

<dt>

<span data-ttu-id="67ecd-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ecd-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ecd-128">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="67ecd-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="67ecd-129">範例</span><span class="sxs-lookup"><span data-stu-id="67ecd-129">Examples</span></span>

<span data-ttu-id="67ecd-130">下列程式碼範例顯示如何檢查檔案服務的開啟資源。</span><span class="sxs-lookup"><span data-stu-id="67ecd-130">The following code example shows how to examine open resources of a file service.</span></span>


```VB
Dim fso As IADsFileServiceOperations
' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate resources.
If (IsEmpty(fso) = False) Then
    For Each resource In fso.resources
        MsgBox "Resource name: " & resource.name
        MsgBox "Resource path: " & resource.path
    Next resource
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



<span data-ttu-id="67ecd-131">下列程式碼範例會列舉資源的集合。</span><span class="sxs-lookup"><span data-stu-id="67ecd-131">The following code example enumerates a collection of resources.</span></span>


```C++
IADsFileServiceOperations *pFso = NULL;
IADsResource *pRes = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
IEnumVARIANT *pEnum = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
HRESULT hr = S_OK;

LPWSTR adsPath =L"WinNT://aMachine/LanmanServer";
hr = ADsGetObject(adsPath, IID_IADsFileServiceOperations,(void**)&pFso);
if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Resources(&pColl);
if(FAILED(hr)) {goto Cleanup;}


// Enumerate print jobs. Code omitted.
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
VariantInit(&var);
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsResource, (void**)&pRes);
        pRes->get_Name(&bstr);
        printf("Resource name: %S\n",bstr);
        SysFreeString(bstr);
        pRes->get_Path(&bstr);
        printf("Resource path: %S\n",bstr);
        SysFreeString(bstr);
        pRes->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pRes) pRes->Release();
    if(pDisp) pDisp->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pFso) pFso->Release();
```



## <a name="requirements"></a><span data-ttu-id="67ecd-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="67ecd-132">Requirements</span></span>



| <span data-ttu-id="67ecd-133">需求</span><span class="sxs-lookup"><span data-stu-id="67ecd-133">Requirement</span></span> | <span data-ttu-id="67ecd-134">值</span><span class="sxs-lookup"><span data-stu-id="67ecd-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67ecd-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67ecd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="67ecd-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67ecd-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="67ecd-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67ecd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="67ecd-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67ecd-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="67ecd-139">標頭</span><span class="sxs-lookup"><span data-stu-id="67ecd-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="67ecd-140"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="67ecd-140"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="67ecd-141">DLL</span><span class="sxs-lookup"><span data-stu-id="67ecd-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67ecd-142"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67ecd-142"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="67ecd-143">IID</span><span class="sxs-lookup"><span data-stu-id="67ecd-143">IID</span></span><br/>                      | <span data-ttu-id="67ecd-144">IID \_ IADsResource 定義為34A05B20-4AAB-11CF-AE2C-00AA006EBFB9</span><span class="sxs-lookup"><span data-stu-id="67ecd-144">IID\_IADsResource is defined as 34A05B20-4AAB-11CF-AE2C-00AA006EBFB9</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="67ecd-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67ecd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ecd-146">**IADsResource**</span><span class="sxs-lookup"><span data-stu-id="67ecd-146">**IADsResource**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsresource)
</dt> <dt>

[<span data-ttu-id="67ecd-147">**IADsFileServiceOperations：： Resources**</span><span class="sxs-lookup"><span data-stu-id="67ecd-147">**IADsFileServiceOperations::Resources**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-resources)
</dt> </dl>

 

 






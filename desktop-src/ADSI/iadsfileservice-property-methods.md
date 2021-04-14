---
title: 'IADsFileService 屬性方法 (Iads .h) '
description: IADsFileService 介面的屬性方法會取得或設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 1455df61-9218-450b-b956-1cf127364f24
ms.tgt_platform: multiple
keywords:
- IADsFileService 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsFileService Property Methods
- IADsFileService.Description
- IADsFileService.get_Description
- IADsFileService.put_Description
- IADsFileService.MaxUserCount
- IADsFileService.get_MaxUserCount
- IADsFileService.put_MaxUserCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f3a46b37522bbdce6e99b969811e2909c8ecc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509031"
---
# <a name="iadsfileservice-property-methods"></a><span data-ttu-id="3442a-105">IADsFileService 屬性方法</span><span class="sxs-lookup"><span data-stu-id="3442a-105">IADsFileService Property Methods</span></span>

<span data-ttu-id="3442a-106">[**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)介面的屬性方法會取得或設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="3442a-106">The property methods of the [**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="3442a-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="3442a-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3442a-108">屬性</span><span class="sxs-lookup"><span data-stu-id="3442a-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="3442a-109">**說明**</span><span class="sxs-lookup"><span data-stu-id="3442a-109">**Description**</span></span>
<span data-ttu-id="3442a-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3442a-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="3442a-111">檔案服務的描述。</span><span class="sxs-lookup"><span data-stu-id="3442a-111">The description of the file service.</span></span>

<dt>

<span data-ttu-id="3442a-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3442a-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3442a-113">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3442a-113">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="3442a-114">**MaxUserCount**</span><span class="sxs-lookup"><span data-stu-id="3442a-114">**MaxUserCount**</span></span>
<span data-ttu-id="3442a-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3442a-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="3442a-116">服務上允許的最大使用者數目。</span><span class="sxs-lookup"><span data-stu-id="3442a-116">The maximum number of users allowed on the service at any time.</span></span>

<dt>

<span data-ttu-id="3442a-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3442a-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3442a-118">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="3442a-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
HRESULT put_MaxUserCount(
  [in] LONG lMaxUserCount
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="3442a-119">備註</span><span class="sxs-lookup"><span data-stu-id="3442a-119">Remarks</span></span>

<span data-ttu-id="3442a-120">您必須經過檔案服務，才能存取電腦上的檔案共用、會話和資源。</span><span class="sxs-lookup"><span data-stu-id="3442a-120">You must go through the file service to access file shares, sessions, and resources on a computer.</span></span>

## <a name="examples"></a><span data-ttu-id="3442a-121">範例</span><span class="sxs-lookup"><span data-stu-id="3442a-121">Examples</span></span>

<span data-ttu-id="3442a-122">下列程式碼範例會寫入的描述，並檢查檔案服務的使用者限制。</span><span class="sxs-lookup"><span data-stu-id="3442a-122">The following code example writes a description for and check the user limit of the file service.</span></span>


```VB
Dim fs As IADsFileService
On Error GoTo Cleanup

' Bind to a file service object on "myComputer" in the local domain.
Set fs = GetObject("WinNT://myComputer/LanmanServer")

fs.Description = "WinNT file service."
n = fs.MaxUserCount
If n = -1 Then
   MsgBox "No limit has been imposed on number of users allowed."
Else
   MsgBox n & " users are allowed."
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
```



<span data-ttu-id="3442a-123">下列程式碼範例會寫入的描述，並檢查檔案服務物件的使用者限制。</span><span class="sxs-lookup"><span data-stu-id="3442a-123">The following code example writes a description for and check the user limit on a file service object.</span></span>


```C++
HRESULT CheckFileService()
{
    IADsFileService *pFs = NULL;
    LPWSTR adsPath = L"WinNT://myComputer/LanmanServer";
    HRESULT hr = S_OK;
    long count = 0;

    hr = ADsGetObject(adsPath, IID_IADsFileService, (void**)&pFs)
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->put_Description(CComBSTR("WinNT File Service"));
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->SetInfo();
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->get_MaxUserCount(&count);
    if(FAILED(hr)) {goto Cleanup;}

    if(count == -1) {
        printf("No limit has been imposed on the number of users.\n");
    } 
    else {
        printf("Number of allowed users are %d\n",count);
    }

Cleanup:
    if(pFs) pFs->Release();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="3442a-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3442a-124">Requirements</span></span>



| <span data-ttu-id="3442a-125">需求</span><span class="sxs-lookup"><span data-stu-id="3442a-125">Requirement</span></span> | <span data-ttu-id="3442a-126">值</span><span class="sxs-lookup"><span data-stu-id="3442a-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3442a-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3442a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3442a-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3442a-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3442a-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3442a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3442a-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3442a-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3442a-131">標頭</span><span class="sxs-lookup"><span data-stu-id="3442a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3442a-132"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="3442a-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="3442a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3442a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3442a-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3442a-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="3442a-135">IID</span><span class="sxs-lookup"><span data-stu-id="3442a-135">IID</span></span><br/>                      | <span data-ttu-id="3442a-136">IID \_ IADsFileService 定義為 A89D1900-31CA-11CF-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="3442a-136">IID\_IADsFileService is defined as A89D1900-31CA-11CF-A98A-00AA006BC149</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="3442a-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3442a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3442a-138">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="3442a-138">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="3442a-139">**IADsFileService**</span><span class="sxs-lookup"><span data-stu-id="3442a-139">**IADsFileService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[<span data-ttu-id="3442a-140">**IADsFileServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="3442a-140">**IADsFileServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[<span data-ttu-id="3442a-141">**IADsServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="3442a-141">**IADsServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> <dt>

[<span data-ttu-id="3442a-142">介面屬性方法</span><span class="sxs-lookup"><span data-stu-id="3442a-142">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 






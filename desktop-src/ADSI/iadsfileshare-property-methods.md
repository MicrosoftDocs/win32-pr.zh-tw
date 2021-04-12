---
title: 'IADsFileShare 屬性方法 (Iads .h) '
description: IADsFileshare 介面的屬性方法會取得或設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: c5a81c42-507f-4a68-b6f4-83097bd0fa01
ms.tgt_platform: multiple
keywords:
- IADsFileShare 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsFileShare Property Methods
- IADsFileShare.CurrentUserCount
- IADsFileShare.get_CurrentUserCount
- IADsFileShare.Description
- IADsFileShare.get_Description
- IADsFileShare.put_Description
- IADsFileShare.HostComputer
- IADsFileShare.get_HostComputer
- IADsFileShare.put_HostComputer
- IADsFileShare.MaxUserCount
- IADsFileShare.get_MaxUserCount
- IADsFileShare.Path
- IADsFileShare.get_Path
- IADsFileShare.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38369a4054f1848d5e35ff8bdb2dda9e9423a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105138"
---
# <a name="iadsfileshare-property-methods"></a><span data-ttu-id="b21df-105">IADsFileShare 屬性方法</span><span class="sxs-lookup"><span data-stu-id="b21df-105">IADsFileShare Property Methods</span></span>

<span data-ttu-id="b21df-106">[**IADsFileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare)介面的屬性方法會取得或設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="b21df-106">The property methods of the [**IADsFileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="b21df-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="b21df-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="b21df-108">屬性</span><span class="sxs-lookup"><span data-stu-id="b21df-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="b21df-109">**CurrentUserCount**</span><span class="sxs-lookup"><span data-stu-id="b21df-109">**CurrentUserCount**</span></span>
<span data-ttu-id="b21df-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b21df-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="b21df-111">連線到共用的使用者數目。</span><span class="sxs-lookup"><span data-stu-id="b21df-111">The number of users connected to the share.</span></span>

<dt>

<span data-ttu-id="b21df-112">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b21df-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b21df-113">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="b21df-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CurrentUserCount(
  [out] LONG* plCurrentUserCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b21df-114">**說明**</span><span class="sxs-lookup"><span data-stu-id="b21df-114">**Description**</span></span>
<span data-ttu-id="b21df-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b21df-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="b21df-116">檔案共用的描述。</span><span class="sxs-lookup"><span data-stu-id="b21df-116">The description of the file share.</span></span>

<dt>

<span data-ttu-id="b21df-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b21df-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b21df-118">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b21df-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="b21df-119">**HostComputer**</span><span class="sxs-lookup"><span data-stu-id="b21df-119">**HostComputer**</span></span>
<span data-ttu-id="b21df-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b21df-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="b21df-121">主機電腦的 ADsPath 參考。</span><span class="sxs-lookup"><span data-stu-id="b21df-121">An ADsPath reference to the host computer.</span></span>

<dt>

<span data-ttu-id="b21df-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b21df-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b21df-123">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b21df-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b21df-124">**MaxUserCount**</span><span class="sxs-lookup"><span data-stu-id="b21df-124">**MaxUserCount**</span></span>
<span data-ttu-id="b21df-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b21df-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="b21df-126">允許一次存取共用的使用者數目上限。</span><span class="sxs-lookup"><span data-stu-id="b21df-126">The maximum number of users allowed to access the share at one time.</span></span>

<dt>

<span data-ttu-id="b21df-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b21df-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b21df-128">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="b21df-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b21df-129">**路徑**</span><span class="sxs-lookup"><span data-stu-id="b21df-129">**Path**</span></span>
<span data-ttu-id="b21df-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b21df-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="b21df-131">共用目錄的檔案系統路徑。</span><span class="sxs-lookup"><span data-stu-id="b21df-131">The file system path to the shared directory.</span></span>

<dt>

<span data-ttu-id="b21df-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b21df-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b21df-133">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b21df-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="b21df-134">範例</span><span class="sxs-lookup"><span data-stu-id="b21df-134">Examples</span></span>

<span data-ttu-id="b21df-135">若要存取電腦上的檔案共用屬性，您必須先系結至電腦上的 "LanmanServer"。</span><span class="sxs-lookup"><span data-stu-id="b21df-135">To access the properties of file shares on a computer, you must first bind to the "LanmanServer" on the machine.</span></span> <span data-ttu-id="b21df-136">下列程式碼範例示範如何針對預設網域中名稱為 "myMachine" 的電腦上的所有公用檔案共用，設定描述和允許的使用者數目上限。</span><span class="sxs-lookup"><span data-stu-id="b21df-136">The following code example shows how to set up the description and the maximum number of allowed users for all the public file shares on the computer, named as "myMachine", in the default domain.</span></span>


```VB
Dim fs As IADsFileService
Dim share As IADsFileShare
On Error GoTo Cleanup

Set fs = GetObject("WinNT://myMachine/LanmanServer")
If (fs.class = "FileService") Then
    For Each share In fs
        share.description = share.name & " is my working folder."
        share.MaxUserCount =  10
        share.SetInfo
    Next share
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
    Set share = Nothing
```



<span data-ttu-id="b21df-137">下列程式碼範例顯示如何將現有的 C： \\ MyFolder 目錄設為公用檔案共用。</span><span class="sxs-lookup"><span data-stu-id="b21df-137">The following code example shows how to make the existing C:\\MyFolder directory a public file share.</span></span>


```VB
Dim fs As IADsFileShare
Dim cont As IADsContainer
On Error GoTo Cleanup
 
Set cont = GetObject("WinNT://yourDomain/yourMachineName/LanmanServer")
 
Set fs = cont.Create("FileShare", "Public")
Debug.Print fs.Class
fs.Path = "C:\MyFolder"
fs.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set fs = Nothing
```



<span data-ttu-id="b21df-138">下列程式碼範例會讓現有的 C： \\ MyFolder 目錄成為公用檔案共用。</span><span class="sxs-lookup"><span data-stu-id="b21df-138">The following code example makes the existing C:\\MyFolder directory a public file share.</span></span>


```C++
IADsFileShare *pShare = NULL;
IADsContainer *pCont = NULL;
LPWSTR adsPath = L"WinNT://yourMachineName/LanmanServer";
HRESULT hr = S_OK;

hr = ADsGetObject(adsPath, IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->Create(CComBSTR("FileShare"), CComBSTR("Public"), (IDispatch**)&pShare);

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->put_Path(CComBSTR("c:\\public"));

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->SetInfo();

Cleanup:
    if(pCont) pCont->Release();
    if(pShare) pShare->Release();
```



## <a name="requirements"></a><span data-ttu-id="b21df-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="b21df-139">Requirements</span></span>



| <span data-ttu-id="b21df-140">需求</span><span class="sxs-lookup"><span data-stu-id="b21df-140">Requirement</span></span> | <span data-ttu-id="b21df-141">值</span><span class="sxs-lookup"><span data-stu-id="b21df-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b21df-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b21df-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b21df-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b21df-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b21df-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b21df-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b21df-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b21df-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b21df-146">標頭</span><span class="sxs-lookup"><span data-stu-id="b21df-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="b21df-147"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="b21df-147"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="b21df-148">DLL</span><span class="sxs-lookup"><span data-stu-id="b21df-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b21df-149"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b21df-149"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="b21df-150">IID</span><span class="sxs-lookup"><span data-stu-id="b21df-150">IID</span></span><br/>                      | <span data-ttu-id="b21df-151">IID \_ IADsFileShare 定義為 EB6DCAF0-4B83-11CF-A995-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="b21df-151">IID\_IADsFileShare is defined as EB6DCAF0-4B83-11CF-A995-00AA006BC149</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="b21df-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b21df-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b21df-153">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="b21df-153">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="b21df-154">**IADsFileShare**</span><span class="sxs-lookup"><span data-stu-id="b21df-154">**IADsFileShare**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileshare)
</dt> <dt>

[<span data-ttu-id="b21df-155">介面屬性方法</span><span class="sxs-lookup"><span data-stu-id="b21df-155">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 






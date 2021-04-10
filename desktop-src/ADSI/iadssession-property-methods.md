---
title: 'IADsSession 屬性方法 (Iads .h) '
description: IADsSession 介面的屬性方法會取得或設定下表所述的屬性。 如需有關屬性方法的詳細資訊和一般討論，請參閱介面屬性方法。
ms.assetid: b2366da7-c51c-4279-8931-2000d3110d72
ms.tgt_platform: multiple
keywords:
- IADsSession 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsSession Property Methods
- IADsSession.Computer
- IADsSession.get_Computer
- IADsSession.ComputerPath
- IADsSession.get_ComputerPath
- IADsSession.ConnectTime
- IADsSession.get_ConnectTime
- IADsSession.IdleTime
- IADsSession.get_IdleTime
- IADsSession.User
- IADsSession.get_User
- IADsSession.UserPath
- IADsSession.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf7dd9abe25d731ba63385cd8d632c4212ea349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843440"
---
# <a name="iadssession-property-methods"></a><span data-ttu-id="65ad7-105">IADsSession 屬性方法</span><span class="sxs-lookup"><span data-stu-id="65ad7-105">IADsSession Property Methods</span></span>

<span data-ttu-id="65ad7-106">[**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession)介面的屬性方法會取得或設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="65ad7-106">The property methods of the [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="65ad7-107">如需有關屬性方法的詳細資訊和一般討論，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="65ad7-107">For more information and a general discussion about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="65ad7-108">屬性</span><span class="sxs-lookup"><span data-stu-id="65ad7-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="65ad7-109">**電腦**</span><span class="sxs-lookup"><span data-stu-id="65ad7-109">**Computer**</span></span>
<span data-ttu-id="65ad7-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="65ad7-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="65ad7-111">用戶端工作站的名稱。</span><span class="sxs-lookup"><span data-stu-id="65ad7-111">Name of the client workstation.</span></span>

<dt>

<span data-ttu-id="65ad7-112">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65ad7-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65ad7-113">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="65ad7-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Computer(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="65ad7-114">**ComputerPath**</span><span class="sxs-lookup"><span data-stu-id="65ad7-114">**ComputerPath**</span></span>
<span data-ttu-id="65ad7-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="65ad7-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="65ad7-116">用戶端工作站的電腦物件 ADsPath。</span><span class="sxs-lookup"><span data-stu-id="65ad7-116">ADsPath of the computer object for the client workstation.</span></span>

<dt>

<span data-ttu-id="65ad7-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65ad7-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65ad7-118">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="65ad7-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerPath(
  [out] BSTR* pbstrComputerPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="65ad7-119">**ConnectTime**</span><span class="sxs-lookup"><span data-stu-id="65ad7-119">**ConnectTime**</span></span>
<span data-ttu-id="65ad7-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="65ad7-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="65ad7-121">會話啟動以來經過的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="65ad7-121">Elapsed time, in seconds, since the session started.</span></span>

<dt>

<span data-ttu-id="65ad7-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65ad7-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65ad7-123">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="65ad7-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ConnectTime(
  [out] LONG* plConnectTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="65ad7-124">**IdleTime**</span><span class="sxs-lookup"><span data-stu-id="65ad7-124">**IdleTime**</span></span>
<span data-ttu-id="65ad7-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="65ad7-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="65ad7-126">會話的閒置時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="65ad7-126">Idle time, in seconds, of the session.</span></span>

<dt>

<span data-ttu-id="65ad7-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65ad7-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65ad7-128">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="65ad7-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IdleTime(
  [out] LONG* plIdleTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="65ad7-129">**使用者**</span><span class="sxs-lookup"><span data-stu-id="65ad7-129">**User**</span></span>
<span data-ttu-id="65ad7-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="65ad7-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="65ad7-131">會話使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="65ad7-131">The name of the user of the session.</span></span>

<dt>

<span data-ttu-id="65ad7-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65ad7-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65ad7-133">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="65ad7-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="65ad7-134">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="65ad7-134">**UserPath**</span></span>
<span data-ttu-id="65ad7-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="65ad7-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="65ad7-136">此會話使用者的使用者物件 ADsPath。</span><span class="sxs-lookup"><span data-stu-id="65ad7-136">The ADsPath of the user object for the user of this session.</span></span>

<dt>

<span data-ttu-id="65ad7-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65ad7-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65ad7-138">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="65ad7-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="65ad7-139">範例</span><span class="sxs-lookup"><span data-stu-id="65ad7-139">Examples</span></span>

<span data-ttu-id="65ad7-140">下列程式碼範例顯示如何檢查檔案服務的會話。</span><span class="sxs-lookup"><span data-stu-id="65ad7-140">The following code example shows how to examine sessions for a file service.</span></span>


```VB
Dim fso As IADsFileServiceOperations
On Error GoTo Cleanup

' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate sessions.
If (IsEmpty(fso) = False) Then
    For Each session In fso.sessions
        MsgBox "Session Computer: " & session.Computer
        MsgBox "Session User: " & session.User
    Next Session
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



<span data-ttu-id="65ad7-141">下列程式碼範例會列舉會話的集合。</span><span class="sxs-lookup"><span data-stu-id="65ad7-141">The following code example enumerates a collection of sessions.</span></span>


```C++
IADsFileServiceOperations *pFso = NULL;
IADsSession *pSes = NULL;
IADsCollection *pColl = NULL;
HRESULT hr = S_OK;
IUnknown *pUnk = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IEnumVARIANT *pEnum = NULL;

VariantInit(&var);

LPWSTR adsPath = L"WinNT://aMachine/LanmanServer";

hr = ADsGetObject(adsPath,IID_IADsFileServiceOperations,
                  (void**)&pFso);

if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Sessions(&pColl);

// Enumerate sessions. 
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsSession, (void**)&pSes);
        pSes->get_Computer(&bstr);
        printf("Session host: %S\n",bstr);
        SysFreeString(bstr);

        pSes->get_User(&bstr);
        printf("Session user: %S\n",bstr);
        SysFreeString(bstr);

        pRes->Release();
    }

    VariantClear(&var);
    pDisp=NULL;
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pFso) pFso->Release();
    if(pColl) pColl->Release();
    if(pUnk) pUnk->Release();
    if(pEnum) pEnum->Release();
```



## <a name="requirements"></a><span data-ttu-id="65ad7-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="65ad7-142">Requirements</span></span>



| <span data-ttu-id="65ad7-143">需求</span><span class="sxs-lookup"><span data-stu-id="65ad7-143">Requirement</span></span> | <span data-ttu-id="65ad7-144">值</span><span class="sxs-lookup"><span data-stu-id="65ad7-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65ad7-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65ad7-145">Minimum supported client</span></span><br/> | <span data-ttu-id="65ad7-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65ad7-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65ad7-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65ad7-147">Minimum supported server</span></span><br/> | <span data-ttu-id="65ad7-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65ad7-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65ad7-149">標頭</span><span class="sxs-lookup"><span data-stu-id="65ad7-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="65ad7-150"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="65ad7-150"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="65ad7-151">DLL</span><span class="sxs-lookup"><span data-stu-id="65ad7-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65ad7-152"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65ad7-152"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="65ad7-153">IID</span><span class="sxs-lookup"><span data-stu-id="65ad7-153">IID</span></span><br/>                      | <span data-ttu-id="65ad7-154">IID \_ IADsSession 定義為398B7DA0-4AAB-11CF-AE2C-00AA006EBFB9</span><span class="sxs-lookup"><span data-stu-id="65ad7-154">IID\_IADsSession is defined as 398B7DA0-4AAB-11CF-AE2C-00AA006EBFB9</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="65ad7-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65ad7-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ad7-156">**IADsFileServiceOperations：：會話**</span><span class="sxs-lookup"><span data-stu-id="65ad7-156">**IADsFileServiceOperations::Sessions**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-sessions)
</dt> <dt>

[<span data-ttu-id="65ad7-157">**IADsSession**</span><span class="sxs-lookup"><span data-stu-id="65ad7-157">**IADsSession**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssession)
</dt> </dl>

 

 






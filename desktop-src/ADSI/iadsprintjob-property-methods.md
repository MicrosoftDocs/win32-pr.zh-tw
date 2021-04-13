---
title: 'IADsPrintJob 屬性方法 (Iads .h) '
description: IADsPrintJob 介面的屬性方法會取得或設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 23e7cbf3-09ce-44ce-b618-2c0fa6b34428
ms.tgt_platform: multiple
keywords:
- IADsPrintJob 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsPrintJob Property Methods
- IADsPrintJob.Description
- IADsPrintJob.get_Description
- IADsPrintJob.put_Description
- IADsPrintJob.HostPrintQueue
- IADsPrintJob.get_HostPrintQueue
- IADsPrintJob.Notify
- IADsPrintJob.get_Notify
- IADsPrintJob.put_Notify
- IADsPrintJob.NotifyPath
- IADsPrintJob.get_NotifyPath
- IADsPrintJob.put_NotifyPath
- IADsPrintJob.Priority
- IADsPrintJob.get_Priority
- IADsPrintJob.put_Priority
- IADsPrintJob.Size
- IADsPrintJob.get_Size
- IADsPrintJob.StartTime
- IADsPrintJob.get_StartTime
- IADsPrintJob.put_StartTime
- IADsPrintJob.TimeSubmitted
- IADsPrintJob.get_TimeSubmitted
- IADsPrintJob.TotalPages
- IADsPrintJob.get_TotalPages
- IADsPrintJob.UntilTime
- IADsPrintJob.get_UntilTime
- IADsPrintJob.User
- IADsPrintJob.get_User
- IADsPrintJob.UserPath
- IADsPrintJob.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1680484ff16d563ef5bc89de6d5abbfec2ce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466244"
---
# <a name="iadsprintjob-property-methods"></a><span data-ttu-id="229cd-105">IADsPrintJob 屬性方法</span><span class="sxs-lookup"><span data-stu-id="229cd-105">IADsPrintJob Property Methods</span></span>

<span data-ttu-id="229cd-106">[**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)介面的屬性方法會取得或設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="229cd-106">Property methods for the [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="229cd-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="229cd-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="229cd-108">屬性</span><span class="sxs-lookup"><span data-stu-id="229cd-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="229cd-109">**說明**</span><span class="sxs-lookup"><span data-stu-id="229cd-109">**Description**</span></span>
<span data-ttu-id="229cd-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="229cd-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="229cd-111">列印工作的描述。</span><span class="sxs-lookup"><span data-stu-id="229cd-111">The description of the print job.</span></span>

<dt>

<span data-ttu-id="229cd-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="229cd-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="229cd-113">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="229cd-113">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="229cd-114">**HostPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="229cd-114">**HostPrintQueue**</span></span>
<span data-ttu-id="229cd-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="229cd-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="229cd-116">處理列印工作之列印佇列的 ADsPath 字串。</span><span class="sxs-lookup"><span data-stu-id="229cd-116">The ADsPath string of the Print Queue that processes the print job.</span></span>

<dt>

<span data-ttu-id="229cd-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="229cd-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="229cd-118">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="229cd-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostPrintQueue(
  [out] BSTR* pbstrHostPrintQueue
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="229cd-119">**通知**</span><span class="sxs-lookup"><span data-stu-id="229cd-119">**Notify**</span></span>
<span data-ttu-id="229cd-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="229cd-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="229cd-121">作業完成時要通知的使用者。</span><span class="sxs-lookup"><span data-stu-id="229cd-121">The user to be notified when job is completed.</span></span>

<dt>

<span data-ttu-id="229cd-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="229cd-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="229cd-123">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="229cd-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Notify(
  [out] BSTR* pbstrNotify
);
HRESULT put_Notify(
  [in] BSTR bstrNotify
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="229cd-124">**NotifyPath**</span><span class="sxs-lookup"><span data-stu-id="229cd-124">**NotifyPath**</span></span>
<span data-ttu-id="229cd-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="229cd-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="229cd-126">要在列印工作完成時收到通知之使用者物件的 ADsPath 字串。</span><span class="sxs-lookup"><span data-stu-id="229cd-126">The ADsPath string of the user object to be notified when the print job is completed.</span></span>

<dt>

<span data-ttu-id="229cd-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="229cd-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="229cd-128">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="229cd-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NotifyPath(
  [out] BSTR* pbstrNotifyPath
);
HRESULT put_NotifyPath(
  [in] BSTR bstrNotifyPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="229cd-129">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="229cd-129">**Priority**</span></span>
<span data-ttu-id="229cd-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="229cd-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="229cd-131">列印工作的優先順序。</span><span class="sxs-lookup"><span data-stu-id="229cd-131">The priority of the print job.</span></span>

<dt>

<span data-ttu-id="229cd-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="229cd-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="229cd-133">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="229cd-133">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Priority(
  [out] LONG* plPriority
);
HRESULT put_Priority(
  [in] LONG lPriority
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="229cd-134">**大小**</span><span class="sxs-lookup"><span data-stu-id="229cd-134">**Size**</span></span>
<span data-ttu-id="229cd-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="229cd-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="229cd-136">列印工作的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="229cd-136">The size, in bytes, of the print job.</span></span>

<dt>

<span data-ttu-id="229cd-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="229cd-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="229cd-138">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="229cd-138">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Size(
  [out] LONG* plSize
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="229cd-139">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="229cd-139">**StartTime**</span></span>
<span data-ttu-id="229cd-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="229cd-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="229cd-141">應該啟動列印工作的最早時間。</span><span class="sxs-lookup"><span data-stu-id="229cd-141">The earliest time when the print job should be started.</span></span>

<dt>

<span data-ttu-id="229cd-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="229cd-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="229cd-143">腳本資料類型： **日期**</span><span class="sxs-lookup"><span data-stu-id="229cd-143">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartTime(
  [out] DATE* pdateStartTime
);
HRESULT put_StartTime(
  [in] DATE dateStartTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="229cd-144">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="229cd-144">**TimeSubmitted**</span></span>
<span data-ttu-id="229cd-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="229cd-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="229cd-146">將作業提交至佇列的時間。</span><span class="sxs-lookup"><span data-stu-id="229cd-146">The time when the job was submitted to the queue.</span></span>

<dt>

<span data-ttu-id="229cd-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="229cd-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="229cd-148">腳本資料類型： **日期**</span><span class="sxs-lookup"><span data-stu-id="229cd-148">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeSubmitted(
  [out] DATE* pdateTimeSubmitted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="229cd-149">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="229cd-149">**TotalPages**</span></span>
<span data-ttu-id="229cd-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="229cd-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="229cd-151">列印工作中的總頁數。</span><span class="sxs-lookup"><span data-stu-id="229cd-151">The total number of pages in the print job.</span></span>

<dt>

<span data-ttu-id="229cd-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="229cd-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="229cd-153">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="229cd-153">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TotalPages(
  [out] LONG* plTotalPages
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="229cd-154">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="229cd-154">**UntilTime**</span></span>
<span data-ttu-id="229cd-155"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="229cd-155"></dt> <dd> <dl></span></span>

<span data-ttu-id="229cd-156">應開始列印工作的最晚時間。</span><span class="sxs-lookup"><span data-stu-id="229cd-156">The latest time when the print job should be started.</span></span>

<dt>

<span data-ttu-id="229cd-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="229cd-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="229cd-158">腳本資料類型： **日期**</span><span class="sxs-lookup"><span data-stu-id="229cd-158">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UntilTime(
  [out] DATE* pdateUntilTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="229cd-159">**使用者**</span><span class="sxs-lookup"><span data-stu-id="229cd-159">**User**</span></span>
<span data-ttu-id="229cd-160"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="229cd-160"></dt> <dd> <dl></span></span>

<span data-ttu-id="229cd-161">提交列印工作的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="229cd-161">The name of user who submitted the print job.</span></span>

<dt>

<span data-ttu-id="229cd-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="229cd-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="229cd-163">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="229cd-163">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="229cd-164">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="229cd-164">**UserPath**</span></span>
<span data-ttu-id="229cd-165"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="229cd-165"></dt> <dd> <dl></span></span>

<span data-ttu-id="229cd-166">提交此列印工作之使用者物件的 ADsPath 字串。</span><span class="sxs-lookup"><span data-stu-id="229cd-166">The ADsPath string of the user object that submitted this print job.</span></span>

<dt>

<span data-ttu-id="229cd-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="229cd-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="229cd-168">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="229cd-168">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="229cd-169">範例</span><span class="sxs-lookup"><span data-stu-id="229cd-169">Examples</span></span>

<span data-ttu-id="229cd-170">下列程式碼範例示範如何使用列印工作物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="229cd-170">The following code example shows how to work with properties of a print job object.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Dim pj As IADsPrintJob
On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    MsgBox "Host Printer: " & pj.HostPrintQueue
    MsgBox "Job description: " & pj.Description
    MsgBox "job requester: " & pj.User 
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pj = Nothing
```



<span data-ttu-id="229cd-171">下列程式碼範例示範如何使用列印工作物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="229cd-171">The following code example shows how to work with properties of a print job object.</span></span>


```C++
IADsPrintQueueOperations *pqo = NULL;
IADsPrintJob *pJob = NULL;
HRESULT hr = S_OK;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
LPWSTR adsPath =L"WinNT://aMachine/aPrinter";

VariantInit(&var);

hr = ADsGetObject(adsPath, 
                  IID_IADsPrintQueueOperations, 
                  (void**)&pqo);
if(FAILED(hr)){goto Cleanup;}


hr = pqo->PrintJobs(&pColl);

// Enumerate print jobs. Code omitted.

hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)){goto Cleanup;}


IEnumVARIANT *pEnum;
hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)){goto Cleanup;}


// Now Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
if(FAILED(hr)){goto Cleanup;}

while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsPrintJob, (void**)&pJob);

        pJob->get_HostPrintQueue(&bstr);
        printf("HostPrintQueue: %S\n",bstr);
        SysFreeString(bstr);

        pJob->get_Description(&bstr);
        printf("Print job name: %S\n",bstr);
        SysFreeString(bstr);

        pJob->get_User(&bstr);
        printf("Requester: %S\n",bstr);
        SysFreeString(bstr);

        pJob->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pqo) pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="229cd-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="229cd-172">Requirements</span></span>



| <span data-ttu-id="229cd-173">需求</span><span class="sxs-lookup"><span data-stu-id="229cd-173">Requirement</span></span> | <span data-ttu-id="229cd-174">值</span><span class="sxs-lookup"><span data-stu-id="229cd-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="229cd-175">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="229cd-175">Minimum supported client</span></span><br/> | <span data-ttu-id="229cd-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="229cd-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="229cd-177">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="229cd-177">Minimum supported server</span></span><br/> | <span data-ttu-id="229cd-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="229cd-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="229cd-179">標頭</span><span class="sxs-lookup"><span data-stu-id="229cd-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="229cd-180"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="229cd-180"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="229cd-181">DLL</span><span class="sxs-lookup"><span data-stu-id="229cd-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="229cd-182"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="229cd-182"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="229cd-183">IID</span><span class="sxs-lookup"><span data-stu-id="229cd-183">IID</span></span><br/>                      | <span data-ttu-id="229cd-184">IID \_ IADsPrintJob 定義為32FB6780-1ED0-11CF-A988-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="229cd-184">IID\_IADsPrintJob is defined as 32FB6780-1ED0-11CF-A988-00AA006BC149</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="229cd-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="229cd-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="229cd-186">**IADsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="229cd-186">**IADsPrintJob**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[<span data-ttu-id="229cd-187">介面屬性方法</span><span class="sxs-lookup"><span data-stu-id="229cd-187">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 






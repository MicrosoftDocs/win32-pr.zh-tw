---
title: 'IADsPrintQueue 屬性方法 (Iads .h) '
description: IADsPrintQueue 介面的屬性方法會取得或設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 7f5b4200-65c8-4230-8561-ad4fefb391f3
ms.tgt_platform: multiple
keywords:
- IADsPrintQueue 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsPrintQueue Property Methods
- IADsPrintQueue.BannerPage
- IADsPrintQueue.get_BannerPage
- IADsPrintQueue.put_BannerPage
- IADsPrintQueue.Datatype
- IADsPrintQueue.get_Datatype
- IADsPrintQueue.put_Datatype
- IADsPrintQueue.DefaultJobPriority
- IADsPrintQueue.get_DefaultJobPriority
- IADsPrintQueue.put_DefaultJobPriority
- IADsPrintQueue.Description
- IADsPrintQueue.get_Description
- IADsPrintQueue.put_Description
- IADsPrintQueue.HostComputer
- IADsPrintQueue.get_HostComputer
- IADsPrintQueue.put_HostComputer
- IADsPrintQueue.Location
- IADsPrintQueue.get_Location
- IADsPrintQueue.put_Location
- IADsPrintQueue.Model
- IADsPrintQueue.get_Model
- IADsPrintQueue.put_Model
- IADsPrintQueue.PrintDevices
- IADsPrintQueue.get_PrintDevices
- IADsPrintQueue.put_PrintDevices
- IADsPrintQueue.PrinterPath
- IADsPrintQueue.get_PrinterPath
- IADsPrintQueue.put_PrinterPath
- IADsPrintQueue.PrintProcessor
- IADsPrintQueue.get_PrintProcessor
- IADsPrintQueue.put_PrintProcessor
- IADsPrintQueue.Priority
- IADsPrintQueue.get_Priority
- IADsPrintQueue.put_Priority
- IADsPrintQueue.StartTime
- IADsPrintQueue.get_StartTime
- IADsPrintQueue.put_StartTime
- IADsPrintQueue.UntilTime
- IADsPrintQueue.get_UntilTime
- IADsPrintQueue.put_UntilTime
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e8b7b2260805dbf5fa144f239111b6e29f5ec78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187296"
---
# <a name="iadsprintqueue-property-methods"></a><span data-ttu-id="91043-105">IADsPrintQueue 屬性方法</span><span class="sxs-lookup"><span data-stu-id="91043-105">IADsPrintQueue Property Methods</span></span>

<span data-ttu-id="91043-106">[**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)介面的屬性方法會取得或設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="91043-106">The property methods of the [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="91043-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="91043-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="91043-108">屬性</span><span class="sxs-lookup"><span data-stu-id="91043-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="91043-109">**BannerPage**</span><span class="sxs-lookup"><span data-stu-id="91043-109">**BannerPage**</span></span>
<span data-ttu-id="91043-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="91043-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="91043-111">指向用來分隔列印工作之橫幅頁面的檔案系統路徑。</span><span class="sxs-lookup"><span data-stu-id="91043-111">The file system path that points to the banner page used to separate print jobs.</span></span> <span data-ttu-id="91043-112">如果是 **Null**，則不會使用任何橫幅頁面。</span><span class="sxs-lookup"><span data-stu-id="91043-112">If **NULL**, no banner page is used.</span></span>

<dt>

<span data-ttu-id="91043-113">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="91043-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="91043-114">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="91043-114">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BannerPage(
  [out] BSTR* pbstrBannerPage
);
HRESULT put_BannerPage(
  [in] BSTR bstrBannerPage
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="91043-115">**資料類型**</span><span class="sxs-lookup"><span data-stu-id="91043-115">**Datatype**</span></span>
<span data-ttu-id="91043-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="91043-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="91043-117">此佇列可以處理的資料類型。</span><span class="sxs-lookup"><span data-stu-id="91043-117">The data type that can be processed by this queue.</span></span>

<dt>

<span data-ttu-id="91043-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="91043-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="91043-119">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="91043-119">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Datatype(
  [out] BSTR* pbstrDatatype
);
HRESULT put_Datatype(
  [in] BSTR bstrDatatype
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="91043-120">**DefaultJobPriority**</span><span class="sxs-lookup"><span data-stu-id="91043-120">**DefaultJobPriority**</span></span>
<span data-ttu-id="91043-121"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="91043-121"></dt> <dd> <dl></span></span>

<span data-ttu-id="91043-122">指派給每個列印工作的預設優先順序。</span><span class="sxs-lookup"><span data-stu-id="91043-122">The default priority assigned to each print job.</span></span>

<dt>

<span data-ttu-id="91043-123">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="91043-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="91043-124">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="91043-124">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultJobPriority(
  [out] LONG* plDefaultJobPriority
);
HRESULT put_DefaultJobPriority(
  [in] BSTR lDefaultJobPriority
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="91043-125">**說明**</span><span class="sxs-lookup"><span data-stu-id="91043-125">**Description**</span></span>
<span data-ttu-id="91043-126"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="91043-126"></dt> <dd> <dl></span></span>

<span data-ttu-id="91043-127">此列印佇列的文字描述。</span><span class="sxs-lookup"><span data-stu-id="91043-127">The text description of this print queue.</span></span>

<dt>

<span data-ttu-id="91043-128">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="91043-128">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="91043-129">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="91043-129">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="91043-130">**HostComputer**</span><span class="sxs-lookup"><span data-stu-id="91043-130">**HostComputer**</span></span>
<span data-ttu-id="91043-131"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="91043-131"></dt> <dd> <dl></span></span>

<span data-ttu-id="91043-132">參考主機電腦的 ADsPath 字串。</span><span class="sxs-lookup"><span data-stu-id="91043-132">The ADsPath string that references the host computer.</span></span>

<dt>

<span data-ttu-id="91043-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="91043-133">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="91043-134">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="91043-134">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="91043-135">**位置**</span><span class="sxs-lookup"><span data-stu-id="91043-135">**Location**</span></span>
<span data-ttu-id="91043-136"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="91043-136"></dt> <dd> <dl></span></span>

<span data-ttu-id="91043-137">由系統管理員所描述的佇列位置。</span><span class="sxs-lookup"><span data-stu-id="91043-137">The location of the queue as described by an administrator.</span></span>

<dt>

<span data-ttu-id="91043-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="91043-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="91043-139">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="91043-139">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Location(
  [out] BSTR* pbstrLocation
);
HRESULT put_Location(
  [in] BSTR bstrLocation
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="91043-140">**型號**</span><span class="sxs-lookup"><span data-stu-id="91043-140">**Model**</span></span>
<span data-ttu-id="91043-141"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="91043-141"></dt> <dd> <dl></span></span>

<span data-ttu-id="91043-142">此列印佇列所使用的驅動程式名稱。</span><span class="sxs-lookup"><span data-stu-id="91043-142">The name of the driver used by this print queue.</span></span>

<dt>

<span data-ttu-id="91043-143">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="91043-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="91043-144">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="91043-144">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Model(
  [out] BSTR* pbstrModel
);
HRESULT put_Model(
  [in] BSTR bstrModel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="91043-145">**PrintDevices**</span><span class="sxs-lookup"><span data-stu-id="91043-145">**PrintDevices**</span></span>
<span data-ttu-id="91043-146"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="91043-146"></dt> <dd> <dl></span></span>

<span data-ttu-id="91043-147">**BSTR** 的 SAFEARRAY，包含這個列印佇列將工作後臺緩衝的列印裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="91043-147">A SAFEARRAY of **BSTR** that contains the names of the print devices to which this print queue spools jobs.</span></span>

<dt>

<span data-ttu-id="91043-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="91043-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="91043-149">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="91043-149">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintDevices(
  [out] VARIANT* pvPrintDevices
);
HRESULT put_PrintDevices(
  [in] VARIANT vPrintDevices
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="91043-150">**PrinterPath**</span><span class="sxs-lookup"><span data-stu-id="91043-150">**PrinterPath**</span></span>
<span data-ttu-id="91043-151"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="91043-151"></dt> <dd> <dl></span></span>

<span data-ttu-id="91043-152">參考可存取共用印表機之路徑的字串。</span><span class="sxs-lookup"><span data-stu-id="91043-152">The string that references the path by which a shared printer can be accessed.</span></span>

<dt>

<span data-ttu-id="91043-153">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="91043-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="91043-154">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="91043-154">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrinterPath(
  [out] BSTR* pbstrPrinterPath
);
HRESULT put_PrinterPath(
  [in] BSTR bstrPrinterPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="91043-155">**PrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="91043-155">**PrintProcessor**</span></span>
<span data-ttu-id="91043-156"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="91043-156"></dt> <dd> <dl></span></span>

<span data-ttu-id="91043-157">與此佇列相關聯的列印處理器。</span><span class="sxs-lookup"><span data-stu-id="91043-157">The print processor associated with this queue.</span></span>

<dt>

<span data-ttu-id="91043-158">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="91043-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="91043-159">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="91043-159">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintProcessor(
  [out] BSTR* pbstrPrintProcessor
);
HRESULT put_PrintProcessor(
  [in] BSTR bstrPrintProcessor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="91043-160">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="91043-160">**Priority**</span></span>
<span data-ttu-id="91043-161"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="91043-161"></dt> <dd> <dl></span></span>

<span data-ttu-id="91043-162">此印表機物件工作佇列的所有已連線裝置的優先順序。</span><span class="sxs-lookup"><span data-stu-id="91043-162">The priority of this printer object job queue for any connected devices.</span></span> <span data-ttu-id="91043-163">較高優先順序的列印佇列物件中的所有工作都會先處理。</span><span class="sxs-lookup"><span data-stu-id="91043-163">All jobs in higher priority print queue objects will be processed first.</span></span>

<dt>

<span data-ttu-id="91043-164">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="91043-164">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="91043-165">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="91043-165">Scripting data type: **LONG**</span></span>
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

<span data-ttu-id="91043-166">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="91043-166">**StartTime**</span></span>
<span data-ttu-id="91043-167"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="91043-167"></dt> <dd> <dl></span></span>

<span data-ttu-id="91043-168">佇列應開始處理工作的時間。</span><span class="sxs-lookup"><span data-stu-id="91043-168">The time when the queue should begin processing jobs.</span></span> <span data-ttu-id="91043-169">時間的日期部分會被忽略。</span><span class="sxs-lookup"><span data-stu-id="91043-169">The date portion of the time is ignored.</span></span>

<dt>

<span data-ttu-id="91043-170">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="91043-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="91043-171">腳本資料類型： **日期**</span><span class="sxs-lookup"><span data-stu-id="91043-171">Scripting data type: **DATE**</span></span>
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

<span data-ttu-id="91043-172">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="91043-172">**UntilTime**</span></span>
<span data-ttu-id="91043-173"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="91043-173"></dt> <dd> <dl></span></span>

<span data-ttu-id="91043-174">佇列應該停止處理工作的時間。</span><span class="sxs-lookup"><span data-stu-id="91043-174">The time when the queue should stop processing jobs.</span></span>

<dt>

<span data-ttu-id="91043-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="91043-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="91043-176">腳本資料類型： **日期**</span><span class="sxs-lookup"><span data-stu-id="91043-176">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UntilTime(
  [out] DATE* pdateUntilTime
);
HRESULT put_UntilTime(
  [in] DATE dateUntilTime
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="91043-177">範例</span><span class="sxs-lookup"><span data-stu-id="91043-177">Examples</span></span>

<span data-ttu-id="91043-178">下列程式碼範例顯示如何判斷指定的印表機是否在線上或離線。</span><span class="sxs-lookup"><span data-stu-id="91043-178">The following code example shows how to determine if a specified printer is online or offline.</span></span>


```VB
Dim pq As IADsPrintQueue
Dim pqo As IADsPrintQueueOperations
On Error GoTo Cleanup
 
Set pq = GetObject("WinNT://aMachine/aPrinter")
Set pqo = pq
If pqo.status = ADS_PRINTER_OFFLINE Then
    MsgBox pq.Model & "@" & pq.Location & is offline."
Else
    MsgBox pq.Model & "@" & pq.Location & is online."
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pq = Nothing
    Set pqo = Nothing
```



<span data-ttu-id="91043-179">下列程式碼範例顯示如何判斷指定的印表機是否在線上或離線。</span><span class="sxs-lookup"><span data-stu-id="91043-179">The following code example shows how to determine if a specified printer is online or offline.</span></span>


```C++
IADsPrintQueue *pq = NULL;
HRESULT hr = S_OK;
IADsPrintQueueOperations *pqo = NULL;
BSTR model = NULL;
BSTR location = NULL;

LPWSTR adsPath = L"WinNT://aMachine/aPrinter";
hr = ADsGetObject(adsPath,
                  IID_IADsPrintQueue,
                  (void**)&pq);
if(FAILED(hr)) {goto Cleanup;}


hr = pq->QueryInterface(IID_IADsPrintQueueOperations,(void**)&pqo);
if(FAILED(hr)) {goto Cleanup;}

long status;
hr = pqo->get_Status(&status);
if(FAILED(hr)) {goto Cleanup;}

hr = pq->get_Model(&model);
if(FAILED(hr)) {goto Cleanup;}

hr =pq->get_Location(&location);
if(FAILED(hr)) {goto Cleanup;}

if(status == ADS_PRINTER_OFFLINE) 
{
    printf("%S @ %S is offline.\n",model,location);
} 
else 
{
    printf("%S @ %S is online.\n",model,location);
}


Cleanup:
    SysFreeString(model);
    SysFreeString(location);
    if(pq) pq->Release();
    if(pqo) pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="91043-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="91043-180">Requirements</span></span>



| <span data-ttu-id="91043-181">需求</span><span class="sxs-lookup"><span data-stu-id="91043-181">Requirement</span></span> | <span data-ttu-id="91043-182">值</span><span class="sxs-lookup"><span data-stu-id="91043-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91043-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91043-183">Minimum supported client</span></span><br/> | <span data-ttu-id="91043-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91043-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91043-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91043-185">Minimum supported server</span></span><br/> | <span data-ttu-id="91043-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91043-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91043-187">標頭</span><span class="sxs-lookup"><span data-stu-id="91043-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="91043-188"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="91043-188"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="91043-189">DLL</span><span class="sxs-lookup"><span data-stu-id="91043-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91043-190"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91043-190"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="91043-191">IID</span><span class="sxs-lookup"><span data-stu-id="91043-191">IID</span></span><br/>                      | <span data-ttu-id="91043-192">IID \_ IADsPrintQueue 定義為 B15160D0-1226-11CF-A985-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="91043-192">IID\_IADsPrintQueue is defined as B15160D0-1226-11CF-A985-00AA006BC149</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="91043-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91043-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91043-194">**IADsPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="91043-194">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="91043-195">介面屬性方法</span><span class="sxs-lookup"><span data-stu-id="91043-195">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 






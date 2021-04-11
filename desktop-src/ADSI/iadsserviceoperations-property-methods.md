---
title: 'IADsServiceOperations 屬性方法 (Iads .h) '
description: IADsServiceOperations 介面的屬性方法會讀取並寫入下列清單中所述的屬性。 如需屬性方法的詳細資訊，請參閱介面屬性方法。
ms.assetid: ebddfc42-1d2f-495b-b57c-f57419b54ff8
ms.tgt_platform: multiple
keywords:
- IADsServiceOperations 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsServiceOperations Property Methods
- IADsServiceOperations.Status
- IADsServiceOperations.get_Status
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 654a92be1052d4e4c70e0274d719a49be965d8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843443"
---
# <a name="iadsserviceoperations-property-methods"></a><span data-ttu-id="02180-105">IADsServiceOperations 屬性方法</span><span class="sxs-lookup"><span data-stu-id="02180-105">IADsServiceOperations Property Methods</span></span>

<span data-ttu-id="02180-106">[**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)介面的屬性方法會讀取並寫入下列清單中所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="02180-106">The property methods of the [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) interface read and write the properties described in the following list.</span></span> <span data-ttu-id="02180-107">如需屬性方法的詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="02180-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="02180-108">屬性</span><span class="sxs-lookup"><span data-stu-id="02180-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="02180-109">**狀態**</span><span class="sxs-lookup"><span data-stu-id="02180-109">**Status**</span></span>
<span data-ttu-id="02180-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="02180-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="02180-111">服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="02180-111">Status of service.</span></span>

<span data-ttu-id="02180-112">以下是可能的值。</span><span class="sxs-lookup"><span data-stu-id="02180-112">The following are possible values.</span></span>

<dt>

<span id="ADS_SERVICE_STOPPED"></span><span id="ads_service_stopped"></span>

<span data-ttu-id="02180-113">**廣告 \_服務 \_ 已停止** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="02180-113">**ADS\_SERVICE\_STOPPED** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_START_PENDING"></span><span id="ads_service_start_pending"></span>

<span data-ttu-id="02180-114">**廣告 \_服務 \_ 開始 \_ 暫** 止 (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="02180-114">**ADS\_SERVICE\_START\_PENDING** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_STOP_PENDING"></span><span id="ads_service_stop_pending"></span>

<span data-ttu-id="02180-115">**廣告 \_服務 \_ 停止 \_ 暫** 止 (0x00000003) </span><span class="sxs-lookup"><span data-stu-id="02180-115">**ADS\_SERVICE\_STOP\_PENDING** (0x00000003)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_RUNNING"></span><span id="ads_service_running"></span>

<span data-ttu-id="02180-116">**廣告 \_服務 \_ 正在** 執行 (0x00000004) </span><span class="sxs-lookup"><span data-stu-id="02180-116">**ADS\_SERVICE\_RUNNING** (0x00000004)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_CONTINUE_PENDING"></span><span id="ads_service_continue_pending"></span>

<span data-ttu-id="02180-117">**廣告 \_服務 \_ 繼續 \_ 擱置** (0x00000005) </span><span class="sxs-lookup"><span data-stu-id="02180-117">**ADS\_SERVICE\_CONTINUE\_PENDING** (0x00000005)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSE_PENDING"></span><span id="ads_service_pause_pending"></span>

<span data-ttu-id="02180-118">**廣告 \_服務 \_ 暫停 \_ 暫** 止 (0x00000006) </span><span class="sxs-lookup"><span data-stu-id="02180-118">**ADS\_SERVICE\_PAUSE\_PENDING** (0x00000006)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSED"></span><span id="ads_service_paused"></span>

<span data-ttu-id="02180-119">**廣告 \_服務已 \_ 暫停** (0x00000007) </span><span class="sxs-lookup"><span data-stu-id="02180-119">**ADS\_SERVICE\_PAUSED** (0x00000007)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR"></span><span id="ads_service_error"></span>

<span data-ttu-id="02180-120">**廣告 \_服務 \_ 錯誤** (0x00000008) </span><span class="sxs-lookup"><span data-stu-id="02180-120">**ADS\_SERVICE\_ERROR** (0x00000008)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

<span data-ttu-id="02180-121">**廣告 \_服務 \_ 自己的 \_ 進程** (0x00000010) </span><span class="sxs-lookup"><span data-stu-id="02180-121">**ADS\_SERVICE\_OWN\_PROCESS** (0x00000010)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

<span data-ttu-id="02180-122">**廣告 \_服務 \_ 共用 \_ 進程** (0x00000020) </span><span class="sxs-lookup"><span data-stu-id="02180-122">**ADS\_SERVICE\_SHARE\_PROCESS** (0x00000020)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

<span data-ttu-id="02180-123">**廣告 \_服務 \_ 核心 \_ 驅動程式** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="02180-123">**ADS\_SERVICE\_KERNEL\_DRIVER** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

<span data-ttu-id="02180-124">**廣告 \_服務 \_ 檔 \_ 系統 \_ 驅動程式** (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="02180-124">**ADS\_SERVICE\_FILE\_SYSTEM\_DRIVER** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span data-ttu-id="02180-125">**廣告 \_服務 \_ 開機 \_** 啟動 (服務 \_ 啟動 \_) </span><span class="sxs-lookup"><span data-stu-id="02180-125">**ADS\_SERVICE\_BOOT\_START** (SERVICE\_BOOT\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span data-ttu-id="02180-126">**廣告 \_服務 \_ 系統 \_ 啟動** (service \_ system \_ 啟動) </span><span class="sxs-lookup"><span data-stu-id="02180-126">**ADS\_SERVICE\_SYSTEM\_START** (SERVICE\_SYSTEM\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span data-ttu-id="02180-127">**廣告 \_服務 \_ 自動 \_ 啟動** (服務 \_ 自動 \_ 啟動) </span><span class="sxs-lookup"><span data-stu-id="02180-127">**ADS\_SERVICE\_AUTO\_START** (SERVICE\_AUTO\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span data-ttu-id="02180-128">**廣告 \_服務 \_ 需求 \_ 開始** (服務 \_ 需求 \_ 開始) </span><span class="sxs-lookup"><span data-stu-id="02180-128">**ADS\_SERVICE\_DEMAND\_START** (SERVICE\_DEMAND\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span data-ttu-id="02180-129">**廣告 \_停 \_ 用服務** (服務 \_ 已停用) </span><span class="sxs-lookup"><span data-stu-id="02180-129">**ADS\_SERVICE\_DISABLED** (SERVICE\_DISABLED)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span data-ttu-id="02180-130">**廣告 \_服務 \_ 錯誤 \_ 忽略** (0) </span><span class="sxs-lookup"><span data-stu-id="02180-130">**ADS\_SERVICE\_ERROR\_IGNORE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span data-ttu-id="02180-131">**廣告 \_服務 \_ 錯誤 \_ 一般** (1) </span><span class="sxs-lookup"><span data-stu-id="02180-131">**ADS\_SERVICE\_ERROR\_NORMAL** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span data-ttu-id="02180-132">**廣告 \_服務 \_ 錯誤 \_ 嚴重** (2) </span><span class="sxs-lookup"><span data-stu-id="02180-132">**ADS\_SERVICE\_ERROR\_SEVERE** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span data-ttu-id="02180-133">**廣告 \_服務 \_ 錯誤 \_ 嚴重** (3) </span><span class="sxs-lookup"><span data-stu-id="02180-133">**ADS\_SERVICE\_ERROR\_CRITICAL** (3)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="02180-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02180-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02180-135">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="02180-135">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* pstatus
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="02180-136">範例</span><span class="sxs-lookup"><span data-stu-id="02180-136">Examples</span></span>

<span data-ttu-id="02180-137">下列程式碼範例示範如何確認 Windows 2000 上執行的 Microsoft 傳真服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="02180-137">The following code example shows how to verify the status of a Microsoft Fax Service running on Windows 2000.</span></span>


```VB
Dim cp As IADsComputer
Dim sr As IADsService
Dim so As IADsServiceOperations
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
Set sr = cp.GetObject("Service", "Fax")
Set so = sr

Select Case so.Status
    Case ADS_SERVICE_STOPPED
        MsgBox "Microsoft Fax Service has stopped."
    Case ADS_SERVICE_RUNNING
        MsgBox "Microsoft Fax Service is running."
    Case ADS_SERVICE_PAUSED
        MsgBox "Microsoft Fax Service has paused."
    Case ADS_SERVICE_ERROR
        MsgBox "Microsoft Fax Service has errors."
End Select

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
    Set sr = Nothing
    Set so = Nothing
```



<span data-ttu-id="02180-138">下列程式碼範例會驗證 Windows 2000 上執行的 Microsoft 傳真服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="02180-138">The following code example verifies the status of a Microsoft Fax Service running on Windows 2000.</span></span>


```C++
IADsContainer *pCont = NULL;
IADsServiceOperations *pSrvOp = NULL;
LPWSTR adsPath = L"WinNT://myMachine,computer";
IDispatch *pDisp = NULL;
long status = 0;

HRESULT hr = S_OK;

hr = ADsGetObject(adsPath,IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->GetObject(CComBSTR("Service"), CComBSTR("Fax"), &pDisp);
if(FAILED(hr)) {goto Cleanup;}

hr = pDisp->QueryInterface(IID_IADsServiceOperations,(void**)&pSrvOp);
if(FAILED(hr)) {goto Cleanup;}

hr = pSrvOp->get_Status(&status);
switch (status) 
{
    case ADS_SERVICE_STOPPED:
        printf("The service has stopped.\n");
        break;
    case ADS_SERVICE_RUNNING:
        printf("The service is running.\n");
        break;
    case ADS_SERVICE_PAUSED:
        printf("The service has paused.\n");
        break;
    case ADS_SERVICE_ERROR:
        printf("The service has errors.\n");
        break;
}

Cleanup:
    if(pDisp) pDisp->Release();
    if(pCont) pCont->Release();
    if(pSrvOp) pSrvOp->Release();
```



## <a name="requirements"></a><span data-ttu-id="02180-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="02180-139">Requirements</span></span>



| <span data-ttu-id="02180-140">需求</span><span class="sxs-lookup"><span data-stu-id="02180-140">Requirement</span></span> | <span data-ttu-id="02180-141">值</span><span class="sxs-lookup"><span data-stu-id="02180-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="02180-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02180-142">Minimum supported client</span></span><br/> | <span data-ttu-id="02180-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02180-143">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="02180-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02180-144">Minimum supported server</span></span><br/> | <span data-ttu-id="02180-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02180-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="02180-146">標頭</span><span class="sxs-lookup"><span data-stu-id="02180-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="02180-147"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="02180-147"><dt>Iads.h</dt></span></span> </dl>        |
| <span data-ttu-id="02180-148">DLL</span><span class="sxs-lookup"><span data-stu-id="02180-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02180-149"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02180-149"><dt>Activeds.dll</dt></span></span> </dl>  |
| <span data-ttu-id="02180-150">IID</span><span class="sxs-lookup"><span data-stu-id="02180-150">IID</span></span><br/>                      | <span data-ttu-id="02180-151">IID \_ IADsServiceOperations 定義為5D7B33F0-31CA-11CF-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="02180-151">IID\_IADsServiceOperations is defined as 5D7B33F0-31CA-11CF-A98A-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02180-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02180-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02180-153">**IADsFileService**</span><span class="sxs-lookup"><span data-stu-id="02180-153">**IADsFileService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[<span data-ttu-id="02180-154">**IADsFileServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="02180-154">**IADsFileServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[<span data-ttu-id="02180-155">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="02180-155">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="02180-156">**IADsServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="02180-156">**IADsServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> </dl>

 

 






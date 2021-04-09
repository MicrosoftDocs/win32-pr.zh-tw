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
# <a name="iadsserviceoperations-property-methods"></a>IADsServiceOperations 屬性方法

[**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)介面的屬性方法會讀取並寫入下列清單中所述的屬性。 如需屬性方法的詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**狀態**
</dt> <dd> <dl>

服務的狀態。

以下是可能的值。

<dt>

<span id="ADS_SERVICE_STOPPED"></span><span id="ads_service_stopped"></span>

**廣告 \_服務 \_ 已停止** (0x00000001) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_START_PENDING"></span><span id="ads_service_start_pending"></span>

**廣告 \_服務 \_ 開始 \_ 暫** 止 (0x00000002) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_STOP_PENDING"></span><span id="ads_service_stop_pending"></span>

**廣告 \_服務 \_ 停止 \_ 暫** 止 (0x00000003) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_RUNNING"></span><span id="ads_service_running"></span>

**廣告 \_服務 \_ 正在** 執行 (0x00000004) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_CONTINUE_PENDING"></span><span id="ads_service_continue_pending"></span>

**廣告 \_服務 \_ 繼續 \_ 擱置** (0x00000005) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSE_PENDING"></span><span id="ads_service_pause_pending"></span>

**廣告 \_服務 \_ 暫停 \_ 暫** 止 (0x00000006) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSED"></span><span id="ads_service_paused"></span>

**廣告 \_服務已 \_ 暫停** (0x00000007) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR"></span><span id="ads_service_error"></span>

**廣告 \_服務 \_ 錯誤** (0x00000008) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

**廣告 \_服務 \_ 自己的 \_ 進程** (0x00000010) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

**廣告 \_服務 \_ 共用 \_ 進程** (0x00000020) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

**廣告 \_服務 \_ 核心 \_ 驅動程式** (0x00000001) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

**廣告 \_服務 \_ 檔 \_ 系統 \_ 驅動程式** (0x00000002) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

**廣告 \_服務 \_ 開機 \_** 啟動 (服務 \_ 啟動 \_) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

**廣告 \_服務 \_ 系統 \_ 啟動** (service \_ system \_ 啟動) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

**廣告 \_服務 \_ 自動 \_ 啟動** (服務 \_ 自動 \_ 啟動) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

**廣告 \_服務 \_ 需求 \_ 開始** (服務 \_ 需求 \_ 開始) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

**廣告 \_停 \_ 用服務** (服務 \_ 已停用) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

**廣告 \_服務 \_ 錯誤 \_ 忽略** (0) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

**廣告 \_服務 \_ 錯誤 \_ 一般** (1) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

**廣告 \_服務 \_ 錯誤 \_ 嚴重** (2) 


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

**廣告 \_服務 \_ 錯誤 \_ 嚴重** (3) 


</dt> <dd></dd> </dl> <dt>

存取類型：唯讀
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* pstatus
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>範例

下列程式碼範例示範如何確認 Windows 2000 上執行的 Microsoft 傳真服務的狀態。


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



下列程式碼範例會驗證 Windows 2000 上執行的 Microsoft 傳真服務的狀態。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>  |
| IID<br/>                      | IID \_ IADsServiceOperations 定義為5D7B33F0-31CA-11CF-A98A-00AA006BC149<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[**IADsFileServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> </dl>

 

 






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
ms.openlocfilehash: a66eaab95195f02fd9b7ff9d824fc354ceb05f4da8b10ac6ada440b5b495adf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017159"
---
# <a name="iadsprintqueue-property-methods"></a>IADsPrintQueue 屬性方法

[**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)介面的屬性方法會取得或設定下表所述的屬性。 如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**BannerPage**
</dt> <dd> <dl>

指向用來分隔列印工作之橫幅頁面的檔案系統路徑。 如果是 **Null**，則不會使用任何橫幅頁面。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
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

**資料類型**
</dt> <dd> <dl>

此佇列可以處理的資料類型。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
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

**DefaultJobPriority**
</dt> <dd> <dl>

指派給每個列印工作的預設優先順序。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
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

**說明**
</dt> <dd> <dl>

此列印佇列的文字描述。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
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

**HostComputer**
</dt> <dd> <dl>

參考主機電腦的 ADsPath 字串。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
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

**位置**
</dt> <dd> <dl>

由系統管理員所描述的佇列位置。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
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

**型號**
</dt> <dd> <dl>

此列印佇列所使用的驅動程式名稱。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
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

**PrintDevices**
</dt> <dd> <dl>

**BSTR** 的 SAFEARRAY，包含這個列印佇列將工作後臺緩衝的列印裝置名稱。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **VARIANT**
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

**PrinterPath**
</dt> <dd> <dl>

參考可存取共用印表機之路徑的字串。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
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

**PrintProcessor**
</dt> <dd> <dl>

與此佇列相關聯的列印處理器。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
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

**優先順序**
</dt> <dd> <dl>

此印表機物件工作佇列的所有已連線裝置的優先順序。 較高優先順序的列印佇列物件中的所有工作都會先處理。

<dt>

存取類型：讀取/寫入
</dt> <dt>

編寫資料類型的腳本： **LONG**
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

**StartTime**
</dt> <dd> <dl>

佇列應開始處理工作的時間。 時間的日期部分會被忽略。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **日期**
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

**UntilTime**
</dt> <dd> <dl>

佇列應該停止處理工作的時間。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **日期**
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

 

## <a name="examples"></a>範例

下列程式碼範例顯示如何判斷指定的印表機是否在線上或離線。


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



下列程式碼範例顯示如何判斷指定的印表機是否在線上或離線。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsPrintQueue 定義為 B15160D0-1226-11CF-A985-00AA006BC149<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[介面屬性方法](interface-property-methods.md)
</dt> </dl>

 

 






---
description: 抓取各種不同的電池資訊。
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: 'IOCTL_BATTERY_QUERY_INFORMATION 控制程式代碼 (Poclass) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: a48514b81ddf5d8f7c0d84d4404eb01752413e73ade43db089fbb6dade673bc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143526"
---
# <a name="ioctl_battery_query_information-control-code"></a>IOCTL \_ 電池 \_ 查詢 \_ 資訊控制項程式碼

抓取各種不同的電池資訊。

若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to battery
  IOCTL_BATTERY_QUERY_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

要傳回其資訊之電池的控制碼。 若要取出設備控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式。

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

作業的控制項程式碼。 此值會識別要執行的特定作業，以及要在其上執行的裝置類型。 使用 **IOCTL \_ 電池 \_ 查詢 \_ 資訊** 進行此作業。

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

[**電池 \_ 查詢 \_ 資訊**](battery-query-information-str.md)結構的指標。

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

輸入緩衝區的大小（以位元組為單位）。

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

傳回緩衝區的指標。  (的資料類型，因此，大小) 的傳回緩衝區，取決於輸入 [**電池 \_ 查詢 \_ 資訊**](battery-query-information-str.md)結構的 **電池 \_ 查詢 \_ 資訊 \_ 層級** 成員所要求的資訊。

下表顯示指定的資訊層級所傳回的資料。



| 資訊層級                 | 傳回的資料                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BatteryDeviceName**             | 以 **Null** 結束的 Unicode 字串，指定電池的名稱。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **BatteryEstimatedTime**          | 指定預估電池執行時間（以秒為單位）的 **ULONG** 。 如果 [**電池 \_ 查詢 \_ 資訊**](battery-query-information-str.md)結構的 **AtRate** 成員中提供的清空率為零，則此計算是以目前的清空率為基礎。 如果 **AtRate** 為非零值，則傳回的時間會是指定速率的預期執行時間。 如果預估的時間不明 (例如，電池未放電，且 **AtRate** 為零) ，則會傳回 **電池 \_ 未知 \_ 時間** 。 請注意，在某些電池系統上，此值不太精確。 此值可能會因為目前的電源使用量而有很大的差異，這可能會受到磁片活動和其他因素所影響。 此值的變更不會有任何通知機制。 |
| **BatteryGranularityInformation** | [**電池 \_ 報告 \_ 規模**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)結構的可變長度陣列，包含從 [**IOCTL \_ 電池 \_ 查詢 \_ 狀態**](ioctl-battery-query-status.md)傳回之電池容量的報告資料細微性。 當資料細微性相依于電池的目前容量時，就會傳回多個專案。 如需專案陣列的解讀，請參閱 **電池 \_ 報告 \_ 規模** 。 專案數目是以傳回的緩衝區大小來表示，並可計算為 (*lpBytesReturned* /Sizeof (**電池 \_ 報表 \_ 規模**) ) 。 將傳回的專案數上限為四個。                                                                                                |
| **BatteryInformation**            | [**電池 \_ 資訊**](battery-information-str.md)結構。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **BatteryManufactureDate**        | [**電池 \_ 製造 \_ 日期**](battery-manufacture-date-str.md)結構。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **BatteryManufactureName**        | 以 **Null** 終止的 Unicode 字串，其中包含電池製造商的名稱。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatterySerialNumber**           | 以 **Null** 終止的 Unicode 字串，其中包含電池的序號。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatteryTemperature**            | 包含電池目前溫度的 **ULONG** ，以10ths 角度的角度。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **BatteryUniqueID**               | 以 **Null** 結束的 Unicode 字串，可唯一識別電池。 這個值可以用來追蹤特定電池。 在智慧電池的情況下，此識別碼將會是製造商名稱、裝置名稱、製造日期，以及序號可列印標記法的串連。 此值不適合顯示給使用者。<br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

輸出緩衝區的大小 (以位元組為單位)。 根據所要求資料的資訊層級，這可能是大小可變大小的緩衝區。

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

變數的指標，此變數會接收 *lpOutBuffer* 緩衝區中傳回的資料大小（以位元組為單位）。

如果輸出緩衝區太小而無法傳回任何資料，則呼叫會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤碼 **錯誤 \_ 的 \_ 緩衝區**，而傳回的位元組計數為零。

如果 *lpOverlapped* 為 **null** (nonoverlapped I/o) ，則 *lpBytesReturned* 不可以是 **null**。

如果 *lpOverlapped* 不是 **null** (重迭的 i/o) ， *lpBytesReturned* 可以是 **null**。 如果這是重迭的作業，您可以藉由呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來取得傳回的位元組數目。 如果 *hDevice* 與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數來取得傳回的位元組數目。

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。

如果使用檔案 **\_ 旗 \_** 標重迭旗標開啟 hDevice， *lpOverlapped* 必須 [**指向有效的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)重迭結構。 在此情況下， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會以 (非同步) 作業的重迭方式執行。 如果裝置是以檔案 **旗標重 \_ \_** 迭旗標開啟，且 *lpOverlapped* 為 **Null**，則函式會以無法預期的方式失敗。

如果在未指定檔案 **\_ 旗 \_** 標重迭旗標的情況下開啟 hDevice，則會忽略 *lpOverlapped* ，並且在作業完成或發生錯誤之前，不會傳回 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)函數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業順利完成， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。

如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

某些電池的相關資訊是選擇性的，或可能對某些電池沒有意義。 如果目前的電池無法使用所要求的特定資料類型，則會傳回 **錯誤 \_ 無效 \_** 的函式。

所有的電池資訊要求都會完成，並在要求的 **BatteryTag** 元素不符合目前電池標記的時 **\_ \_ \_ 找不到錯誤** 檔案的狀態。 這可確保傳回的電池資訊符合要求電池的資訊。  (查看 [電池標記](battery-information.md) 以取得詳細資訊。 ) 

## <a name="remarks"></a>備註

此電池 IOCTL 會抓取各種不同的電池資訊。 輸入參數結構（ [**電池 \_ 查詢 \_ 資訊**](battery-query-information-str.md)）表示要傳回的資訊類型，以及應傳回的電池資訊。 輸出緩衝區的資料類型和內容會根據所要求的資料而有所不同。

如需這項作業的重迭 i/o 含意，請參閱 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 主題的「備註」一節。

## <a name="examples"></a>範例

如需範例，請參閱 [列舉電池裝置](enumerating-battery-devices.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                                                                                                                                                                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                                                                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>Poclass .h;</dt><dt>Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP 上的 BatClass .h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[電池資訊](battery-information.md)
</dt> <dt>

[電源管理控制碼](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**電池 \_ 查詢 \_ 資訊**](battery-query-information-str.md)
</dt> <dt>

[**電池 \_ 報告 \_ 規模**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**IOCTL \_ 電池 \_ 查詢 \_ 狀態**](ioctl-battery-query-status.md)
</dt> <dt>

[**IOCTL \_ 電池 \_ 查詢 \_ 標記**](ioctl-battery-query-tag.md)
</dt> <dt>

[**IOCTL \_ 電池 \_ 設定 \_ 資訊**](ioctl-battery-set-information.md)
</dt> </dl>

 


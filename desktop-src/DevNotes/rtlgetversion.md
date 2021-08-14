---
description: 取得目前正在執行之作業系統的版本資訊。
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: 'RtlGetVersion 函式 (Ntddk) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetVersion
api_type:
- DllExport
api_location:
- Ntdll.dll
- NtosKrnl.exe
ms.openlocfilehash: 7420b9dba03e3b136331f4463f476908882ca5564d0fc7ac563036c7acccb356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161680"
---
# <a name="rtlgetversion-function"></a>RtlGetVersion 函式

取得目前正在執行之作業系統的版本資訊。

## <a name="syntax"></a>語法


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpVersionInformation* \[擴展\]
</dt> <dd>

[**Rtl \_ OSVERSIONINFOW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow)結構或 [**rtl \_ OSVERSIONINFOEXW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw)結構的指標，其中包含目前執行之作業系統的版本資訊。 呼叫端會將結構的 **dwOSVersionInfoSize** 成員設定為所使用之結構的大小（以位元組為單位），以指定要使用哪一個輸入結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回狀態 \_ 成功。

## <a name="remarks"></a>備註

**RtlGetVersion** 等同于 Windows SDK 中的 [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)函數。 請參閱 Windows SDK 中的範例，其中顯示如何取得系統版本。

使用 **RtlGetVersion** 來判斷特定版本的作業系統是否正在執行時，呼叫端應該檢查是否有大於或等於所需版本號碼的版本號碼。 這可確保版本測試可在 Windows 更新版本時成功。

因為可以在可轉散發 DLL 中新增作業系統功能，所以只檢查主要和次要版本號碼，並不是確認特定系統功能是否存在的最可靠方式。 驅動程式應該使用 [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) 來測試特定系統功能是否存在。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 目標平台<br/>          | <dl> <dt>[通用](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl>                  |
| 標頭<br/>                   | <dl> <dt>Ntddk (包含 Ntddk) </dt> </dl>                                                     |
| 程式庫<br/>                  | <dl> <dt>Ntdll.dll .lib;</dt><dt>Ntoskrnl.exe .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll;</dt><dt>NtosKrnl.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PsGetVersion**](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 

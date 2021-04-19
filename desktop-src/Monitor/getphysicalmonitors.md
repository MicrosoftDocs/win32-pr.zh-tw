---
title: GetPhysicalMonitors 函式
description: 取得與顯示裝置相關聯的實體監視器。
ms.assetid: 8bbbad0a-2e45-439c-9312-f922a920c7fd
keywords:
- GetPhysicalMonitors 函式監視設定
topic_type:
- apiref
api_name:
- GetPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d95ccb801dbf06e096534754bd0adffbe36b5084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967337"
---
# <a name="getphysicalmonitors-function"></a>GetPhysicalMonitors 函式

> [!IMPORTANT]
> 監視器設定 API 會使用此函式來存取顯示驅動程式中的功能。 應用程式不應該呼叫此函式。

 

取得與顯示裝置相關聯的實體監視器。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI GetPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _In_  DWORD          dwPhysicalMonitorArraySize,
  _Out_ DWORD          *pdwNumPhysicalMonitorHandlesInArray,
  _Out_ HANDLE         *phPhysicalMonitorArray
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pstrDeviceName* \[在\]
</dt> <dd>

[**UNICODE \_ 字串**](/windows/desktop/api/subauth/ns-subauth-unicode_string)結構的指標，其中包含 [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa)函式所傳回之顯示裝置的名稱。

</dd> <dt>

*dwPhysicalMonitorArraySize* \[在\]
</dt> <dd>

*PdwNumPhysicalMonitorHandlesInArray* 陣列中的元素數目。 若要取得陣列的所需大小，請呼叫 [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md)。

</dd> <dt>

*pdwNumPhysicalMonitorHandlesInArray* \[擴展\]
</dt> <dd>

接收函數複製到 *phPhysicalMonitorArray* 陣列的專案數。

</dd> <dt>

*phPhysicalMonitorArray* \[擴展\]
</dt> <dd>

接收實體監視器之控制碼的陣列。 每個控制碼都必須藉由呼叫 [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor)來釋放。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回 **狀態 \_ 成功**。 否則，它會傳回一個 **NTSTATUS** 錯誤碼。

## <a name="remarks"></a>備註

應用程式應該呼叫下列其中一項功能，而不是使用此函式：

-   [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

此函數沒有相關聯的匯入程式庫。 若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[監視設定函數](monitor-configuration-functions.md)
</dt> </dl>

 


---
title: GetNumberOfPhysicalMonitors 函式
description: 取得與顯示裝置相關聯的實體監視器數目。
ms.assetid: 498404e7-867d-4971-bea1-16e9f8fd9838
keywords:
- GetNumberOfPhysicalMonitors 函式監視設定
topic_type:
- apiref
api_name:
- GetNumberOfPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bec6abf296d807f80ab77cdc7ad8b4062fea9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843524"
---
# <a name="getnumberofphysicalmonitors-function"></a>GetNumberOfPhysicalMonitors 函式

> [!IMPORTANT]
> 監視器設定 API 會使用此函式來存取顯示驅動程式中的功能。 應用程式不應該呼叫此函式。

 

取得與顯示裝置相關聯的實體監視器數目。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI GetNumberOfPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _Out_ LPDWORD        pdwNumberOfPhysicalMonitors
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pstrDeviceName* \[在\]
</dt> <dd>

[**UNICODE \_ 字串**](/windows/desktop/api/subauth/ns-subauth-unicode_string)結構的指標，其中包含 [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa)函式所傳回之顯示裝置的名稱。

</dd> <dt>

*pdwNumberOfPhysicalMonitors* \[擴展\]
</dt> <dd>

接收實體監視器的數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回 **狀態 \_ 成功**。 否則，它會傳回一個 **NTSTATUS** 錯誤碼。

## <a name="remarks"></a>備註

應用程式應該呼叫下列其中一項功能，而不是使用此函式：

-   [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)
-   [**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9)

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

 


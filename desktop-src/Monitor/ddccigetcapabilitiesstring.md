---
title: DDCCIGetCapabilitiesString 函式
description: 取得描述監視功能的字串。
ms.assetid: 54041126-b710-4448-a9f0-9b644d6b8186
keywords:
- DDCCIGetCapabilitiesString 函式監視設定
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesString
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a49a6d7672ee505b4095afd3c6603c719679f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965714"
---
# <a name="ddccigetcapabilitiesstring-function"></a>DDCCIGetCapabilitiesString 函式

> [!IMPORTANT]
> 監視器設定 API 會使用此函式來存取顯示驅動程式中的功能。 應用程式不應該呼叫此函式。

 

取得描述監視功能的字串。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesString(
  _In_  HANDLE hMonitor,
  _Out_ LPSTR  pszString,
  _In_  DWORD  dwLength
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hMonitor* \[在\]
</dt> <dd>

實體監視器的控制碼。

</dd> <dt>

*pszString* \[擴展\]
</dt> <dd>

接收功能字串的緩衝區指標。 若要取得功能字串的長度，請呼叫 [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md)。

</dd> <dt>

*dwLength* \[在\]
</dt> <dd>

*PszString* 緩衝區的大小（以字元為單位），包括結束的 null 字元。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回 **狀態 \_ 成功**。 否則，它會傳回一個 **NTSTATUS** 錯誤碼。

## <a name="remarks"></a>備註

應用程式應該呼叫 [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) ，而不是呼叫此函式。

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

 


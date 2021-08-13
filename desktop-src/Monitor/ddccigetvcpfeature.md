---
title: DDCCIGetVCPFeature 函式
description: 取得虛擬主控台的目前值、最大值和程式碼類型 (VCP) 程式碼的監視器。
ms.assetid: 7749d45c-a0d5-44ee-8f91-811677cbf59f
keywords:
- DDCCIGetVCPFeature 函式監視設定
topic_type:
- apiref
api_name:
- DDCCIGetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15549d69bb446d7a7e6d5c44517bade3e9158d1a6d5f9b9ae839d6b1b547717a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640996"
---
# <a name="ddccigetvcpfeature-function"></a>DDCCIGetVCPFeature 函式

> [!IMPORTANT]
> 監視器設定 API 會使用此函式來存取顯示驅動程式中的功能。 應用程式不應該呼叫此函式。

 

取得虛擬主控台的目前值、最大值和程式碼類型 (VCP) 程式碼的監視器。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI DDCCIGetVCPFeature(
  _In_      HANDLE             hMonitor,
  _In_      DWORD              dwVCPCode,
  _Out_opt_ LPMC_VCP_CODE_TYPE pvct,
  _Out_     DWORD              *pdwCurrentValue,
  _Out_opt_ DWORD              *pdwMaximumValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hMonitor* \[在\]
</dt> <dd>

實體監視器的控制碼。

</dd> <dt>

*dwVCPCode* \[在\]
</dt> <dd>

要查詢的 VCP 程式碼。

</dd> <dt>

*pvct* \[out、optional\]
</dt> <dd>

以 [**MC \_ VCP 程式 \_ 代碼 \_ 類型**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) 列舉的成員形式接收 VCP 程式碼類型。

</dd> <dt>

*pdwCurrentValue* \[擴展\]
</dt> <dd>

接收 VCP 程式碼的目前值。

</dd> <dt>

*pdwMaximumValue* \[out、optional\]
</dt> <dd>

接收 VCP 程式碼的最大值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回 **狀態 \_ 成功**。 否則，它會傳回一個 **NTSTATUS** 錯誤碼。

## <a name="remarks"></a>備註

應用程式應該呼叫 [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) ，而不是呼叫此函式。

此函數沒有相關聯的匯入程式庫。 若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[監視設定函數](monitor-configuration-functions.md)
</dt> </dl>

 


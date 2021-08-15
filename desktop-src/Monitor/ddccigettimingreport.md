---
title: DDCCIGetTimingReport 函式
description: 取得監視器的水準和垂直同步處理頻率。
ms.assetid: d490cb89-082a-42a1-ac0a-335c929cd5d7
keywords:
- DDCCIGetTimingReport 函式監視設定
topic_type:
- apiref
api_name:
- DDCCIGetTimingReport
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 930149ebc2acfa69f479c889c6fa2c33acdfb3f528a67f83ee0bfbe7ab0467a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382361"
---
# <a name="ddccigettimingreport-function"></a>DDCCIGetTimingReport 函式

> [!IMPORTANT]
> 監視器設定 API 會使用此函式來存取顯示驅動程式中的功能。 應用程式不應該呼叫此函式。

 

取得監視器的水準和垂直同步處理頻率。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI DDCCIGetTimingReport(
  _In_  HANDLE             hMonitor,
  _Out_ LPMC_TIMING_REPORT pmtr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hMonitor* \[在\]
</dt> <dd>

實體監視器的控制碼。

</dd> <dt>

*pmtr* \[擴展\]
</dt> <dd>

可接收計時資訊之 [**MC \_ 計時 \_ 報表**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回 **狀態 \_ 成功**。 否則，它會傳回一個 **NTSTATUS** 錯誤碼。

## <a name="remarks"></a>備註

應用程式應該呼叫 [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) ，而不是呼叫此函式。

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

 


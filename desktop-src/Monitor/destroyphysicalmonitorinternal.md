---
title: DestroyPhysicalMonitorInternal 函式
description: 關閉實體監視器的控制碼。
ms.assetid: 86705f1b-6445-444c-8e04-66a435927af3
keywords:
- DestroyPhysicalMonitorInternal 函式監視設定
topic_type:
- apiref
api_name:
- DestroyPhysicalMonitorInternal
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94232ff1cd9d92c9f7ea1a0fb76418cbd59a48c408ea157725287b7c7ce93f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805859"
---
# <a name="destroyphysicalmonitorinternal-function"></a>DestroyPhysicalMonitorInternal 函式

> [!IMPORTANT]
> 監視器設定 API 會使用此函式來存取顯示驅動程式中的功能。 應用程式不應該呼叫此函式。

 

關閉實體監視器的控制碼。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI DestroyPhysicalMonitorInternal(
  _In_ HANDLE hMonitor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hMonitor* \[在\]
</dt> <dd>

實體監視器的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回 **狀態 \_ 成功**。 否則，它會傳回一個 **NTSTATUS** 錯誤碼。

## <a name="remarks"></a>備註

應用程式應該呼叫 [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor) ，而不是呼叫此函式。

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

 


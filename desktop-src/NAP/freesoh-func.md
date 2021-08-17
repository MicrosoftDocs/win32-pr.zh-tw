---
title: 'FreeSoH 函式 (NapUtil) '
description: 釋出 SoH 資料結構。
ms.assetid: 587acf64-31be-46c8-9d49-b5014c1a90ba
keywords:
- FreeSoH 函數 NAP
topic_type:
- apiref
api_name:
- FreeSoH
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b7e8236fcc8f0a2eaadd5b6f2ef81a393d68943d7fc5aeac5b00706ea06ec26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368680"
---
# <a name="freesoh-function"></a>FreeSoH 函式

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**FreeSoH** 函數會釋出 **SoH** 資料結構。

## <a name="syntax"></a>語法


```C++
NAPAPI VOID WINAPI FreeSoH(
  _In_ SoH *soh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*soh* \[在\]
</dt> <dd>

要釋放的 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 資料結構指標。

</dd> </dl>

## <a name="remarks"></a>備註

NAP 系統支援的所有 COM 介面都會使用標準 COM 記憶體管理規則和 COM 記憶體配置器 (**CoTaskMemAlloc** 和 **CoTaskMemFree**) ：

-   呼叫端會配置和釋放 **In** 參數。
-   **Out** 參數是由被呼叫端所配置，且由呼叫者使用 **CoTaskMem** 釋放。
-   **In/out** 參數是由呼叫端所配置、由被呼叫端釋出和重新配置，最後由呼叫端釋放，並使用 **CoTaskMem**。

釋放記憶體的所有 NAP 函式也會釋放所有內嵌指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>NapUtil。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 






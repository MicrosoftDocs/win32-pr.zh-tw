---
title: 'FreeIsolationInfo 函式 (NapUtil) '
description: 釋放 IsolationInfo 資料結構。
ms.assetid: 639cfa74-0823-4a19-9cbe-dd6f0a38e7eb
keywords:
- FreeIsolationInfo 函數 NAP
topic_type:
- apiref
api_name:
- FreeIsolationInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ed154d35b32edab0f1a68d84f78c10cfd1cfe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965930"
---
# <a name="freeisolationinfo-function"></a>FreeIsolationInfo 函式

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**FreeIsolationInfo** 函式會釋出 [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo)的資料結構。

## <a name="syntax"></a>語法


```C++
NAPAPI VOID WINAPI FreeIsolationInfo(
  _In_ IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*isolationInfo* \[在\]
</dt> <dd>

要釋放的 [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) 資料結構指標。

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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>NapUtil。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 






---
title: 'FreeSystemHealthAgentState 函式 (NapUtil) '
description: 釋放 SystemHealthAgentState 資料結構。
ms.assetid: e9bfa8ee-c335-416e-94cf-28646709d419
keywords:
- FreeSystemHealthAgentState 函數 NAP
topic_type:
- apiref
api_name:
- FreeSystemHealthAgentState
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5161b24f983936b2eb380f1863489ea6c5c927d9b18a278e5942e162f156c6fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891648"
---
# <a name="freesystemhealthagentstate-function"></a>FreeSystemHealthAgentState 函式

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**FreeSystemHealthAgentState** 函數會釋出 [**SystemHealthAgentState**](/windows/win32/api/naptypes/ns-naptypes-systemhealthagentstate)資料結構。

## <a name="syntax"></a>語法


```C++
NAPAPI VOID WINAPI FreeSystemHealthAgentState(
  _In_ SystemHealthAgentState *state
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*狀態* \[在\]
</dt> <dd>

要釋放的 [**SystemHealthAgentState**](/windows/win32/api/naptypes/ns-naptypes-systemhealthagentstate) 資料結構指標。

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



 

 






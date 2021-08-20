---
title: 'FreeNetworkSoH 函式 (NapUtil) '
description: 釋放 NetworkSoH 資料結構。
ms.assetid: a27d54a0-8b9c-4bf7-909c-1de5db55f429
keywords:
- FreeNetworkSoH 函數 NAP
topic_type:
- apiref
api_name:
- FreeNetworkSoH
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0c2d3db800860295e0fa6173422ffeec0ca144550cc3ddfdf8a1ea391b6c6eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134749"
---
# <a name="freenetworksoh-function"></a>FreeNetworkSoH 函式

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**FreeNetworkSoH** 函數會釋出 [**NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh)資料結構。

## <a name="syntax"></a>語法


```C++
NAPAPI VOID WINAPI FreeNetworkSoH(
  _In_ NetworkSoH *networkSoh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*networkSoh* \[在\]
</dt> <dd>

要釋放的 [**NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh) 資料結構指標。

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



 

 






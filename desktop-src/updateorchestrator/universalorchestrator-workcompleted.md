---
title: IUniversalOrchestrator::WorkCompleted
description: 呼叫通用協調器以表示工作已完成
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 5094ae864b4df9a3dd53b90c3b7d099a206a0ad8db1d1176b603b5ba45ca8194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966070"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a>IUniversalOrchestrator：： WorkCompleted 方法

> [!NOTE] 
> 此 API 屬於通用 Orchestrator API。

允許用戶端通知通用協調器，先前已排程的工作已完成，並停止回呼來執行工作，直到下一次成功的 ScheduleWork 呼叫為止。

## <a name="syntax"></a>語法

```C++
HRESULT WorkCompleted(
  LPCWSTR callerIdentifier,
  BOOL    workCompleted);
```

## <a name="parameters"></a>參數

`callerIdentifier`

識別此特定用戶端所有呼叫的唯一字串。

`workCompleted`

如果工作已順利完成，**則為 TRUE** 。 否則，如果工作嘗試失敗，而且未來應該重試，則 **為 FALSE** 。 

## <a name="return-value"></a>傳回值
如果這個方法成功，它會傳回 **S_OK**。  否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

| 需求 | 版本 |
|---|---|
| 最低支援的用戶端 | Windows 10 1903 |
|   |   |



 

 




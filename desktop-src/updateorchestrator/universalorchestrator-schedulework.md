---
title: IUniversalOrchestrator::ScheduleWork
description: 呼叫通用協調器來排程工作
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 4c49d06a28497c33e86cc1e919fdb59f2363d1f5
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991815"
---
# <a name="iuniversalorchestratorschedulework-method"></a>IUniversalOrchestrator：： ScheduleWork 方法

> [!NOTE] 
> 此 API 屬於通用 Orchestrator API。

允許用戶端通知通用協調器，其工作已暫止，並提供可供通用協調器呼叫的二進位檔，以在稍後執行更新工作。

回呼二進位檔必須使用有效的 Microsoft 憑證進行簽署，而且呼叫端必須從系統內容叫用 ScheduleWork 呼叫。

## <a name="syntax"></a>語法

```C++
HRESULT ScheduleWork(
  LPCWSTR callerIdentifier,
  LPCWSTR cmdLine
  LPCWSTR startArg,
  LPCWSTR pauseArg);
```

## <a name="parameters"></a>參數

`callerIdentifier`

識別此特定用戶端所有呼叫的唯一字串。

`cmdLine`

將由通用協調器叫用來執行工作的回呼二進位檔的完整路徑。

`startArg`

要求傳遞至回呼二進位檔的參數，以表示要求啟動。

`pauseArg`

*(選擇性)* 要傳遞至回呼二進位檔以表示已要求暫停的參數。

## <a name="return-value"></a>傳回值
如果這個方法成功，它會傳回 **S_OK**。  否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

| 需求 | 版本 |
|---|---|
| 最低支援的用戶端 | Windows 10 1903 |
|   |   |



 

 




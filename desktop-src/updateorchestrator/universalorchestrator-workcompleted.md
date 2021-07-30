---
title: IUniversalOrchestrator::WorkCompleted
description: 呼叫通用協調器以表示工作已完成
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: e36a3ba744df807abbebc6332ac8433010afd667
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991825"
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



 

 




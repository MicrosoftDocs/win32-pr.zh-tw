---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: 查詢通用協調器，以判斷是否已超過過了時間（OOBE）。
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 2ed354d365b795a0c959396e6b26d6bc73baad97
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/21/2021
ms.locfileid: "106974734"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a>IUniversalOrchestrator：： HasMoratoriumPassed 方法

> [!NOTE] 
> 此 API 屬於通用 Orchestrator API。

可讓用戶端判斷通用協調器是否在新的裝置現成體驗之後立即運作，這會限制工作嘗試將使用者中斷降至最低。 

## <a name="syntax"></a>語法

```C++
HRESULT HasMoratoriumPassed(
  LPCWSTR callerIdentifier,
  BOOL*   moratoriumPassed);
```

## <a name="parameters"></a>參數

`callerIdentifier`

識別此特定用戶端所有呼叫的唯一字串。

`hasMoratoriumPassed`

輸出參數，可儲存查詢的結果。

## <a name="return-value"></a>傳回值
如果這個方法成功，它會傳回 **S_OK**。  否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

| 需求 | 版本 |
|---|---|
| 最低支援的用戶端 | Windows 10 1903 |
|   |   |



 

 




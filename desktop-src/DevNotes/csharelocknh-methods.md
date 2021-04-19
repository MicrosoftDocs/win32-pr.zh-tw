---
description: 用來操作鎖定的方法群組。
ms.assetid: ba4cc37c-bd2f-446f-8b3d-bc2a2e2e4de4
title: CShareLockNH 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16a979c5d1f111c92a64376c48f4c0ed1a165ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970101"
---
# <a name="csharelocknh-methods"></a>CShareLockNH 方法

用來操作鎖定的方法群組。

## <a name="methods"></a>方法

以下是 Rwnh.dll 匯出的方法。



| 方法                                                                   | 描述                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**ExclusiveLock**](csharelocknh--exclusivelock.md)                     | 取得讀取器/寫入器鎖定。                                  |
| [**ExclusiveToPartial**](csharelocknh--exclusivetopartial.md)           | 變更狀態。                                              |
| [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md)                 | 釋放鎖定。                                                |
| [**FirstPartialToExclusive**](csharelocknh--firstpartialtoexclusive.md) | 用來將部分鎖定轉換為獨佔鎖定。         |
| [**PartialLock**](csharelocknh--partiallock.md)                         | 防止一個以上的執行緒完成取得鎖定。 |
| [**PartialUnlock**](csharelocknh--partialunlock.md)                     | 釋放部分鎖定。                                        |
| [**ShareLock**](csharelocknh--sharelock.md)                             | 取得共用模式的鎖定。                                 |
| [**ShareUnlock**](csharelocknh--shareunlock.md)                         | 從共用模式釋放鎖定。                               |
| [**SharedToPartial**](csharelocknh--sharedtopartial.md)                 | 取得部分鎖定。                                         |
| [**TryExclusiveLock**](csharelocknh--tryexclusivelock.md)               | 取得獨佔鎖定。                                     |



 

 

 




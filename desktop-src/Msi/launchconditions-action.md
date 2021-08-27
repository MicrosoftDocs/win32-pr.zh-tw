---
description: LaunchConditions 動作會查詢 LaunchCondition 資料表，並評估記錄在該處的每個條件陳述式。 如果上述任一條件陳述式失敗，則會向使用者顯示錯誤訊息，並結束安裝。
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: LaunchConditions 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a973e6e1de81091039de12e07e8edb890c860e5be54e942f00406e39e62e229
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086028"
---
# <a name="launchconditions-action"></a>LaunchConditions 動作

LaunchConditions 動作會查詢 [LaunchCondition 資料表](launchcondition-table.md) ，並評估記錄在該處的每個條件陳述式。 如果上述任一條件陳述式失敗，則會向使用者顯示錯誤訊息，並結束安裝。

## <a name="sequence-restrictions"></a>順序限制

LaunchConditions 動作是選擇性的。 此動作通常是序列中的第一個動作，但 [AppSearch 動作](appsearch-action.md) 可能會在 LaunchConditions 動作之前排序。 如果沒有適用于所有安裝模式的啟動條件，則應該在適當的順序資料表中的條件運算式中使用適當的安裝模式屬性。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

 

 




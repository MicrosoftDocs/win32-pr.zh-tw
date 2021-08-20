---
description: 通知 CBasePin 篩選狀態變更
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: 通知 CBasePin 篩選狀態變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7193402331f150f88217e2d200279e93314c40a9056f52bc31d8100106d4f960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152988"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a>通知 CBasePin 篩選狀態變更

當擁有篩選準則的狀態變更時，就會通知 **CBasePin** 類別。 針對每個狀態轉換，篩選準則會在 pin 上呼叫對應的方法，如下表所示。



| 新的篩選準則狀態 | CBasePin 方法                                 |
|------------------|-------------------------------------------------|
| 已停止          | [**CBasePin：：非使用中**](cbasepin-inactive.md) |
| 已暫停           | [**CBasePin：： Active**](cbasepin-active.md)     |
| 執行中          | [**CBasePin：： Run**](cbasepin-run.md)           |



 

衍生類別應該覆寫這些方法，以回應狀態變更。 根據篩選準則，pin 可能會啟動可傳遞範例、認可或取消認可其記憶體配置器等的工作者執行緒。

 

 




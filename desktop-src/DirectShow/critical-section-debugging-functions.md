---
description: 重要區段調試函數
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: 重要區段調試函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098558a97e38168595dc89c3c81175c9d6635c5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509909"
---
# <a name="critical-section-debugging-functions"></a>重要區段調試函數

這些函式可協助您在程式碼中的重要區段中進行偵錯工具，以便更輕鬆地找出鎖死的原因。 這些函數會使用 [**CCritSec**](ccritsec.md) helper 類別。



| 函式                             | 描述                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [**CritCheckIn**](critcheckin.md)   | 如果目前的執行緒擁有指定的重要區段，則傳回 **TRUE** 。  |
| [**CritCheckOut**](critcheckout.md) | 如果目前線程擁有指定的重要區段，則傳回 **FALSE** 。 |
| [**DbgLockTrace**](dbglocktrace.md) | 啟用或停用指定之重要區段的偵錯工具記錄。              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[偵錯工具](debugging-utilities.md)
</dt> </dl>

 

 




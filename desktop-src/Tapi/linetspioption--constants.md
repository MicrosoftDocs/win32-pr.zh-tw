---
description: LINETSPIOPTION \_ 常數描述應呼叫的訂單服務提供者。
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: 'LINETSPIOPTION_ 常數 (Tspi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5d4a57edd80a83ab442313706fd40a2fbd79f545a0b3e9485e5d8c88b8c2f8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404851"
---
# <a name="linetspioption_-constants"></a>LINETSPIOPTION \_ 常數

**LINETSPIOPTION \_ 常數** 描述應呼叫的訂單服務提供者。

<dl> <dt>

<span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION \_ NONREENTRANT**
</dt> <dd> <dl> <dt>



TAPI 應一次呼叫此服務提供者中的函式;它應該等候每個函式傳回 (但不是非同步函式，以便在相同或不同的處理器上，于相同或不同的執行緒上呼叫相同或不同的函式，以完成) 。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tspi。h</dt> </dl> |



 

 





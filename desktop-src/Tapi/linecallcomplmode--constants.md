---
description: LINECALLCOMPLMODE \_ 位旗標常數描述呼叫可以完成的不同方式。
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: 'LINECALLCOMPLMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43f76c9b8012f9ecb60c6b0ffd787d5a0bad87794eb833cc4095c276ba983f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761752"
---
# <a name="linecallcomplmode_-constants"></a>LINECALLCOMPLMODE \_ 常數

**LINECALLCOMPLMODE \_** 位旗標常數描述呼叫可以完成的不同方式。

<dl> <dt>

<span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**LINECALLCOMPLMODE \_ 回呼**
</dt> <dd> <dl> <dt>



要求被呼叫的工作站傳回閒置時的呼叫。


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE \_ CAMPON**
</dt> <dd> <dl> <dt>



將呼叫排在佇列中，直到呼叫可以完成為止。


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE \_ INTRUDE**
</dt> <dd> <dl> <dt>



將應用程式新增至) 中被呼叫的工作站 (barge 的現有呼叫。


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**LINECALLCOMPLMODE \_ 訊息**
</dt> <dd> <dl> <dt>



留下一小段預先定義的訊息給被呼叫的工作站 (讓 Word 呼叫) 。 要傳送的訊息會分開指定。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 





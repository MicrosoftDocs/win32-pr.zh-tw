---
description: LINEGATHERTERM \_ 位旗標常數描述終止緩衝處理數位收集時所依據的條件。
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: 'LINEGATHERTERM_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968492a584024c7750b417a9fd03b68ac1df42ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987977"
---
# <a name="linegatherterm_-constants"></a>LINEGATHERTERM \_ 常數

**LINEGATHERTERM \_** 位旗標常數描述終止緩衝處理數位收集時所依據的條件。

<dl> <dt>

<span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM \_ BUFFERFULL**
</dt> <dd> <dl> <dt>



已收集要求的數位數目。 緩衝區已滿。


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**LINEGATHERTERM \_ 取消**
</dt> <dd> <dl> <dt>



此應用程式已由另一個應用程式取消要求，或因為呼叫終止。


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM \_ FIRSTTIMEOUT**
</dt> <dd> <dl> <dt>



第一個位數 timeout 已過期。 緩衝區不包含任何數位。


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**LINEGATHERTERM \_ INTERTIMEOUT**
</dt> <dd> <dl> <dt>



的位數 timeout 已過期。 緩衝區包含至少一個數位。


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM \_ TERMDIGIT**
</dt> <dd> <dl> <dt>



其中一個終止數位符合接收的數位。 相符的終止數位是緩衝區中的最後一個數位。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 





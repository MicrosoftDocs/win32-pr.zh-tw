---
description: LINEDIGITMODE \_ 常數描述不同類型的 inband 數位產生。
ms.assetid: d603ea28-2b93-4548-bb16-78e93087f828
title: 'LINEDIGITMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bedd7f508368a84ab2fa70fac37c316dcc6c85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975966"
---
# <a name="linedigitmode_-constants"></a>LINEDIGITMODE \_ 常數

**LINEDIGITMODE \_** 常數描述不同類型的 inband 數位產生。

<dl> <dt>

<span id="LINEDIGITMODE_DTMF"></span><span id="linedigitmode_dtmf"></span>**LINEDIGITMODE \_ DTMF**
</dt> <dd> <dl> <dt>



使用 DTMF 聲對數位進行信號。 有效位數為0到9、' \* '、' \# '、' A '、' B '、' C ' 和 ' d '。


</dt> </dl> </dd> <dt>

<span id="LINEDIGITMODE_DTMFEND"></span><span id="linedigitmode_dtmfend"></span>**LINEDIGITMODE \_ DTMFEND**
</dt> <dd> <dl> <dt>



使用 DTMF 聲來表示數位，並偵測到下邊緣。 有效位數為0到9、' \* '、' \# '、' A '、' B '、' C ' 和 ' d '。


</dt> </dl> </dd> <dt>

<span id="LINEDIGITMODE_PULSE"></span><span id="linedigitmode_pulse"></span>**LINEDIGITMODE \_ 脈衝**
</dt> <dd> <dl> <dt>



使用旋轉脈衝順序來表示數位。 有效位數為0到9。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

當產生或偵測位數時，可以指定數位模式。 請注意，脈衝數位是藉由建立和中斷本機迴圈電路來產生的。 交換器會吸收這些跳動。 遠端端只是觀察到一連串的 inband 音訊點擊。 因此，偵測以脈衝傳送的數位必須能夠偵測到可按下1到10聲的順序。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 





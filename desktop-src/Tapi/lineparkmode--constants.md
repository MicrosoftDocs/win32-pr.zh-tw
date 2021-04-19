---
description: LINEPARKMODE \_ 位旗標常數描述停車呼叫的不同方式。
ms.assetid: 4b182c16-9d58-4244-bc5a-05c393800948
title: 'LINEPARKMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef27aaf35f86b02834c93992e8f427c54ffb903
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978450"
---
# <a name="lineparkmode_-constants"></a>LINEPARKMODE \_ 常數

**LINEPARKMODE \_** 位旗標常數描述停車呼叫的不同方式。

<dl> <dt>

<span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE \_ 導向**
</dt> <dd> <dl> <dt>



指定導向撥打電話。 要暫停呼叫的位址必須提供給參數。


</dt> </dl> </dd> <dt>

<span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE \_ NONDIRECTED**
</dt> <dd> <dl> <dt>



指定 nondirected 呼叫公園。 切換時，會選取要放置呼叫的位址，並由參數提供給應用程式。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

在停車呼叫時，會使用 **LINEPARKMODE \_ 常數** 。 請參閱線路的位址裝置功能，找出可用的公園模式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 





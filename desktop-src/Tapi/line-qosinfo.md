---
description: TSPI LINE \_ QOSINFO message 會導致 TAPI 引發 QOS 事件。 如需其他資訊，請參閱 ITQOSEvent。
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: 'LINE_QOSINFO 訊息 (Tspi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35ff19601ab6acd9a3d8e8aebf1e59b06a4f17e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995771"
---
# <a name="line_qosinfo-message"></a>行 \_ QOSINFO 訊息

TSPI **LINE \_ QOSINFO** MESSAGE 會導致 TAPI 引發 QOS 事件。 如需其他資訊，請參閱 [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) 。


```C++
        
```



## <a name="parameters"></a>參數

<dl> <dt>

*htLine* 
</dt> <dd>

線路的 TAPI 控制碼。

</dd> <dt>

*htCall* 
</dt> <dd>

呼叫的 TAPI 控制碼。

</dd> <dt>

*dwMsg* 
</dt> <dd>

值行 \_ QOSINFO。

</dd> <dt>

*dwParam1* 
</dt> <dd>

[**QOS \_ 事件**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)列舉值的成員，可識別事件的類型。

</dd> <dt>

*dwParam2* 
</dt> <dd>

用來識別與這個事件相關聯之呼叫媒體的 [媒體類型](./tapiprotocol--constants.md) 常數。

</dd> <dt>

*dwParam3* 
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2。2<br/>                                                      |
| 標頭<br/>       | <dl> <dt>Tspi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**QOS \_ 事件**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 


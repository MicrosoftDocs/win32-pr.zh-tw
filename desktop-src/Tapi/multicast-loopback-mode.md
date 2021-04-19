---
description: 多播 \_ 回送 \_ 模式列舉會描述多播回送模式。
ms.assetid: bf9c3665-71cc-4cde-9ad4-1a8b62eddf9f
title: 'MULTICAST_LOOPBACK_MODE 列舉 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a15505efcd1a9e399866b104da0582ccf846689
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993687"
---
# <a name="multicast_loopback_mode-enumeration"></a>多播 \_ 回送 \_ 模式列舉

\[**多播 \_回送 \_ 模式** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**多播 \_ 回送 \_ 模式** 列舉會描述多播回送模式。

## <a name="syntax"></a>Syntax


```C++
} MULTICAST_LOOPBACK_MODE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM \_ 無 \_ 回送**
</dt> <dd>

多播回送已停用。 這表示在同一部電腦上聯結相同多播群組的兩個應用程式，可以取得彼此的封包。

</dd> <dt>

<span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**MM \_ 完整 \_ 回送**
</dt> <dd>

送出的所有封包也會回復。 此模式只適用于測試。

</dd> <dt>

<span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**MM \_ 選擇性 \_ 回送**
</dt> <dd>

已啟用選擇性回送。 這表示在一部電腦上啟用多個應用程式可以加入相同的多播群組，而不會有混淆。 封包會從堆疊環回，且每個 RTP 會話都會負責篩選掉不需要的封包。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMulticastControl：： get \_ LoopbackMode**](imulticastcontrol-get-loopbackmode.md)
</dt> <dt>

[**IMulticastControl：:p 的 \_ LoopbackMode**](imulticastcontrol-put-loopbackmode.md)
</dt> </dl>

 

 





---
description: H245 \_ 功能列舉描述音訊和影片格式支援。
ms.assetid: 76aeb3a1-3233-4425-b9db-efacbedc309e
title: 'H245_CAPABILITY 列舉 (H323priv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1666eb918748696263247f00f0d0e17ac9424e6c4bf85c5574f866bb10e28be1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140551"
---
# <a name="h245_capability-enumeration"></a>H245 \_ 功能列舉

\[**H245 \_功能** 無法在 Windows Vista、Windows Server 2008 及後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**H245 \_ 功能** 列舉描述音訊和影片格式支援。

## <a name="syntax"></a>Syntax


```C++
} H245_CAPABILITY;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="HC_G711"></span><span id="hc_g711"></span>**HC \_ G711**
</dt> <dd>

支援 g.711 音訊通訊協定。

</dd> <dt>

<span id="HC_G723"></span><span id="hc_g723"></span>**HC \_ G723**
</dt> <dd>

支援723音訊通訊協定。

</dd> <dt>

<span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC \_ H263QCIF**
</dt> <dd>

支援 h. video 通訊協定。

</dd> <dt>

<span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC \_ H261QCIF**
</dt> <dd>

支援 h. video 通訊協定。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>H323priv。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IH323LineEx::SetDefaultCapabilityPreferrence**](ih323lineex-setdefaultcapabilitypreferrence.md)
</dt> </dl>

 

 





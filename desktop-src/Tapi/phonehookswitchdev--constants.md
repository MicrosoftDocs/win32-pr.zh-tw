---
description: PHONEHOOKSWITCHDEV \_ 位旗標常數會描述各種音訊 i/o 裝置，每個裝置都有自己的 hookswitch 能從電腦控制。
ms.assetid: b3272a75-87b0-4afc-b2e2-2d65e4b49300
title: 'PHONEHOOKSWITCHDEV_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77e6b776b89adf6224d6feaef8deeef1f9f71b9888929f3aea08b5342adc1dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796748"
---
# <a name="phonehookswitchdev_-constants"></a>PHONEHOOKSWITCHDEV \_ 常數

**PHONEHOOKSWITCHDEV \_** 位旗標常數會描述各種音訊 i/o 裝置，每個裝置都有自己的 hookswitch 能從電腦控制。

<dl> <dt>

<span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**PHONEHOOKSWITCHDEV \_ 聽筒**
</dt> <dd> <dl> <dt>



這是標準的 ear 和 mouthpiece 電話。


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**PHONEHOOKSWITCHDEV \_ 耳機**
</dt> <dd> <dl> <dt>



這是連線到電話集合的耳機。


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV \_ 喇叭**
</dt> <dd> <dl> <dt>



這是內建的 loudspeaker 和麥克風。 這也可能是連至電話集合的外部連線附屬喇叭。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

這些常數會在 [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) 資料結構中用來指出電話裝置的 hookswitch 裝置功能。 [**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus)結構會報告電話 hookswitch 裝置的狀態。 [**PhoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch)和 [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch)函式會使用它做為參數，以選取手機的 i/o 裝置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 





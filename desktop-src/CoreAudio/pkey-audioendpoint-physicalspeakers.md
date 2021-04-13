---
description: 深入瞭解： PKEY_AudioEndpoint_PhysicalSpeakers
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: 'PKEY_AudioEndpoint_PhysicalSpeakers (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a627ec97dc329f50cc58a15d0df516f598af86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510681"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a>PKEY \_ AudioEndpoint \_ PhysicalSpeakers

**PKEY \_ AudioEndpoint \_ PhysicalSpeakers** 屬性會指定音訊端點裝置的通道設定遮罩。 遮罩會指出一組喇叭的實體設定，並指定喇叭的通道指派。 如需通道設定遮罩的詳細資訊，請參閱下列各項：

1.  \_ \_ Windows DDK 檔中 KSPROPERTY 音訊通道設定屬性的描述 \_ 。
2.  標題為「家用劇院喇叭設定的音訊驅動程式支援」的白皮書， [適用于 Windows 網站的音訊裝置技術](https://www.microsoft.com/whdc/device/audio/default.mspx) 。

**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ UI4。

**PROPVARIANT** 結構的 **uintVal** 成員包含轉換成 **UINT** 型別的通道設定遮罩。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Mmdeviceapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**音訊端點屬性**](audio-endpoint-properties.md)
</dt> <dt>

[核心音訊屬性](core-audio-properties.md)
</dt> </dl>

 

 





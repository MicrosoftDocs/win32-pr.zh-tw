---
description: PKEY \_ AudioEndpoint \_ FormFactor 屬性會指定音訊端點裝置的外型規格。 外型規格表示使用者操作之音訊端點裝置的實體屬性。
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: 'PKEY_AudioEndpoint_FormFactor (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5833470e2a2848f9454f3b5eefbf852f452f033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468428"
---
# <a name="pkey_audioendpoint_formfactor"></a>PKEY \_ AudioEndpoint \_ FormFactor

**PKEY \_ AudioEndpoint \_ FormFactor** 屬性會指定音訊端點裝置的外型規格。 外型規格表示使用者操作之音訊端點裝置的實體屬性。

**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ UI4。

**PROPVARIANT** 結構的 **uintVal** 成員包含轉換成 UINT 類型的列舉值。 它會設定為下列其中一個 [**EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) 列舉值：

-   RemoteNetworkDevice
-   Speakers
-   LineLevel
-   耳機
-   麥克風
-   Headset
-   手機
-   UnknownDigitalPassthrough
-   後部
-   HDMI
-   UnknownFormFactor

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

 

 





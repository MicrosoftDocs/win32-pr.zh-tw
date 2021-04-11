---
description: PKEY \_ AudioEndpoint \_ 支援 \_ EventDriven \_ 模式屬性，指出端點是否支援事件驅動模式。
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: 'PKEY_AudioEndpoint_Supports_EventDriven_Mode (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2707de83721d546040ac878b337faea12f533bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936444"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a>PKEY \_ AudioEndpoint \_ 支援 \_ EventDriven \_ 模式

**PKEY \_ AudioEndpoint \_ 支援 \_ EventDriven \_ 模式** 屬性，指出端點是否支援事件驅動模式。

**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ UI4。

**PROPVARIANT** 結構的 **uintVal** 成員是一個 **DWORD** ，表示端點是否支援事件驅動模式。

## <a name="remarks"></a>備註

這個屬性值是由 .inf 檔案中的音訊 OEM 填入，表示 HDAudio 硬體支援根據 WHQL 需求的事件驅動模式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Mmdeviceapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**音訊端點屬性**](audio-endpoint-properties.md)
</dt> <dt>

[核心音訊屬性](core-audio-properties.md)
</dt> </dl>

 

 





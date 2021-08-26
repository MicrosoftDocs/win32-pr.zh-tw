---
description: 取得音訊位串流中音訊頻道的喇叭設定。
ms.assetid: ec13bb55-47af-4d79-9560-d297bce8e236
title: 'AVAudioChannelConfig 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba9c497305292abeb34b86a7989fb05fbb872c898d10743ebd93b3982089e00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983788"
---
# <a name="avaudiochannelconfig-property"></a>AVAudioChannelConfig 屬性

取得音訊位串流中音訊頻道的喇叭設定。

這是唯讀的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVAudioChannelConfig**

## <a name="property-value"></a>屬性值

這個屬性的值是 [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) 列舉之成員的位 or。

## <a name="remarks"></a>備註

通道數目包含 (LFE) 通道的低頻率效果（如果有的話）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop apps \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器 API 屬性](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI 介面**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 





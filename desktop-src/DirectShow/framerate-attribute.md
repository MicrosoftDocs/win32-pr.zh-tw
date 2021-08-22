---
description: 畫面播放速率屬性指定畫面播放速率（以每秒畫面格數為單位）。
ms.assetid: 541a86e3-7736-4de4-b509-f8d61ef9bc58
title: " (DirectShow) 的畫面播放速率屬性"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2939126dbd849538bb30fcf7729e5f91dafa292b6db512398c915c8f8de2c9a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015656"
---
# <a name="framerate-attribute-directshow"></a> (DirectShow) 的畫面播放速率屬性

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`framerate`屬性指定畫面播放速率（以每秒畫面格數為單位）。

## <a name="possible-values"></a>可能的值

浮點值。 值必須在小數點之前包含前置零。 例如，0.3，而不是. 3。 請勿使用超過7個小數位數。

## <a name="applies-to"></a>套用至

[**剪輯**](clip-element.md)、 [**群組**](group-element.md)、 [**時間軸**](timeline-element.md)

## <a name="remarks"></a>備註

若為 **剪切** 元素，這個屬性會指定來源的預設畫面播放速率。 指定 [靜止影像 andDIB 順序] 的屬性。 若為靜止影像，請將值設定為零。 若為 DIB 順序，請使用非零值。 預設值為零。

針對 **群組** 專案，這個屬性會指定群組的輸出畫面播放速率。

若為 **時間軸** 元素，這個屬性會指定所有群組的預設畫面播放速率。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 屬性](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md)
</dt> <dt>

[**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md)
</dt> <dt>

[**IAMTimeline::SetDefaultFPS**](iamtimeline-setdefaultfps.md)
</dt> </dl>

 

 




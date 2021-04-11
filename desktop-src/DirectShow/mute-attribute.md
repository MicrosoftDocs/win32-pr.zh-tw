---
description: 靜音屬性指定物件的靜音狀態。
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: 靜音屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4e43feb16d75312cedd0caf5c217af2dd71332
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109433"
---
# <a name="mute-attribute"></a>靜音屬性

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`mute`屬性會指定物件的靜音狀態。 如果值為 **TRUE**，則不會轉譯物件和其子系。 如果此值為 **FALSE**，則會轉譯物件，並根據其本身的靜音狀態來呈現其子系。 預設值為 **FALSE**。

## <a name="possible-values"></a>可能的值

下列值定義為 TRUE： y、Y、t、T、1。 下列值定義為 FALSE： n、N、f、F、0 (零) 。

## <a name="applies-to"></a>套用至

[**剪輯**](clip-element.md)、 [**複合**](composite-element.md)、 [**效果**](effect-element.md)、 [**群組**](group-element.md)、 [**時間軸**](timeline-element.md)、 [**轉換**](transition-element.md)

## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 屬性](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetMuted**](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 




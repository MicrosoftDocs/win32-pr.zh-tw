---
description: Lock 屬性指定是否應編輯物件。 如果該值為 TRUE，則應用程式應該將物件視為鎖定，而且不允許對該物件或其子系進行變更。 預設值為 FALSE。
ms.assetid: 1aa92665-ab3b-4f04-9e6b-905942c197ef
title: lock 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdd1718c25aab136219af436543df064bd8f68bb53ea15b00e09e6a18188c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502318"
---
# <a name="lock-attribute"></a>lock 屬性

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`lock`屬性指定是否應編輯物件。 如果該值為 **TRUE**，則應用程式應該將物件視為鎖定，而且不允許對該物件或其子系進行變更。 預設值為 **FALSE**。

## <a name="possible-values"></a>可能的值

可能的值會將下列值定義為 TRUE： y、Y、t、T、1。 下列值定義為 FALSE： n、N、f、F、0 (零) 。

## <a name="applies-to"></a>套用至

[**剪輯**](clip-element.md)、 [**複合**](composite-element.md)、 [**效果**](effect-element.md)、 [**群組**](group-element.md)、 [**時間軸**](timeline-element.md)、 [**轉換**](transition-element.md)

## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 屬性](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetLocked**](iamtimelineobj-setlocked.md)
</dt> </dl>

 

 




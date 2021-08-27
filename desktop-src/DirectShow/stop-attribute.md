---
description: Stop 屬性會指定相對於父物件之物件的停止時間。
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: stop 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f8ccae1ff4a9a067ccf8ee90438cfb87e3260d41a7fac009afb4b4153e4ddf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050169"
---
# <a name="stop-attribute"></a>stop 屬性

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`stop`屬性會指定相對於父物件之物件的停止時間。

## <a name="possible-values"></a>可能的值

必須是格式為 *hh： mm： ss* 格式的字串，其中 *hh* = hours， *mm* = 分鐘， *ss* = 秒，而 *ff* = 秒數的分數。 範例：1：04：30.512。 您可以省略前置單位。 例如，3:00 (三分鐘) 和 45 (45 秒) 都有效。

## <a name="applies-to"></a>套用至

[**剪輯**](clip-element.md)、 [**效果**](effect-element.md)、 [**轉換**](transition-element.md)

## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 屬性](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 




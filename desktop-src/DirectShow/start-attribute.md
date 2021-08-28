---
description: Start 屬性會指定相對於父物件之物件的開始時間。
ms.assetid: 971de88e-c1ee-4e07-bf8e-3153e4fd11f3
title: start 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 227b04a8cd7dc366a9cf10a4930233cd834e2bea7faa64bb59c248049b9e9abe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650988"
---
# <a name="start-attribute"></a>start 屬性

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`start`屬性會指定相對於父物件之物件的開始時間。

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

 

 




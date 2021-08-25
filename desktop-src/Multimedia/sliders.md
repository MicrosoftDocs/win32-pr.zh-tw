---
title: " (Windows 多媒體) 的滑杆"
description: 滑桿
ms.assetid: cfd82672-5b22-4b59-82b5-15ca68a451fc
keywords:
- 音訊 mixers，控制項
- 音訊 mixers、滑杆
- mixers，控制項
- mixers、滑杆
- 滑桿
- MIXERCONTROLDETAILS_SIGNED 結構
- 平移控制項
- QSound pan 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e902e3ead0416cb4b2a7d56d289f91779563109cb9494784635affc75069dfe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805348"
---
# <a name="sliders-windows-multimedia"></a> (Windows 多媒體) 的滑杆

滑杆控制項通常是可向左或向右調整的水準控制項。 這些控制項使用 [**MIXERCONTROLDETAILS \_ 簽署**](/previous-versions//dd757297(v=vs.85)) 的結構來抓取和設定控制項屬性。 下表描述滑杆的類型。



| 控制    | 描述                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| Slider     | 的範圍為–32768到32767。 混音器驅動程式會定義此控制項的限制。                               |
| 移動瀏覽        | 的範圍為–32768到32767。 混音器驅動程式會定義此控制項的限制，並以0作為中型值。 |
| QSound Pan | 提供透過 QSound 展開的音效控制項。 此控制項的範圍為–15到15。                               |



 

 

 

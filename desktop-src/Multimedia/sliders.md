---
title: Windows 多媒體) 滑杆 (
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
ms.openlocfilehash: 4d1d7644255e2fa9ee6384cbb5102df81c2a1eb0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383630"
---
# <a name="sliders-windows-multimedia"></a>Windows 多媒體) 滑杆 (

滑杆控制項通常是可向左或向右調整的水準控制項。 這些控制項使用 [**MIXERCONTROLDETAILS \_ 簽署**](/previous-versions//dd757297(v=vs.85)) 的結構來抓取和設定控制項屬性。 下表描述滑杆的類型。



| 控制    | 描述                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| 滑桿     | 的範圍為–32768到32767。 混音器驅動程式會定義此控制項的限制。                               |
| 移動瀏覽        | 的範圍為–32768到32767。 混音器驅動程式會定義此控制項的限制，並以0作為中型值。 |
| QSound Pan | 提供透過 QSound 展開的音效控制項。 此控制項的範圍為–15到15。                               |



 

 

 

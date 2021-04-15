---
title: 米
description: 米
ms.assetid: 11a98d2a-7cdd-4249-bba9-7edc51d7f8b0
keywords:
- 音訊 mixers，控制項
- 音訊 mixers，計量
- mixers，控制項
- mixers，計量
- 計量控制項
- MIXERCONTROLDETAILS_BOOLEAN 結構
- MIXERCONTROLDETAILS_SIGNED 結構
- MIXERCONTROLDETAILS_UNSIGNED 結構
- 布林值控制項
- 尖峰控制
- 簽署的控制項
- 未簽署的控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36f1bebfca22b963e5c1eb6fede3f2786b35199
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463144"
---
# <a name="meters"></a>米

量測計控制項會測量透過音訊行傳遞的資料。 這些控制項使用 [**MIXERCONTROLDETAILS 的 \_ 布林值**](/previous-versions//dd757295(v=vs.85))、 [**MIXERCONTROLDETAILS \_ 簽署**](/previous-versions//dd757297(v=vs.85))和 [**MIXERCONTROLDETAILS 不 \_ 帶正負**](/previous-versions//dd757298(v=vs.85)) 號的結構來取得和設定控制項屬性。 下表描述計量的類型。



| 控制  | 描述                                                                                                                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boolean  | 測量整數值是否為 FALSE/OFF (零) 或 TRUE/ON (非零) 。                                                                            |
| Peak     | 從0開始測量正面和負面方向的偏離。 尖峰計量的整數值範圍是–32768到32767。 |
| 簽署人   | 測量介於-231 到 (231 – 1) 範圍內的整數值。 混音器驅動程式會定義此計量的限制。                                     |
| 不帶正負號 | 測量0到 (232 – 1) 範圍內的整數值。 混音器驅動程式會定義此計量的限制。                                        |



 

 

 
---
title: Windows 多媒體) 的數位 (
description: 數字
ms.assetid: d416c4c2-a3e1-45a2-9ae1-82050a5e471b
keywords:
- 音訊 mixers，控制項
- 音訊 mixers，數位
- mixers，控制項
- mixers，數位
- 數位控制項
- MIXERCONTROLDETAILS_SIGNED 結構
- MIXERCONTROLDETAILS_UNSIGNED 結構
- 分貝控制項
- 控制百分比
- 簽署的控制項
- 未簽署的控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c9e1bacdea3f52129d78eea2f0bc7134df08b7077c83510bd8de824777e524
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806618"
---
# <a name="numbers-windows-multimedia"></a>Windows 多媒體) 的數位 (

Number 控制項可讓使用者輸入與線條相關聯的數值資料。 數值資料會以帶正負號的整數、不帶正負號的整數或整數分貝值表示。 這些控制項使用 [**MIXERCONTROLDETAILS \_ 簽署**](/previous-versions//dd757297(v=vs.85)) 和 [**MIXERCONTROLDETAILS 不 \_ 帶正負**](/previous-versions//dd757298(v=vs.85)) 號的結構來取得和設定控制項屬性。 下表描述數位控制項的類型。



| 控制  | 描述                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| 簽署人   | 允許在–231到 (231 – 1) 範圍中輸入的整數值。                                                               |
| 不帶正負號 | 允許從0到 (232 – 1) 的範圍輸入整數值。                                                                   |
| 分貝  | 允許輸入整數分貝值（以分貝為單位）。 此控制項的值範圍為–32768到32767。 |
| 百分比  | 允許將值輸入為百分比。                                                                                         |



 

 

 

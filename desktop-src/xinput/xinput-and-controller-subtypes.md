---
title: XINPUT 和控制器子類型
description: XInput 中可用的控制器子類型資料表。
ms.assetid: 4674028b-98cf-5346-7b93-f940150f3051
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd03fe292e2b8d59b99416bded26945a71dfb9f
ms.sourcegitcommit: b3839bea8d55c981d53cb8802d666bf49093b428
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/16/2021
ms.locfileid: "114373212"
---
# <a name="xinput-and-controller-subtypes"></a>XINPUT 和控制器子類型

XInput 中可用的控制器子類型資料表。



| Subtype                               | 值 | 意義                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| XINPUT \_ DEVSUBTYPE \_ 不明           | 0x00  | 未知。<br/> 控制器類型未知。<br/>                                                                                                                                                                                                                                                                                                                                                                |
| XINPUT \_ DEVSUBTYPE \_ 遊戲           | 0x01  | 遊戲台控制器。<br/> 包含左右箭號、左和右觸發程式、方向板，以及所有標準按鈕 (A、B、X、Y、START、BACK、LB、RB、LSB、RSB) 。<br/>                                                                                                                                                                                                                                     |
| XINPUT \_ DEVSUBTYPE \_ 輪子             | 0x02  | 賽車控制器。 <br/> 左搖杆 X 報告滾輪旋轉、Right 觸發程式是加速踏板，而左方觸發程式是煞車踏板。 包含方向板和大部分標準按鈕 (A、B、X、Y、START、BACK、LB、RB) 。 LSB 和 RSB 是選擇性的。<br/>                                                                                                                                        |
| XINPUT \_ DEVSUBTYPE \_ ARCADE \_ 搖杆     | 0x03  | Arcade 杆控制器。 <br/> 包含的數位杆會以 DPAD 的方式報告， (向上、向下、向左、右) ，以及大部分標準按鈕 (A、B、X、Y、START、BACK) 。 左邊和右邊的觸發程式會實作為數位按鈕，並報告0或0xFF。 LB、LSB、RB 和 RSB 是選擇性的。<br/>                                                                                                                  |
| XINPUT \_ DEVSUBTYPE \_ 航班 \_ 杆     | 0x04  | 飛行杆控制器。 <br/> 包含用來報告為左方杆的 POV Hat、會回報為右邊的 POV Hat (、滾輪會處理報告為左方觸發程式的扭曲或) ，以及做為右邊觸發程式的節流閥控制項。 包含主要武器的支援 () 、次要武器 (B) ，以及其他標準按鈕 (X、Y、START、BACK) 。 LB、LSB、RB 和 RSB 是選擇性的。<br/>  |
| XINPUT \_ DEVSUBTYPE \_ DANCE \_ PAD        | 0x05  | Dance pad 控制器。 <br/> 包含方向板和標準按鈕 (A、B、X、Y) 板上，再加上一步和開始。<br/>                                                                                                                                                                                                                                                                                  |
| XINPUT \_ DEVSUBTYPE \_ 吉他            | 0x06  | 吉他控制器。 <br/> Strum 列會對應至 DPAD (向上和向下) ，而 frets 會指派給 (綠色) 、B (紅色) 、Y (黃色) 、X (藍色) 和 LB (橙色) 。 右搖杆 Y 與垂直方向感應器相關聯;右搖杆 X 是 whammy 橫條。 包括對 BACK、START、DPAD (left、right) 的支援。 左方觸發程式 (取貨選取器) 、Right Trigger、RB、LSB (煩惱修飾詞) 、RSB 是選擇性的。<br/> |
| XINPUT \_ DEVSUBTYPE \_ 吉他 \_ 替代 | 0x07  | 替代吉他控制器。 <br/> 針對垂直方向感應器支援更大範圍的移動。<br/>                                                                                                                                                                                                                                                                                                  |
| XINPUT \_ DEVSUBTYPE \_ 鼓 \_ 套件         | 0x08  | 鼓控制器。<br/> 硒鼓板會指派給按鈕： A 代表綠色 (地面 Tom) 、B 代表紅色 (Snare 鼓) 、X 表示藍色 (低 Tom) 、Y 代表黃色 (高 Tom) ，以及 LB 的踏板 (低音鼓) 。 包含方向板、背面和開始。 RB、LSB 和 RSB 是選擇性的。<br/>                                                                                                                                     |
| XINPUT \_ DEVSUBTYPE \_ 吉他 \_ 低音      | 0x0B  | 低音吉他控制器。 <br/> 與吉他相同，其具有相異子類型，以簡化安裝。<br/>                                                                                                                                                                                                                                                                                                              |
| XINPUT \_ DEVSUBTYPE \_ ARCADE \_ PAD       | 0x13  | Arcade pad 控制器。 <br/> 包含方向板和大部分標準按鈕 (A、B、X、Y、START、BACK、LB、RB) 。 左邊和右邊的觸發程式會實作為數位按鈕，並報告0或0xFF。 左搖杆、右搖杆、LSB 和 RSB 是選擇性的。<br/>                                                                                                                                           |
> [!Note]  
> Windows Vista (XINPUT 9.1.0) 的舊版 XINPUT，一律會傳回 **XINPUT \_ DEVSUBTYPE \_ 遊戲台** 的固定子類型，而不論連接的裝置為何。

---
title: 色調效果
description: 這會影響來源影像的色彩，方法是將來源影像乘以指定的色彩。 它有單一輸入。
ms.assetid: b0fd3598-26b6-faee-4f10-ebba96241bc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f12e7593f9cb0695a6adb7b955fb66b13c8d00b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934305"
---
# <a name="tint-effect"></a>色調效果

這會影響來源影像的色彩，方法是將來源影像乘以指定的色彩。 它有單一輸入。

這項效果的 CLSID 是 CLSID \_ D2D1Tint。

## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                    | 類型和預設值                              | Description                                                      |
|-------------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------|
| ColorD2D1 \_ 色調 \_ 的 \_ 色彩<br/>               | D2D1 \_ VECTOR \_ 4F (1.0 f、1.0 f、1.0 f、1.0 f) <br/> | 來源影像中的色彩會乘以此值。       |
| ClampOutputD2D1 \_ 色調 \_ 的 \_ 夾具 \_ 輸出<br/> | BOOLFALSE<br/>                                | 是否要將輸出值夾具至範圍 \[ 0，1 \] 。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|---------------------------------------------------|
| 最低支援的用戶端 | Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\] |
| 最低支援的伺服器 | Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\] |
| 標頭                   | d2d1effects \_ 2。h                                  |
| 程式庫                  | d2d1 .lib，dxguid .lib                              |



 ## <a name="related-topics"></a>相關主題

* [ID2D1Effect 介面](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

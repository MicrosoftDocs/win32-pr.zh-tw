---
title: 交叉淡出效果
description: 此效果結合了兩個影像，方法是從輸入影像新增加權圖元。 它有兩個輸入，名為 [目的地] 和 [來源]。
ms.assetid: 5214b70a-d024-ba3e-771f-07d98d2278ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904ac8e4e27efc646bb71b1766c8763bd64beb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508543"
---
# <a name="cross-fade-effect"></a>交叉淡出效果

此效果結合了兩個影像，方法是從輸入影像新增加權圖元。 它有兩個輸入，名為 [目的地] 和 [來源]。

交叉淡化公式是 **輸出 = 權數 \* 目的地 + (1 權數) \* 來源**。

這項效果的 CLSID 是 CLSID \_ D2D1CrossFade。

## <a name="effect-properties"></a>效果屬性

| 顯示名稱和索引列舉             | 類型和預設值 | Description                                                                                                                                                                                                                                                       |
|------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WeightD2D1 \_ CROSSFADE 的值 \_ \_ 加權<br/> | FLOAT 0.5 f<br/>   | 要對來源影像的色彩值與目的影像進行權衡的程度。 最小值為 0.0 f (以獨佔方式使用目的影像來判斷輸出) ，最大值為 1.0 f (以獨佔方式使用來源映射來判斷輸出) 。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|---------------------------------------------------|
| 最低支援的用戶端 | Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\] |
| 最低支援的伺服器 | Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\] |
| 標頭                   | d2d1effects \_ 2。h                                  |
| 程式庫                  | d2d1 .lib，dxguid .lib                              |

## <a name="related-topics"></a>相關主題

* [ID2D1Effect 介面](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

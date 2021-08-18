---
title: 不透明度效果
description: 此效果會將輸入的 Alpha 色板乘以指定的不透明度值，以調整影像的不透明度。 它有單一輸入。
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58073e3b692b45f86f57c61571d81f5add47427c8a1a801ac43121b37aa43a67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636228"
---
# <a name="opacity-effect"></a>不透明度效果

此效果會將輸入的 Alpha 色板乘以指定的不透明度值，以調整影像的不透明度。 它有單一輸入。

這項效果的 CLSID 是 CLSID \_ D2D1Opacity。

## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉              | 類型和預設值 | 描述                                                                                                 |
|-------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| 不透明度 \_ D2D1 不透明度的情況 \_ \_<br/> | FLOAT 1.0 f<br/>   | 輸入影像 Alpha 色板的乘數。 最小值為 0.0 f，最大值為 1.0 f。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|---------------------------------------------------|
| 最低支援的用戶端 | Windows 10 \[桌面應用程式 \| Windows 儲存應用程式\] |
| 最低支援的伺服器 | Windows 10 \[桌面應用程式 \| Windows 儲存應用程式\] |
| 標頭                   | d2d1effects \_ 2。h                                  |
| 程式庫                  | d2d1 .lib，dxguid .lib                              |


## <a name="related-topics"></a>相關主題

* [ID2D1Effect 介面](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

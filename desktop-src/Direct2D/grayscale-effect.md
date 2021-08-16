---
title: 灰階效果
description: 將影像轉換為灰色。
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b74e553074b3ee0c9ad4e0d5121b9b084884ddb030c75308eb9964531fc6b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075327"
---
# <a name="grayscale-effect"></a>灰階效果

將影像轉換為灰色。

灰階使用下列矩陣，將色彩矩陣效果轉換成灰階：

![轉換矩陣](images/grayscale-effect-matrix.png)

這項效果的 CLSID 是 CLSID \_ D2D1Grayscale。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

![效果輸出的範例](images/grayscale-effect.png)

## <a name="effect-properties"></a>效果屬性

此效果沒有屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|---------------------------------------------------|
| 最低支援的用戶端 | Windows 10 \[桌面應用程式 \| Windows 儲存應用程式\] |
| 最低支援的伺服器 | Windows 10 \[桌面應用程式 \| Windows 儲存應用程式\] |
| 標頭                   | d2d1effects \_ 2。h                                  |
| 程式庫                  | d2d1 .lib，dxguid .lib                              |


## <a name="related-topics"></a>相關主題

* [ID2D1Effect 介面](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

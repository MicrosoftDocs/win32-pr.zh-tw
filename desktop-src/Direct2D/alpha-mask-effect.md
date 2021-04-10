---
title: Alpha 遮罩效果
description: 此效果會將 Alpha 遮罩套用至影像。 它有兩個輸入，名為 Destination 和 Mask。 目的地影像中的色彩值會乘以遮罩影像的 Alpha 色板。
ms.assetid: fddad107-ec70-3a24-f4ae-9dc4f3716536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87669608ab75ab7a655c072e174dbcd19df4bb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106560"
---
# <a name="alpha-mask-effect"></a>Alpha 遮罩效果

此效果會將 Alpha 遮罩套用至影像。 它有兩個輸入，名為 Destination 和 Mask。 目的地影像中的色彩值會乘以遮罩影像的 Alpha 色板。

這項效果的 CLSID 是 CLSID \_ D2D1AlphaMask。

## <a name="effect-properties"></a>效果屬性

此效果沒有任何作用中的特定屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|---------------------------------------------------|
| 最低支援的用戶端 | Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\] |
| 最低支援的伺服器 | Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\] |
| 標頭                   | d2d1effects \_ 2。h                                  |
| 程式庫                  | d2d1 .lib，dxguid .lib                              |

## <a name="related-topics"></a>相關主題

* [ID2D1Effect 介面](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)


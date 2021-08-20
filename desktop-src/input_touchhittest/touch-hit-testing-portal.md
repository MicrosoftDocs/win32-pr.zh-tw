---
title: 觸控點擊測試
description: 本節中的主題提供 Windows 8 中觸控點擊測試支援的總覽。
ms.assetid: bdd7630c-b2d8-4080-a149-efec018f697d
keywords:
- 使用者互動
- input
- 指標
- 觸控
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 0fe92769a3b7a9325f5cdea47e52d4b849d77db75cbf0eda4b1df8a4280f6f8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884315"
---
# <a name="touch-hit-testing"></a>觸控點擊測試

## <a name="purpose"></a>目的

本節中的主題提供 Windows 中觸控點擊測試支援的總覽。 觸控點擊測試可讓您根據 UI 元素的內容區域是否落在連絡人區域內，或包含連絡人點，來識別輸入目標。

觸控點擊測試會針對整個觸控區域使用複雜的連絡人幾何，而不是單一的插補 x y 座標。 當您識別觸控輸入最可能的目標時，使用整個連絡人幾何可大幅提升精確度和精確度。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
| --- | --- |
| [觸控點擊測試參考](touchhittest-reference.md)<br/> | 本節中的主題提供 [觸控點擊測試](touch-hit-testing-portal.md)的參考規格。<br/> |

## <a name="developer-audience"></a>開發人員對象

觸控點擊測試 Api 是針對建立 UI 架構的開發人員所設計，可在桌面應用程式之間提供一致的觸控優化使用者體驗。

## <a name="related-topics"></a>相關主題

[使用者互動](../user-interaction.md)

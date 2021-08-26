---
description: 您可以使用漸層筆刷，以逐漸變更的色彩填滿形狀。
ms.assetid: e37b4c3a-b753-483a-990f-da3bcc70acf5
title: 使用漸層筆刷填滿圖案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d471e9d3e2d7fb6d151d50ab3b5f10212874180b4554769b5c00a552085391
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015048"
---
# <a name="filling-shapes-with-a-gradient-brush"></a>使用漸層筆刷填滿圖案

您可以使用漸層筆刷，以逐漸變更的色彩填滿形狀。 例如，您可以使用水準漸層來填滿圖形，其色彩會隨著您從圖形的左邊緣移至右邊緣而逐漸變更。 Imagine 矩形，其左邊緣為黑色 (以紅色、綠色和藍色元件表示的黑色以紅色、綠色和藍色元件0、0、0) 和右邊緣（以255、0、0) 表示的紅色 (表示）。 如果矩形的寬度為256圖元，則指定圖元的紅色元件將會大於其左邊圖元的紅色元件。 資料列中最左邊的圖元具有色彩元件 (0、0、0) 、第二個圖元 (1、0、0) 、第三個圖元有 (2、0、0) 等，直到您到達最右邊的圖元，其中有色彩元件 (255、0、0) 。 這些插補色彩值會構成色彩漸層。

當您以水準、垂直或平行方式移動至指定的斜線時，線性漸層會變更色彩。 當您移動路徑的內部和界限時，路徑漸層會變更色彩。 您可以自訂路徑漸層以達成各種效果。

GDI+ 提供 [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)和 [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush)類別，這兩個類別都會繼承自 [**筆刷**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)類別。

下列主題會更詳細地討論線性和路徑漸層：

-   [建立線性漸層](-gdiplus-creating-a-linear-gradient-use.md)
-   [建立路徑漸層](-gdiplus-creating-a-path-gradient-use.md)
-   [將 Gamma 修正套用至漸層](-gdiplus-applying-gamma-correction-to-a-gradient-use.md)

 

 




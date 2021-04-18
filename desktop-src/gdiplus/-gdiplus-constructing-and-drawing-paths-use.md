---
description: 路徑是圖形基本專案的序列， (線條、矩形、曲線、文字和類似的) ，可操作並繪製為單一單位。 路徑可以分割成已開啟或已關閉的圖形。 圖可包含數個基本類型。
ms.assetid: dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4
title: 建構和繪製路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe5f1528e58e3df19afbc83bb6acfdc2a6fca19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991375"
---
# <a name="constructing-and-drawing-paths"></a>建構和繪製路徑

路徑是圖形基本專案的序列， (線條、矩形、曲線、文字和類似的) ，可操作並繪製為單一單位。 路徑可以分割成已開啟或已關閉的 *圖形* 。 圖可包含數個基本類型。

您可以藉由呼叫 graphics 類別的 [**graphics：:D rawpath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath)方法來繪製路徑，而且可以藉由呼叫 **Graphics** [**類別的**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) [**graphics：： FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)方法來填滿路徑。

下列主題會更詳細地討論路徑：

-   [從線條、曲線和形狀建立圖形](-gdiplus-creating-figures-from-lines-curves-and-shapes-use.md)
-   [填滿開放圖形](-gdiplus-filling-open-figures-use.md)

 

 




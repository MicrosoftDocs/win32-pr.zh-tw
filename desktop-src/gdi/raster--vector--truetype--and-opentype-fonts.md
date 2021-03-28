---
description: 點陣、向量、TrueType 和 OpenType 字型
ms.assetid: 4fe98f04-3fb0-4a03-86c3-d0ea6f07f8f0
title: 點陣、向量、TrueType 和 OpenType 字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9b4be20ac7d02075fcd5c6cdbefe9eb516ea21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991179"
---
# <a name="raster-vector-truetype-and-opentype-fonts"></a>點陣、向量、TrueType 和 OpenType 字型

應用程式可以使用四種不同的字型技術來顯示和列印文字：

-   光柵
-   向量
-   TrueType
-   Microsoft OpenType

這些字型之間的差異反映了每個字元或 *符號的圖像* 儲存在個別字型資源檔中的方式：

-   在點陣字型中，圖像是系統用來在字型中繪製單一字元或符號的點陣圖。
-   在向量字型中，圖像是線條端點的集合，可定義系統用來在字型中繪製字元或符號的線段。
-   在 TrueType 和 OpenType 字型中，圖像是線條和曲線命令的集合，以及提示的集合。

系統會使用 line 和 curve 命令，為 TrueType 或 Microsoft OpenType 字型中的字元或符號定義點陣圖的外框。 系統會使用提示來調整用來繪製字元或符號之曲線的線條和圖形長度。 這些提示和個別的調整是根據用來減少或增加點陣圖大小的縮放量。 OpenType 字型相當於 TrueType 字型，不同之處在于 OpenType 字型除了 TrueType 圖像定義之外，還允許 PostScript 圖像定義。

由於點陣字型中每個字元的點陣圖都是針對特定的裝置解析度所設計，因此，通常會將點陣字型視為裝置相依。 相反地，向量字型與裝置無關，因為每個圖像都會儲存為可擴充行的集合。 不過，向量字型的繪製速度通常比點陣或 TrueType 和 OpenType 字型更慢。 TrueType 和 OpenType 字型提供相對快速的繪圖速度和真正的裝置獨立性。 藉由使用與圖像相關聯的提示，開發人員可以將 TrueType 或 OpenType 字型的字元向上或向下調整，並仍維持其原始圖形。

如先前所述，字型的字元會儲存在字型資源檔中。 字型資源檔實際上是包含資料的 DLL，沒有任何程式碼。 針對點陣和向量字型，此資料分為兩個部分：描述字型計量和字元資料的標頭。 點陣或向量字型的字型資源檔是以 fon 副檔名來識別。 針對 TrueType 和 OpenType 字型，每個字型都有兩個檔案：第一個檔案包含相對較短的標頭，而第二個則包含實際的字型資料。 第一個檔案是以受副檔名來識別，而第二個檔案則是以 ttf 副檔名來識別。

 

 




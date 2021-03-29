---
description: GraphicsPath 物件會儲存一連串的行和 B&\# 233; zier 曲線。
ms.assetid: 8ce77146-dc28-4c0b-bcf0-dad4bf3d86e8
title: 簡維路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caee9b8d760d9702b6a3ea7711090f001a57912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987717"
---
# <a name="flattening-paths"></a>簡維路徑

[**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath)物件會儲存一連串的線條和貝茲曲線。 您可以將數種類型的曲線 (省略號、弧形、基線曲線) 至路徑，但每個曲線都會轉換成貝茲曲線，然後才會將它儲存在路徑中。 簡維路徑包含將路徑中的每個貝茲曲線轉換成一連串的直線。

若要壓平合併路徑，請呼叫 [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath)物件的 [**GraphicsPath：：**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-flatten)簡維方法。 **GraphicsPath：：** 簡維方法會收到 flatness 引數，以指定壓平合併路徑與原始路徑之間的最大距離。 下圖顯示簡維之前和之後的路徑。

![顯示藍色的連接貝茲曲線序列，以及紅色的對應行的圖例](images/aboutgdip02-art32a.png)

 

 




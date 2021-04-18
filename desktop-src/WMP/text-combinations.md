---
title: 文字組合
description: 文字組合
ms.assetid: 0220b77e-5f1e-4569-a8fe-5085e0c16338
keywords:
- Windows Media Player 行動外觀、字幕
- 外觀、字幕
- 外觀、字幕的參考
- 外觀、文字組合中的字幕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5668a9e18555b871c82bae7ed1826766ec9429e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507284"
---
# <a name="text-combinations"></a>文字組合

此值是文字顯示方塊組合的清單，以逗號分隔。 文字顯示方塊可透過加號聯結在一起，以建立新的天棚顯示值，而且在 [文字類型] 區段中定義的任何文字類型都可以在您的字幕中使用。

當您決定要顯示的內容時，Windows Media Player 行動裝置會評估清單中的每個專案，以查看是否有可用的元件。 如果沒有，則會評估下一個專案，依此類推，直到找到所有可用的部分為止。 例如，如果您想要顯示 [作者] 和 [標題]，但不確定兩者是否可用，請使用下列值：


```C++
Title+Author, Title, Author

```



在上述範例中，如果已針對媒體專案定義標題和作者，則會顯示 [標題 + 作者]。 如果兩者都未定義，則會評估標題，並在已定義時顯示。 如果未定義標題，則會顯示作者（若已定義）。 如果未定義任何專案，則不會顯示任何內容。

使用加號進行串連時，請確定加號的任一邊都沒有空格。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Marquee**](marquee.md)
</dt> <dt>

[**文字類型**](text-type.md)
</dt> </dl>

 

 





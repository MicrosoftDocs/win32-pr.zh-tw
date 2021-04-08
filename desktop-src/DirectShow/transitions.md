---
description: 轉換
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: 轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fef1cd888293ad83ab1ba9f05ab4bb83ddafa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852147"
---
# <a name="transitions"></a>轉換

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

轉換是一種從某個影片播放軌 segue 至另一個影片播放軌的方式，使用淡出或抹除等視覺效果。 下圖顯示具有轉換的時程表：

![具有轉換的時程表](images/timeline3.png)

轉換物件是在 track 1，它代表從 track 0 到 track 1 的轉換。 在轉換開始時，轉譯的影片完全取自追蹤 0 (來源 A) 。 最後，影片完全取自追蹤 1 (來源 C) 。 從開始，輸出會從來源 A 轉換成來源 C。例如，在淡化轉換中，有一個來源會逐漸淡化為另一個來源。 最後的輸出會沿著圖底部架構化。

轉換無法在相同的播放軌內重迭，但您可以使用組合物件建立重迭的轉換，如 [撰寫和分層](composition-and-layering.md)中所述。

轉換有方向。 根據預設，它會從較低優先順序的追蹤開始， (來源 A （在先前的範例中）。 ) ，並以較高優先順序的播放軌 (來源 C) 。 在兩者之間，影片是兩個來源的混合。 不過，您可以指定相對的行為，如下圖所示：

![具有兩個轉換的 ntrack](images/fade.png)

在這裡，第一個轉換會淡出曲目0淡化 track 1，這是預設行為。 第二個轉換會從曲目1淡回以追蹤0。 請注意，這兩個轉換都位於曲目1上。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DirectShow 編輯服務開始使用](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[轉換和效果](transitions-and-effects.md)
</dt> <dt>

[使用效果和轉換](working-with-effects-and-transitions.md)
</dt> </dl>

 

 




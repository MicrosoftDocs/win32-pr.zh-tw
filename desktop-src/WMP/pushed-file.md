---
title: 推送的檔案
description: 推送的檔案
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Windows Media Player 行動外觀、美工檔案
- 外觀、美工檔案
- 適用于外觀、藝術的檔案
- 面板的美工檔案，推送的檔案
- Windows Media Player 行動面板，推送的檔案
- 外觀，推送的檔案
- 面板中推送的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a6a4fd00eee7040d2fadb8fb80db343dc0ac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372273"
---
# <a name="pushed-file"></a>推送的檔案

推送的檔案包含當使用者按下按鈕時將顯示的影像。 您也可以在 [PlayPause] 按鈕的暫停狀態中包含正常和推送的影像。

下圖是典型的推送檔案。

![推送的檔案](images/cesdkpus.png)

這會儲存在點擊點擊類型按鈕時所顯示的影像。 也儲存在此檔案中，是 PlayPause 按鈕暫停影像的一般和推送映射。 除了右邊的 PlayPause 次要影像之外，另一個按鈕影像會以背景影像對齊，並使用在面板定義檔的 [點陣圖] 區段中定義的位移。

請注意，按鈕影像的背景完全符合背景檔案中對應的區域。 這點很重要，因為當使用者按下 [點擊類型] 按鈕時，針對推送影像定義的整個矩形將會取代背景檔案中的相符區域。 讓圖形保持與背景影像一致，以確保只有您想要顯示的按鈕部分會實際變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**美工檔案**](art-files-mobile.md)
</dt> </dl>

 

 





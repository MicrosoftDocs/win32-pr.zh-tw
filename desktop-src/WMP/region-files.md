---
title: 區域檔案
description: 區域檔案
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Windows Media Player 行動外觀、美工檔案
- 外觀、美工檔案
- 適用于外觀、藝術的檔案
- 適用于外觀、區域檔案的美工檔案
- Windows Media Player 行動外觀、區域檔案
- 外觀，區域檔案
- 外觀中的區域檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d258afeab029df7218d3616b8aecdb62c72806
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311114"
---
# <a name="region-files"></a>區域檔案

如果您使用任何類型的點擊按鈕 (2PushHit、PushHit 或 ToggleHit) ，就需要區域檔案。

區域檔案是用來定義區域，這些區域會在特定按鈕上回應點一下，也稱為點擊。 針對每個點擊按鈕，區域點陣圖中的區域會獲得特定的 Web 色彩 (例如 \# FF0000，這是純紅色) 的值。 顏色編號是在區域按鈕定義中指定的。 當使用者顯示面板時，按鈕影像會使用區域點陣圖中區域的座標來重迭到背景。

例如，您可以在對應至 [下一步] 按鈕位置的位置繪製紅色圓圈，並將其設為純紅色 (\# FF0000) 。 然後，在按鈕定義中，您可以指派255、0、0 (的點擊 RGB 值，這是 FF0000) 的 RGB 對等專案 \# 。 在此情況下，[下一步] 按鈕只會回應在紅色圓圈內) 的點擊 (叫用。

當您想要定義矩形以外的圖形時，就會使用點擊按鈕。 您仍然必須定義每個按鈕的座標，才能正確地找出已推送和已停用的次要影像。 在實務上，每個按鈕都會以矩形來系結，而這些虛數界限矩形不得重迭。

> [!Note]  
> Windows Media Player 10 行動面板中不需要區域藝術檔案，因為 Windows Media Player 10 行動裝置版或更新版本不支援按鈕類型。

 

下圖是一般的區域檔案。

![區域檔案](images/cesdkreg.png)

此檔案會定義每個點擊類型按鈕的面板部分。 每個色彩都會依面板定義檔之按鈕區段中的色彩數位來識別。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**美工檔案**](art-files-mobile.md)
</dt> </dl>

 

 





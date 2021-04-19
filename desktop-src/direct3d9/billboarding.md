---
description: 在建立3D 場景時，應用程式有時會以使其成為3D 物件的方式轉譯2D 物件，以獲得效能優勢。 這是 billboarding 技術背後的基本概念。
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: 'Billboarding (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e287624ef8800f0b66941e826e211d044b7bf27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970740"
---
# <a name="billboarding-direct3d-9"></a>Billboarding (Direct3D 9) 

在建立3D 場景時，應用程式有時會以使其成為3D 物件的方式轉譯2D 物件，以獲得效能優勢。 這是 billboarding 技術背後的基本概念。

單字正常意義的佈告欄是一種 roadway 的正負號。 Microsoft Direct3D 應用程式可以藉由定義矩形實線並對其套用材質，來建立和轉譯這種類型的佈告欄。 以更特製化的3D 圖形方式 Billboarding 是此的延伸。 目標是讓2D 物件顯示為3D。 技術是將包含物件影像的材質套用至矩形基本。 原始物件會旋轉，讓它一律會臉部給使用者。 如果物件的影像不是矩形，就不會有任何影響。 您可以將佈告欄的部分設為透明，所以看不到您不想要看到的佈告欄影像部分。

許多遊戲都採用 billboarding 來進行動畫 sprite。 例如，當使用者透過3D 迷宮移動時，可能會看到可挑選的武器或獎勵。 這些通常是以矩形為基本的2D 影像。 Billboarding 通常會在遊戲中用來呈現樹狀結構、bushes 和雲端的影像。

將影像套用至佈告欄時，必須先旋轉矩形基本型別，使產生的影像臉部給使用者。 然後，您的應用程式必須將它轉譯成位置。 然後，應用程式可以將材質套用至基本。

Billboarding 最適用于對稱物件，尤其是沿著垂直軸對稱的物件。 這也需要觀點的高度不會增加太多。 如果允許使用者查看上述的 billboarded，就會很容易看出物件是2D 而非3D。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Alpha 範例](alpha-examples.md)
</dt> </dl>

 

 




---
description: 系統會以不同于畫筆、筆刷和文字的色彩，來處理點陣圖中的色彩。
ms.assetid: c315dd6e-87ee-4905-b193-186ea580ac0a
title: 點陣圖中的色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 834744f35ccc8bd0c8714fa5bbb438b59c8b8db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114701"
---
# <a name="color-in-bitmaps"></a>點陣圖中的色彩

系統會以不同于畫筆、筆刷和文字的色彩，來處理點陣圖中的色彩。 使用 [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) 或 [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) 函式所建立的相容點陣圖是裝置特定的，而且會以裝置相依的格式保留色彩資訊。 不會使用任何色彩值，而且色彩不會受限於近似值和遞色。

與裝置無關的點陣圖 (Dib) 將色彩資訊保留為色彩值或調色板索引。 如果使用色彩值，色彩會受限於近似值，但不能遞色。 色階索引只能與支援調色板的裝置搭配使用。 雖然系統不會計算索引所識別的近似或遞色色彩，但產生的色彩可能會與預期的色彩不同，因為索引只會在建立點陣圖時的最新色彩選擇器內容中產生有效的結果。 如果選擇區變更，則點陣圖中的色彩。 如需有關調色板索引的詳細資訊，請參閱預設的 [ [調色板](default-palette.md) ] 和 [ [**調色盤索引**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex)]。

除了參考邏輯調色板之外，應用程式也可以參考 DIB 色彩表中的值。 若要選取 DIB 色彩表中的色彩，請呼叫 [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex)。 請注意，這只適用于已選取 DIB 的裝置內容。

 

 




---
title: 判斷及變更目前的位置
description: 判斷及變更目前的位置
ms.assetid: 20f78dcd-3259-43c2-8da3-8cfc299252e6
keywords:
- MCIWndGetStart 宏
- MCIWndGetEnd 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a8e7022bdfcede526a730014a07deaf22fe66d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462285"
---
# <a name="determining-and-changing-the-current-position"></a>判斷及變更目前的位置

當檔案或裝置與 MCIWnd 視窗相關聯時，會一開始就在內容開頭設定播放位置，不論媒體類型為何。 在播放期間，播放位置會以線性方式在內容中移動，如果播放是不中斷的，最後會到達內容的結尾。 如果發生中斷，則目前的播放位置是停止或暫停播放的位置。

您可以使用 [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) 和 [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) 宏來取出內容開頭和結尾的位置。 您可以藉由從 **MCIWndGetEnd** 所傳回的值減去 **MCIWndGetStart** 傳回的值，或使用 [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)宏來判斷內容的長度。 您可以使用 [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) 宏來取出目前的播放位置，也可以使用 [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) 宏，以以 null 終止的字串形式取出播放位置。

若要變更目前的播放位置，請使用 [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome)、 [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)和 [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) 宏。 您可以使用 **MCIWndHome** 或使用 **MCIWndEnd**，將播放位置移至內容的開頭。 使用 **MCIWndSeek** 將播放位置移至內容中的任何位置。

您也可以使用 [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) 宏來逐步執行內容。 從目前的播放位置開始，此宏會以指定的增量向前或向後移動播放位置。

> [!Note]  
> 用來指定位置的單位會因不同的媒體類型和裝置而有所不同。 例如，MCIAVI 裝置所使用之 AVI 檔案的播放位置會以畫面格來測量;CD 音訊、波形音訊和 MIDI 檔案的播放位置會以毫秒為單位來測量。

 

其他媒體類型和協力廠商裝置的裝置可能會使用其他單位。 如需決定這些單位的詳細資訊，請參閱 [播放增強功能](playback-enhancements.md)。

 

 





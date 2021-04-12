---
title: 關於 MCIWnd 視窗類別
description: 關於 MCIWnd 視窗類別
ms.assetid: 7dde7346-5853-4c8f-8788-bf74d01ece83
keywords:
- MCIWnd 視窗類別，關於
- MCIWndCreate 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e459a0e7d93543af126287a776b64130595ad11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372233"
---
# <a name="about-the-mciwnd-window-class"></a>關於 MCIWnd 視窗類別

MCIWnd 視窗類別很容易使用。 藉由使用單一函式， [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 您的應用程式可以建立一個控制項，來播放任何使用 media control 介面 (MCI) 的裝置。 這些裝置包括 CD 音訊、波形音訊、MIDI 和影片裝置。

自動化播放也是快速又簡單的。 只要使用一個函式和兩個宏，應用程式就可以建立具有適當媒體裝置的 MCIWnd 視窗、播放裝置，並在內容完成播放時關閉裝置和視窗。

> [!Note]  
> 有些裝置會播放儲存在檔案中的內容。 其他裝置，例如 CD 音訊裝置，則會播放儲存在另一個媒體中的內容。 為了清楚起見，此總覽將這兩種情況都稱為「播放裝置」。

 

 

 





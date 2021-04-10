---
title: 啟動、暫停和繼續播放
description: 啟動、暫停和繼續播放
ms.assetid: 4af92781-5461-4195-82f5-a9213a9bdbd7
keywords:
- MCIWndPlay 宏
- MCIWndPause 宏
- MCIWndResume 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734a186b90b8d6701923d0ffa1f743cc8c5ae378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184133"
---
# <a name="starting-pausing-and-resuming-playback"></a>啟動、暫停和繼續播放

[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) 是最常見的播放宏。 此宏可讓您從目前的播放位置播放檔案或裝置。 除非已中斷，否則播放會繼續直到內容結束為止。

您可以使用 [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) 宏暫時中斷現正播放的裝置。 若要從暫停的位置繼續播放，請使用 [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) 宏。 有些裝置不支援暫停和繼續命令。 這些裝置通常會將 **MCIWndPause** 對應至 [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) 宏，以停止播放或錄製。 您可以使用 **MCIWndPlay** 重新開機不支援暫停或繼續的裝置，這會從目前的播放位置開始播放。

 

 





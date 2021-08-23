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
ms.openlocfilehash: 49977b9bc741c6b32ce0da0c0ae9f63bd875a24268a00bb4782cd71531a4ef31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688668"
---
# <a name="starting-pausing-and-resuming-playback"></a>啟動、暫停和繼續播放

[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) 是最常見的播放宏。 此宏可讓您從目前的播放位置播放檔案或裝置。 除非已中斷，否則播放會繼續直到內容結束為止。

您可以使用 [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) 宏暫時中斷現正播放的裝置。 若要從暫停的位置繼續播放，請使用 [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) 宏。 有些裝置不支援暫停和繼續命令。 這些裝置通常會將 **MCIWndPause** 對應至 [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) 宏，以停止播放或錄製。 您可以使用 **MCIWndPlay** 重新開機不支援暫停或繼續的裝置，這會從目前的播放位置開始播放。

 

 





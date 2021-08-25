---
title: 播放和定位
description: 播放和定位
ms.assetid: fbf9294e-c644-45c7-ab60-dd903409a44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9993c2ed4402184d2b15d5c3e54bb0137d1e7a3fe34f8cca36559ca329ada9d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892968"
---
# <a name="playback-and-positioning"></a>播放和定位

多個 MCI 命令，例如 [**play**](play.md) ([**mci \_ play**](mci-play.md)) 、 [**停止**](stop.md) ([**mci \_ 停止**](mci-stop.md)) 、 [**暫停**](pause.md) ([**mci \_ 暫停**](mci-pause.md)) 、 [**繼續**](resume.md) ([**mci 搜尋) \_**](mci-resume.md) ，以及 [**搜尋**](seek.md) (mci [**\_ 搜尋**](mci-seek.md)) ，以影響多媒體檔案的播放或定位。 如果 MCI 裝置在另一個播放命令正在進行時收到播放命令，它會接受命令，並停止或取代上一個命令。

許多 MCI 命令（例如 [**set**](set.md) ([**mci \_ set**](mci-set.md)) ）不會影響播放。 只要沒有從驅動程式的相同實例執行通知，來自其中一個命令的通知就不會干擾暫止的播放或定位命令。 例如，您可以在裝置執行 **搜尋** 命令而不停止或取代 **搜尋** 命令的情況下， ([**MCI \_ 狀態**](mci-status.md)) 命令發出 **設定** 或 [**狀態**](status.md)。

不過，只能有一個暫止的通知。 例如，如果應用程式要求 **播放** 通知，並遵循「開始位置通知」 **狀態** 的要求，則 **播放** 通知會傳回「已取代」，而「狀態」命令的通知會在完成時傳回。 不過，在此情況下，即使應用程式未收到通知， **播放** 命令仍會成功。

 

 





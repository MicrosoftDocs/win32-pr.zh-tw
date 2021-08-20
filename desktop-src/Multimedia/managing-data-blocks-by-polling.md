---
title: 藉由輪詢管理資料區塊
description: 藉由輪詢管理資料區塊
ms.assetid: 0a517f1d-4993-49b8-be86-bc63e5687cba
keywords:
- 波形音訊，輪詢資料區塊
- 音訊資料區塊，輪詢
- 輪詢音訊資料區塊
- WAVEHDR 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c84e75eccaf34ef16ccadefb4dae42931854a0c6c4278003fb5c01b0c551f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139163"
---
# <a name="managing-data-blocks-by-polling"></a>藉由輪詢管理資料區塊

除了使用回呼函式，您還可以輪詢 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的 **dwFlags** 成員，以判斷音訊裝置何時完成資料區塊。 有時候最好是輪詢 **dwFlags** ，而不是等待其他機制從驅動程式接收訊息。 例如，在您呼叫 [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) 函式釋放暫止的資料區塊之後，您可以立即進行輪詢，以確定在呼叫 [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) 並釋出資料區塊的記憶體之前，已釋放資料區塊。

您可以使用 [WHDR \_ 完成] 旗標來測試 **dwFlags** 成員。 一旦在 \_ **WAVEHDR** 結構的 **DWFLAGS** 成員中設定 WHDR 完成旗標，驅動程式就會使用資料區塊完成。

 

 
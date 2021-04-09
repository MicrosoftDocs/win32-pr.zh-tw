---
description: ReceiveConnection
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: ReceiveConnection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fd9fe31f87a34dc3bfdfc4ecfb532255138b9c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109281"
---
# <a name="receiveconnection"></a>ReceiveConnection

當新的格式需要較大的緩衝區時，此機制可讓輸出釘選將格式變更建議給其下游對等。 輸出圖釘會執行下列動作：

1.  在下游輸入 pin 上呼叫 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 。
2.  如果 `ReceiveConnection` 成功，則在輸入 pin 上呼叫 [**IMemInputPin：： NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) 。

此外，輸出 pin 可能需要呼叫 [**IMemAllocator：： SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) ，然後取消認可和重新認可配置器，以便變更緩衝區大小。 在變更緩衝區大小之前，請務必以舊格式傳遞所有暫止的範例。

有些 MPEG-2 的解碼器會使用這種機制，在 MPEG-2 和 MPEG-2 輸出之間切換，或在影片大小變更時切換。

 

 




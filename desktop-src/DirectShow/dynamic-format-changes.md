---
description: 動態格式變更
ms.assetid: ff60de5a-3edc-405d-aa02-8704b96d5e87
title: 動態格式變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49496e0b43d9b120f6daf27007cde98191a7765b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970502"
---
# <a name="dynamic-format-changes"></a>動態格式變更

當兩個篩選準則連線時，它們會同意媒體類型，以描述上游篩選器將傳遞的資料格式。 在大部分的情況下，媒體類型在連線期間都是固定的。 但是，DirectShow 確實提供篩選器的有限支援來變更媒體類型。 當篩選參數切換媒體類型時，它稱為 *動態格式變更*。 如果您正在撰寫 DirectShow 篩選器，您應該留意動態格式變更的機制。 即使您的篩選不支援這類變更，如果另一個篩選要求新的格式，則應該會正確地回應。

DirectShow 定義了數種不同的動態格式變更機制，視篩選圖形的狀態以及所需的變更類型而定。

-   如果圖形已停止，則 pin 可以重新連接並重新協商媒體類型。 如需詳細資訊，請參閱重新 [連接 pin](reconnecting-pins.md)。
-   某些篩選器可以重新連接釘選，即使圖形處於作用中狀態 (執行中或已暫停) 。 如需此機制的詳細資訊，請參閱 [動態重新連接](dynamic-reconnection.md)。

否則，如果圖形正在使用中，但有問題的篩選器不支援動態 pin 重新連接，則有三種可能的機制可以變更格式：

-   如果輸出圖釘建議將格式變更提供給其下游對等，但只有在新的格式不需要較大的緩衝區時，就會使用[QueryAccept (下游) ](queryaccept--downstream.md) 。
-   [QueryAccept (上游) ](queryaccept--upstream.md) 是在輸入 pin 提議對其上游對等的格式變更時使用。 新格式可以是相同大小，也可以較大。
-   當輸出釘選對其下游對等的格式變更時，會使用[ReceiveConnection](receiveconnection.md) ，而新的格式需要較大的緩衝區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[處理影片轉譯器的格式變更](handling-format-changes-from-the-video-renderer.md)
</dt> </dl>

 

 




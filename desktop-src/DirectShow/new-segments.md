---
description: 新區段
ms.assetid: 6c470b38-481f-4e52-93b8-eb6b343dcefc
title: 新區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28701a29a3b4edd61e9eb408aeab744297eac56408c49dc77dd4328a5afd24b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790928"
---
# <a name="new-segments"></a>新區段

*區段* 是一組共用一般開始時間、停止時間和播放速率的媒體範例。 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)方法會為新區段的開頭髮出信號。 它提供一種方法讓來源篩選準則通知下游篩選準則，指出時間和費率資訊已變更。 例如，如果來源篩選搜尋到資料流程中的新點，則會以新的開始時間來呼叫 **NewSegment** 。

某些下游篩選器會在處理範例時使用區段資訊。 例如，使用幀壓縮的格式，如果停止時間落在差異框架上，來源篩選可能需要在停止時間之後傳送額外的範例。 這可讓解碼器解碼最終的 delta frame。 為了判斷正確的最後框架，此解碼器會參考區段停止時間。 另一個範例是，音訊轉譯器會使用區段速率以及音訊取樣率，以產生正確的音訊輸出。

在推送模型中，來源篩選準則會起始 **NewSegment** 呼叫。 在提取模型中，這是由剖析器篩選所完成。 無論是哪一種情況，篩選準則都會呼叫下游輸入 pin 的 **NewSegment** ，這會將呼叫傳播至下一個篩選器，直到呼叫到達轉譯器為止。 篩選準則必須將 **NewSegment** 呼叫與其他串流呼叫序列化，例如 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)。

資料流程時間會在每個新區段之後重設為零。 區段從零開始之後所傳遞樣本的時間戳記。

 

 




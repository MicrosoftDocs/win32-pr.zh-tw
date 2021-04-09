---
description: 頻率資料表
ms.assetid: 58a680ea-1f88-4900-8820-c30a2f3e3901
title: 頻率資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933152c7ac38eefe91468aff8bc3a8eb3ced05df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108541"
---
# <a name="frequency-tables"></a>頻率資料表

電視調諧器篩選器 (kstvtune.ax) 具有頻率資料表的內部清單。 每個頻率資料表都包含頻率清單，並且對應至特定國家/地區的廣播或纜線頻率。 應用程式會藉由呼叫 [**IAMTuner：:p ui \_ 通道**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) 方法，並以所需的頻率索引來調整為特定的頻率。

在某些國家/地區中，頻率資料表的索引編號會直接對應至頻道號碼。 不過，固定的通道號碼並非適用于所有市場。 例如，取用者實際上不會使用歐洲頻道號碼。 相反地，消費者預期會選擇並為其區域中的廣播或纜線操作員所使用的頻率，指派自己的頻道號碼。 針對這些國家/地區，應用程式不應該直接向使用者公開索引編號。 Instread，應用程式應該將通道號碼之間的內部對應 (呈現給使用者) 和頻率索引 (以進行微調) 。

大部分的非美國纜線運算子都可自由地在其選擇的頻率上進行廣播，通常會將不同標準的頻率混合為相同的頻道組合。 因此，所有缺少標準纜線通道標準授權單位的國家/地區，都會使用 "Unicable" 頻率表。 此外，也會提供一種機制來覆寫頻率資料表中的個別頻率。 下一節的 [頻率覆寫](frequency-overrides.md)會說明這項機制。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[國際類比電視微調](international-analog-tv-tuning.md)
</dt> </dl>

 

 




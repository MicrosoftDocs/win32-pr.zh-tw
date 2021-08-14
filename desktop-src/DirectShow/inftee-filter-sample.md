---
description: InfTee 篩選範例
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: InfTee 篩選範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd0bbbb4df30f549a8ea0ba15d33696dcb7c108cbeffa6658bbb1842291517d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398016"
---
# <a name="inftee-filter-sample"></a>InfTee 篩選範例

## <a name="description"></a>Description

InfTee 篩選器提供 DirectShow[無限 Pin 指標](infinite-pin-tee-filter.md)篩選準則的範例執行。 篩選器具有一個輸入的 pin 和動態的輸出圖釘數目。 所有傳送至篩選器的媒體範例都會從所有輸出圖釘同時傳遞。

此篩選器會出現在 GraphEdit 的「範例無限 Pin 碼 t」名稱底下，以與 DirectShow 中提供的標準無限 Pin 指標篩選準則區別。

## <a name="usage"></a>使用方式

因為此篩選不會變更其所接收的資料，所以所有的 pin 都必須同意相同的媒體類型。 在連接過程中，篩選器可能會重新連接某些 pin，以使媒體類型相符。

到達輸入 pin 的資料在傳送至輸出圖釘之前，不會先複製。 篩選準則也可確保將資料傳遞至下游篩選器，以保證這兩個輸出都會收到及時的服務。 尤其是，如果其中一個輸出可以在 [**COutputQueue：： Receive**](coutputqueue-receive.md) 成員函式中封鎖，則 t 會將執行緒旋轉以傳遞範例。 如果沒有可傳遞範例的執行緒，則傳遞範例至 t 輸入 pin 的執行緒可能會將資料傳遞至下游篩選;屆時，它可能會封鎖，並保留其他下游篩選的資料很長一段時間。

## <a name="downloading-the-sample"></a>下載範例

若要下載 DirectShow SDK 範例，請安裝最新版本的[Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。

此範例安裝在下列路徑下： *\[ SDK \] 根* \\ 範例 \\ 多媒體 \\ DirectShow \\ 篩選 \\ InfTee。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow樣品](directshow-samples.md)
</dt> </dl>

 

 




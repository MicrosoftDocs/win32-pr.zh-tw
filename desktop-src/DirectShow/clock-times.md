---
description: 時鐘時間
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: 時鐘時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0639fd2b38e312f30f932fcf508427cd71c054
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385597"
---
# <a name="clock-times"></a>時鐘時間

DirectShow 定義了兩個相關的時鐘時間：參考時間和資料流程時間。

-   *參考時間* 是參考時鐘所傳回的絕對時間。  (參閱 [參考時鐘](reference-clocks.md). ) 
-   *資料流程時間* 的定義是相對於圖形上次開始執行的時間。
    -   當圖形正在執行時，資料流程時間等於參考時間減去開始時間。
    -   當圖形暫停時，資料流程時間會在資料流程時間保持暫停狀態。
    -   在搜尋作業之後，資料流程時間會重設為零。
    -   當圖形停止時，資料流程時間是未定義的。

當媒體範例有時間戳記 *t* 時，即表示範例應該在資料流程時間 *t* 轉譯。 基於這個理由，資料流程時間也稱為 *呈現時間*。

當應用程式呼叫 [**IMediaControl：： run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) 來執行篩選圖形時，篩選圖形管理員會在每個篩選器上呼叫 [**IMediaFilter：： run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) 。 為了補償篩選器開始執行所需的時間，篩選圖形管理員會指定未來的開始時間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)
</dt> <dt>

[時間戳記](time-stamps.md)
</dt> </dl>

 

 




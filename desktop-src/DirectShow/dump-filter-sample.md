---
description: 傾印篩選範例
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: 傾印篩選範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd64d1f16b0b504743890543b617a24df6bbaab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510265"
---
# <a name="dump-filter-sample"></a>傾印篩選範例

## <a name="description"></a>Description

傾印篩選器是轉譯器篩選器，可將其接收的媒體範例寫入文字檔。

此範例說明如何使用基底篩選類別 [**CBaseFilter**](cbasefilter.md) 和轉譯的輸入針腳類別 [**CRenderedInputPin**](crenderedinputpin.md)。 它也會示範如何執行 [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) 介面。 傾印篩選器具有單一輸入 pin，會將它直接接收的每個範例寫入檔案。

## <a name="usage"></a>使用方式

此篩選是實用的偵錯工具。 例如，您可以驗證轉換篩選的結果（以位為單位）。 您可以使用 GraphEdit 來手動建立圖形，並將傾印篩選連接到轉換篩選器或任何其他輸出的輸出。 您也可以連接到 t-sql 篩選器，並將傾印篩選放在 t-sql 篩選器的一個階段，並將一般輸出放在另一個階段，以在即時案例中監視結果。

## <a name="downloading-the-sample"></a>下載範例

若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。

此範例安裝在下列路徑下： *\[ SDK 根 \]* \\ 範例 \\ 多媒體 \\ DirectShow \\ 篩選 \\ 傾印。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 範例](directshow-samples.md)
</dt> </dl>

 

 




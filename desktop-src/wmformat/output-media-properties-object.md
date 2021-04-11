---
title: 輸出媒體屬性物件
description: 輸出媒體屬性物件
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- Windows Media Format SDK，輸出媒體屬性物件
- Advanced Systems Format (ASF) 、output media properties 物件
- ASF (Advanced Systems Format) 、output media properties 物件
- 物件、輸出媒體屬性物件
- 輸出媒體屬性物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61490464381a0b4e58be7994dfaeb0dfec2baa76
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104023172"
---
# <a name="output-media-properties-object"></a>輸出媒體屬性物件

輸出媒體屬性物件是用來取出和設定 output 屬性。 輸出媒體屬性物件是針對載入至讀取器物件的檔案中所支援的資料流程輸出格式所建立。 針對壓縮的資料流程，輸出屬性取決於解壓縮編解碼器的可能輸出。

輸出媒體屬性物件是由 [**IWMReader：： GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) 建立的，此方法會建立輸出媒體屬性物件，其中包含預設輸出格式的屬性。 輸出可能支援其他格式。 若要取得其他輸出格式，您可以呼叫 [**IWMReader：： GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) 來取得支援的輸出格式數目，然後使用 [**IWMReader：： GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat)的呼叫對它們執行迴圈。 **GetOutputFormat** 會建立輸出媒體屬性物件，其中填入所選輸出格式的資料。

輸出媒體屬性物件也可以使用同步讀取器來建立。 所有方法名稱與讀取器中的名稱相同，而且全部都是由 [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) 介面所公開。

**GetOutputProps** 和 **GetOutputFormat** 都會將指標設定為 [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) 介面。 您可以藉由呼叫 **QueryInterface** 方法來取得輸出媒體屬性物件的其他介面。

每個輸出媒體屬性物件都支援下列介面。



| 介面                                          | 描述                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | 用作其他媒體屬性介面的基底介面， (輸入、輸出和影片) 。             |
| [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | 捕獲輸出的屬性。                                                                     |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | 管理影片資料流程的屬性。 這是選擇性的介面，僅適用于影片串流。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件**](objects.md)
</dt> <dt>

[**讀取器物件**](reader-object.md)
</dt> </dl>

 

 





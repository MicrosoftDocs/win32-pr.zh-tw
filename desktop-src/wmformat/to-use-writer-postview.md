---
title: 使用寫入器 Postview
description: 使用寫入器 Postview
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Advanced Systems Format (ASF) 、writer postview
- ASF (Advanced Systems Format) 、writer postview
- Advanced Systems Format (ASF) ，postviewing
- ASF (Advanced Systems Format) ，postviewing
- 寫入器 postview
- postviewing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb3c1c83ebd38ff04c2022e529693d3d43b8b35
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104507836"
---
# <a name="to-use-writer-postview"></a>使用寫入器 Postview

寫入器物件提供 postviewing 功能，讓您可以驗證撰寫的內容，而不需要設定 reader 物件。 寫入器物件不支援音訊內容的 postviewing。

寫入器 postviewer 的運作方式與非同步讀取器物件的方式大致相同，只是使用較少的功能。 如需有關讀取數位媒體的詳細資訊，請參閱 [讀取 ASF](reading-asf-files.md)檔。

若要執行 postviewer，請執行下列步驟。

1.  執行 [**IWMWriterPostViewCallback：： OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) 回呼。 這個方法基本上與 [**IWMReaderCallback：： OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) 相同，不同之處在于它會指定資料流程號碼，而不是輸出。
2.  設定為正常寫入。
3.  藉由呼叫 **IWMWriter：： QueryInterface**，取得寫入器物件之 [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview)介面的指標。
4.  藉由呼叫 [**IWMWriterPostView：： SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback)，設定要使用之 postviewer 的回呼。
5.  針對您想要接收 postview 範例的每個資料流程，呼叫 [**IWMWriterPostView：： SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples)。 您可以藉由呼叫 [**IWMWriterPostView：： GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples)，查看資料流程是否已設定為接收 postview 範例。
6.  您可以操作範例格式，就像是讀取器物件或同步讀取器物件中的輸出格式一樣。
7.  當您開始寫入檔案時，您將開始在 **OnPostViewSample** 回呼方法的執行中收到範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMWriterPostViewCallback 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 





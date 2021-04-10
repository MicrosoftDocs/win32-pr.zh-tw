---
title: 使用同步讀取器取出壓縮的範例
description: 使用同步讀取器取出壓縮的範例
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- Advanced Systems Format (ASF) ，正在抓取壓縮的範例
- ASF (Advanced 系統格式) ，正在抓取壓縮的範例
- Advanced Systems Format (ASF) 、同步讀取器
- ASF (Advanced Systems Format) ，同步讀取器
- Advanced Systems Format (ASF) 、壓縮的範例
- ASF (Advanced Systems Format) ，壓縮的範例
- 同步讀取器，正在抓取壓縮的範例
- 同步讀取器，壓縮的範例
- 壓縮的範例，正在抓取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f0051fc14a14500b2c6e69c5e32f7ec0c39a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104092540"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a>使用同步讀取器取出壓縮的範例

如同非同步讀取器，同步讀取器也可以取出壓縮的範例。 將資料流程從某個檔案複製到另一個檔案時，應使用壓縮的範例。

Windows Media Format SDK 不提供任何方法，可在資料從 ASF 檔案解壓縮之後進行解碼。 如果您收到壓縮的範例，之後想要將它們解壓縮，您必須提供自己的程式碼來進行。 解決這項限制的其中一種方法是將壓縮的範例寫入至新的 ASF 檔案，然後將它們重新讀取為一般、未壓縮的範例。

若要使用同步讀取器接收壓縮的範例，請在播放之前或期間呼叫 [**IWMSyncReader：： SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) 。 針對 *fCompressed* 傳遞 true。

> [!Note]  
> 影像串流對壓縮的資料流程傳遞而言無效。 如果您將影像串流從某個檔案複製到另一個檔案，它就無法在新的檔案中使用。 若要從檔案複製影像串流至檔案，請依輸出號碼抓取影像串流範例，並將它們包含在新的檔案中，如同包含新的影像串流一樣。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用同步讀取器讀取檔案**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 





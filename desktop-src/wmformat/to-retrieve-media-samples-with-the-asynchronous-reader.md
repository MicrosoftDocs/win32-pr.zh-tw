---
title: 使用非同步讀取器取出媒體範例
description: 使用非同步讀取器取出媒體範例
ms.assetid: 0d8c3099-f068-4074-b717-2f5b9ed9eeb8
keywords:
- Advanced Systems Format (ASF) ，正在抓取媒體範例
- ASF (Advanced 系統格式) ，正在抓取媒體範例
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- 非同步讀取器，正在抓取媒體範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0419619ea99bd3734db67f8e658b1f3ff058a3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023027"
---
# <a name="to-retrieve-media-samples-with-the-asynchronous-reader"></a>使用非同步讀取器取出媒體範例

當您 \_ 在 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)的執行中收到 WMT 開啟狀態訊息之後，您可以藉由呼叫 [**IWMReader：： Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start)來開始接收範例。 非同步讀取器會將範例提供給 [**IWMReaderCallback：： OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample)的實作為。 範例會以展示時間順序傳遞。

**Start** 是非同步呼叫。 它幾乎會立即傳回，而且會繼續在不同的執行緒上執行。 非同步讀取器在解碼內容和傳遞範例時，會使用多個執行緒。 到達檔案結尾時，讀取器會將 WMT \_ EOF 狀態訊息傳送至您的 **OnStatus** 回呼的執行。 當 \_ 傳送 WMT EOF 時，讀取器會停止它自己的處理; 您不需要透過 \_ 呼叫 [**IWMReader：： STOP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop)來回應 WMT EOF。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**在 OnStatus 回呼中執行讀取器訊息**](to-implement-reader-messages-in-the-onstatus-callback.md)
</dt> <dt>

[**若要執行 OnSample 回呼**](to-implement-the-onsample-callback.md)
</dt> </dl>

 

 





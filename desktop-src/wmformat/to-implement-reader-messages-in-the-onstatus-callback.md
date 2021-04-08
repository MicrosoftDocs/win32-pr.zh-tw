---
title: 在 OnStatus 回呼中執行讀取器訊息
description: 在 OnStatus 回呼中執行讀取器訊息
ms.assetid: f0535e02-a283-48bf-9242-ebcc17a6fb66
keywords:
- Advanced Systems Format (ASF) ，執行讀取器訊息
- ASF (Advanced Systems Format) ，執行讀取器訊息
- Advanced Systems Format (ASF) 、OnStatus 回呼
- ASF (Advanced Systems Format) 、OnStatus 回呼
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- 非同步讀取器，執行讀取器訊息
- OnStatus 回呼方法，執行讀取器訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384cf8df8628efa9bd2cc17920dc6b1303655691
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023030"
---
# <a name="to-implement-reader-messages-in-the-onstatus-callback"></a>在 OnStatus 回呼中執行讀取器訊息

若要使用非同步讀取器從 ASF 檔案傳遞內容，您必須至少執行兩個回呼方法： [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 和 [**IWMReaderCallback：： OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample)。 本節說明如何執行 **IWMStatusCallback：： OnStatus** ，以接收和回應讀取器所傳送的狀態訊息。 Windows Media 格式 SDK 中的其他物件會使用 **OnStatus** 。 如需 **OnStatus** 的一般資訊，請參閱 [使用 OnStatus 回呼](using-the-onstatus-callback.md)。

使用非同步讀取器時，您必須在 **IWMStatusCallback：： OnStatus** 中將下列訊息設為陷阱。



| 狀態訊息 | Description                                     |
|----------------|-------------------------------------------------|
| WMT \_ 開啟    | 檔案開啟作業完成時傳送。 |
| WMT \_ 已關閉    | 在檔案關閉作業完成時傳送。 |



 

您應該使用上列的狀態訊息來控制讀取應用程式的執行。 例如，您必須等到收到 **WMT \_ 開啟** 的訊息，才能啟動讀取器，或呼叫需要讀取器備妥檔案的其他方法。 通常，使用非同步讀取器建立的應用程式會使用事件來表示非同步呼叫完成，並繼續處理。 如需使用事件來通知作業完成的詳細資訊，請參閱 [使用事件與非同步呼叫](using-events-with-asynchronous-calls.md)。

讀取器物件會將許多其他訊息傳送至 **OnStatus** ，讓應用程式能夠回應讀取作業的狀態。 可能的狀態訊息值是在 [**WMT \_ 狀態**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) 列舉類型中定義。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)
</dt> <dt>

[**使用非同步讀取器讀取檔案**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**使用 OnStatus 回呼**](using-the-onstatus-callback.md)
</dt> </dl>

 

 





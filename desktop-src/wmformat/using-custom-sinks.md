---
title: 使用自訂接收器
description: 使用自訂接收器
ms.assetid: 7151583a-c7ab-40b0-a7bf-ddd56f93b7aa
keywords:
- Advanced Systems Format (ASF) 、自訂接收器
- ASF (Advanced Systems Format) ，自訂接收器
- Advanced Systems Format (ASF) 、接收
- ASF (Advanced 系統格式) 、接收
- 接收器，自訂接收器
- 自訂接收，關於
- 寫入器接收、自訂接收器
- 自訂接收，IWMWriterSink 介面
- IWMWriterSink
- 寫入器接收、IWMWriterSink 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e324d654fa8c85d6145b0f4bf8f20de1f06e125f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681404"
---
# <a name="using-custom-sinks"></a>使用自訂接收器

如果您有特殊的撰寫需求，可以建立自己的寫入器接收器。 寫入器會藉由呼叫 [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)的方法，來與接收保持單向通訊。 若要建立您自己的接收，請在應用程式的類別中執行 **IWMWriterSink** 介面。 此程式非常類似于執行 Windows Media 格式 SDK 的物件所使用的任何其他回呼介面。 如需回呼的詳細資訊，請參閱 [使用回呼方法](using-the-callback-methods.md)。

[**IWMWriterSink：： OnHeader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader)中收到的緩衝區應寫入至檔案的開頭，而在 [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit)中接收的所有緩衝區都應依序寫出。 **OnHeader** 會在一開始就呼叫，但可能也會在其他時間呼叫，如果可能的話，您應該覆寫原始的標頭。 如果您的應用程式因某些原因而無法這麼做，請直接忽略後續的 **OnHeader** 呼叫。

您的自訂接收應該呼叫 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 回呼方法，以將其狀態傳達給您的寫入應用程式。 如果您將接收器實作為 COM 物件，您可能會想要公開 [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) 介面。 不過，您可以將 **OnStatus** 回呼的位址傳遞至接收器，並以任何您喜歡的方式設定內容。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用寫入器接收器**](working-with-writer-sinks.md)
</dt> </dl>

 

 





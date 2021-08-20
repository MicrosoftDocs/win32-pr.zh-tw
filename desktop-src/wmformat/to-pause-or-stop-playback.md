---
title: 暫停或停止播放
description: 暫停或停止播放
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- Advanced Systems Format (ASF) ，暫停播放
- ASF (Advanced Systems Format) ，暫停播放
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- Advanced Systems Format (ASF) ，停止播放
- ASF (Advanced 系統格式) ，停止播放
- Advanced Systems Format (ASF) 、播放暫停或停止
- ASF (Advanced 系統格式) 、播放暫停或停止
- 非同步讀取器，暫停播放
- 非同步讀取器，停止播放
- 非同步讀取器，播放暫停或停止
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7ae7f3c1dd2c045a35b8d3ee8950ace849a032136371f9da7ff1bcc2b12de27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845363"
---
# <a name="to-pause-or-stop-playback"></a>暫停或停止播放

當您呼叫 [**IWMReader：： Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) 來開始播放檔案時，非同步讀取器將會在其本身的個別執行緒中繼續處理，直到到達檔案結尾為止。 您可以使用 [**IWMReader：:P ause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) 或 [**IWMReader：： stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) 方法，分別暫停或停止傳遞範例。

## <a name="pausing"></a>正在暫停

當您呼叫 **IWMReader：:P ause** 來暫停檔案的播放時，讀取器會持續追蹤檔案中的目前位置。 若要在暫停之後繼續播放，請呼叫 [**IWMReader：： resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume)。 播放將從暫停的點繼續。

## <a name="stopping"></a>停止中

當您呼叫 **IWMReader：： Stop** 以停止播放檔案時，讀取器不會追蹤播放進度的任何相關資訊。 若要使用 **Stop** 和更新版本返回停止點，您必須儲存最後一個範例所提供的呈現時間，並將它用於您對 **IWMReader：： Start** 的呼叫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**使用非同步讀取器讀取檔案**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 





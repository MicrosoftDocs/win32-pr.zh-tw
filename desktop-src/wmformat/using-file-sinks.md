---
title: 使用檔案接收
description: 使用檔案接收
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- Advanced Systems Format (ASF) ，file 接收
- ASF (Advanced Systems Format) ，file 接收
- Advanced Systems Format (ASF) 、接收
- ASF (Advanced 系統格式) 、接收
- 接收，檔案接收
- 檔接收，關於
- 檔案接收，建立
- 檔案接收，停止
- 檔案接收，開始
- 檔案接收，關閉
- 接收、統計資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7a7f09a08788128719ea80a2a06d339f6398e6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104092583"
---
# <a name="using-file-sinks"></a>使用檔案接收

在一般情況下，您可以使用 [**IWMWriter：： SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) 方法，直接傳遞寫入器的輸出檔名稱，而寫入器物件會自動將檔案寫入磁片。 在此情況下，寫入器實際上是建立和控制寫入器檔案接收物件，該物件會處理將檔案寫入磁片的程式。 寫入器檔案接收物件可控制從寫入器物件到單一檔案的資料流程。

您可以建立自己的檔案接收，以更充分掌控接收器寫入檔案的方式。 您也可以存取寫入器所建立的預設寫入器檔案接收，以回應 **SetOutputFilename** 的呼叫。

## <a name="creating-file-sinks"></a>建立檔案接收

若要建立檔案接收並將它新增至寫入器，請執行下列步驟。

1.  藉由呼叫 [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) 函數來建立新的接收。
2.  藉由呼叫 [**IWMWriterFileSink：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open)，提供接收的檔案名。
3.  藉由呼叫 [**IWMWriterAdvanced：： AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink)，將 file 接收新增至寫入器。
4.  以一般方式執行撰寫。
5.  寫入完成後，接收會自動關閉檔案。

## <a name="stopping-and-starting-file-sinks"></a>停止和開機檔案接收

開始寫入作業之後，您可以藉由呼叫 [**IWMWriterFileSink2：： stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop)來停止寫入至檔案接收。

您可能會想要停止寫入接收的原因很多。 例如，如果您是從即時來源進行錄製，您可能只對部分內容感興趣。

您可以藉由呼叫 [**IWMWriterFileSink2：： Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start)來繼續寫入至檔案接收。 [ **停止** 並 **開始** ] 會使用呈現時間來控制大約執行命令的時間。 您可以使用 [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) 方法來更充分掌控開始和停止時間。

## <a name="closing-file-sinks"></a>關閉檔接收

一般情況下，檔案接收會自動關閉。 如果您已完成寫入至接收，但是將作業寫入其他接收，則應該明確地關閉接收以節省資源。 若要關閉 file 接收器，請呼叫 [**IWMWriterFileSink2：： close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close)。

## <a name="getting-sink-statistics"></a>取得接收統計資料

您可以分別呼叫 [**IWMWriterFileSink2：： GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) 和 [**IWMWriterFileSink2：： GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) ，來取得開啟接收器的檔案大小和持續時間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMWriterFileSink 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[**IWMWriterFileSink2 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[**IWMWriterFileSink3 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[**寫入器檔案接收物件**](writer-file-sink-object.md)
</dt> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 





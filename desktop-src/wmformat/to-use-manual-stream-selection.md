---
title: 使用手動資料流程選取
description: 使用手動資料流程選取
ms.assetid: 49ec283f-670a-4a0e-9477-c60a80919a1e
keywords:
- Advanced Systems Format (ASF) 、手動資料流程選取
- ASF (Advanced Systems Format) ，手動資料流程選取
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- Advanced Systems Format (ASF) ，資料流程選取範圍
- ASF (Advanced 系統格式) ，資料流程選取範圍
- Advanced Systems Format (ASF) ，相互排除
- ASF (Advanced Systems Format) ，相互排除
- 非同步讀取器，手動資料流程選取
- 非同步讀取器，資料流程選取
- 資料流程，手動選取
- 相互排除，手動資料流程選取
- 資料流程，非同步讀取器
- 相互排除，非同步讀取器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d73f7829736bc36f2362fde0bc86b5c88daf88a6b9e7ef22fb5d6c46ce7ee55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653883"
---
# <a name="to-use-manual-stream-selection"></a>使用手動資料流程選取

使用 reader 物件傳遞未壓縮的範例時，您只能透過輸出編號傳遞這些範例。 在互斥資料流程的情況下，這表示您只可以從一次互斥的資料流程接收樣本。 選擇要傳遞之互斥資料流程的處理方式，稱為資料流程選取。

針對位元速率互斥，讀取器會根據播放時主機電腦上的條件自動選取資料流程。 對於其他類型的互斥，除非您自行手動選取不同的資料流程，否則讀取器將會從預設資料流程傳遞範例。 當您想要從位元速率互斥中手動選取資料流程時，也可能會有實例。

針對整個檔案，手動選取的資料流程為開啟或關閉。 如果檔案包含位元速率互斥，以及一些其他互斥類型，您必須手動選取以位速率為基礎的資料流程。

若要以手動方式選取互斥的資料流程，您必須執行下列步驟。

1.  藉由呼叫 **IWMReader：： QueryInterface**，取得讀取器物件之 [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)介面的指標。
2.  藉由呼叫 [**IWMReaderAdvanced：： SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection)來啟用手動資料流程選取。
3.  若要找出特定的資料流程是否已選取，請呼叫 [**IWMReaderAdvanced：： GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected)。 您必須將指標傳遞至 [**WMT \_ 資料流程 \_ 選取**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) 列舉型別的變數。 當呼叫傳回時，變數中的值將會描述資料流程目前的選取類型。
4.  若要選取資料流程，請呼叫 [**IWMReaderAdvanced：： SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected)。 這個方法可讓您同時為同步處理的資料流程切換指定多個資料流程。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用非同步讀取器讀取檔案**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 





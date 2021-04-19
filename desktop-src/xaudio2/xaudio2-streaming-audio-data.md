---
description: 串流處理是指只在記憶體中維護一小部分的播放音訊檔案。 如此一來，就可以播放大型音訊檔案（例如背景音樂），而不會佔用大量的記憶體。
ms.assetid: 7a938ea6-15ef-66b1-0276-88eabf9a722b
title: XAudio2 串流音訊資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1766b20f539f8bbe4d11204b681b7eddca58578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975478"
---
# <a name="xaudio2-streaming-audio-data"></a>XAudio2 串流音訊資料

串流處理是指只在記憶體中維護一小部分的播放音訊檔案。 如此一來，就可以播放大型音訊檔案（例如背景音樂），而不會佔用大量的記憶體。

串流處理音訊檔案時，會以區塊的方式從磁片讀取其資料，而不是一次載入整個檔案。 串流處理是透過將音訊資料非同步地讀入磁碟緩衝區佇列來完成。 每個緩衝區都會填滿，然後提交至來源語音。 當語音完成播放緩衝區之後，緩衝區就會變成可供再次讀取。 以這種方式逐一查看磁碟緩衝區，可在只載入部分資料的時候播放大型音訊檔案。 串流程式碼應該放在個別的執行緒中，在等待長時間執行的磁片和音訊作業完成時，它可以進入睡眠狀態。 回呼類別是用來在音訊作業完成時觸發事件，藉此喚醒執行緒。

如需如何使用 XAudio2 來完成串流處理的範例，請參閱 [如何：從磁片串流音效](how-to--stream-a-sound-from-disk.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[串流音訊資料](streaming-audio-data.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> </dl>

 

 




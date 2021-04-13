---
title: 撰寫範例
description: 撰寫範例
ms.assetid: 9ce10a77-9e80-45e0-a7e7-2ffdf8b57773
keywords:
- Advanced Systems Format (ASF) 、撰寫範例
- ASF (Advanced Systems Format) ，撰寫範例
- Advanced Systems Format (ASF) ，將範例傳遞給寫入器
- ASF (Advanced Systems Format) ，將範例傳遞給寫入器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738014b3c42441e878105d12a8ebf23ce4b266f7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374426"
---
# <a name="to-write-samples"></a>撰寫範例

當您識別並設定所撰寫之檔案的輸入時，可以開始將範例傳遞給寫入器。 您應盡可能以表示階段的順序傳遞範例，以使撰寫程式更有效率。

在傳遞任何範例之前，您必須藉由呼叫 [**IWMWriter：： BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)，將寫入器設定為接受這些範例。

若要將範例傳遞給寫入器，請執行下列步驟：

1.  藉由呼叫 [**IWMWriter：： AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample)，配置緩衝區並取出 [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)介面的指標。
2.  藉由呼叫 [**INSSBuffer：： GetBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer)，取出在步驟1中建立的緩衝區位址。
3.  將範例資料複製到緩衝區位置，確定傳遞的範例符合配置的緩衝區。 您可以使用任何記憶體複製函數來複製您的資料。 常見的選擇是 memcpy，它包含在 standard C 執行時間程式庫中。
4.  藉由呼叫 [**INSSBuffer：： SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength)來更新緩衝區中使用的資料量，以反映樣本的實際大小。
5.  使用 [**IWMWriter：： WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) 方法，將緩衝區介面傳遞至寫入器以及輸入編號和取樣時間。 輸入的所有音訊範例都代表相同的內容持續時間，因此您可以藉由將範例持續時間新增至執行總計來找出範例時間。 針對影片，您需要根據畫面播放速率來計算時間。

**WriteSample** 會以非同步方式運作，而且在您的應用程式準備好再次呼叫方法之前，可能不會完成從緩衝區寫入資料的作業。 因此，請務必針對 **WriteSample** 的每個呼叫呼叫 **AllocateSample** 一次。 不過，您可以在呼叫 **WriteSample** 之後立即釋放 **INSSBuffer** 介面。

當您完成傳遞範例時，請呼叫 [**IWMWriter：： EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting)。

**注意** 很重要的是，檔案中所有資料流程的範例都必須在同步處理之間傳遞給寫入器。 也就是說，您應該盡可能在 [**IWMWriterAdvanced：： SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance)指定的同步容錯內，將範例以展示時間順序傳遞給寫入器。 當資料以一秒或更少的單位傳遞至每個資料流程時，就可以達到最佳效果。

資料流程也應該在大約相同的時間結束。 例如，您不應該使用長度為45秒的音訊串流，以及長度為50秒的影片串流來寫入檔案。 如果您使用未改變的輸入將這類檔案編碼，則會卸載資料流程結尾的某些音訊資料 (即使它是較短的資料流程) 也是一樣。 若要讓檔案編碼正常運作，您應該將5秒的靜音新增至音訊輸入，讓一個資料流程不會在另一個串流之前結束數秒鐘。 具有間歇樣本（例如文字或影像資料流程）的資料流程類型不需要以這種方式填補。 指令碼命令資料流程也應遵循所有這些規則。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**INSSBuffer 介面**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**IWMWriter 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 





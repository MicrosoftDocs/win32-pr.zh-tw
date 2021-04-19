---
description: 使用編輯決策清單進行編碼語音
ms.assetid: a3d88483-acc9-47cf-8735-f17bd3b4ad57
title: 使用編輯決策清單進行編碼語音
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970cc40bc5749b9edc1017546020fa3806a9730b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975022"
---
# <a name="using-an-editing-decision-list-for-encoding-voice"></a>使用編輯決策清單進行編碼語音

 (EDL) 的編輯決策清單是提供給編解碼器的資料，提供有關內容特定部分之編碼方式的資訊。 Windows Media 音訊9語音編解碼器支援簡單的 EDL，您可以在其中指定包含音樂的內容部分。 根據預設，編解碼器會在設定成編碼混合的內容時，偵測到音樂本身的段落。 只有當編解碼器未正確偵測內容類型時，才應該使用 EDL。

若要使用 EDL，必須將語音編碼器設定為編碼混合的內容。 將 [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) 屬性設定為2，以將語音編解碼器的模式設定為「混合」。 使用 [MFPKEY \_ WMAVOICE \_ ENC \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) 屬性來設定 EDL。 這個屬性的值是一個字串，其中包含以逗號分隔的清單，其中包含應編碼為音樂的內容中的時間範圍。 清單中的第一個專案是 EDL 的版本，一律為1。 第二個專案是清單中所述的音樂區段數目。 之後，第二個專案是等於第二個專案的幾個值配對;每一對值會描述音樂在內容中的開始和結束點（以毫秒為單位）。

例如，EDL 字串 "1，4，1000，2000，5000，6000，9000，10000，13000，14000" 指定四個樂譜段，每個都是一秒。 如果 EDL 字串中的資訊無效，則會予以忽略。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Windows Media 音訊9語音編解碼器](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[使用音訊](workingwithaudio.md)
</dt> </dl>

 

 




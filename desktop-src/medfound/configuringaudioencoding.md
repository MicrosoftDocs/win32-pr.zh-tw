---
description: 設定音訊編碼
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: '設定音訊編碼 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2344808decffd4b50d5926074dbf71d60445580adb4556703367369e1e146d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880363"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a>設定音訊編碼 (Microsoft 媒體基礎) 

Windows Media 音訊編碼器會以其完整格式列舉所有支援的輸出類型。 藉由呼叫 **IMediaObject：： GetOutputType** 或 **IMFTransform：： GetAvailableOutputType** 來取出您想要的類型，然後藉由呼叫 **IMediaObject：： SetOutputType** 或 **IMFTransform：： SetOutputType**，將未改變的取出型別設定為輸出類型。

音訊編碼器變更支援的輸出媒體類型已設定為編碼器屬性。 您必須在列舉輸出類型之前，設定您想要使用的所有編碼器屬性。

音訊編碼器支援雙通路和 VBR 模式，但其設定方式不同于影片。 如需詳細資訊，請參閱 [列舉特定編碼模式的音訊類型](enumeratingaudiotypesforspecificencodingmodes.md)。

除非您設定輸出類型，否則無法使用音訊編碼器所支援的輸入類型。 如果您在設定輸出型別之前呼叫 **IMediaObject：： GetInputType** 或 **IMFTransform：： GetInputType** ，此方法會傳回 DMO 不會再有其他 \_ \_ \_ \_ 專案或 MFT \_ e 的 \_ \_ 其他 \_ 類型。 設定輸出類型之後，編碼器會列舉針對所選取輸出類型所支援的輸入類型。

Windows Media 音訊編碼器不會執行任何音訊重新取樣。 這表示編碼器輸出類型和編碼器輸入類型必須有相同數目的通道、每個樣本的位數，以及取樣率。 如需詳細資訊，請參閱 [尋找音訊編碼器輸出類型](findingaudioencoderoutputtypes.md)。

> [!Note]  
>    音訊編碼器所列舉的每個輸出類型都包含 **WAVEFORMATEX** 結構， (由 **AM \_ 媒體 \_ 類型指向。 pbFormat**) 並附加擴充的資料。 擴充資料的大小是由 **WAVEFORMATEX. cbSize** 所指定。 這種資料必須與編碼的內容一起保存，才能傳遞給解碼器。 如果沒有延伸格式資料，就無法解壓縮內容。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用音訊](workingwithaudio.md)
</dt> </dl>

 

 




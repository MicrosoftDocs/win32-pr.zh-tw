---
description: 設定音訊解碼
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: '設定音訊解碼 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee274fd714065a1c89c9d634dd80de4d59c9eb567d67ed8045d2b89bece87d74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664640"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a>設定音訊解碼 (Microsoft 媒體基礎) 

解碼 Windows Media 音訊內容比編碼更容易。 建立音訊解碼物件之後，請使用 **IMediaObject：： SetInputType** 或 **IMFTransform：： SetInputType** 方法設定輸入類型。 您用於解碼器輸入的媒體類型，必須符合編碼內容時所使用的輸出類型。 這包括附加至 **WAVEFORMATEX** 結構的延伸格式資料。 您必須確保這項資料正確無誤，因為解碼器無法處理沒有它的範例。

設定輸入類型之後，您可以設定您想要使用的任何解碼功能。 使用 **IPropertyBag** 或 **IPropertyStore** 的方法，可以設定像用於編碼的編碼器功能。

設定輸入型別並設定所有的解碼器功能之後，您可以呼叫 **IMediaObject：： GetOutputType** 或 **IMFTransform：： GetOutputType**，以列舉此解碼器所支援的輸出類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用音訊](workingwithaudio.md)
</dt> </dl>

 

 




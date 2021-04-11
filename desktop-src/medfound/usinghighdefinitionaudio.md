---
description: 使用 High-Definition 音訊
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: '使用 High-Definition 音訊 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05e7bd9311574c3d25f9069ea60c9d269d24390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692296"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a>使用 High-Definition 音訊 (Microsoft 媒體基礎) 

高定義音訊在 Windows Media 音訊編解碼器的內容中，是具有兩個以上頻道或每個樣本超過16個位的任何音訊類型。 [Windows Media 音訊編碼器](windowsmediaaudioencoder.md)的 Professional 和無損類別支援高定義音訊。

未壓縮的高定義音訊類型會使用 [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) 結構來定義。 **WAVEFORMATEXTENSIBLE** 是 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構的結構化延伸。 當您使用 DMOs 時， **formattype** 成員（描述高 [**定義 \_ \_ 音訊類型）**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) 必須設定為 WMCFORMAT \_ WaveFormatEx，就如同一般音訊一樣， **WAVEFORMATEXTENSIBLE** 沒有特殊的格式識別碼。 如果格式使用 **WAVEFORMATEXTENSIBLE** ，您必須將 **WAVEFORMATEX** 結構的 **cbSize** 成員設定為22。

使用媒體基礎時，您可以使用函數 [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex)，從 [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))結構建立正確的媒體類型。

Windows Media 音訊10專業版編解碼器所支援的多通道輸出類型不會使用 [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))，但會在 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構中報告每個樣本的正確通道數目和位數。 如同所有會描述壓縮 Windows Media 音訊內容的音訊類型，額外的資訊會附加至 **WAVEFORMATEX** 結構，以供解碼器用於解壓縮。

## <a name="decoding-high-definition-audio"></a>解碼 High-Definition 音訊

若要解碼高定義音訊，您必須將 [MFPKEY \_ WMADEC \_ HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) 屬性設定為 VARIANT \_ TRUE。 如果未設定此屬性，則不論壓縮格式為何，此解碼器都會傳遞最多每個樣本16位的身歷聲內容。

> [!Note]  
> 只有 Windows XP、Windows Vista 及更新版本才支援高定義音訊。 在舊版的 Windows 上，使用 high 定義編碼的 Windows Media 音訊內容會轉譯為雙聲道音訊，每個樣本最多16個位。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用音訊](workingwithaudio.md)
</dt> </dl>

 

 

---
description: 列舉特定編碼模式的音訊類型
ms.assetid: d44960eb-da5e-4379-ba9d-cb804559dc53
title: '列舉特定編碼模式的音訊類型 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16a8b97afdd48cb1d7828f80778aa9fcf8dc1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386029"
---
# <a name="enumerating-audio-types-for-specific-encoding-modes-microsoft-media-foundation"></a>列舉特定編碼模式的音訊類型 (Microsoft 媒體基礎) 

音訊編碼器所接受的輸入和輸出媒體類型都是結構化的。 您必須藉由呼叫 **IMediaObject：： GetOutputType** 方法或 **IMFTransform：： GetOutputType** 來取得支援的輸出類型。 取得輸出型別之後，您就不能修改它。

如果您想要使用非單向 CBR 的編碼模式，您必須設定模式，然後列舉該模式的輸出類型。編碼器會根據設定的模式變更支援的輸出類型。 控制編碼模式的屬性為 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 和 [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)。 當您在編碼器中設定模式時，您必須使用它來列舉和選取輸出類型，而不需要變更，就像使用 CBR 一樣。

## <a name="identifying-quality-based-vbr-types"></a>識別以品質為基礎的 VBR 類型

識別品質型 VBR 類型的程式，取決於編碼器是否作為 DirectX 媒體物件 (的) 或作為媒體基礎的轉換 (MFT) 。 如需編碼器作為一或 MFT 的詳細資訊，請參閱 [編解碼器物件](codecobjects.md)底下的個別編解碼器參考頁面。

當音訊編碼器作為一，且您將編碼器設定為使用一次的 VBR 時，它會列舉所有支援的輸出類型。 不過，您通常會想要根據 quality 參數選取一次傳遞的 VBR 型別。 編碼器會在 WAVEFORMATEX 結構的 NAvgBytesPerSec 成員中，將單一傳遞的 VBR 輸出類型的品質值放在結構的成員中 **\_ \_ 。 pbFormat**。

此值會以下列格式儲存：0x7FFFFFXX，其中 XX 是從0到 100)  (的品質值。 例如，0x7FFFFF62 的 **nAvgBytesPerSec** 值會指定品質層級 98 (0x62 = 98) 。

下列範例將示範如何在編碼器作為的時候，檢查格式的品質等級。


```
void ShowQuality(WAVEFORMATEX* pWave)
{
    // Store the average bytes per second in a local variable
    // with a more manageable name.
    DWORD dwBps = pWave->nAvgBytesPerSec;

    // Verify that the value is a VBR quality level by using 
    // a bitmask to check for the bit pattern 0x7FFFFFXX. 
    if(dwBps & 0x7FFFFF00 == 0x7FFFFF00)
        printf("VBR Quality: %d%%\n",(dwBps & 0x000000FF));
    else // Not a valid VBR quality value.
        printf("Not a valid one-pass VBR audio format.\n");
}
```



當編碼器做為 MFT 時，它會在呼叫 **GetAvailableOutputType** 時列舉輸出型別，您可以針對 **MFPKEY 最近列舉的 \_ \_ \_ \_ VBRQUALITY** 屬性查詢 MFT。 傳回的值表示最近傳回之輸出媒體類型的 VBR 品質。 然後您可以使用該值來設定編碼器的 [**MFPKEY \_ 所需 \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) 屬性。

## <a name="setting-peak-constraints"></a>設定尖峰條件約束

針對以品質為基礎的 VBR (一次傳遞) 和未受限制的雙向 VBR，在抓取輸出類型之後，不需要其他設定。 若要使用尖峰限制的 VBR，請取出啟用 VBR 的輸出類型，並設定兩個階段。 此類型（沒有變更）描述未受限制的 VBR 設定。 若要設定尖峰條件約束，請設定 [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) 和 [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) 屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定音訊編碼](configuringaudioencoding.md)
</dt> <dt>

[尋找音訊編碼器輸出類型](findingaudioencoderoutputtypes.md)
</dt> <dt>

[使用 Two-Pass 編碼](usingtwoencodingpasses.md)
</dt> <dt>

[使用 VBR 編碼](usingvbrencoding.md)
</dt> </dl>

 

 




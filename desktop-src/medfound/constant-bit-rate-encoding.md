---
description: 常數位元速率編碼
ms.assetid: 0f084f3f-7432-4514-ae6a-c8179a99dec7
title: 常數位元速率編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea372a12d03a962f08e449bd707654391a2313b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936560"
---
# <a name="constant-bit-rate-encoding"></a>常數位元速率編碼

以固定位元速率 (CBR) 編碼方式，編碼器會在編碼會話開始之前，知道輸出媒體範例的位元速率，以及緩衝區視窗 (有漏洞 bucket 參數) 。 編碼器會使用相同數目的位數來編碼整個檔案期間的每秒樣本，以達到資料流程的目標位元速率。 這會限制資料流程範例大小的變化。 此外，編碼會話期間的位元速率不會完全符合指定的值，但會保持接近目標位速率。

CBR 編碼在您想要在不剖析完整檔案的情況下，想知道位元速率或檔案的約略長度時十分好用。 這在即時資料流中是必要的，因為媒體內容需要以可預測的位元速率以及固定的頻寬用量來進行串流。

CBR 編碼的缺點是編碼內容的品質不會是常數。 因為有些內容較難壓縮，所以 CBR 串流的部分會比其他部分的品質低。 例如，典型的電影有一些相當靜態的場景，以及一些完全行動的場景。 如果您使用 CBR 將電影編碼、靜態的場景，因此可以有效率地編碼，則其品質會比動作場景高，但需要較高的取樣大小才能維持相同的品質。

一般而言，CBR 檔案品質的變化會以較低的位元速率更明顯。 以較高的位元速率來說，CBR 編碼檔案的品質仍會有所不同，但對使用者而言，品質問題將會比較不明顯。 使用 CBR 編碼時，您應該在傳遞案例允許的情況下設定最高的頻寬。

-   [CBR 設定](#cbr-configuration-settings)
-   [有漏洞 Bucket 設定](#leaky-bucket-settings)

### <a name="cbr-configuration-settings"></a>CBR 設定

您必須在編碼會話之前，指定編碼類型和各種資料流程特定設定，以設定編碼器。

**設定用於 CBR 編碼的編碼器**

1.  指定 CBR 編碼模式。

    根據預設，編碼器會設定為使用 CBR 編碼。 編碼器設定會透過屬性值設定。 這些屬性是在 wmcodecdsp 中定義。 您可以將 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 屬性設定為 VARIANT FALSE，以明確指定此模式 \_ 。 如需有關如何設定編碼器屬性的詳細資訊，請參閱設定 [編碼器](configuring-the-encoder.md)。

2.  選擇編碼位元速率。

    針對 CBR 編碼，您必須在編碼會話開始之前，知道您想要對資料流程進行編碼的位元速率。 您必須在設定編碼器的期間設定位元速率。 若要執行這項操作，請在執行媒體類型協商時，檢查音訊串流的 [ [**mf \_ mt \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md) ] 屬性 () 或 [適用于影片) 串流的 [**mf \_ mt \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md) ] 屬性 (針對可用的輸出媒體類型，並選擇最接近您要達到的目標位速率的輸出媒體類型。 如需詳細資訊，請參閱 [編碼器上的媒體類型協商](media-type-negotiation-on-the-encoder.md)。

下列程式碼範例顯示 SetEncodingProperties 的執行。 此函式會設定 CBR 和 VBR 的資料流程層級編碼屬性。


```C++
//-------------------------------------------------------------------
//  SetEncodingProperties
//  Create a media source from a URL.
//
//  guidMT:  Major type of the stream, audio or video
//  pProps:  A pointer to the property store in which 
//           to set the required encoding properties.
//-------------------------------------------------------------------

HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
{
    if (!pProps)
    {
        return E_INVALIDARG;
    }

    if (EncodingMode == NONE)
    {
        return MF_E_NOT_INITIALIZED;
    }
   
    HRESULT hr = S_OK;

    PROPVARIANT var;

    switch (EncodingMode)
    {
        case CBR:
            // Set VBR to false.
            hr = InitPropVariantFromBoolean(FALSE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the video buffer window.
            if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        case VBR:
            //Set VBR to true.
            hr = InitPropVariantFromBoolean(TRUE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Number of encoding passes is 1.

            hr = InitPropVariantFromInt32(1, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the quality level.

            if (guidMT == MFMediaType_Audio)
            {
                hr = InitPropVariantFromUInt32(98, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromUInt32(95, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        default:
            hr = E_UNEXPECTED;
            break;
    }    

done:
    PropVariantClear(&var);
    return hr;
}
```



### <a name="leaky-bucket-settings"></a>有漏洞 Bucket 設定

針對 CBR 編碼，資料流程的平均和最大有漏洞 bucket 值相同。 如需這些參數的詳細資訊，請參閱 [有漏洞 Bucket 緩衝區模型](the-leaky-bucket-buffer-model.md)。

若要對音訊串流進行 CBR 編碼，您必須在在編碼器上協商輸出媒體類型之後，設定有漏洞值區的值。 編碼器會根據輸出媒體類型上設定的平均位元速率，在內部計算緩衝區視窗。

若要設定有漏洞值區值，請建立 Dword 陣列，以便在媒體接收器的屬性存放區中，于 [**MFPKEY \_ ASFSTREAMSINK \_ 更正 \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) 屬性中設定下列值。 如需詳細資訊，請參閱 [設定 File 接收中的屬性](setting-properties-in-the-file-sink.md)。

-   平均位元速率：從媒體類型協商期間選取的輸出媒體類型取得平均位元速率。 使用「 [**\_ 每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md) 」屬性。
-   緩衝區視窗：查詢 [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) 介面的編碼器，然後呼叫 [**IWMCodecLeakyBucket：： GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces .h，wmcodecdspuuid .lib) 。
-   初始緩衝區大小：設定為0。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 編碼類型](asf-encoding-types.md)
</dt> <dt>

[教學課程： 1-傳遞 Windows Media 編碼](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[教學課程：使用 CBR 編碼方式撰寫 WMA 檔案](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 

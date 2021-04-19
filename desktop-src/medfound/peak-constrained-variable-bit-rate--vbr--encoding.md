---
description: 在以尖峰限制的變數位速率 (VBR) 中，內容會編碼為指定的位元速率和尖峰值：尖峰位元速率和尖峰緩衝區視窗。
ms.assetid: bc37362e-d66d-4552-8357-d22093d5d0ad
title: Peak-Constrained 變數位速率編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8a32ed6b6f90ce1e112cf5afd19f33e65f541a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987428"
---
# <a name="peak-constrained-variable-bit-rate-encoding"></a>Peak-Constrained 變數位速率編碼

在以尖峰限制的變數位速率 (VBR) 中，內容會編碼為指定的位元速率和尖峰 *值*：尖峰位元速率和尖峰緩衝區視窗。 這些尖峰值也稱為 *尖峰有漏洞 bucket 值*。 檔案經過編碼，以符合尖峰值所描述的緩衝區，因此資料流程的整體平均位元速率等於或小於您指定的平均位元速率值。

通常，尖峰位速率很高。 編碼器可確保指定的平均位元速率值會在資料流程的持續時間內維持 (平均位元速率 >= (以秒為單位的資料流程大小總計（以秒為單位）) ) 。 請考慮下列範例：您設定的資料流程具有每秒16000位的平均位元速率、每秒48000位的尖峰位速率，以及 3000 (3 秒) 的尖峰緩衝區視窗。 用於資料流程的緩衝區大小是每秒144000個位 (48000 位， \*) 由尖峰值決定。 編碼器會壓縮資料以符合該緩衝區。 此外，資料流程的平均位元速率必須為16000或更少。 如果編碼器必須建立大型樣本來處理複雜的內容區段，它可以利用大型緩衝區大小。 但是資料流程的其他部分必須以較低的位元速率編碼，以將平均值帶到指定的層級。 尖峰限制的 VBR 編碼適用于具有有限緩衝區容量和資料速率條件約束的播放裝置。 其中一個常見的範例是在裝置上的晶片執行解碼時，用於 Dvd 的編碼方式是必須考慮的硬體限制。

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a>設定 Peak-Constrained VBR 的編碼器

尖峰限制的 VBR 就像是不受 [限制的 vbr](unconstrained-variable-bit-rate--vbr--encoding.md) ，因為它會限制為數據流持續時間的平均位元速率。 此外，尖峰限制的 VBR 會符合尖峰緩衝區。 此緩衝區是使用尖峰位元速率和尖峰緩衝區視窗來描述。 此模式會使用兩種編碼方式，並提供編碼器在編碼個別樣本的方式時的彈性，同時遵守尖峰限制。

編碼器設定會透過屬性值設定。 這些屬性是在 wmcodecdsp 中定義。 必須先在編碼器上設定設定屬性，才能協商輸出媒體類型。 如需有關如何設定編碼器屬性的詳細資訊，請參閱設定 [編碼器](configuring-the-encoder.md)。 根據指定的屬性值，您可以列舉支援的 VBR 輸出類型，並根據平均位元速率，在編碼器 [媒體基礎轉換](media-foundation-transforms.md) (MFT) 。

您必須設定下列 propertiesfor 這種類型的編碼方式：

-   將 MFPKEY \_ VBRENABLED 屬性設定為 VARIANT TRUE，以指定 VBR 編碼模式 \_ 。
-   將 MFPKEY \_ PASSESUSED 設定為2，因為尖峰限制的 VBR 模式會使用兩個編碼階段。
-   設定 MFPKEY \_ RMAX 指定尖峰位速率，並設定 MFPKEY \_ BMAX 來指定尖峰緩衝區視窗。
-   在列舉輸出媒體類型時，請檢查音訊串流的 [ [**mf \_ mt \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md) ] 屬性 (針對 [音訊串流]) 或 [適用于影片) 串流的 [**mf \_ mt \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md) ] 屬性 (針對可用的輸出媒體類型，並選擇最接近您希望編碼器在編碼內容中維護之平均位元速率的平均位元速率的輸出媒體類型。 如需有關選取輸出媒體類型的詳細資訊，請參閱 [編碼器上的媒體類型協商](media-type-negotiation-on-the-encoder.md)。

> [!Note]  
> 建議您將尖峰位速率設定為至少兩倍的平均位元速率。 將尖峰速率設定為較低的值，可能會導致編碼器將內容編碼為兩次傳遞 CBR，而不是尖峰限制的 VBR。

 

若要取得由編碼器設定的緩衝區視窗值，請在編碼會話之後，呼叫 **IWMCodecLeakyBucket：： GetBufferSizeBits**（定義于 wmcodecifaces. h，wmcodecdspuuid）中。 若要為數據流新增未受限制的 VBR 支援，您必須在設定 ASF 設定檔時，于串流設定物件上 (尖峰有漏洞值區值) ，在 [ [**MF \_ \_**](mf-asfstreamconfig-leakybucket2-attribute.md) 值區值] 中設定此值。

下列程式碼範例會修改範例類別 CEncoder 的 SetEncodingType 方法，以設定尖峰限制的 VBR 模式。 如需此類別的詳細資訊，請參閱 [編碼器範例程式碼](encoder-example-code.md)。 如需此範例中所使用之 helper 宏的詳細資訊，請參閱使用媒體基礎程式碼範例。


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to peak-constrained VBR mode.
//
/////////////////////////////////////////////////////////////////////////

HRESULT CEncoder::SetEncodingType(EncodeMode mode)
{
    if (!m_pMFT)
    {
        return MF_E_NOT_INITIALIZED;
    }

    HRESULT hr = S_OK;

    IPropertyStore* pProp = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    // Query the encoder for its property store.
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Peak)
    {
        // Set the VBR property to TRUE, which indicates VBR encoding.
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        // Set number of passes.
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);

        // Set the peak bit rate.
        var.vt = VT_I4;
        var.lVal  =48000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_RMAX, var));
        PropVariantClear(&var);

        // Set the peak buffer window.
        var.vt = VT_I4;
        var.lVal  =3000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_BMAX, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 編碼類型](asf-encoding-types.md)
</dt> <dt>

[有漏洞 Bucket 緩衝區模型](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[如何建立 Two-Pass Windows Media 編碼的拓撲](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 




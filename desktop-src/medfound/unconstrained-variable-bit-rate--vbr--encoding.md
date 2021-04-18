---
description: 不受限制的變數位速率編碼
ms.assetid: 35fb4bd7-87c5-4f46-ae71-10278670ef9c
title: 不受限制的變數位速率編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b216629991b466aa8560e26e0ada623f9c26efa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983419"
---
# <a name="unconstrained-variable-bit-rate-encoding"></a>不受限制的變數位速率編碼

在不受限制的變數位速率 (VBR) 編碼模式中，內容會編碼為可能的最高品質，同時維持指定的位元速率。

未受限制的 VBR 編碼會使用兩種編碼階段。 使用不受限制的 VBR 編碼時，您可以指定資料流程的位元速率，如同使用 [常數的位元速率編碼](constant-bit-rate-encoding.md)一樣。 不過，編碼器只會使用此值做為資料流程的平均位元速率，並進行編碼，讓品質盡可能高，同時維持平均。 編碼器所產生的個別樣本會因大小而異，而不會有任何明確的緩衝區限制。 不過，編碼會話期間的平均位元速率與資料流程的持續時間必須不超過您所指定的值。 編碼資料流程中任何時間點的實際位元速率可能會有極大的差異。 您未針對未受限制的 VBR 編碼設定緩衝區視窗。 相反地，編碼器會根據編碼範例的需求，計算所需緩衝區視窗的大小。 這表示，只要平均位元速率小於或等於您設定的值，資料流程中個別樣本的大小就沒有任何限制。

未受限制的 VBR 編碼的優點在於壓縮的資料流程具有最高的可能品質，同時維持在可預測的平均頻寬內。 當您需要指定頻寬，但可接受指定頻寬的波動時，請使用此值;例如，針對本機檔案或僅限下載。

這種編碼模式的缺點是，編碼器可以在編碼之後將緩衝區視窗設定為任何需要的值，讓您無法控制緩衝區大小。 在大部分情況下，如果您不在意緩衝區大小或頻寬使用量的一致性，您應該使用 [品質型變數位元速率編碼](quality-based-variable-bit-rate--vbr--encoding.md)

### <a name="configuring-the-encoder-for-unconstrained-vbr"></a>設定未受限制 VBR 的編碼器

編碼器設定會透過屬性值設定。 這些屬性是在 wmcodecdsp 中定義。 必須先在編碼器上設定設定屬性，才能協商輸出媒體類型。 如需有關如何設定編碼器屬性的詳細資訊，請參閱設定 [編碼器](configuring-the-encoder.md)。 根據指定的屬性值，您可以列舉支援的 VBR 輸出類型，並根據平均位元速率，在編碼器 [媒體基礎轉換](media-foundation-transforms.md) (MFT) 。

下列清單顯示您必須為這種編碼類型設定的屬性：

-   將 MFPKEY \_ VBRENABLED 屬性設定為 VARIANT TRUE，以指定 VBR 編碼模式 \_ 。
-   將 MFPKEY \_ PASSESUSED 設定為2，因為未受限制的 VBR 模式會使用兩個編碼階段。
-   列舉輸出媒體類型時，請檢查音訊串流的 [ [**mf \_ mt \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md) ] 屬性 () 或 [ [**mf \_ mt \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md) ] 屬性 (適用于可用輸出媒體類型的影片資料流程) 。 選擇輸出媒體類型，其平均位元速率最接近您希望編碼器在編碼內容中維護的所需平均位元速率。 如需有關選取輸出媒體類型的詳細資訊，請參閱 [編碼器上的媒體類型協商](media-type-negotiation-on-the-encoder.md)。

若要取得緩衝區視窗值，請在編碼會話之後，呼叫 **IWMCodecLeakyBucket：： GetBufferSizeBits**（定義于 wmcodecifaces .h 和 wmcodecdspuuid 中）。 若要為數據流新增不受限制的 VBR 支援，您必須在設定 ASF 設定檔時，于串流設定物件上 (平均有漏洞值區值) ，在 [ [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) ] 屬性中設定這個值。

下列範例會修改範例類別 CEncoder 的 SetEncodingType 方法，以設定未受限制的 VBR 模式。 如需此類別的詳細資訊，請參閱 [編碼器範例程式碼](encoder-example-code.md)。 如需此範例中所使用之 helper 宏的詳細資訊，請參閱使用媒體基礎程式碼範例。


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to unconstrained VBR
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

    //Query the encoder for its property store
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Unconstrained)
    {
        //Set the VBR property to TRUE, which indicates VBR encoding
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        //Set number of passes
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
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

 

 




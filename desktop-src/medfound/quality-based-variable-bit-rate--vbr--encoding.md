---
description: Quality-Based 變數位速率編碼
ms.assetid: e07c3f31-3d53-4250-9634-f66690357f26
title: Quality-Based 變數位速率編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12a60ab41b0ebf45c23fdb8a3f7ed330abda2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989926"
---
# <a name="quality-based-variable-bit-rate-encoding"></a>Quality-Based 變數位速率編碼

不同于 [常數的位元速率編碼](constant-bit-rate-encoding.md) (CBR) ，編碼器會致力於維持編碼媒體的特定位元速率，以變數位元速率 (VBR) 模式，而編碼器會致力於達到編碼媒體的最佳品質。 CBR 和 VBR 之間的主要差異在於使用的緩衝區視窗大小。 相較于 CBR 編碼的資料流程，VBR 編碼的資料流程通常會有大型的緩衝區視窗。

編碼內容的品質取決於壓縮內容時遺失的資料量。 許多因素會影響壓縮進程中的資料遺失;但一般而言，原始資料越複雜，壓縮的比率越高，壓縮程式就會遺失更多詳細資料。

在以品質為基礎的 VBR 模式中，您不會定義位元速率或編碼器必須遵循的緩衝區視窗。 相反地，您可以指定數位媒體串流的品質層級，而不是位元速率。 編碼器會壓縮內容，讓所有範例都具有相當的品質;這可確保在整個播放期間的品質都一致，不論產生之資料流程的緩衝區需求為何。

以品質為基礎的 VBR 編碼通常會建立大型的壓縮資料流程。 一般而言，這種編碼方式非常適合本機播放或高頻寬網路連線， (或下載並播放) 。 例如，您可以撰寫應用程式，從 CD 將歌曲複製到電腦上的 ASF 檔案。 使用以品質為基礎的 VBR 編碼，可確保複製的所有歌曲都具有相同的品質。 在這些情況下，一致的品質將提供更好的使用者體驗。

以品質為基礎之 VBR 編碼的缺點是，在編碼會話之前，沒有任何方法可以得知編碼媒體的大小或頻寬需求，因為編碼器會使用單一編碼階段。 這可以讓以品質為基礎的 VBR 編碼檔案不適用於記憶體或頻寬受限的情況，例如在便攜媒體播放機上播放內容，或透過低頻寬網路進行串流處理。

## <a name="configuring-the-encoder-for-quality-based-vbr-encoding"></a>設定 Quality-Based VBR 編碼的編碼器

編碼器設定會透過屬性值設定。 這些屬性是在 wmcodecdsp 中定義。 必須先在編碼器上設定設定屬性，才能協商輸出媒體類型。 如需有關如何設定編碼器屬性的詳細資訊，請參閱設定 [編碼器](configuring-the-encoder.md)。

下列清單顯示您必須為這種編碼類型設定的屬性：

-   將 **MFPKEY \_ VBRENABLED** 屬性設定為 VARIANT TRUE，以指定 VBR 編碼模式 \_ 。
-   將 **MFPKEY \_ PASSESUSED** 設定為1，因為這個 VBR 模式會使用一次編碼。
-   藉由設定 **MFPKEY \_ 所需的 \_ VBRQUALITY** 屬性，將所需的品質層級 (從0到 100) 。 以品質為基礎的 VBR 不會將內容編碼為任何預先定義的緩衝區參數。 此品質層級會針對整個資料流程進行維護，而不論所產生的位元速率需求為何。
-   若為影片串流，請在編碼器的輸出媒體類型上，將平均位元速率設定為 [ [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md) ] 屬性中的非零值。 編碼會話完成後，會更新正確的位元速率。

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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 編碼類型](asf-encoding-types.md)
</dt> </dl>

 

 




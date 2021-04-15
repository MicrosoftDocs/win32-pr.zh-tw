---
description: 設定設定檔和其他 ASF 檔案屬性
ms.assetid: c43df556-9d8a-4010-9ed6-f84d8ac6d9bc
title: 設定設定檔和其他 ASF 檔案屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e26dcbb49cb5ff8309dccafc3f1d8d66397871
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385759"
---
# <a name="configuring-profiles-and-other-asf-file-properties"></a>設定設定檔和其他 ASF 檔案屬性

下列專案說明如何執行與建立 ASF 檔案相關的各種工作。 本主題所提及的部分介面記載于 Windows Media Format SDK 檔中。

建立設定檔

ASF 設定檔會在 Windows Media Format SDK 中詳細討論;基本上，它們會描述 Windows Media 格式檔案的屬性，例如位元速率、資料流程的數目和類型，以及壓縮品質。 此篩選器會使用設定檔來決定要寫入的 Windows Media 格式檔案種類、必須設定多少輸入 pin，以及它們可以接受的媒體類型。

若要建立自訂設定檔，請使用 Windows Media Format SDK，直接使用 **WMCreateProfileManager** 函式建立配置檔案管理員物件。 接下來，使用 [**IConfigASFWriter：： ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile)方法建立設定檔，並將其傳遞至 [WM ASF 寫入器](wm-asf-writer-filter.md)。 這是使用 Windows Media 音訊和 Video 9 系列編解碼器的設定檔來設定篩選器的唯一方式。 您可以使用 [**IConfigASFWriter：： ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) 方法，新增這些編解碼器舊版的系統設定檔。

只要新的設定檔不需要任何額外的輸入釘選，您就可以在篩選的輸入 pin 連線時重設設定檔。 例如，如果您將設定檔從單一輸入的僅限音訊設定檔變更為雙輸入音訊和影片設定檔，則只會重新連線音訊 pin 碼，而且不會為影片串流建立新的 pin。

新增中繼資料

若要將中繼資料新增至檔案，請查詢 **IWMHeaderInfo** 介面的 [WM ASF 寫入](wm-asf-writer-filter.md)器篩選器。 將設定檔提供給篩選器之後，請使用 **IWMHeaderInfo** 介面方法來寫入中繼資料。

為檔案編制索引

在預設情況下，WM ASF 寫入器會建立暫時的索引檔案。 若要建立框架索引檔案，請使用 [**IConfigAsfWriter：： SetIndexMode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) 方法來停用所有的索引，然後建立檔案。 完成時，請直接使用 Windows Media Format SDK 來建立檔案的框架型索引。

Two-Pass 編碼

只有在第8版和更新版本的 Windows 媒體編解碼器上，才支援雙通過編碼。 藉由呼叫 [**IConfigAsfWriter2：： SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam)並在 \_ \_ DWPARAM 參數中指定 AM CONFIGASFWRITER PARAM \_ MULTIPASS，並在 *dwParam1* 參數中指定 **TRUE** ，將 WM ASF 寫入器放入前置處理模式。

然後執行篩選圖形。 當所有前置處理階段完成時 (通常只會執行一次前置處理階段) ，應用程式會從篩選器收到 EC 前置處理 [**\_ \_ 完成**](ec-preprocess-complete.md) 事件。 收到此事件時，請使用 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 將資料流程指標重設回開頭，然後再次執行篩選圖形。 最後一次通過之後 (通常是第二次傳遞) ，應用程式將會收到 [**EC \_ 完成**](ec-complete.md) 事件，以表示編碼程式已完成。 如果在收到 EC 前置處理 **\_ \_ 完成** 事件之前取消前置處理階段，請先呼叫 [**IConfigAsfWriter2：： ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) 來重設篩選，然後再嘗試執行其他前置處理。

只有當您想要將篩選器完全移出前置處理模式時，才需要將 AM \_ CONFIGASFWRITER \_ PARAM \_ MULTIPASS 參數設定為 **FALSE** 。

> [!IMPORTANT]
> 應用程式會負責根據將用於編碼的設定檔來啟用前置處理模式。 有些設定檔需要兩次傳遞編碼;如果您嘗試使用這類設定檔來編碼檔案，且未將 AM \_ CONFIGASFWRITER \_ PARAM MULTIPASS 設定 \_ 為 **TRUE**，則會產生 [**EC \_ USERABORT**](ec-userabort.md) 錯誤。 如需詳細資訊，請參閱 Windows Media Format SDK 檔。

 

在執行時間取得和設定緩衝區屬性

在某些情況下（例如，如果您想要在寫入檔案時強制插入金鑰框架），應用程式可能需要在執行時間取得或設定 Windows Media 緩衝區的相關資訊。 [WM Asf 讀取](wm-asf-reader-filter.md)器和 [WM asf 寫入](wm-asf-writer-filter.md)器篩選器都支援回呼機制，可讓應用程式在讀取或寫入檔案期間，存取每個個別媒體緩衝區上的 **INSSBuffer3** 介面。 應用程式可以使用此介面將特定範例指定為主要畫面格、設定 SMPTE 時間代碼、指定交錯設定，或將任何類型的私用資料新增至資料流程。

使用 [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) 介面，從處理影片串流的 pin 註冊回呼。 Pin 會為每個緩衝區呼叫您的 [**IAMWMBufferPassCallback：： Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) 方法。

非正方形圖元

WM ASF 寫入器會連接到輸出圖元外觀比例資訊的上游篩選器，例如 DV 解碼器。 WM ASF 寫入器會將這項資訊寫入檔案中每個範例的資料單位延伸模組。

當 WM ASF 讀取器在檔案標頭中或在範例的資料單位延伸中遇到圖元外觀比例資訊時，它會提供 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式作為其輸出圖釘的第一個選擇。 結構的 **dwPictAspectRatioX** 和 **dwPictAspectRatioY** 成員（描述影片矩形的外觀比例）將會正確調整以考慮圖元外觀比例。

維護交錯格式

如果您從電視或 DV 攝影機捕捉交錯的影片，如果您預期在電視或其他交錯顯示裝置上播放編碼的檔案，您可能會想要將原始影片保留為獨立欄位。  (電腦監視器是漸進式掃描裝置。 ) 如果您將影片進行逐行掃描，然後 reinterlace 以在電視上播放，將會產生部分資料遺失。 在 ASF 檔案中，會使用先前所述的 [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) 方法，將交錯資訊儲存為數據單位延伸，讓應用程式套用至每個範例。 若要編碼保留原始隔行設定的檔案，請遵循下列步驟：

1.  執行支援 **IAMWMBufferPassCallback** 的類別，並撰寫可設定每個範例之交錯旗標的通知函數。 在處理每個範例之前，會先由 WM ASF 寫入器呼叫此函數。
    ```C++
    // Set to WM_CT_TOP_FIELD_FIRST if that is your format.
    BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
    HRESULT hr = S_OK;

    hr = pNSSBuffer3->SetProperty(
        WM_SampleExtensionGUID_ContentType, 
        (void*) &flag, 
        WM_SampleExtension_ContentType_Size
        );         
    ```

    

2.  在您將設定檔傳遞至篩選之前，請先設定設定檔上的資料單位延伸。
    ```C++
    hr = pWMStreamConfig2->AddDataUnitExtension(
        WM_SampleExtensionGUID_ContentType, 
        WM_SampleExtension_ContentType_Size, 
        NULL, 
        0 
        );
    ```

    

3.  使用設定檔設定篩選準則之後，請從 WM ASF 寫入器取得 **IWMWriterAdvanced2** 介面，然後呼叫 **SetInputSettings** 方法。

    ``

    ``

    ```C++
    // Must do this first.
    hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);
      
    CComPtr<IServiceProvider> pProvider;
    CComPtr<IWMWriterAdvanced2> pWMWA2;

    hr = pConfigAsfWriter2->QueryInterface( __uuidof(IServiceProvider),
                                             (void**)&pProvider);
    if (SUCCEEDED(hr))
    {
        hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
            IID_IWMWriterAdvanced2,
            (void**)&pWMWA2);
    }

    BOOL pValue = TRUE;

    // Set the first parameter to your actual input number.
    hr = pWMWA2->SetInputSetting(0, g_wszInterlacedCoding,
        WMT_TYPE_BOOL, (BYTE*) &pValue, sizeof(WMT_TYPE_BOOL));
                
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 DirectShow 中建立 ASF 檔案](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 




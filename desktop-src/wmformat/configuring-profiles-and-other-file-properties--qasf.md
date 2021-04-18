---
title: " (QASF) 設定設定檔和其他檔案屬性"
description: " (QASF) 設定設定檔和其他檔案屬性"
ms.assetid: a462fc8b-5a2e-4c93-828d-177d1965b734
keywords:
- 'Windows Media 格式 SDK，設定設定檔 (QASF) '
- 'Windows Media 格式 SDK，設定檔案屬性 (QASF) '
- 'Windows Media 格式 SDK，中繼資料 (QASF) '
- 'Advanced Systems Format (ASF) 、設定設定檔 (QASF) '
- 'ASF (Advanced Systems Format) 、設定設定檔 (QASF) '
- 'Advanced Systems Format (ASF) ，設定檔案屬性 (QASF) '
- 'ASF (Advanced Systems Format) ，設定檔案屬性 (QASF) '
- 'Advanced Systems Format (ASF) 、metadata (QASF) '
- 'ASF (Advanced Systems Format) ，metadata (QASF) '
- Windows Media Format SDK、QASF
- Advanced Systems Format (ASF) ，QASF
- ASF (Advanced Systems Format) ，QASF
- 中繼資料、QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb6afedfa00813e7447e5bcaefe1f251c02575
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463456"
---
# <a name="configuring-profiles-and-other-file-properties-qasf"></a> (QASF) 設定設定檔和其他檔案屬性

下列專案說明如何執行與建立 ASF 檔案相關的各種工作。

## <a name="creating-a-profile-qasf"></a> (QASF) 建立設定檔

若要建立自訂設定檔，請使用 Windows Media Format SDK，直接使用 [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) 函式建立配置檔案管理員物件。 接下來，使用 [**IConfigASFWriter：： ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md)方法建立設定檔，並將其傳遞至 [WM ASF 寫入器](wm-asf-writer-filter.md)。 這是使用 Windows Media 音訊和 Video 9 系列編解碼器的設定檔來設定篩選器的唯一方式。 您可以使用 [**IConfigASFWriter：： ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) 方法，新增這些編解碼器舊版的系統設定檔。

## <a name="adding-metadata-qasf"></a>新增中繼資料 (QASF) 

若要將中繼資料新增至檔案，請從 [WM ASF 寫入器](wm-asf-writer-filter.md)上的 **IBaseFilter** 介面呼叫 **QueryInterface** ，以取出 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)介面。 將設定檔提供給篩選器之後，請使用 **IWMHeaderInfo** 介面方法來寫入中繼資料。

## <a name="indexing-a-file-qasf"></a> (QASF) 為檔案編制索引

在預設情況下，WM ASF 寫入器會建立暫時的索引檔案。 若要建立框架索引檔案，請使用 [**IConfigAsfWriter：： SetIndexMode**](iconfigasfwriter-setindexmode.md) 方法來停用所有的索引，然後建立檔案。 完成時，請直接使用 Windows Media Format SDK 來建立檔案的框架型索引。

## <a name="performing-two-pass-encoding-qasf"></a>執行 Two-Pass 編碼 (QASF) 

只有在第8版和更新版本的 Windows 媒體編解碼器上，才支援雙通過編碼。 藉由呼叫 [**IConfigAsfWriter2：： SetParam**](iconfigasfwriter2-setparam.md)並在 \_ \_ DWPARAM 參數中指定 AM CONFIGASFWRITER PARAM \_ MULTIPASS，並在 *dwParam1* 參數中指定 **TRUE** ，將 WM ASF 寫入器放入前置處理模式。

然後執行篩選圖形。 當所有前置處理階段完成時 (通常只會執行一次前置處理階段) ，應用程式會從篩選器收到 EC 前置處理 **\_ \_ 完成** 事件。 收到此事件時，請使用 **IMediaSeeking：： SetPositions** 將資料流程指標重設回開頭，然後再次執行篩選圖形。 最後一次通過之後 (通常是第二次傳遞) ，應用程式將會收到 **EC \_ 完成** 事件，以表示編碼程式已完成。 如果在收到 EC 前置處理 **\_ \_ 完成** 事件之前取消前置處理階段，請先呼叫 [**IConfigAsfWriter2：： ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) 來重設篩選，然後再嘗試執行其他前置處理。

只有呼叫 **IConfigAsfWriter：： SetParam** (AM \_ CONFIGASFWRITER \_ PARAM \_ MULTIPASS，) **FALSE** 才能將篩選器完全移出前置處理模式。

> [!IMPORTANT]
> 應用程式會負責根據將用於編碼的設定檔來啟用前置處理模式。 有些設定檔需要兩次傳遞編碼;如果您嘗試使用這類設定檔來編碼檔案，且未將 AM \_ CONFIGASFWRITER \_ PARAM MULTIPASS 設定 \_ 為 **TRUE**，則 \_ 會產生 EC USERABORT 錯誤。 如需如何判斷指定的設定檔是否需要雙向編碼的詳細資訊，請參閱 [使用 Two-Pass 編碼](using-two-pass-encoding.md) 或 [撰寫變數位速率資料流程](writing-variable-bit-rate-streams.md)。

 

## <a name="getting-and-setting-buffer-properties-at-run-time-qasf"></a>在執行時間取得和設定緩衝區屬性 (QASF) 

在某些情況下（例如，如果您想要在寫入檔案時強制插入金鑰框架），應用程式可能需要在執行時間取得或設定 Windows Media 緩衝區的相關資訊。 [WM Asf 讀取](wm-asf-reader-filter.md)器和 [WM asf 寫入](wm-asf-writer-filter.md)器篩選器都支援回呼機制，可讓應用程式在讀取或寫入檔案期間，存取每個個別媒體緩衝區上的 [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)介面。 應用程式可以使用此介面將特定範例指定為主要畫面格（或 [*cleanpoints*](wmformat-glossary.md)），以設定 SMPTE 時間代碼、指定交錯設定，或將任何類型的私用資料新增至資料流程。

使用 [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) 介面，從處理影片串流的 pin 註冊回呼。 當 pin 呼叫您的 [**IAMWMBufferPassCallback：： Notify**](iamwmbufferpasscallback-notify.md) 方法時，請檢查緩衝區上的時間戳記，並在適當的情況下呼叫 [**INSSBuffer3：： SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) 將緩衝區上的 **WM \_ SampleExtensionGUID \_ OutputCleanPoint** 屬性設定為 **TRUE**。

## <a name="non-square-pixel-support-qasf"></a> (QASF) 的非方形圖元支援

WM ASF 寫入器會連接到輸出圖元外觀比例資訊的上游篩選器，例如 DV 解碼器。 WM ASF 寫入器會將這項資訊寫入檔案中每個範例的資料單位延伸模組。

當 WM ASF 讀取器遇到檔案標頭中的圖元外觀比例資訊，或在範例的資料單位延伸中，它會提供 **VIDEOINFOHEADER2** 媒體類型作為其輸出圖釘的第一個選擇。 結構的 **dwPictAspectRatioX** 和 **dwPictAspectRatioY** 成員（描述影片矩形的外觀比例）將會正確調整以考慮圖元外觀比例。

## <a name="maintaining-interlaced-format"></a>維護交錯格式

如果您從電視或 DV 攝影機捕捉交錯的影片，如果您預期在電視或其他交錯顯示裝置上播放編碼的檔案，您可能會想要將原始影片保留為獨立欄位。  (電腦監視器是漸進式掃描裝置。 ) 如果您將影片進行逐行掃描，然後 reinterlace 以在電視上播放，將會產生部分資料遺失。 在 ASF 檔案中，會使用先前所述的 **IAMWMBufferPassCallback** 方法，將交錯資訊儲存為數據單位延伸，讓應用程式套用至每個範例。 若要編碼保留原始隔行設定的檔案，請遵循下列步驟：

-   執行支援 **IAMWMBufferPassCallback** 的類別，並撰寫可設定每個範例之交錯旗標的通知函數。 在處理每個範例之前，會先由 WM ASF 寫入器呼叫此函數。


```C++
// Set to WM_CT_TOP_FIELD_FIRST if that is your format.
BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
            HRESULT hr = pNSSBuffer3->SetProperty(WM_SampleExtensionGUID_ContentType, (void*) &flag, WM_SampleExtension_ContentType_Size);
           
```



-   在您將設定檔傳遞至篩選之前，請先設定設定檔上的資料單位延伸。


```C++
hr = pWMStreamConfig2->AddDataUnitExtension( WM_SampleExtensionGUID_ContentType, WM_SampleExtension_ContentType_Size, NULL, 0 );
```



-   使用設定檔設定篩選準則之後，請從 WM ASF 寫入器取得 **IWMWriterAdvanced2** 介面，然後呼叫 **SetInputSettings** 方法。

`// Must do this first.`

`hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);`


```C++
  
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



 

 
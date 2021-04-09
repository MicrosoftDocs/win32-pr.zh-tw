---
title: 將音訊解碼為 S/PDIF
description: 將音訊解碼為 S/PDIF
ms.assetid: b56c2d0a-a7c6-44f8-832a-bbbe7ae053e6
keywords:
- Windows Media Format SDK，將音訊解碼為 S/PDIF
- 'Windows Media Format SDK、索尼/Philips 數位互連格式 (S/PDIF) '
- Advanced Systems Format (ASF) ，將音訊解碼為 S/PDIF
- ASF (Advanced Systems Format) ，將音訊解碼成 S/PDIF
- 'Advanced Systems Format (ASF) 、索尼/Philips 數位互連格式 (S/PDIF) '
- 'ASF (Advanced Systems Format) 、索尼/Philips 數位互連格式 (S/PDIF) '
- 索尼/Philips 數位互連格式 (S/PDIF) ，解碼音訊
- S/PDIF (索尼/Philips 數位互連格式) ，解碼音訊
- 解碼音訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa063baa8e9a88c2fb7a4d9c67375965282167
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103681558"
---
# <a name="to-decode-audio-to-spdif"></a>將音訊解碼為 S/PDIF

使用 Windows Media 音訊 9 Professional 編解碼器編碼的音訊可以解碼成索尼/Philips 數位互連格式 (S/PDIF) 。 若要產生 S/PDIF 輸出，請執行下列步驟：

1.  藉由呼叫 [**IWMReader：： open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) 方法，開啟包含 Windows Media 音訊 9 Professional 串流的檔案。
2.  識別您想要的資料流程輸出編號。 如需詳細資訊，請參閱 [識別輸出數目](to-identify-output-numbers.md)。
3.  呼叫 [**IWMReaderAdvanced2：： SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) 方法來設定 S/PDIF 輸出。 請使用 g \_ wszEnableWMAProSPDIFOutput 作為設定名稱。 資料類型為 **WMT \_ 類型 \_ BOOL**; 將值設定為 **TRUE** 以啟用 S/PDIF 輸出。
4.  藉由呼叫 [**IWMReader：： GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat)方法，取得所需輸出格式的輸出屬性介面 ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) 。 如需列舉輸出格式的詳細資訊，請參閱 [指派輸出格式](assigning-output-formats.md)。
5.  藉由呼叫 [**IWMReader：： SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) 方法來設定輸出格式。 將指標傳入在步驟4中取得的 **IWMOutputMediaProps** 介面。
6.  進行任何其他設定變更並開始播放。

> [!Note]  
> 您可以使用 [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) 介面的對應方法，在同步讀取器上執行上述步驟。

 

下列範例程式碼示範如何設定音訊串流，以將音訊輸出為 S/PDIF 資料。 此函式會假設已在讀取器中載入檔案，且已識別出輸出編號。 如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。


```C++
HRESULT SetSPDIF(DWORD dwOutputNum, IWMReader* pReader)
{
    HRESULT hr = S_OK;

    IWMReaderAdvanced2*  pReaderAdv   = NULL;
    IWMOutputMediaProps* pOutputProps = NULL; 

    BOOL fValue = TRUE;

    // Get the advanced reader interface.
    hr = pReader->QueryInterface(IID_IWMReaderAdvanced2,
                                 (void**)&pReaderAdv);
    GOTO_EXIT_IF_FAILED(hr);

    // Set S/PDIF output.
    hr = pReaderAdv->SetOutputSetting(dwOutputNum, 
                                      g_wszEnableWMAProSPDIFOutput, 
                                      WMT_TYPE_BOOL, 
                                      (BYTE*)&fValue, 
                                      sizeof(BOOL));
    GOTO_EXIT_IF_FAILED(hr);

    // Get the first output format for the stream.
    // NOTE: You could also enumerate the available output formats
    // and pick one to use.

    hr = pReader->GetOutputFormat(dwOutputNum, 0, &pOutputProps);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the output properties back on the reader.
    hr = pReader->SetOutputProps(dwOutputNum, pOutputProps);

Exit:
    SAFE_RELEASE(pReaderAdv);
    SAFE_RELEASE(pOutputProps);

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Advanced 主題**](advanced-topics.md)
</dt> <dt>

[**讀取 ASF 檔案**](reading-asf-files.md)
</dt> <dt>

[**IWMReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMReaderAdvanced2 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**IWMSyncReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 





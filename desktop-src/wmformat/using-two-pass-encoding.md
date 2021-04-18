---
title: '使用 Two-Pass 編碼 (Windows Media Format 11 SDK) '
description: 使用 Two-Pass 編碼
ms.assetid: 55fc768b-15f0-4236-ad0d-3792ccaa9b4f
keywords:
- Advanced Systems Format (ASF) ，兩次傳遞編碼
- ASF (Advanced Systems Format) ，雙通編碼
- 雙通路編碼，關於
- 2-通過編碼，關於
- 編解碼器，雙通路編碼
- 雙通編碼，IWMWriterPreprocess 介面
- 2-傳遞編碼，IWMWriterPreprocess 介面
- IWMWriterPreprocess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3794856f47c1656cc53006268c41a063cdde96
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508280"
---
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a>使用 Two-Pass 編碼 (Windows Media Format 11 SDK) 

某些編解碼器支援某些格式的雙通編碼。 在某些情況下，編解碼器會要求使用兩個傳遞來編碼指定的格式。 使用雙重傳遞編碼時，您會在編碼傳遞之前將資料流程的範例傳送至編解碼器。 編解碼器會分析範例，並根據分析設定編碼傳遞。 這會產生更有效率的編碼檔案。

若要判斷編解碼器是否支援一次傳遞編碼或雙向（或兩者），請針對指定的格式，使用 g wszNumPasses 和適當的值呼叫 [**IWMCodecInfo3：： SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) ，然後 \_ 列舉格式以查看是否傳回您想要的格式。 如需支援雙向編碼的 Windows Media 編解碼器的詳細資訊，請參閱 [選擇編碼方法](choosing-an-encoding-method.md)。

您可以藉由呼叫 [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) 介面的方法，搭配 Windows MEDIA 格式 SDK 來使用雙通路編碼。

如果特定格式需要雙向編碼，但應用程式無法執行前置處理階段，則第一次呼叫 [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) 將會失敗，並出現 NS \_ E \_ 不正確 \_ \_ 次數。

下列範例函式示範如何執行兩次傳遞編碼。 使用設定檔設定寫入器並啟動之後，會呼叫這個函式。 如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。


```C++
HRESULT PreProcess(IWMWriter* pWriter, DWORD dwInputNum)
{
    HRESULT hr        = S_OK;
    DWORD   dwMaxPass = 0;

    IWMWriterPreprocess* pPreProc = NULL;

    // Get the writer preprocessor interface.
    hr = pWriter->QueryInterface(IID_IWMWriterPreprocess, 
                                 (void**) &pPreProc);
    GOTO_EXIT_IF_FAILED(hr);

    // Check that the input can be preprocessed.
    hr = pPreProc->GetMaxPreprocessingPasses(dwInputNum,0, &dwMaxPass);
    GOTO_EXIT_IF_FAILED(hr);

    if(dwMaxPass == 0)
    {
        hr = NS_E_INVALID_REQUEST;
        goto Exit;
    }

    // Set the number of preprocessing passes to the maximum.
    hr = pPreProc->SetNumPreprocessingPasses(dwInputNum, 0, dwMaxPass);
    GOTO_EXIT_IF_FAILED(hr);

    // Call BeginWriting before calling BeginPreprocessingPass
    hr = pWriter->BeginWriting();

    // Start preprocessing the first pass.
    hr = pPreProc->BeginPreprocessingPass(dwInputNum, 0);
    GOTO_EXIT_IF_FAILED(hr);

    // TODO: Make repeated calls to pPreProc->PreprocessSample to
    // preprocess all the samples in the stream.

    // End preprocessing.
    hr = pPreProc->EndPreprocessingPass(dwInputNum, 0);
    GOTO_EXIT_IF_FAILED(hr);

    // TODO: If the maximum number of preprocessing passes is greater
    // than one, repeat the preprocessing steps for each pass.

Exit:
    SAFE_RELEASE(pPreProc);
    Return hr;
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 





---
title: 依數位識別輸入
description: 依數位識別輸入
ms.assetid: f468f74d-7eed-4819-957d-241903f44d2d
keywords:
- Advanced Systems Format (ASF) ，以數位識別輸入
- ASF (Advanced Systems Format) ，依數位識別輸入
- 設定檔，依編號識別輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ff09a81cac98edc6f14ded98ba9852501bfdfef4c5e40affa908c0ff710e1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807528"
---
# <a name="to-identify-inputs-by-number"></a>依數位識別輸入

您傳遞給寫入器的每個範例都必須與輸入編號相關聯。 每個輸入號碼都會對應到寫入器用來寫入檔案的設定檔中的一或多個資料流程。 在設定檔中，媒體來源是以連接名稱來識別。 當您設定寫入器的設定檔時，寫入器會將輸入編號與每個連接名稱產生關聯。 在您可以將範例傳遞給寫入器之前，您必須決定每個輸入所預期的資料。 您無法假設輸入的順序與設定檔中的資料流程相同，即使通常是如此。 因此，將輸入與資料流程相符的唯一可靠方式是將輸入的連接名稱與資料流程的連接名稱進行比較。

若要識別已載入設定檔的連線名稱和對應的輸入編號，請執行下列步驟：

1.  建立寫入器物件，並設定要使用的設定檔。 如需在寫入器中設定設定檔的詳細資訊，請參閱搭配 [使用設定檔與寫入器](to-use-profiles-with-the-writer.md)。 您應該知道設定檔中的資料流程所使用的連接名稱。 您可以取得每個資料流程的串流設定物件，並呼叫 [**IWMStreamConfig：： GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname)，以從設定檔中取得連接名稱。 如需設定檔和串流設定物件的詳細資訊，請參閱 [使用設定檔](working-with-profiles.md)。
2.  藉由呼叫 [**IWMWriter：： GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount)來取出輸入總數。
3.  迴圈執行所有輸入，為每個輸入執行下列步驟。
    -   藉由呼叫 [**IWMWriter：： GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)，來取得輸入的 [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)介面。
    -   藉由呼叫 [**IWMInputMediaProps：： GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname)，以抓取與輸入編號對應的連接名稱。 連接名稱之後，您就知道與寫入器指派的輸入編號相關聯的資料流程。

下列程式碼範例會顯示每個輸入的連接名稱。 如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。


```C++
HRESULT GetNamesForInputs(IWMWriter* pWriter)
{
    DWORD    cInputs  = 0;
    HRESULT  hr       = S_OK;
    WCHAR*   pwszName = NULL;
    WORD     cchName  = 0;

    IWMInputMediaProps* pProps = NULL;

    // Get the total number of inputs for the file.
    hr = pWriter->GetInputCount(&cInputs);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all supported inputs.
    for (DWORD inputIndex = 0; inputIndex < cInputs; inputIndex++)
    {
        // Get the input properties for the input.
        hr = pWriter->GetInputProps(inputIndex, &pProps);  
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size of the connection name.
        hr = pProps->GetConnectionName(0, &cchName);
        GOTO_EXIT_IF_FAILED(hr);

        if (cchName > 0)
        {
            // Allocate memory for the connection name.
            pwszName = new WCHAR[cchName];
            if (wszName == NULL)
            {
                hr = E_OUTOFMEMORY;
                goto Exit;
            }

            // Get the connection name.
            hr = pProps->GetConnectionName(pwszName, &cchName);
            GOTO_EXIT_IF_FAILED(hr);
            
            // Display the name.
            printf("Input # %d = %S\n", pwszName);
        } // end if

        // Clean up for next iteration.
        SAFE_ARRAY_DELETE(pwszName);
        SAFE_RELEASE(pProps);
    } // end for inputIndex

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_RELEASE(pProps);
    return hr;
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMWriter 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 





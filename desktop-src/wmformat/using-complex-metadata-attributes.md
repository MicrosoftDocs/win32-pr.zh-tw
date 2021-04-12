---
title: 使用複雜的中繼資料屬性
description: 使用複雜的中繼資料屬性
ms.assetid: 8269efe4-331f-4b4b-b888-66b45c638153
keywords:
- Windows Media Format SDK，複雜的中繼資料屬性
- Advanced Systems Format (ASF) 、複雜的中繼資料屬性
- ASF (Advanced Systems Format) ，複雜的中繼資料屬性
- 中繼資料、複雜屬性
- 複雜的中繼資料屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cd03c656a8cba5342d21e41932365455daa8bfa
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314280"
---
# <a name="using-complex-metadata-attributes"></a>使用複雜的中繼資料屬性

Windows Media Format SDK 支援複雜的中繼資料屬性，這些屬性是具有以結構表示之值的屬性。 由於所有屬性都必須在 [**WMT \_ ATTR \_ 資料**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) 類型列舉中定義資料類型，因此所有複雜的中繼資料屬性都會被視為 **WMT \_ 類型的 \_ 二進位**。 撰寫複雜屬性時，請將結構的指標轉換為位元組指標。 當您取出複雜屬性時，請將 [**IWMHeaderInfo3：： GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) 所設定的位元組陣列轉換為適當的結構。

下列程式碼範例示範如何設定和取出複雜的中繼資料屬性。 第一個函式會新增使用者的 text 屬性，第二個函式會抓取一個。 如需如何使用這些範例的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。


```C++
HRESULT AddText(IWMHeaderInfo3* pHeaderInfo, 
                WCHAR* pwszDesc, 
                WCHAR* pwszText, 
                WORD* pwIndex)
{
    HRESULT hr         = S_OK;
    WORD    wIndex     = 0;
    
    WM_USER_TEXT textStruct;
    
    // Populate the text structure.
    textStruct.pwszDescription = pwszDesc;
    textStruct.pwszText = pwszText;

    // Add the attribute.
    hr = pHeaderInfo->AddAttribute(0, 
                                   g_wszWMText, 
                                   &wIndex, 
                                   WMT_TYPE_BINARY, 
                                   0, 
                                   (BYTE*)&textStruct, 
                                   sizeof(WM_USER_TEXT));

    // Pass the index of the text attribute back to the caller.
    if(SUCCEEDED(hr))
    {
        *pwIndex = wIndex;
    }
    
    return hr;
}

HRESULT DisplayText(IWMHeaderInfo3* pHeaderInfo, WORD wIndex)
{
    HRESULT hr = S_OK;

    WCHAR*  pwszName = NULL;
    WORD    cchName  = 0;
    WORD    Language = 0;
    BYTE*   pbValue  = NULL;
    DWORD   cbValue  = 0;
    

    WM_USER_TEXT*     pText    = NULL;
    WMT_ATTR_DATATYPE AttType;

    
    // Find the lengths of the attribute name and value.
    hr = pHeaderInfo->GetAttributeByIndexEx(0, 
                                            wIndex, 
                                            NULL, 
                                            &cchName, 
                                            NULL, 
                                            NULL, 
                                            NULL, 
                                            &cbValue);
    GOTO_EXIT_IF_FAILED(hr);

    // Allocate memory for the name and value.
    pwszName = new WCHAR[cchName];
    pbValue  = new BYTE[cbValue];
    
    if(pwszName == NULL || pbValue == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit;
    }

    // Get the attribute.
    hr = pHeaderInfo->GetAttributeByIndexEx(0, 
                                            wIndex, 
                                            pwszName, 
                                            &cchName, 
                                            &AttType, 
                                            &Language, 
                                            pbValue, 
                                            &cbValue);
    GOTO_EXIT_IF_FAILED(hr);

    // Make sure the attribute is WM/Text, as expected.
    if(wcscmp(pwszName, g_wszWMText))
    {
        // Somehow we got the wrong attribute.
        hr = E_UNEXPECTED;
        goto Exit;
    }

    // Set the structure pointer to the retrieved value.
    pText = (WM_USER_TEXT*) pbValue;

    // Print the strings from the structure.
    printf("Description : %S\n", pText->pwszDescription);
    printf("Text        : %S\n", pText->pwszText);

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_ARRAY_DELETE(pbValue);
    return hr;
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用中繼資料**](working-with-metadata.md)
</dt> </dl>

 

 





---
title: 取得檔案中的所有中繼資料
description: 取得檔案中的所有中繼資料
ms.assetid: c1de58d7-25a8-4416-9ee9-6ebe641ed640
keywords:
- Windows媒體格式 SDK，正在抓取中繼資料
- Advanced Systems Format (ASF) ，正在抓取中繼資料
- ASF (Advanced Systems Format) ，正在抓取中繼資料
- 中繼資料，全部取回
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fab81f151cbb661cc7769128e2d4371dd0b24869317d1888769ed66a60de86f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807468"
---
# <a name="to-retrieve-all-metadata-in-a-file"></a>取得檔案中的所有中繼資料

下列程式碼範例是一個函式，它會顯示檔案中的所有中繼資料。 若要使用函式，您必須將指標傳遞至中繼資料編輯器物件、讀取器物件、同步讀取器物件或寫入器物件的 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) 介面。 您也必須在專案中的某處包含 Stdio.h 標頭檔。 如需如何使用此範例的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。

為了清楚起見，此範例不會顯示 binary 和 GUID 屬性的值。 針對二進位屬性，您應該檢查屬性名稱是否符合任何已知的複雜中繼資料屬性。 如果有的話，您應該根據用於該屬性的結構來格式化輸出。 同樣地，GUID 屬性值也可以用數種方式來顯示。 您可以選擇一次顯示一個結構的每個成員，或是將結構轉換成字串，並將它顯示為一個值。


```C++
HRESULT ShowAllAttributes(IWMHeaderInfo3* pHeaderInfo)
{
    HRESULT hr          = S_OK;
    
    WORD    cAttributes = 0;
    WCHAR*  pwszName    = NULL;
    WORD    cchName     = 0;
    BYTE*   pbValue     = NULL;
    DWORD   cbValue     = 0;
    WORD    langIndex   = 0;
    WORD    attIndex    = 0;

    WMT_ATTR_DATATYPE attType;

    // Get the total number of attributes in the file.

    hr = pHeaderInfo->GetAttributeCountEx(0xFFFF, &cAttributes);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all the attributes, retrieving and displaying each.

    for(attIndex = 0; attIndex < cAttributes; attIndex++)
    {
        // Get the required buffer lengths for the name and value.

        hr = pHeaderInfo->GetAttributeByIndexEx(0xFFFF,
                                                attIndex,
                                                NULL,
                                                &cchName,
                                                NULL,
                                                NULL,
                                                NULL,
                                                &cbValue);
        GOTO_EXIT_IF_FAILED(hr);

        // Allocate the buffers.

        pwszName = new WCHAR[cchName];
        if(pwszName == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }

        pbValue = new BYTE[cbValue];
        if(pbValue == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }

        // Get the attribute.

        hr = pHeaderInfo->GetAttributeByIndexEx(0xFFFF,
                                                attIndex,
                                                pwszName,
                                                &cchName,
                                                &attType,
                                                &langIndex,
                                                pbValue,
                                                &cbValue);
        GOTO_EXIT_IF_FAILED(hr);

        // Display the attribute global index and name.

        printf("%3d - %S (Language %d):\n\t ", attIndex, pwszName, langIndex);

        // Display the attribute depending upon type.

        switch(attType)
        {
        case WMT_TYPE_DWORD:
        case WMT_TYPE_QWORD:
        case WMT_TYPE_WORD:
            printf("%d\n\n", (DWORD) *pbValue);
            break;
        case WMT_TYPE_STRING:
            printf("%S\n\n", (WCHAR*) pbValue);
            break;
        case WMT_TYPE_BINARY:
            printf("<binary value>\n\n");
            break;
        case WMT_TYPE_BOOL:
            printf("%s\n\n", ((BOOL) *pbValue == TRUE) ? "True" : "False");
            break;
        case WMT_TYPE_GUID:
            printf("<GUID value>\n\n", (DWORD) *pbValue);
            break;
        }

        // Release allocated memory for the next pass.

        SAFE_ARRAY_DELETE(pwszName);
        SAFE_ARRAY_DELETE(pbValue);
        cchName = 0;
        cbValue = 0;
    } // End for attIndex.

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_ARRAY_DELETE(pbValue);
    return hr;
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**正在抓取中繼資料屬性**](retrieving-metadata-attributes.md)
</dt> </dl>

 

 





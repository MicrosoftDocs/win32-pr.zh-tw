---
description: 指定語言識別項清單，指定 Advanced Systems 格式所包含的語言 (ASF) 檔。 這個屬性會對應至在 ASF 規格中定義的語言清單物件。
ms.assetid: 07b8a991-b392-47c1-a6d7-a1f5dcc82e5c
title: 'MF_PD_ASF_LANGLIST 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba22004001df2ba6be8fb7a173a3ea9bed1b0a73863ae111e61d36efa853e079
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119103700"
---
# <a name="mf_pd_asf_langlist-attribute"></a>MF \_ PD \_ ASF \_ LANGLIST 屬性

指定語言識別項清單，指定 Advanced Systems 格式所包含的語言 (ASF) 檔。 這個屬性會對應至在 ASF 規格中定義的語言清單物件。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

此屬性適用于 ASF 內容的表示描述項。

[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會建立展示描述項，並從語言清單物件標頭產生這個屬性。 下表顯示 blob 的格式：



| 語言清單物件欄位 | 資料類型    | 大小    | 描述                            |
|----------------------------|--------------|---------|----------------------------------------|
| 語言識別項記錄計數  | **DWORD**    | 4 個位元組 | 語言數目                    |
| 語言識別項記錄        | **位元組**\[\] | 不定  | 語言字串的陣列 (請參閱下面的) 。 |



 

第一個 **DWORD** 是語言的數目，後面接著語言識別項字串的陣列。 每個字串的格式如下：



| 語言清單物件欄位 | 資料類型     | 大小    | 描述                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| 語言識別項長度         | **DWORD**     | 4 個位元組 | 字串的長度（以位元組為單位），包括尾端 **Null** 字元的大小。 |
| 語言識別碼                | **WCHAR**\[\] | 不定  | 以 null 終止的字串，包含 RFC 1766 語言名稱。                           |



 

每個字串都是符合 RFC 1766 的語言標記。

若要取得 ASF 檔案中特定資料流程的語言標記，請查詢適用于 [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ 語言 \_ 識別碼 \_ 索引**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) 屬性的資料流程描述元。

## <a name="examples"></a>範例

下列範例顯示如何剖析語言清單。


```C++
class LanguageList
{
private:
    UINT8   *pRawList;          // Unparsed blob
    UINT32  cbList;             // Size of the blob, in bytes
    DWORD   cLangs;             // Number of languages
    WCHAR   **ppszLanguages;    // Array of pointers to strings.
                                // These are pointers into pRawList.
public:
    LanguageList() : 
        pRawList(NULL), cbList(0), ppszLanguages(NULL), cLangs(0)
    {
    }
    ~LanguageList()
    {
        Clear();
    }

    // Clear: Clears the list.
    void Clear()
    {
        CoTaskMemFree(pRawList);
        cbList = 0;
        cLangs = 0;
        delete [] ppszLanguages;

        ppszLanguages = NULL;
    }

    // GetCount: Returns the number of languages.
    DWORD GetCount() const { return cLangs; }

    // GetLanguage: Return the i'th string in the list.
    const WCHAR* GetLanguage(DWORD i)
    {
        if (i >= cLangs)
        {
            return NULL;
        }
        return ppszLanguages[i];
    }

    // Initialize: Get the language list, if specified, and parse it.
    HRESULT Initialize(IMFPresentationDescriptor *pPD)
    {
        if (pPD == NULL)
        {
            return E_POINTER;
        }
        Clear();

        HRESULT hr = pPD->GetAllocatedBlob(
            MF_PD_ASF_LANGLIST, &pRawList, &cbList);

        if (FAILED(hr))
        {
            goto done;
        }


        // Parse the language blob.

        // Record count.
        if (cbList < sizeof(DWORD))
        {
            hr = E_FAIL;
            goto done;
        }

        cLangs = ((DWORD*)pRawList)[0];

        // Allocate an array of pointers to language strings.
        ppszLanguages = new (std::nothrow) WCHAR*[cLangs];
        if (ppszLanguages == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto done;
        }
        ZeroMemory(ppszLanguages, cLangs * sizeof(WCHAR*));

        BYTE *pNext = pRawList + sizeof(DWORD); // Next byte.
        BYTE *pEnd = pRawList + cbList;         // End of the blob.

        for (DWORD i = 0; i < cLangs; i++)
        {
            if (pNext > pEnd - sizeof(DWORD))
            {
                hr = E_FAIL;
                goto done;
            }

            // Language ID length
            DWORD cbStr = ((DWORD*)pNext)[0];
            pNext += sizeof(DWORD);

            // Calculate the pointer to the language ID string.
            if ((cbStr > (size_t)(pEnd - pNext)) ||
                (cbStr < sizeof(WCHAR)) || 
                (cbStr % sizeof(WCHAR) != 0))
            {
                hr = E_FAIL;
                goto done;
            }

            ppszLanguages[i] = (WCHAR*)pNext;

            // Verify the string is NULL-terminated.
            if (ppszLanguages[i][(cbStr / sizeof(WCHAR)) - 1] != L'\0')
            {
                hr = E_FAIL;
                goto done;
            }
            pNext += cbStr;
        }

done:
        if (FAILED(hr))
        {
            Clear();
        }

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // There was no language list attribute in the PD.
            // This is not a failure case.
            hr = S_OK;  
        }
        return hr;
    }

private:
    LanguageList(const LanguageList& lang);
    LanguageList& operator=(const LanguageList& lang);
};
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Wmcontainer。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF 標頭物件](asf-file-structure.md)
</dt> <dt>

ASF 標頭物件
</dt> <dt>

[簡報描述項](presentation-descriptors.md)
</dt> </dl>

 

 





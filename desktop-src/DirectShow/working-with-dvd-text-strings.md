---
description: 使用 DVD 文字字串
ms.assetid: 6d415ebb-5cd0-4631-9404-f2ebabef2476
title: 使用 DVD 文字字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d04a786e46c795f028edbe2b955e71715aaefb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997102"
---
# <a name="working-with-dvd-text-strings"></a>使用 DVD 文字字串

某些 DVD 光碟（尤其是卡拉卡拉）可能包含文字字串清單來補充影片或音訊內容。 這些文字字串包含內容的相關中繼資料，例如歌曲標題、演出者名稱、內容類型資訊等等。 文字字串可以存在於一種以上的語言中。 這些字串是選擇性的，而許多光碟都沒有它們。

若要從 DVD 取出文字字串，請使用 [dvd 導覽器](dvd-navigator-filter.md)所公開的 [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)介面。 您實際上不需要建立 DVD 播放圖形來取出文字字串。 您可以直接建立 DVD Navigator、設定 DVD 音量，然後呼叫相關的文字字串方法：



| 方法                                                                                  | 描述                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDvdInfo2::GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) | 取得包含文字字串的語言數目。                                                                                                                                  |
| [**IDvdInfo2::GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo)           | 取得一種語言之文字字串的相關資訊。                                                                                                                                       |
| [**IDvdInfo2::GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)     | 依索引取得指定之語言的文字字串。                                                                                                                                          |
| [**IDvdInfo2::GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)       | 取得文字字串做為原始位元組陣列。 如果文字字串使用 [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)不支援的字元編碼，請使用這個方法。 |



 

以下是取得文字字串的基本程式：

1.  呼叫 [**IDvdInfo2：： GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) ，以尋找文字字串出現的總語言數。 如果數位為零，則表示 DVD 沒有任何文字字串。  (這可能是最常見的情況，也就是最常見的情況。 ) 
2.  如果語言的數目至少為一個，請呼叫 [**IDvdInfo2：： GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) 來取得每個語言的相關資訊。 此語言是以索引指定。 方法會傳回該語言中的文字字串總數、語言的地區設定識別碼 (**LCID**) ，以及字元編碼 (Unicode 或其他) 。 DVD 文字字串可以使用數個不同的字元集;這些會列在 [**DVD \_ TextCharSet 列舉**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset)中。
3.  若要取得文字字串，請呼叫 [**IDvdInfo2：： GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) 或 [**IDvdInfo2：： GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)。 第一個方法會傳回寬字元字串，但不支援每個字元集。 第二個方法會傳回包含原始文字資料的位元組陣列。 針對這兩種方法，您可以使用 **Null** 緩衝區指標來呼叫方法，以找出字串的大小和文字類型。 接著配置緩衝區，並再次呼叫方法以取得字串。

每個文字字串都有相關聯的識別碼代碼，表示文字字串的意義。 此識別碼會以 [**DVD \_ TextStringType**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) 值的形式傳回。 有兩種類別的識別碼： *結構識別碼* 和 *內容識別碼*。 結構識別碼的數值代碼範圍為0x00 –0x02F。 內容識別碼的範圍為0x30< 和更高。  (**DVD \_ TextStringType** 列舉會定義最常見識別碼的子集，但 [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) 方法可以傳回任何識別碼代碼。 ) 結構識別碼描述 DVD 的邏輯部分，例如音量、標題或標題的一部分 (platform ptt) 。 內容識別碼表示特定文字字串的意義，例如電影標題、歌曲標題或內容類型。

結構識別碼沒有相關聯的文字字串。 當結構識別碼出現在文字字串資料中時，它會指出下列文字字串會套用至 DVD 的該邏輯部分，直到下一個結構識別碼為止。 文字資料中結構識別碼的位置會對應至 DVD 磁片區的邏輯階層。 例如，第一次出現的 DVD \_ 結構 \_ 標題識別碼 (0x02) 代表磁片區中的第一個標題，而下一個出現專案代表第二個標題。

下表說明如何針對有兩個標題的 DVD 定義文字字串。



| DVD \_ TextStringType        | 文字字串  | Description                                    |
|----------------------------|--------------|------------------------------------------------|
| DVD \_ 結構 \_ 磁片區 (0x01)  | ""           | 整個光碟端的結構識別碼。 |
| DVD \_ 一般 \_ 名稱 (0x30<)   | 「DVD 音量」 | DVD 磁片區名稱。                               |
| DVD \_ 結構 \_ 標題 (0x02)   | ""           | 第一個標題的結構識別碼。      |
| DVD \_ 一般 \_ 名稱 (0x30<)   | "Title 1"    | 第一個標題的名稱。                       |
| DVD \_ 結構 \_ 標題 (0x02)   | ""           | 第二個標題的結構識別碼。     |
| DVD \_ 一般 \_ 名稱 (0x30<)   | "Title 2"    | 第二個標題的名稱。                      |



 

[**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)和 [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)方法會將結構識別碼和內容識別碼視為相同。 唯一的差別在於，在結構識別碼中，相關聯的文字緩衝區是空的。 應用程式會負責追蹤文字字串與 DVD 邏輯部分之間的關聯性。

下列範例顯示如何從 DVD 取得文字字串。 此範例會忽略實際應用程式需要的一些詳細資料。  (例如，它會忽略結構識別碼。 ) 此範例只會顯示正確的呼叫順序。


```C++
#define CHECK_HR(hr) if (FAILED(hr)) { goto done; }
#define SAFE_ARRAY_DELETE(x) { if (x != NULL) { delete [] x; x = NULL; } }

HRESULT GetDVDTextStrings()
{
    HRESULT hr = S_OK;
    ULONG cLangs = 0;       // Number of languages.
    ULONG cStrings = 0;     // Number of text strings.
    ULONG cchBuffer = 0;    // Buffer size.
    ULONG cchActual = 0;    // Actual string size.

    LCID lcid;              // Locale identifier.
    DVD_TextCharSet     characterSet;
    DVD_TextStringType  stringType;

    WCHAR *pszBuffer = NULL;

    CComPtr<IBaseFilter> pFilter;
    CComPtr<IDvdInfo2> pInfo;
    CComPtr<IDvdControl2> pControl;

    // Set up the DVD Navigator.
    CHECK_HR(hr = pFilter.CoCreateInstance(CLSID_DVDNavigator));
    CHECK_HR(hr = pFilter.QueryInterface(&pInfo));
    CHECK_HR(hr = pFilter.QueryInterface(&pControl));
    CHECK_HR(hr = pControl->SetDVDDirectory(NULL));

    // Find the number of text-string languages.
    CHECK_HR(hr = pInfo->GetDVDTextNumberOfLanguages(&cLangs));
    if (cLangs == 0)
    {
        return S_FALSE; // No text strings.
    }

    // Get information about the 0'th language.
    CHECK_HR(hr = pInfo->GetDVDTextLanguageInfo(
        0, &cStrings, &lcid, &characterSet));

    // First check if this character set is compatible with the 
    // GetDVDTextStringAsUnicode method.

    if (characterSet == DVD_CharSet_Unicode || 
        characterSet == DVD_CharSet_ISO646)
    {
        // Loop through all of the strings.
        for (ULONG i = 0; i < cStrings; i++)
        {
            // Get the i'th string for the 0'th language.

            // Find the required buffer size and the string type.
            CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                0,            // Language index.
                i,            // String index.
                NULL,         // Pass NULL pointer to get the buffer size.
                0,            // Size of the buffer we are passing in.
                &cchBuffer,   // Receives the required buffer size.
                &stringType   // Receives the identifier code.
                ));

            // Skip structure identifiers (0x00 - 0x2F).
            if ((cchBuffer > 0) && (stringType >= 0x30))
            {
                // Allocate a buffer and get the text string.
                pszBuffer = new WCHAR[cchBuffer];
                if (pszBuffer == NULL)
                {
                    CHECK_HR(hr = E_OUTOFMEMORY);
                }

                CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                    0, i, pszBuffer, cchBuffer, &cchActual, &stringType));

                // TODO: Display the text string.

                SAFE_ARRAY_DELETE(pszBuffer);
            }
        }
    }

done:
    SAFE_ARRAY_DELETE(pszBuffer);
    return hr;
}
```



如需 DVD 文字字串的詳細資訊，請參閱 [Dvd 論壇的網站](https://go.microsoft.com/fwlink/?LinkId=8677)。

DVDSample 應用程式中的 **CDvdCore：： GetDvdText** 方法會示範列舉和顯示 DVD 文字字串的基本步驟。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> </dl>

 

 




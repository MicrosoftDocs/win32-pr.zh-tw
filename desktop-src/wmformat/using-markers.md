---
title: 使用標記
description: 使用標記
ms.assetid: b801c985-4ec7-441e-9f8a-40c69b1299a9
keywords:
- Windows Media Format SDK，標記
- Advanced Systems Format (ASF) ，標記
- ASF (Advanced Systems Format) ，標記
- Advanced Systems Format (ASF) ，搜尋標記
- ASF (Advanced Systems Format) ，搜尋標記
- 標記，關於
- 標記，加入
- 標記，移除
- 標記，正在抓取
- 標記，搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cc585b8c71e3bfbae85953650809ad031d36a2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103681561"
---
# <a name="using-markers"></a>使用標記

*標記* 是 ASF 檔案內的命名點。 每個標記都是由名稱和相關聯的時間所組成，其測量方式為從檔案開頭算起的位移。 應用程式可以使用標記，將名稱指派給內容內的不同點，將這些名稱顯示給使用者，然後搜尋標記位置。 應用程式可以從現有的 ASF 檔案新增或移除標記。

[**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)介面包含使用標記的方法。 中繼資料編輯器物件支援加入和移除標記。 寫入器和讀取器物件可以取出標記，但無法新增或移除標記。

## <a name="adding-markers"></a>新增標記

若要加入標記，請查詢 **IWMHeaderInfo** 介面的中繼資料編輯器。 然後呼叫 [**IWMHeaderInfo：： AddMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) 方法，將標記名稱指定為寬字元字串，並將時間指定為 100-毫微秒單位。 時間不得超過檔案持續時間。 兩個標記可以有相同的時間。

下列範例會將數個標記新增至檔案：


```C++
IWMMetadataEditor *pEdit = 0;
IWMHeaderInfo     *pInfo = 0;

// Create the metadata editor object.

WMCreateEditor(&pEdit);
pEdit->Open(L"C:\\example.wmv");
pEdit->QueryInterface(IID_IWMHeaderInfo, (void**)&pInfo);

// Add the markers. Note that we add the last ones first. Do this when possible
// for improved performance when writing the markers to the file.
hr = pInfo->AddMarker(L"End",  520000000);   // 52 sec.
hr = pInfo->AddMarker(L"Segue",  350000000); // 35 sec.
hr = pInfo->AddMarker(L"Intro",  15000000);  // 1.5 sec.

// Commit changes and clean up.

pEdit->Flush();
pEdit->Close(); 
pInfo->Release();
pEdit->Release();

```



## <a name="removing-markers"></a>移除標記

若要移除標記，請呼叫 [**IWMHeaderInfo：： RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker)，並指定要移除之標記的索引。 標記會自動依遞增的時間順序排序，因此索引0一律是第一個標記。 請注意，呼叫 **RemoveMarker** 會變更後面任何標記的索引編號。 下列程式碼，其中 *pInfo* 是 **IWMHeaderInfo** 介面的指標，會從檔案中移除所有標記：


```C++
WORD count = 0;
pInfo->GetMarkerCount(&count);
while (count--)
{
    pInfo->RemoveMarker(0);
}

```



## <a name="retrieving-markers"></a>正在抓取標記

若要取出標記的名稱和時間，請執行下列步驟：

1.  呼叫 [**IWMHeaderInfo：： GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) 方法，以判斷檔案包含多少個標記。
2.  取得包含標記名稱所需的字串大小。 若要這樣做，請呼叫 [**IWMHeaderInfo：： GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) 方法。 指定要抓取之標記的索引，並在 *pwszMarkerName* 參數)  (字串緩衝區的 **Null** 。 方法會在 PcchMarkerNameLen 參數中傳回字串的長度，包括結尾的 ' \\ 0 ' 字元。 
3.  配置寬字元字串以接收名稱。
4.  再次呼叫 **GetMarker** ，但這次在 *pwszMarkerName* 參數中傳遞字串的位址。 方法會將標記名稱寫入字串中，並傳回 *pcnsMarkerTime* 參數中的標記時間。

下列程式碼會依序執行每個標記的迴圈，並抓取名稱和時間：


```C++
WORD cMarkers = 0;
HRESULT hr = pInfo->GetMarkerCount(&cMarkers);

WCHAR *wszName = 0;
WORD  len = 0;
for (WORD iMarker = 0; iMarker < cMarkers; ++iMarker)
{
    QWORD rtTime = 0;
    WORD req_len = 0;
    hr = pInfo->GetMarker(iMarker, 0, &req_len, &rtTime);
    
    // Reallocate if necessary.
    if (len < req_len)
    {
        delete[] wszName;
        wszName = new WCHAR[req_len];
        len = req_len;
    }
    hr = pInfo->GetMarker(iMarker, wszName, &req_len, &rtTime);
    // Display the name...
}
delete[] wszName;

```



## <a name="seeking-to-a-marker"></a>搜尋標記

若要從標記位置開始播放，請呼叫 reader 物件的 [**IWMReaderAdvanced2：： StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) 方法，並指定標記的索引。 其餘的參數與 [**IWMReader：： Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) 方法的參數相同。 下列範例會查詢 [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) 介面的讀取器，並搜尋第一個標記。


```C++
IWMReaderAdvanced2 *pReader2 = 0
WORD iMarkerIndex = 0;
hr = pReader->QueryInterface(IID_IWMReaderAdvanced2, (void**)&pReader2);
if (SUCCEEDED(hr))
{
    hr = pPlayer2->StartAtMarker(iMarkerIndex, 0, 1.0, 0);
    pPlayer2->Release();
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMHeaderInfo 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)
</dt> <dt>

[**使用中繼資料**](working-with-metadata.md)
</dt> </dl>

 

 





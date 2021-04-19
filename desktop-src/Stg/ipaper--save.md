---
title: IPaper 儲存
description: 此範例程式碼中的主要焦點是 COPaper 可以如何載入並將其紙張資料儲存在複合檔案中。 詳細討論 IPaper、載入和儲存方法的執行。
ms.assetid: 62154658-ff47-425f-94da-ee2806de5318
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ea49f194e64ab3f0cfd78569b1e6ff9ddee577
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965187"
---
# <a name="ipapersave"></a>IPaper：： Save

此範例程式碼中的主要焦點是 COPaper 可以如何載入並將其紙張資料儲存在複合檔案中。 詳細討論 [**IPaper**](ipaper-methods.md)、 [**載入**](ipaper--load.md)和 **儲存** 方法的執行。

以下是從 .cpp **IPaper：： Save** 方法。


```C++
STDMETHODIMP COPaper::CImpIPaper::Save(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    ULONG ulToWrite, ulWritten;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
        // Use the COM service to mark this compound file as one 
        // that is handled by our server component, DllPaper.
        WriteClassStg(pIStorage, CLSID_DllPaper);

        // Use the COM Service to write user-readable clipboard 
        // format into the compound file.
        WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, 
                            TEXT(CLIPBDFMT_STR));

        // Create the stream to be used for the actual paper data.
        // Call it "PAPERDATA".
        hr = pIStorage->CreateStream(
               STREAM_PAPERDATA_USTR,
        STGM_CREATE | STGM_WRITE | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained a stream. Write data to it.
          // First, write PAPER_PROPERTIES structure.
          m_PaperProperties.lInkArraySize = m_lInkDataEnd+1;
          m_PaperProperties.crWinColor = m_crWinColor;
          m_PaperProperties.WinRect.right = m_WinRect.right;
          m_PaperProperties.WinRect.bottom = m_WinRect.bottom;
          ulToWrite = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Write(&m_Paper_Properties, ulToWrite, 
                               &ulWritten);
          if (SUCCEEDED(hr) && ulToWrite != ulWritten)
            hr = STG_E_CANTSAVE;
          if (SUCCEEDED(hr))
          {
            // Now, write the complete array of Ink Data.
            ulToWrite = m_PaperProperties.lInkArraySize * 
                                                     sizeof(INKDATA);
            hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
            if (SUCCEEDED(hr) && ulToWrite != ulWritten)
              hr = STG_E_CANTSAVE;
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify all other connected clients that Paper is now saved.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_SAVED, 0, 0, 0, 0);

    return hr;
  }
```



在此用戶端和伺服器關聯性中，COPaper 不會建立用來儲存紙張資料的複合檔案。 針對 **儲存** 和 [**載入**](ipaper--load.md) 方法，用戶端會針對現有的複合檔案傳遞 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面指標。 然後，它會使用 **IStorage** 來寫入和讀取該複合檔案中的資料。 在 **IPaper：： Save** 上方，儲存了數種類型的資料。

DllPaper、CLSID DllPaper 的 CLSID \_ 會序列化，並儲存在名為 "001CompObj" 的儲存物件內的特殊 COM 控制資料流程中 \\ 。 [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg)服務函數會執行此儲存體。 此儲存的 CLSID 資料可以用來將儲存體內容與所建立的 DllPaper 元件產生關聯，並可加以解讀。 在此範例中，根儲存體是由 **StoClien** 傳遞，因此整個複合檔案會與 DllPaper 元件相關聯。 您稍後可以使用 [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) 服務函式的呼叫來取出此 CLSID 資料。

由於 DllPaper 會處理可編輯的資料，因此也適合在儲存體中記錄剪貼簿格式。 呼叫 [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) 服務函式來儲存剪貼簿格式指定和使用者可讀取的格式名稱。 使用者可讀取的名稱適用于在挑選清單中顯示 GUI。 以上傳遞的名稱會使用 CLIPBDFMT STR 的宏， \_ 在檔中定義為 "DllPaper 1.0"。 此儲存的剪貼簿資料可以在稍後透過呼叫服務函式 [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg)來取出。 此函數會傳回使用工作記憶體配置器所配置的字串值。 呼叫端負責釋放字串。

**[下一** 步] 會在儲存體中為 COPaper 的紙張資料建立資料流程。 資料流程稱為 "DATA"，並使用 STREAM \_ data \_ USTR 宏傳遞。 [**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)方法要求這個字串必須是 Unicode。 因為字串是在編譯時期固定的，所以宏在 Paper 中會定義為 Unicode。

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

字串前面的 ' L ' （指出 LONG）會達到這個條件。

[**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)方法會在指定的儲存體內建立並開啟資料流程。 新資料流程的 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 介面指標會在呼叫端介面指標變數中傳遞。 在 **CreateStream** 中的這個介面指標上呼叫 AddRef，呼叫端必須在使用後釋放此指標。 **CreateStream** 方法會傳遞給許多存取模式旗標，如下所示。

STGM \_ CREATE \| STGM \_ WRITE \| STGM \_ DIRECT \| STGM \_ SHARE \_ EXCLUSIVE

[**STGM \_CREATE**](stgm-constants.md) 會建立新的資料流程，或覆寫現有的相同名稱。 [**STGM \_寫入**](stgm-constants.md) 會開啟具有寫入權限的資料流程。 [**STGM \_直接**](stgm-constants.md) 開啟串流以進行直接存取，而非交易存取。 [**STGM \_共用 \_ 獨佔**](stgm-constants.md) 會開啟檔案，以供呼叫端獨佔、非共用使用。

順利建立 DATA 資料流程之後，會使用 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 介面寫入資料流程。 **IStream：： Write** 方法是用來先儲存紙張 \_ 屬性結構的內容。 這基本上是資料流程前端的屬性標頭。 因為版本號碼是檔案中的第一個專案，所以可以獨立讀取，以決定如何處理接下來的資料。 如果實際寫入的資料量不等於所要求的數量，儲存方法會中止，並傳回 STG. \_ E \_ CANTSAVE。

將筆跡資料的整個陣列儲存至資料流程很簡單。


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



由於 [**IStream：： Write**](/windows/desktop/api/Objidl/nn-objidl-istream) 方法會在位元組陣列上運作，因此會計算陣列中儲存的筆墨資料位元組數目，並且在陣列的開頭開始寫入作業。 如果實際寫入的資料量不等於所要求的數量， **Save** 方法會傳回 Stg. \_ E \_ CANTSAVE。

寫入資料流程之後， **IPaper：： Save** 方法會釋放它所使用的 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 指標。

**Save** 方法也會在 COPaper 內部 NotifySinks 方法中呼叫用戶端 [**IPaperSink**](ipapersink-methods.md) (，) 通知用戶端儲存作業已完成。 此時 **Save** 方法會傳回呼叫用戶端，這通常會釋放 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 指標。

 

 





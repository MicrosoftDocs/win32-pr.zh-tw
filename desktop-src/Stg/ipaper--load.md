---
title: IPaper 載入
description: 下列 c + + 程式碼範例示範如何在儲存體中開啟現有的資料流程、讀取中的新紙張屬性，然後將它們設定為目前的 COPaper 值。
ms.assetid: a1559d97-387f-4d1a-8a9d-fa5c27abd545
keywords:
- IPaper 載入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b5f16b8fe649d08226b2cff5a4b1a5234bddb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932450"
---
# <a name="ipaperload"></a>IPaper：： Load

下列 c + + 程式碼範例示範如何在儲存體中開啟現有的資料流程、讀取中的新紙張屬性，然後將它們設定為目前的 COPaper 值。

以下是來自 .cpp 的 **IPaper：： Load** 方法。


```
STDMETHODIMP COPaper::CImpIPaper::Load(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    INKDATA* paInkData;
    ULONG ulToRead, ulReadIn;
    LONG lNewArraySize;
    PAPER_PROPERTIES NewProps;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
       // Open the "PAPERDATA" stream where the paper data is stored.
        hr = pIStorage->OpenStream(
               STREAM_PAPERDATA_USTR,
               0,
               STGM_READ | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained paper data stream. Read the Paper Properties.
          ulToRead = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Read(
                           &NewProps,
                           ulToRead,
                           &ulReadIn);
          if (SUCCEEDED(hr) && ulToRead != ulReadIn)
            hr = E_FAIL;
          if (SUCCEEDED(hr))
          {
            // Handle the different versions of ink data format.
            switch (NewProps.lInkDataVersion)
            {
              case INKDATA_VERSION10:
                // Allocate an ample-sized ink data array.
                lNewArraySize = NewProps.lInkArraySize + 
                                               INKDATA_ALLOC;
                paInkData = new INKDATA[(LONG) lNewArraySize];
                if (NULL != paInkData)
                {
                  // Delete the old ink data array.
                  delete [] m_paInkData;

                  // Assign the new array.
                  m_paInkData = paInkData;
                  m_lInkDataMax = lNewArraySize;

                  // Read the complete array of Ink Data.
                  ulToRead = NewProps.lInkArraySize * sizeof(INKDATA);
                  hr = pIStream->Read(m_paInkData, 
                                      ulToRead, &ulReadIn);
                  if (SUCCEEDED(hr) && ulToRead != ulReadIn)
                    hr = E_FAIL;
                  if (SUCCEEDED(hr))
                  {
                    // Set COPaper to use the new PAPER_PROPERTIES
                    // data.
                    m_lInkDataEnd = NewProps.lInkArraySize-1;
                    m_crWinColor = NewProps.crWinColor;
                    m_WinRect.right = NewProps.WinRect.right;
                    m_WinRect.bottom = NewProps.WinRect.bottom;

                    // Copy the new properties into current 
                    // properties.
                    memcpy(
                      &m_PaperProperties,
                      &NewProps,
                      sizeof(PAPER_PROPERTIES));
                  }
                }
                else
                  hr = E_OUTOFMEMORY;
                break;
              default:
                hr = E_FAIL;  // Bad version.
                break;
            }
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify other connected clients that Paper is now loaded.
    // If Paper not loaded, then erase to a safe, empty ink data 
    // array.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_LOADED, 0, 0, 0, 0);
    else
      Erase(nLockKey);

    return hr;
  }
```



現在，會呼叫 [**IStorage：： OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) 方法，在名為 "data" 的儲存體中開啟現有的資料流程。 存取模式旗標適用于唯讀、直接及非共用的獨佔存取權。 當資料流程開啟時，會呼叫 [**IStream：： read**](/windows/desktop/api/Objidl/nn-objidl-istream) 方法以讀取紙張 \_ 屬性結構。 如果實際讀取的數量不等於所要求的數量，則會中止載入作業，並 \_ 傳回 E 失敗。 如果無法辨識新的 [檔] 屬性中的格式版本 \_ ，載入作業就會中止，且 **load** 會傳回 E \_ FAIL。

使用有效的筆墨資料格式版本時，所讀取之紙張屬性中的新筆墨資料陣列大小， \_ 會用來配置所需大小的新筆墨資料陣列。 現有的筆墨資料會刪除，而且其資料會遺失。 如果這是很重要的資料，應該在呼叫 **Load** 之前儲存。 配置新的陣列之後，會再次呼叫 [**IStream：： read**](/windows/desktop/api/Objidl/nn-objidl-istream) ，以將資料從資料流程讀取到陣列。 如果這個呼叫成功，就會採用新讀取的紙張屬性中的值做為目前的 COPaper 值。

在此載入作業期間，會使用暫存檔案 \_ 屬性結構 NewProps 來保存讀入的新屬性。 如果載入成功，NewProps 會複製到檔 \_ 屬性結構中，m \_ PaperProperties。 如同之前一樣，在完成載入並不再需要 [**istream**](/windows/desktop/api/Objidl/nn-objidl-istream) 之後，會釋放 **istream** 指標。

如果 **載入** 結束時發生錯誤，則會清除筆墨資料陣列，因為它可能包含損毀的資料。

如果 **載入** 結束時沒有錯誤，則會在 COPaper 內部 NotifySinks 方法中呼叫 client [**IPaperSink：：**](ipapersink-methods.md) load 方法，以通知用戶端載入作業已完成。 這是用戶端的重要通知，因為它必須顯示這項新載入的筆墨資料。 此通知會大量使用 COPaper 中的可連線物件功能。

 

 





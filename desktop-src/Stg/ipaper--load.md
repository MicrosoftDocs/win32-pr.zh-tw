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
# <a name="ipaperload"></a><span data-ttu-id="fa8a8-104">IPaper：： Load</span><span class="sxs-lookup"><span data-stu-id="fa8a8-104">IPaper::Load</span></span>

<span data-ttu-id="fa8a8-105">下列 c + + 程式碼範例示範如何在儲存體中開啟現有的資料流程、讀取中的新紙張屬性，然後將它們設定為目前的 COPaper 值。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-105">The following C++ sample code shows how to open the existing stream in the storage, read new paper properties in and then set them as the current values for COPaper.</span></span>

<span data-ttu-id="fa8a8-106">以下是來自 .cpp 的 **IPaper：： Load** 方法。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-106">The following is the **IPaper::Load** method from Paper.cpp.</span></span>


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



<span data-ttu-id="fa8a8-107">現在，會呼叫 [**IStorage：： OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) 方法，在名為 "data" 的儲存體中開啟現有的資料流程。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-107">Now, the [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) method is called to open the existing stream in the storage called "PAPERDATA".</span></span> <span data-ttu-id="fa8a8-108">存取模式旗標適用于唯讀、直接及非共用的獨佔存取權。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-108">Access mode flags are for read-only, direct, and non-shared exclusive access.</span></span> <span data-ttu-id="fa8a8-109">當資料流程開啟時，會呼叫 [**IStream：： read**](/windows/desktop/api/Objidl/nn-objidl-istream) 方法以讀取紙張 \_ 屬性結構。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-109">When the stream is open, the [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) method is called to read the PAPER\_PROPERTIES structure.</span></span> <span data-ttu-id="fa8a8-110">如果實際讀取的數量不等於所要求的數量，則會中止載入作業，並 \_ 傳回 E 失敗。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-110">If the amount actually read does not equal the amount requested, the load operation is aborted, and E\_FAIL is returned.</span></span> <span data-ttu-id="fa8a8-111">如果無法辨識新的 [檔] 屬性中的格式版本 \_ ，載入作業就會中止，且 **load** 會傳回 E \_ FAIL。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-111">If the format version in the newly read PAPER\_PROPERTIES is not recognized, then the load operation is aborted and **Load** returns E\_FAIL.</span></span>

<span data-ttu-id="fa8a8-112">使用有效的筆墨資料格式版本時，所讀取之紙張屬性中的新筆墨資料陣列大小， \_ 會用來配置所需大小的新筆墨資料陣列。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-112">With a valid ink data format version, the size of the new ink data array from the PAPER\_PROPERTIES that was read in is used to allocate a new ink data array of the required size.</span></span> <span data-ttu-id="fa8a8-113">現有的筆墨資料會刪除，而且其資料會遺失。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-113">The existing ink data is deleted, and its data is lost.</span></span> <span data-ttu-id="fa8a8-114">如果這是很重要的資料，應該在呼叫 **Load** 之前儲存。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-114">If this data was valuable, it should have been saved before **Load** was called.</span></span> <span data-ttu-id="fa8a8-115">配置新的陣列之後，會再次呼叫 [**IStream：： read**](/windows/desktop/api/Objidl/nn-objidl-istream) ，以將資料從資料流程讀取到陣列。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-115">After the new array is allocated, [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) is called again to read the data into the array from the stream.</span></span> <span data-ttu-id="fa8a8-116">如果這個呼叫成功，就會採用新讀取的紙張屬性中的值做為目前的 COPaper 值。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-116">If this call succeeds, the values in the newly read paper properties are adopted as the current values for COPaper.</span></span>

<span data-ttu-id="fa8a8-117">在此載入作業期間，會使用暫存檔案 \_ 屬性結構 NewProps 來保存讀入的新屬性。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-117">During this load operation, a temporary PAPER\_PROPERTIES structure, NewProps, was used to hold the new properties read in.</span></span> <span data-ttu-id="fa8a8-118">如果載入成功，NewProps 會複製到檔 \_ 屬性結構中，m \_ PaperProperties。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-118">If all succeeds with the load, NewProps is copied into the PAPER\_PROPERTIES structure, m\_PaperProperties.</span></span> <span data-ttu-id="fa8a8-119">如同之前一樣，在完成載入並不再需要 [**istream**](/windows/desktop/api/Objidl/nn-objidl-istream) 之後，會釋放 **istream** 指標。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-119">As before, after Load is done and the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) is no longer required, the **IStream** pointer is released.</span></span>

<span data-ttu-id="fa8a8-120">如果 **載入** 結束時發生錯誤，則會清除筆墨資料陣列，因為它可能包含損毀的資料。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-120">If there is an error at the end of **Load**, the ink data array is erased, because it may contain damaged data.</span></span>

<span data-ttu-id="fa8a8-121">如果 **載入** 結束時沒有錯誤，則會在 COPaper 內部 NotifySinks 方法中呼叫 client [**IPaperSink：：**](ipapersink-methods.md) load 方法，以通知用戶端載入作業已完成。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-121">If there is no error at the end of **Load**, the client [**IPaperSink::Loaded**](ipapersink-methods.md) method is called, in the COPaper internal NotifySinks method, to notify the client that the load operation is completed.</span></span> <span data-ttu-id="fa8a8-122">這是用戶端的重要通知，因為它必須顯示這項新載入的筆墨資料。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-122">This is an important notification for the client, because it must display this new loaded ink data.</span></span> <span data-ttu-id="fa8a8-123">此通知會大量使用 COPaper 中的可連線物件功能。</span><span class="sxs-lookup"><span data-stu-id="fa8a8-123">This notification makes significant use of connectable object features in COPaper.</span></span>

 

 





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
# <a name="ipapersave"></a><span data-ttu-id="fd0dc-104">IPaper：： Save</span><span class="sxs-lookup"><span data-stu-id="fd0dc-104">IPaper::Save</span></span>

<span data-ttu-id="fd0dc-105">此範例程式碼中的主要焦點是 COPaper 可以如何載入並將其紙張資料儲存在複合檔案中。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-105">The principal focus in this sample code is how COPaper can load and save its paper data in compound files.</span></span> <span data-ttu-id="fd0dc-106">詳細討論 [**IPaper**](ipaper-methods.md)、 [**載入**](ipaper--load.md)和 **儲存** 方法的執行。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-106">The [**IPaper**](ipaper-methods.md), [**Load**](ipaper--load.md), and **Save** method implementations are discussed in detail.</span></span>

<span data-ttu-id="fd0dc-107">以下是從 .cpp **IPaper：： Save** 方法。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-107">The following is the **IPaper::Save** method from Paper.cpp.</span></span>


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



<span data-ttu-id="fd0dc-108">在此用戶端和伺服器關聯性中，COPaper 不會建立用來儲存紙張資料的複合檔案。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-108">In this client and server relationship, COPaper does not create the compound file used to store paper data.</span></span> <span data-ttu-id="fd0dc-109">針對 **儲存** 和 [**載入**](ipaper--load.md) 方法，用戶端會針對現有的複合檔案傳遞 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-109">For both the **Save** and [**Load**](ipaper--load.md) methods, the client passes an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface pointer for an existing compound file.</span></span> <span data-ttu-id="fd0dc-110">然後，它會使用 **IStorage** 來寫入和讀取該複合檔案中的資料。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-110">It then uses the **IStorage** to write and read data in that compound file.</span></span> <span data-ttu-id="fd0dc-111">在 **IPaper：： Save** 上方，儲存了數種類型的資料。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-111">In **IPaper::Save** above, several types of data are stored.</span></span>

<span data-ttu-id="fd0dc-112">DllPaper、CLSID DllPaper 的 CLSID \_ 會序列化，並儲存在名為 "001CompObj" 的儲存物件內的特殊 COM 控制資料流程中 \\ 。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-112">The CLSID for DllPaper, CLSID\_DllPaper, is serialized and stored in a special COM-controlled stream within the storage object called "\\001CompObj".</span></span> <span data-ttu-id="fd0dc-113">[**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg)服務函數會執行此儲存體。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-113">The [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) service function performs this storage.</span></span> <span data-ttu-id="fd0dc-114">此儲存的 CLSID 資料可以用來將儲存體內容與所建立的 DllPaper 元件產生關聯，並可加以解讀。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-114">This stored CLSID data can be used to associate the storage content with the DllPaper component that created and can interpret it.</span></span> <span data-ttu-id="fd0dc-115">在此範例中，根儲存體是由 **StoClien** 傳遞，因此整個複合檔案會與 DllPaper 元件相關聯。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-115">In this sample, the root storage is passed by **StoClien**, and thus the entire compound file is associated with the DllPaper component.</span></span> <span data-ttu-id="fd0dc-116">您稍後可以使用 [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) 服務函式的呼叫來取出此 CLSID 資料。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-116">This CLSID data can be retrieved later with a call to the [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) service function.</span></span>

<span data-ttu-id="fd0dc-117">由於 DllPaper 會處理可編輯的資料，因此也適合在儲存體中記錄剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-117">Because DllPaper deals with editable data, it is also appropriate to record a clipboard format in the storage.</span></span> <span data-ttu-id="fd0dc-118">呼叫 [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) 服務函式來儲存剪貼簿格式指定和使用者可讀取的格式名稱。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-118">The [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) service function is called to store both a clipboard format designation and a user-readable name for the format.</span></span> <span data-ttu-id="fd0dc-119">使用者可讀取的名稱適用于在挑選清單中顯示 GUI。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-119">The user-readable name is meant for GUI display in selection lists.</span></span> <span data-ttu-id="fd0dc-120">以上傳遞的名稱會使用 CLIPBDFMT STR 的宏， \_ 在檔中定義為 "DllPaper 1.0"。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-120">The name passed above uses a macro, CLIPBDFMT\_STR, which is defined as "DllPaper 1.0" in Paper.h.</span></span> <span data-ttu-id="fd0dc-121">此儲存的剪貼簿資料可以在稍後透過呼叫服務函式 [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg)來取出。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-121">This stored clipboard data can be retrieved later with a call to the service function [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg).</span></span> <span data-ttu-id="fd0dc-122">此函數會傳回使用工作記憶體配置器所配置的字串值。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-122">This function returns a string value that is allocated using the task memory allocator.</span></span> <span data-ttu-id="fd0dc-123">呼叫端負責釋放字串。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-123">The caller is responsible for freeing the string.</span></span>

<span data-ttu-id="fd0dc-124">**[下一** 步] 會在儲存體中為 COPaper 的紙張資料建立資料流程。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-124">**Save** next creates a stream in the storage for the COPaper paper data.</span></span> <span data-ttu-id="fd0dc-125">資料流程稱為 "DATA"，並使用 STREAM \_ data \_ USTR 宏傳遞。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-125">The stream is called "PAPERDATA" and is passed using the STREAM\_PAPERDATA\_USTR macro.</span></span> <span data-ttu-id="fd0dc-126">[**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)方法要求這個字串必須是 Unicode。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-126">The [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method requires that this string be in Unicode.</span></span> <span data-ttu-id="fd0dc-127">因為字串是在編譯時期固定的，所以宏在 Paper 中會定義為 Unicode。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-127">Because the string is fixed at compile time, the macro is defined as Unicode in Paper.h.</span></span>

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

<span data-ttu-id="fd0dc-128">字串前面的 ' L ' （指出 LONG）會達到這個條件。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-128">The 'L' before the string, indicating LONG, achieves this.</span></span>

<span data-ttu-id="fd0dc-129">[**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)方法會在指定的儲存體內建立並開啟資料流程。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-129">The [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method creates and opens a stream within the specified storage.</span></span> <span data-ttu-id="fd0dc-130">新資料流程的 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 介面指標會在呼叫端介面指標變數中傳遞。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-130">An [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface pointer for the new stream is passed in a caller interface pointer variable.</span></span> <span data-ttu-id="fd0dc-131">在 **CreateStream** 中的這個介面指標上呼叫 AddRef，呼叫端必須在使用後釋放此指標。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-131">AddRef is called on this interface pointer within **CreateStream**, and the caller must release this pointer after using it.</span></span> <span data-ttu-id="fd0dc-132">**CreateStream** 方法會傳遞給許多存取模式旗標，如下所示。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-132">The **CreateStream** method is passed numerous access mode flags, as follows.</span></span>

<span data-ttu-id="fd0dc-133">STGM \_ CREATE \| STGM \_ WRITE \| STGM \_ DIRECT \| STGM \_ SHARE \_ EXCLUSIVE</span><span class="sxs-lookup"><span data-stu-id="fd0dc-133">STGM\_CREATE \| STGM\_WRITE \| STGM\_DIRECT \| STGM\_SHARE\_EXCLUSIVE</span></span>

<span data-ttu-id="fd0dc-134">[**STGM \_CREATE**](stgm-constants.md) 會建立新的資料流程，或覆寫現有的相同名稱。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-134">[**STGM\_CREATE**](stgm-constants.md) creates a new stream or overwrites an existing one of the same name.</span></span> <span data-ttu-id="fd0dc-135">[**STGM \_寫入**](stgm-constants.md) 會開啟具有寫入權限的資料流程。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-135">[**STGM\_WRITE**](stgm-constants.md) opens the stream with write permission.</span></span> <span data-ttu-id="fd0dc-136">[**STGM \_直接**](stgm-constants.md) 開啟串流以進行直接存取，而非交易存取。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-136">[**STGM\_DIRECT**](stgm-constants.md) opens the stream for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="fd0dc-137">[**STGM \_共用 \_ 獨佔**](stgm-constants.md) 會開啟檔案，以供呼叫端獨佔、非共用使用。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-137">[**STGM\_SHARE\_EXCLUSIVE**](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="fd0dc-138">順利建立 DATA 資料流程之後，會使用 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 介面寫入資料流程。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-138">After the PAPERDATA stream is successfully created, the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface is used to write into the stream.</span></span> <span data-ttu-id="fd0dc-139">**IStream：： Write** 方法是用來先儲存紙張 \_ 屬性結構的內容。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-139">The **IStream::Write** method is used to first store the content of the PAPER\_PROPERTIES structure.</span></span> <span data-ttu-id="fd0dc-140">這基本上是資料流程前端的屬性標頭。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-140">This is essentially a properties header at the front of the stream.</span></span> <span data-ttu-id="fd0dc-141">因為版本號碼是檔案中的第一個專案，所以可以獨立讀取，以決定如何處理接下來的資料。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-141">Because the version number is the first thing in the file, it can be read independently to determine how to deal with the data that follows.</span></span> <span data-ttu-id="fd0dc-142">如果實際寫入的資料量不等於所要求的數量，儲存方法會中止，並傳回 STG. \_ E \_ CANTSAVE。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-142">If the amount of data actually written does not equal the amount requested, the Save method is aborted, and it returns STG\_E\_CANTSAVE.</span></span>

<span data-ttu-id="fd0dc-143">將筆跡資料的整個陣列儲存至資料流程很簡單。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-143">Saving the entire array of ink data into the stream is simple.</span></span>


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



<span data-ttu-id="fd0dc-144">由於 [**IStream：： Write**](/windows/desktop/api/Objidl/nn-objidl-istream) 方法會在位元組陣列上運作，因此會計算陣列中儲存的筆墨資料位元組數目，並且在陣列的開頭開始寫入作業。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-144">Because the [**IStream::Write**](/windows/desktop/api/Objidl/nn-objidl-istream) method operates on a byte array, the number of bytes of stored ink data in the array is calculated and the write operation begins at the start of the array.</span></span> <span data-ttu-id="fd0dc-145">如果實際寫入的資料量不等於所要求的數量， **Save** 方法會傳回 Stg. \_ E \_ CANTSAVE。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-145">If the amount of data actually written does not equal the amount requested, the **Save** method returns STG\_E\_CANTSAVE.</span></span>

<span data-ttu-id="fd0dc-146">寫入資料流程之後， **IPaper：： Save** 方法會釋放它所使用的 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 指標。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-146">After the stream is written, the **IPaper::Save** method releases the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pointer it was using.</span></span>

<span data-ttu-id="fd0dc-147">**Save** 方法也會在 COPaper 內部 NotifySinks 方法中呼叫用戶端 [**IPaperSink**](ipapersink-methods.md) (，) 通知用戶端儲存作業已完成。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-147">The **Save** method also calls the client [**IPaperSink**](ipapersink-methods.md) (in the COPaper internal NotifySinks method) to notify the client that the save operation is complete.</span></span> <span data-ttu-id="fd0dc-148">此時 **Save** 方法會傳回呼叫用戶端，這通常會釋放 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 指標。</span><span class="sxs-lookup"><span data-stu-id="fd0dc-148">At this point the **Save** method returns to the calling client, which will typically release the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pointer.</span></span>

 

 





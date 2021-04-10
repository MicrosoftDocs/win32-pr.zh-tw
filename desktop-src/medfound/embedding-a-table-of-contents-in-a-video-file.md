---
description: 將目錄嵌入影片檔案中
ms.assetid: 1546388a-7868-4411-be20-34d28becbe76
title: 將目錄嵌入影片檔案中
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8303082e454dde181de336ee0f64ff9d583312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111780"
---
# <a name="embedding-a-table-of-contents-in-a-video-file"></a><span data-ttu-id="8abe2-103">將目錄嵌入影片檔案中</span><span class="sxs-lookup"><span data-stu-id="8abe2-103">Embedding a Table of Contents in a Video File</span></span>

<span data-ttu-id="8abe2-104">本主題示範如何建立目錄 (TOC) 並將其內嵌在影片檔案中。</span><span class="sxs-lookup"><span data-stu-id="8abe2-104">This topic demonstrates how to create a table of contents (TOC) and embed it in a video file.</span></span> <span data-ttu-id="8abe2-105">為了保持範例程式碼的簡短，目錄很簡單;它只包含一個專案，並以最少的資訊填入專案。</span><span class="sxs-lookup"><span data-stu-id="8abe2-105">To keep the example code short, the table of contents is very simple; it contains only one entry, and the entry is populated with a minimum of information.</span></span>

<span data-ttu-id="8abe2-106">若要建立目錄，並將它內嵌在檔案中，您必須藉由呼叫 **CoCreateInstance** 來建立下列四個物件。</span><span class="sxs-lookup"><span data-stu-id="8abe2-106">To create a table of contents and embed it in a file, you must create the following four objects by calling **CoCreateInstance**.</span></span>

-   <span data-ttu-id="8abe2-107">TOC 專案</span><span class="sxs-lookup"><span data-stu-id="8abe2-107">TOC Entry</span></span>
-   <span data-ttu-id="8abe2-108">目錄專案清單</span><span class="sxs-lookup"><span data-stu-id="8abe2-108">TOC Entry List</span></span>
-   <span data-ttu-id="8abe2-109">目錄</span><span class="sxs-lookup"><span data-stu-id="8abe2-109">TOC</span></span>
-   <span data-ttu-id="8abe2-110">TOC 剖析器</span><span class="sxs-lookup"><span data-stu-id="8abe2-110">TOC Parser</span></span>

<span data-ttu-id="8abe2-111">在目錄剖析器的 [類別識別碼](class-identifiers-for-toc-parser.md)中，會提供物件的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="8abe2-111">Class identifiers for the objects are given in [Class Identifiers for Table of Contents Parser](class-identifiers-for-toc-parser.md).</span></span>

<span data-ttu-id="8abe2-112">先在 TOC 專案中填入描述影片檔案一部分的資訊。</span><span class="sxs-lookup"><span data-stu-id="8abe2-112">First populate the TOC entry with information that describes one portion of the video file.</span></span> <span data-ttu-id="8abe2-113">將 TOC 專案加入至 TOC 專案清單，然後將 TOC 專案清單新增至目錄。</span><span class="sxs-lookup"><span data-stu-id="8abe2-113">Add the TOC entry to the TOC entry list, and then add the TOC entry list to the TOC.</span></span> <span data-ttu-id="8abe2-114">最後，將 TOC 新增至 TOC 剖析器，以提供在影片檔案中內嵌目錄的功能。</span><span class="sxs-lookup"><span data-stu-id="8abe2-114">Finally, add the TOC to the TOC parser, which provides the functionality for embedding the TOC in the video file.</span></span> <span data-ttu-id="8abe2-115">下列清單提供更詳細的步驟。</span><span class="sxs-lookup"><span data-stu-id="8abe2-115">The following list gives the steps in more detail.</span></span>

1.  <span data-ttu-id="8abe2-116">建立 TOC 專案物件，並在其上取得 [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) 介面。</span><span class="sxs-lookup"><span data-stu-id="8abe2-116">Create a TOC Entry object and obtain an [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) interface on it.</span></span>
2.  <span data-ttu-id="8abe2-117">填入 [**TOC \_ 專案 \_ 描述**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) 元結構，並將它傳遞給 [**ITocEntry：： SetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor)。</span><span class="sxs-lookup"><span data-stu-id="8abe2-117">Populate a [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure and pass it to [**ITocEntry::SetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).</span></span>
3.  <span data-ttu-id="8abe2-118">建立 TOC 專案清單物件，並在其上取得 [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) 介面。</span><span class="sxs-lookup"><span data-stu-id="8abe2-118">Create a TOC Entry List object and obtain an [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) interface on it.</span></span>
4.  <span data-ttu-id="8abe2-119">藉由呼叫 [**ITocEntryList：： AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex)，將您在步驟1中建立的 toc 專案物件新增至 Toc 專案清單物件。</span><span class="sxs-lookup"><span data-stu-id="8abe2-119">Add the TOC Entry object you created in step 1 to the TOC Entry List object by calling [**ITocEntryList::AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).</span></span>
5.  <span data-ttu-id="8abe2-120">建立 TOC 物件，並在其上取得 [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) 介面。</span><span class="sxs-lookup"><span data-stu-id="8abe2-120">Create a TOC object and obtain an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface on it.</span></span>
6.  <span data-ttu-id="8abe2-121">藉由呼叫 [**IToc：： AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex)，將您在步驟3中建立的 Toc 專案清單物件新增至 toc 物件。</span><span class="sxs-lookup"><span data-stu-id="8abe2-121">Add the TOC Entry List object you created in step 3 to the TOC object by calling [**IToc::AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).</span></span>
7.  <span data-ttu-id="8abe2-122">建立 TOC 剖析器物件，並在其上取得 [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) 介面。</span><span class="sxs-lookup"><span data-stu-id="8abe2-122">Create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface on it.</span></span>
8.  <span data-ttu-id="8abe2-123">呼叫 [**ITocParser：： Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) 以初始化 TOC 剖析器物件，並將它與影片檔案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8abe2-123">Call [**ITocParser::Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) to initialize the TOC Parser object and associate it with a video file.</span></span>
9.  <span data-ttu-id="8abe2-124">藉由呼叫 [**ITocParser：： AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)，將您在步驟5中建立的 toc 物件新增至 toc 剖析器物件。</span><span class="sxs-lookup"><span data-stu-id="8abe2-124">Add the TOC object you created in step 5 to the TOC Parser object by calling [**ITocParser::AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).</span></span>
10. <span data-ttu-id="8abe2-125">藉由呼叫 [**ITocParser：： Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit)，將目錄內嵌于影片檔案中。</span><span class="sxs-lookup"><span data-stu-id="8abe2-125">Embed the table of contents in the video file by calling [**ITocParser::Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).</span></span>

<span data-ttu-id="8abe2-126">下列程式碼示範上述清單中提供的步驟。</span><span class="sxs-lookup"><span data-stu-id="8abe2-126">The following code demonstrates the steps given in the preceding list.</span></span>


```C++
#include <wmcodecdsp.h>
HRESULT InitTocParserAndCommit(IToc* pToc);

void main()
{
   HRESULT hr = CoInitialize(NULL);
   
   if(SUCCEEDED(hr))
   {    
      ITocEntry* pEntry = NULL;
      hr = CoCreateInstance(CLSID_CTocEntry, NULL, 
         CLSCTX_INPROC_SERVER, IID_ITocEntry, (VOID**)&pEntry); 

      if(SUCCEEDED(hr))
      {
         TOC_ENTRY_DESCRIPTOR tocDesc = {0};
         tocDesc.qwStartTime = 4; 
         tocDesc.qwEndTime = 8;
         pEntry->SetDescriptor(&tocDesc); // HRESULT ignored for simplicity.    
    
         ITocEntryList* pEntryList = NULL;
         hr = CoCreateInstance(CLSID_CTocEntryList, NULL, 
            CLSCTX_INPROC_SERVER, IID_ITocEntryList, (VOID**)&pEntryList);

         if(SUCCEEDED(hr))
         {
            pEntryList->AddEntryByIndex(0, pEntry); // HRESULT ignored.
      
            IToc* pToc = NULL;
            hr = CoCreateInstance(CLSID_CToc, NULL, 
               CLSCTX_INPROC_SERVER, IID_IToc, (VOID**)&pToc);

            if(SUCCEEDED(hr))
            {
               pToc->AddEntryListByIndex(0, pEntryList); // HRESULT ignored.
               hr = InitTocParserAndCommit(pToc);
            }
         }
      }
     
      CoUninitialize();
   }
}

HRESULT InitTocParserAndCommit(IToc* pToc)
{
   ITocParser* pTocParser = NULL;
   HRESULT hr = CoCreateInstance(CLSID_CTocParser, NULL, 
      CLSCTX_INPROC_SERVER, IID_ITocParser, (VOID**)&pTocParser);

   if(SUCCEEDED(hr))
   {
      hr = pTocParser->Init(L"\\\\?\\c:\\experiment\\seattle.wmv");

      if(SUCCEEDED(hr))
      {
         DWORD tocIndex = 0;
         hr = pTocParser->AddToc(TOC_POS_TOPLEVELOBJECT, pToc, &tocIndex);

         if(SUCCEEDED(hr))
         {
            hr = pTocParser->Commit();
         }
      }

      pTocParser->Release();
      pTocParser = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="8abe2-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="8abe2-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8abe2-128">從影片檔案讀取目錄</span><span class="sxs-lookup"><span data-stu-id="8abe2-128">Reading a Table of Contents From a Video File</span></span>](reading-a-table-of-contents-from-a-video-file.md)
</dt> <dt>

[<span data-ttu-id="8abe2-129">目錄剖析器物件</span><span class="sxs-lookup"><span data-stu-id="8abe2-129">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> <dt>

[<span data-ttu-id="8abe2-130">目錄剖析器程式設計指南</span><span class="sxs-lookup"><span data-stu-id="8abe2-130">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 




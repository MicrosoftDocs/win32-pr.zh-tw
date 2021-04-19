---
description: 從影片檔案讀取目錄
ms.assetid: 10c4f4ca-cb30-453c-b18d-0470bfecc14e
title: 從影片檔案讀取目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d75d1101b2ad0a2ecd57dcf53acbe6a6e7d435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973912"
---
# <a name="reading-a-table-of-contents-from-a-video-file"></a><span data-ttu-id="c29d3-103">從影片檔案讀取目錄</span><span class="sxs-lookup"><span data-stu-id="c29d3-103">Reading a Table of Contents from a Video File</span></span>

<span data-ttu-id="c29d3-104">本主題示範如何讀取已內嵌于影片檔案中的目錄。</span><span class="sxs-lookup"><span data-stu-id="c29d3-104">This topic demonstrates how to read a table of contents that has already been embedded in a video file.</span></span>

<span data-ttu-id="c29d3-105">首先呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立 TOC 剖析器物件，並取得 [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) 介面。</span><span class="sxs-lookup"><span data-stu-id="c29d3-105">Start by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface.</span></span> <span data-ttu-id="c29d3-106">然後藉由呼叫方法來取得下列介面。</span><span class="sxs-lookup"><span data-stu-id="c29d3-106">Then obtain the following interfaces by calling methods.</span></span>

-   [<span data-ttu-id="c29d3-107">**IToc**</span><span class="sxs-lookup"><span data-stu-id="c29d3-107">**IToc**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc)
-   [<span data-ttu-id="c29d3-108">**ITocEntryList**</span><span class="sxs-lookup"><span data-stu-id="c29d3-108">**ITocEntryList**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist)
-   [<span data-ttu-id="c29d3-109">**ITocEntry**</span><span class="sxs-lookup"><span data-stu-id="c29d3-109">**ITocEntry**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry)

<span data-ttu-id="c29d3-110">使用 [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) 的方法來檢查目錄中的個別專案。</span><span class="sxs-lookup"><span data-stu-id="c29d3-110">Use the methods of [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) to inspect an individual entry in the table of contents.</span></span> <span data-ttu-id="c29d3-111">例如，您可以檢查項目的標題、開始時間和結束時間。</span><span class="sxs-lookup"><span data-stu-id="c29d3-111">For example, you can inspect the title, the start time, and the end time of the entry.</span></span>

<span data-ttu-id="c29d3-112">下列清單提供更詳細的步驟。</span><span class="sxs-lookup"><span data-stu-id="c29d3-112">The following list gives the steps in more detail.</span></span>

1.  <span data-ttu-id="c29d3-113">呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立 TOC 剖析器物件，並在其上取得 [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) 介面。</span><span class="sxs-lookup"><span data-stu-id="c29d3-113">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface on it.</span></span>
2.  <span data-ttu-id="c29d3-114">呼叫 [**ITocParser：： Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) 以初始化 TOC 剖析器，並將它與影片檔案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="c29d3-114">Call [**ITocParser::Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) to initialize the TOC parser and associate it with a video file.</span></span>
3.  <span data-ttu-id="c29d3-115">藉由呼叫 [**ITocParser：： GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)來取得 [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc)介面。</span><span class="sxs-lookup"><span data-stu-id="c29d3-115">Obtain an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface by calling [**ITocParser::GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex).</span></span>
4.  <span data-ttu-id="c29d3-116">藉由呼叫 [**IToc：： GetEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex)來取得 [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist)介面。</span><span class="sxs-lookup"><span data-stu-id="c29d3-116">Obtain an [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) interface by calling [**IToc::GetEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex).</span></span>
5.  <span data-ttu-id="c29d3-117">藉由呼叫 [**ITocEntryList：： GetEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex)來取得 [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry)介面。</span><span class="sxs-lookup"><span data-stu-id="c29d3-117">Obtain an [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) interface by calling [**ITocEntryList::GetEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex).</span></span>
6.  <span data-ttu-id="c29d3-118">配置 [**目錄 \_ 專案 \_ 描述**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) 元結構。</span><span class="sxs-lookup"><span data-stu-id="c29d3-118">Allocate a [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure.</span></span>
7.  <span data-ttu-id="c29d3-119">藉由呼叫 [**ITocEntry：： GetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor)來填入 [**TOC \_ 專案 \_ 描述**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor)元結構。</span><span class="sxs-lookup"><span data-stu-id="c29d3-119">Populate the [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure by calling [**ITocEntry::GetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor).</span></span>

<span data-ttu-id="c29d3-120">下列程式碼示範上述清單中的步驟。</span><span class="sxs-lookup"><span data-stu-id="c29d3-120">The following code demonstrates the steps in the preceding list.</span></span>


```C++
#include <stdio.h>
#include <wmcodecdsp.h>

HRESULT ShowEntryInfo(ITocEntry* pEntry);

void main()
{
   HRESULT hr = CoInitialize(NULL);
   
   if(SUCCEEDED(hr))
   {    
      ITocParser* pTocParser = NULL;

      hr = CoCreateInstance(CLSID_CTocParser, NULL, CLSCTX_INPROC_SERVER, 
         IID_ITocParser, (VOID**)&pTocParser);  
      
      if(SUCCEEDED(hr))
      {  
         hr = pTocParser->Init(L"\\\\?\\c:\\experiment\\seattle.wmv");

         if(SUCCEEDED(hr))
         {
            IToc* pToc = NULL;
            hr = pTocParser->GetTocByIndex(TOC_POS_TOPLEVELOBJECT, 0, &pToc);

            if(SUCCEEDED(hr))
            {
               ITocEntryList* pEntryList = NULL;
               hr = pToc->GetEntryListByIndex(0, &pEntryList);

               if(SUCCEEDED(hr))
               {
                  ITocEntry* pEntry = NULL;
                  hr = pEntryList->GetEntryByIndex(0, &pEntry);

                  if(SUCCEEDED(hr))
                  {
                     hr = ShowEntryInfo(pEntry);
                     pEntry->Release();
                     pEntry = NULL;
                  }

                  pEntryList->Release();
                  pEntryList = NULL;
               }

               pToc->Release();
               pToc = NULL;
            }
         }

         pTocParser->Release();
         pTocParser = NULL;  
      }
                   
      CoUninitialize();
   }
}

HRESULT ShowEntryInfo(ITocEntry* pEntry)
{
   HRESULT hr = E_FAIL;

   TOC_ENTRY_DESCRIPTOR entryDesc = {0};
   hr = pEntry->GetDescriptor(&entryDesc);

   if(SUCCEEDED(hr))
   {
      printf_s("qwStartTime: %x\n", entryDesc.qwStartTime);
      printf_s("qwEndTime: %x\n", entryDesc.qwEndTime);
      printf_s("qwStartStartPacketOffset: %x\n", entryDesc.qwStartPacketOffset);
      printf_s("qwEndPacketOffset: %x\n", entryDesc.qwEndPacketOffset);
      printf_s("qwRepresentativeFrameTime: %x\n", entryDesc.qwRepresentativeFrameTime);
   }

   return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c29d3-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="c29d3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c29d3-122">將目錄嵌入影片檔案中</span><span class="sxs-lookup"><span data-stu-id="c29d3-122">Embedding a Table of Contents in a Video File</span></span>](embedding-a-table-of-contents-in-a-video-file.md)
</dt> <dt>

[<span data-ttu-id="c29d3-123">目錄剖析器物件</span><span class="sxs-lookup"><span data-stu-id="c29d3-123">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> <dt>

[<span data-ttu-id="c29d3-124">目錄剖析器程式設計指南</span><span class="sxs-lookup"><span data-stu-id="c29d3-124">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 

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
# <a name="embedding-a-table-of-contents-in-a-video-file"></a>將目錄嵌入影片檔案中

本主題示範如何建立目錄 (TOC) 並將其內嵌在影片檔案中。 為了保持範例程式碼的簡短，目錄很簡單;它只包含一個專案，並以最少的資訊填入專案。

若要建立目錄，並將它內嵌在檔案中，您必須藉由呼叫 **CoCreateInstance** 來建立下列四個物件。

-   TOC 專案
-   目錄專案清單
-   目錄
-   TOC 剖析器

在目錄剖析器的 [類別識別碼](class-identifiers-for-toc-parser.md)中，會提供物件的類別識別碼。

先在 TOC 專案中填入描述影片檔案一部分的資訊。 將 TOC 專案加入至 TOC 專案清單，然後將 TOC 專案清單新增至目錄。 最後，將 TOC 新增至 TOC 剖析器，以提供在影片檔案中內嵌目錄的功能。 下列清單提供更詳細的步驟。

1.  建立 TOC 專案物件，並在其上取得 [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) 介面。
2.  填入 [**TOC \_ 專案 \_ 描述**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) 元結構，並將它傳遞給 [**ITocEntry：： SetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor)。
3.  建立 TOC 專案清單物件，並在其上取得 [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) 介面。
4.  藉由呼叫 [**ITocEntryList：： AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex)，將您在步驟1中建立的 toc 專案物件新增至 Toc 專案清單物件。
5.  建立 TOC 物件，並在其上取得 [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) 介面。
6.  藉由呼叫 [**IToc：： AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex)，將您在步驟3中建立的 Toc 專案清單物件新增至 toc 物件。
7.  建立 TOC 剖析器物件，並在其上取得 [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) 介面。
8.  呼叫 [**ITocParser：： Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) 以初始化 TOC 剖析器物件，並將它與影片檔案產生關聯。
9.  藉由呼叫 [**ITocParser：： AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)，將您在步驟5中建立的 toc 物件新增至 toc 剖析器物件。
10. 藉由呼叫 [**ITocParser：： Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit)，將目錄內嵌于影片檔案中。

下列程式碼示範上述清單中提供的步驟。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[從影片檔案讀取目錄](reading-a-table-of-contents-from-a-video-file.md)
</dt> <dt>

[目錄剖析器物件](toc-parser-objects.md)
</dt> <dt>

[目錄剖析器程式設計指南](toc-parser-programming-guide.md)
</dt> </dl>

 

 




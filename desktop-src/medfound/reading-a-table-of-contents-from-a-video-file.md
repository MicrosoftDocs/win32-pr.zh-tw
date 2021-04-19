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
# <a name="reading-a-table-of-contents-from-a-video-file"></a>從影片檔案讀取目錄

本主題示範如何讀取已內嵌于影片檔案中的目錄。

首先呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立 TOC 剖析器物件，並取得 [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) 介面。 然後藉由呼叫方法來取得下列介面。

-   [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc)
-   [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist)
-   [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry)

使用 [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) 的方法來檢查目錄中的個別專案。 例如，您可以檢查項目的標題、開始時間和結束時間。

下列清單提供更詳細的步驟。

1.  呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立 TOC 剖析器物件，並在其上取得 [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) 介面。
2.  呼叫 [**ITocParser：： Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) 以初始化 TOC 剖析器，並將它與影片檔案產生關聯。
3.  藉由呼叫 [**ITocParser：： GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)來取得 [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc)介面。
4.  藉由呼叫 [**IToc：： GetEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex)來取得 [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist)介面。
5.  藉由呼叫 [**ITocEntryList：： GetEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex)來取得 [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry)介面。
6.  配置 [**目錄 \_ 專案 \_ 描述**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) 元結構。
7.  藉由呼叫 [**ITocEntry：： GetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor)來填入 [**TOC \_ 專案 \_ 描述**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor)元結構。

下列程式碼示範上述清單中的步驟。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[將目錄嵌入影片檔案中](embedding-a-table-of-contents-in-a-video-file.md)
</dt> <dt>

[目錄剖析器物件](toc-parser-objects.md)
</dt> <dt>

[目錄剖析器程式設計指南](toc-parser-programming-guide.md)
</dt> </dl>

 

 

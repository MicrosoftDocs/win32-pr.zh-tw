---
description: 用來產生目錄的 BuildGraph 函式
ms.assetid: f70740ef-4c58-4944-9be6-dd056e12ad93
title: 用來產生目錄的 BuildGraph 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53f1f175095573a5f0f53a5274d997d85db7b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318003"
---
# <a name="buildgraph-function-for-generating-a-table-of-contents"></a><span data-ttu-id="47d18-103">用來產生目錄的 BuildGraph 函式</span><span class="sxs-lookup"><span data-stu-id="47d18-103">BuildGraph Function for Generating a Table of Contents</span></span>

<span data-ttu-id="47d18-104">下列函式是範例程式中的 helper 函式，會在 [自動產生目錄](generating-a-table-of-contents-automatically.md)中討論。</span><span class="sxs-lookup"><span data-stu-id="47d18-104">The following function is a helper function in an example program that is discussed in [Generating a Table of Contents Automatically](generating-a-table-of-contents-automatically.md).</span></span>


```C++
HRESULT BuildGraph(IGraphBuilder* pGraph, IDMOWrapperFilter* pWrap)
{
   IBaseFilter* pTocGeneratorBase = NULL;
   HRESULT hr = pWrap->QueryInterface(IID_IBaseFilter, (VOID**)&pTocGeneratorBase);

   if(SUCCEEDED(hr))
   {
      hr = pGraph->AddFilter(pTocGeneratorBase, L"TOC Generator");

      if(SUCCEEDED(hr))
      {
         IBaseFilter* pSourceBase = NULL;
         hr = pGraph->AddSourceFilter(g_sourceFile, L"Source", &pSourceBase);

         if(SUCCEEDED(hr))
         { 
            IEnumPins* pTocGenPins = NULL;
            hr = pTocGeneratorBase->EnumPins(&pTocGenPins);

            if(SUCCEEDED(hr))
            {                            
               ULONG numPins = 0;
               IPin* pTocGenInput = NULL;  // 1st pin is input.
               hr = pTocGenPins->Next(1, &pTocGenInput, &numPins);

               if(SUCCEEDED(hr))
               {                           
                  numPins = 0;
                  IPin* pTocGenOutput = NULL;  // 2nd pin is output.
                  hr = pTocGenPins->Next(1, &pTocGenOutput, &numPins);

                  if(SUCCEEDED(hr))
                  {
                     IEnumPins* pSourcePins = NULL;
                     hr = pSourceBase->EnumPins(&pSourcePins);

                     if(SUCCEEDED(hr))
                     {
                        numPins = 0;
                        IPin* pSourceInput = NULL;
                        hr = pSourcePins->Next(1, &pSourceInput, &numPins);
                      
                        // We don't need the first pin, so discard it.
                        if(NULL != pSourceInput)
                        {
                           pSourceInput->Release();
                           pSourceInput = NULL;
                        }

                        IPin* pSourceOutput = NULL;  // 2nd pin is output.
                        hr = pSourcePins->Next(1, &pSourceOutput, &numPins);

                        if(SUCCEEDED(hr))
                        { 
                           hr = pGraph->Connect(pSourceOutput, pTocGenInput);

                           if(SUCCEEDED(hr))
                           {
                              hr = pGraph->Render(pTocGenOutput);
                           }

                           pSourceOutput->Release();
                           pSourceOutput = NULL;
                        }

                        pSourcePins->Release();
                        pSourcePins = NULL;
                     }

                     pTocGenOutput->Release();
                     pTocGenOutput = NULL;
                  }

                  pTocGenInput->Release();
                  pTocGenInput = NULL;
               }

               pTocGenPins->Release();
               pTocGenPins = NULL;
            }
                                               
            pSourceBase->Release();
            pSourceBase = NULL;
         }
      }

      pTocGeneratorBase->Release();
      pTocGeneratorBase = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="47d18-105">相關主題</span><span class="sxs-lookup"><span data-stu-id="47d18-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47d18-106">自動產生目錄</span><span class="sxs-lookup"><span data-stu-id="47d18-106">Generating a Table of Contents Automatically</span></span>](generating-a-table-of-contents-automatically.md)
</dt> </dl>

 

 




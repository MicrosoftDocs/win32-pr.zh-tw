---
description: 取得 DVD 介面指標
ms.assetid: 3d9315fc-dcfb-483a-9437-55c440813dc2
title: 取得 DVD 介面指標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24825b2d24ffae70e3def131e8aa522a987c11d0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970685"
---
# <a name="obtaining-the-dvd-interface-pointers"></a><span data-ttu-id="7c433-103">取得 DVD 介面指標</span><span class="sxs-lookup"><span data-stu-id="7c433-103">Obtaining the DVD Interface Pointers</span></span>

<span data-ttu-id="7c433-104">建立篩選圖形之後，您的應用程式可以取得所需的指標，以控制 DVD 導覽器、篩選圖形管理員和影片視窗。</span><span class="sxs-lookup"><span data-stu-id="7c433-104">After the filter graph is built, your application can obtain the pointers it needs to control the DVD Navigator, the Filter Graph Manager, and the video window.</span></span> <span data-ttu-id="7c433-105">下列程式碼範例將說明基本步驟（包含錯誤檢查和其他程式碼，以簡化方式）。</span><span class="sxs-lookup"><span data-stu-id="7c433-105">The basic steps, with error-checking and other code left out for simplicity, are illustrated in the following code example.</span></span> <span data-ttu-id="7c433-106">完整的程式碼可在 CDvdCore：： BuildGraph 方法的 DVD 範例應用程式中找到。</span><span class="sxs-lookup"><span data-stu-id="7c433-106">The complete code is found in the DVD Sample application in the CDvdCore::BuildGraph method.</span></span> <span data-ttu-id="7c433-107"> (需詳細資訊，請參閱 [DirectShow 範例](directshow-samples.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="7c433-107">(For more information, see [DirectShow Samples](directshow-samples.md).)</span></span>


```C++
// Create an instance of the DVD Graph Builder object.
HRESULT hr;
hr = CoCreateInstance(CLSID_DvdGraphBuilder,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IDvdGraphBuilder,
                          reinterpret_cast<void**>(&m_pIDvdGB));

// Build the DVD filter graph.
AM_DVD_RENDERSTATUS buildStatus;
hr = m_pIDvdGB->RenderDvdVideoVolume(pszwDiscPath, m_dwRenderFlags, &buildStatus);

// Get the pointers to the DVD Navigator interfaces.
hr = m_pIDvdGB->GetDvdInterface(IID_IDvdInfo2, reinterpret_cast<void**>(&m_pIDvdI2));
hr = m_pIDvdGB->GetDvdInterface(IID_IDvdControl2, reinterpret_cast<void**>(&m_pIDvdC2));
   ...    
// Get a pointer to the filter graph manager.
hr = m_pDvdGB->GetFiltergraph(&m_pGraph);
...   
// Use the graph pointer to get a pointer to IMediaControl,
// for controlling the filter graph as a whole.
hr = m_pGraph->QueryInterface(IID_IMediaControl, reinterpret_cast<void**>(&m_pIMC));
...   
// Get a pointer to IMediaEventEx,
// used for handling DVD and other filter graph events.
hr = m_pGraph->QueryInterface(IID_IMediaEventEx, reinterpret_cast<void**>(&m_pME)); 
...                
// Use the graph builder pointer again to get the IVideoWindow interface,
// to set the window style and message-handling behavior of the video renderer filter.
hr = m_pIDvdGB->GetDvdInterface(IID_IVideoWindow, reinterpret_cast<void**>(&m_pIVW));
  
hr = m_pDvdGB->GetDvdInterface(IID_IAMLine21Decoder, reinterpret_cast<void**>(&pL21Dec));
```



## <a name="related-topics"></a><span data-ttu-id="7c433-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="7c433-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c433-109">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="7c433-109">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 




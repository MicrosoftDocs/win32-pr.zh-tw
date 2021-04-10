---
description: 建立 ASF 分隔器物件
ms.assetid: 448e2b38-70f7-4491-aac8-ee988a6f7473
title: 建立 ASF 分隔器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42c8033a0861102f6d66b22e43516a616d6428b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847638"
---
# <a name="creating-the-asf-splitter-object"></a><span data-ttu-id="b835f-103">建立 ASF 分隔器物件</span><span class="sxs-lookup"><span data-stu-id="b835f-103">Creating the ASF Splitter Object</span></span>

<span data-ttu-id="b835f-104">ASF *分隔器* 物件是 WMContainer 層物件，可剖析 Advanced Systems 格式的 Asf 資料物件 (asf) 檔。</span><span class="sxs-lookup"><span data-stu-id="b835f-104">The ASF *splitter* object is a WMContainer layer object that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="b835f-105">若要建立 ASF 分隔器物件的新實例，請呼叫 [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) 函數。</span><span class="sxs-lookup"><span data-stu-id="b835f-105">To create a new instance of the ASF splitter object, call the [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) function.</span></span> <span data-ttu-id="b835f-106">此函式會傳回 [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) 介面的指標，該介面表示空的分隔器物件。</span><span class="sxs-lookup"><span data-stu-id="b835f-106">This function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface that represents an empty splitter object.</span></span>

<span data-ttu-id="b835f-107">在分隔器開始剖析之前，應用程式必須使用 ASF 標頭物件的資訊來初始化分隔器。</span><span class="sxs-lookup"><span data-stu-id="b835f-107">Before the splitter can begin parsing, the application must initialize the splitter with information from the ASF Header Object.</span></span> <span data-ttu-id="b835f-108">若要初始化分隔器，請呼叫 [**IMFASFSplitter：： initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) 方法。</span><span class="sxs-lookup"><span data-stu-id="b835f-108">To initialize the splitter, call the [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) method.</span></span> <span data-ttu-id="b835f-109">這個方法會採用 [Asf ContentInfo 物件](asf-contentinfo-object.md) 的指標，其中包含要剖析之 ASF 檔案的標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="b835f-109">This method takes a pointer to the [ASF ContentInfo Object](asf-contentinfo-object.md) that contains header information of the ASF file to parse.</span></span> <span data-ttu-id="b835f-110">應用程式必須先初始化 ContentInfo 物件，才能將它傳遞給分隔器，讓應用程式知道媒體檔案的特性。</span><span class="sxs-lookup"><span data-stu-id="b835f-110">The application must initialize the ContentInfo object before passing it to the splitter so that the characteristics of the media file are known to the application.</span></span> <span data-ttu-id="b835f-111">分隔器的 **Initialize** 方法會從 ContentInfo 物件（例如資料流程號碼）解壓縮資料流程資訊，讓分隔器可以剖析資料封包。</span><span class="sxs-lookup"><span data-stu-id="b835f-111">The splitter's **Initialize** method extracts stream information from the ContentInfo object, such as stream numbers, so the splitter can parse the data packets.</span></span>

### <a name="example"></a><span data-ttu-id="b835f-112">範例</span><span class="sxs-lookup"><span data-stu-id="b835f-112">Example</span></span>

<span data-ttu-id="b835f-113">下列程式碼範例示範如何建立分隔器，並使用現有的 ContentInfo 物件將它初始化。</span><span class="sxs-lookup"><span data-stu-id="b835f-113">The following code example shows how to create a splitter and initialize it with an existing ContentInfo object.</span></span>


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="b835f-114">此範例會使用 [SafeRelease](saferelease.md) 函式來釋放介面指標。</span><span class="sxs-lookup"><span data-stu-id="b835f-114">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b835f-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="b835f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b835f-116">ASF 分隔器</span><span class="sxs-lookup"><span data-stu-id="b835f-116">ASF Splitter</span></span>](asf-splitter.md)
</dt> </dl>

 

 




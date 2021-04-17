---
description: 載入專案檔
ms.assetid: f8d142bd-e51d-4714-893b-8e3d02506891
title: 載入專案檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9a710795a29481740bf85390cc7122cc801a22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187470"
---
# <a name="loading-a-project-file"></a><span data-ttu-id="5bd3b-103">載入專案檔</span><span class="sxs-lookup"><span data-stu-id="5bd3b-103">Loading a Project File</span></span>

<span data-ttu-id="5bd3b-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="5bd3b-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="5bd3b-105">若要載入專案檔，您需要兩個元件： XML 剖析器和空白的時間軸。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-105">To load a project file, you need two components: the XML parser and an empty timeline.</span></span> <span data-ttu-id="5bd3b-106">XML 剖析器會讀取 XML 專案檔，並建立檔案中定義的每個物件。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-106">The XML parser reads an XML project file and creates each object defined in the file.</span></span> <span data-ttu-id="5bd3b-107">然後，它會將物件插入至時間軸，並設定任何時間軸屬性，例如預設的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-107">Then it inserts the objects into the timeline and sets any timeline attributes, such as the default frame rate.</span></span> <span data-ttu-id="5bd3b-108">下列程式碼範例會載入檔案。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-108">The following code example loads a file.</span></span>


```C++
HRESULT         hr;
IAMTimeline     *pTL = NULL;
IXml2Dex        *pXML = NULL; 
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
            IID_IAMTimeline, (void**)&pTL);
hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
            IID_IXml2Dex, (void**)&pXML);
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.xtl"), 15);
hr = pXML->ReadXMLFile(pTL, bstrFile); 
SysFreeString(bstrFile);
pXML->Release();
```



<span data-ttu-id="5bd3b-109">剖析器會公開 [**IXml2Dex**](ixml2dex.md) 介面，其中包含載入和儲存專案檔案的方法。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-109">The parser exposes the [**IXml2Dex**](ixml2dex.md) interface, which contains methods for loading and saving project files.</span></span> <span data-ttu-id="5bd3b-110">時間軸會顯示 [**IAMTimeline**](iamtimeline.md) 介面，其中包含操作時間軸和建立新時程表物件的方法。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-110">The timeline exposes the [**IAMTimeline**](iamtimeline.md) interface, which contains methods for manipulating the timeline and creating new timeline objects.</span></span> <span data-ttu-id="5bd3b-111">呼叫 **CoCreateInstance** 函數以建立每個元件，如下所示。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-111">Call the **CoCreateInstance** function to create each component, as shown.</span></span> <span data-ttu-id="5bd3b-112">請記住，藉由建立新的實例，您將會遞增介面上的參考計數。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-112">Remember that by creating a new instance, you are incrementing the reference count on the interface.</span></span> <span data-ttu-id="5bd3b-113">若要避免記憶體流失，請一律在使用介面時釋放介面。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-113">To avoid memory leaks, always release an interface when you are through with it.</span></span> <span data-ttu-id="5bd3b-114">在此範例中，不需要 **IXml2Dex** 的指標來進行任何動作，因此您可以釋放介面。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-114">In this example, the pointer to **IXml2Dex** is not needed for anything more, so you can release the interface.</span></span> <span data-ttu-id="5bd3b-115">預覽時間軸仍需要 **IAMTimeline** 的指標。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-115">The pointer to **IAMTimeline** is still needed for previewing the timeline.</span></span>

<span data-ttu-id="5bd3b-116">[**IXml2Dex：： ReadXMLFile**](ixml2dex-readxmlfile.md)方法會讀取指定的檔案，並將檔案中定義的物件填入時間軸。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-116">The [**IXml2Dex::ReadXMLFile**](ixml2dex-readxmlfile.md) method reads the specified file and populates the timeline with the objects defined in the file.</span></span> <span data-ttu-id="5bd3b-117">使用 **BSTR** 值指定檔案名。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-117">The file name is specified using a **BSTR** value.</span></span> <span data-ttu-id="5bd3b-118">為了縮短範例，範例中的檔案名會以常值字串的形式提供。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-118">To shorten the example, the file name in the example is given as a literal string.</span></span> <span data-ttu-id="5bd3b-119">一般來說，您可以從 [開啟檔案] 對話方塊或類似的內容取得它。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-119">Normally, you obtain it from an Open File dialog or something similar.</span></span>

<span data-ttu-id="5bd3b-120">如果 **ReadXML** 方法成功，它會傳回成功的程式碼。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-120">If the **ReadXML** method is successful, it returns a success code.</span></span> <span data-ttu-id="5bd3b-121">否則，它會傳回錯誤碼，例如 VFW \_ E \_ 不正確 \_ 檔 \_ 格式。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-121">Otherwise, it returns an error code such as VFW\_E\_INVALID\_FILE\_FORMAT.</span></span> <span data-ttu-id="5bd3b-122">請一律檢查傳回值，以便正常地處理錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-122">Always check the return value, in order to handle error conditions gracefully.</span></span> <span data-ttu-id="5bd3b-123">同樣地，為了簡潔起見，範例程式碼不會檢查錯誤。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-123">Again for brevity, the example code does not check for errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5bd3b-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="5bd3b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bd3b-125">載入和預覽專案</span><span class="sxs-lookup"><span data-stu-id="5bd3b-125">Loading and Previewing a Project</span></span>](loading-and-previewing-a-project.md)
</dt> </dl>

 

 




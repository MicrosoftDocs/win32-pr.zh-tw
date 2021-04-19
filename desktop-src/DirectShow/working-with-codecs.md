---
description: 使用編解碼器
ms.assetid: c69e0ecf-5f72-4d77-90e6-0f493325c0f4
title: 使用編解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe6d45608c3d95fee8f67344bdec0fc77431919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988687"
---
# <a name="working-with-codecs"></a><span data-ttu-id="43ce1-103">使用編解碼器</span><span class="sxs-lookup"><span data-stu-id="43ce1-103">Working with Codecs</span></span>

<span data-ttu-id="43ce1-104">Microsoft Windows 提供數個編解碼器作為作業系統元件。</span><span class="sxs-lookup"><span data-stu-id="43ce1-104">Microsoft Windows provides several codecs as operating system components.</span></span> <span data-ttu-id="43ce1-105">可用的編解碼器一律會包含隨附于任何版本的 DirectX 和 Windows Media Player 隨附于 Windows 版本中的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="43ce1-105">The available codecs always include those that ship with whichever version of the DirectX and Windows Media Player was included in the Windows release.</span></span> <span data-ttu-id="43ce1-106">安裝較新版本的 DirectX 或 Windows Media Player 或 Windows Media SDK 執行時間時，可能會安裝其他編解碼器。</span><span class="sxs-lookup"><span data-stu-id="43ce1-106">Additional codecs may be installed when newer versions of DirectX or Windows Media Player or the Windows Media SDK runtimes are installed.</span></span> <span data-ttu-id="43ce1-107">協力廠商可能會在主機系統上安裝其他編解碼器;這些編解碼器可以設計成隻能搭配特定應用程式使用，或可支援任何 DirectShow 應用程式一般使用。</span><span class="sxs-lookup"><span data-stu-id="43ce1-107">Third parties may install additional codecs on a host system; these codecs may be designed to work only with a particular application, or they may support general use by any DirectShow application.</span></span>

<span data-ttu-id="43ce1-108">編解碼器可以用三種不同的方式來實行：</span><span class="sxs-lookup"><span data-stu-id="43ce1-108">Codecs may be implemented in one of three different ways:</span></span>

-   <span data-ttu-id="43ce1-109">影片壓縮管理員所載入的 Windows 類型音訊或可安裝影片的編解碼器， (BC-VCM-LVM-HYPERV) 或音訊壓縮管理員)  (的。</span><span class="sxs-lookup"><span data-stu-id="43ce1-109">As a Video for Windows-type audio or video installable codec that is loaded by the Video Compression Manager (VCM) or Audio Compression Manager (ACM).</span></span> <span data-ttu-id="43ce1-110">一般而言，這項技術會被視為已淘汰，不建議使用。</span><span class="sxs-lookup"><span data-stu-id="43ce1-110">In general, this technology is considered deprecated and its use is not recommended.</span></span> <span data-ttu-id="43ce1-111">可安裝的編解碼器會透過 AVI 解壓縮程式包裝函式篩選器，參與 DirectShow 篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="43ce1-111">Installable codecs participate in DirectShow filter graphs through the AVI Decompressor wrapper filter.</span></span>
-   <span data-ttu-id="43ce1-112">作為 DirectShow 篩選。</span><span class="sxs-lookup"><span data-stu-id="43ce1-112">As a DirectShow filter.</span></span> <span data-ttu-id="43ce1-113">許多協力廠商編解碼器會實作為原生的 DirectShow 篩選。</span><span class="sxs-lookup"><span data-stu-id="43ce1-113">Many third party codecs are implemented as native DirectShow filters.</span></span> <span data-ttu-id="43ce1-114">其中一個篩選準則是 Frauenhofer MP3 解壓縮程式篩選器。</span><span class="sxs-lookup"><span data-stu-id="43ce1-114">One such filter is the Frauenhofer MP3 decompressor filter.</span></span> <span data-ttu-id="43ce1-115">一般而言，這些篩選器可能會以一般方式新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="43ce1-115">In general, these filters may be added to the filter graph in the usual ways.</span></span> <span data-ttu-id="43ce1-116">這項規則的唯一例外狀況是，某些 Windows Media™音訊或 Windows Media 視訊編解碼器，而 Microsoft MPEG-2 編解碼器無法手動新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="43ce1-116">One exception to this rule is that some Windows Media™ Audio or Windows Media Video codecs, and the Microsoft MPEG-4 codec, cannot be added to a filter graph manually.</span></span> <span data-ttu-id="43ce1-117">這些篩選準則只能由 ASF 讀取器和 ASF 寫入器篩選準則新增。</span><span class="sxs-lookup"><span data-stu-id="43ce1-117">These filters can only be added by the ASF Reader and ASF Writer filters.</span></span>
-   <span data-ttu-id="43ce1-118">作為 DirectX 媒體物件 (DMOs) 。</span><span class="sxs-lookup"><span data-stu-id="43ce1-118">As DirectX Media Objects (DMOs).</span></span> <span data-ttu-id="43ce1-119">DMOs 是執行編解碼器的建議方式，因為它們可以在使用 SQL-DMO 包裝函式的 DirectShow 篩選圖形內使用，或在任何其他非 DirectShow 串流應用程式中獨立使用。</span><span class="sxs-lookup"><span data-stu-id="43ce1-119">DMOs are the recommended way to implement codecs because they can be used either within a DirectShow filter graph using the DMO Wrapper filter, or else independently in any other non-DirectShow-based streaming application.</span></span> <span data-ttu-id="43ce1-120">某些 Windows Media 音訊和 Windows Media 視訊編解碼器會實作為 DMOs。</span><span class="sxs-lookup"><span data-stu-id="43ce1-120">Some Windows Media Audio and Windows Media Video codecs are implemented as DMOs.</span></span> <span data-ttu-id="43ce1-121">如同 Windows Media 篩選器，這些 DMOs 無法在 Windows Media SDK 的內容之外使用。</span><span class="sxs-lookup"><span data-stu-id="43ce1-121">As with the Windows Media filters, these DMOs cannot be used outside the context of the Windows Media SDK.</span></span> <span data-ttu-id="43ce1-122">這表示在 DirectShow 中，只能透過 ASF 讀取器或 ASF 寫入器篩選器，將它們新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="43ce1-122">That means that in DirectShow, they can only be added to a graph through the ASF Reader or ASF Writer filters.</span></span>

<span data-ttu-id="43ce1-123">在 GraphEdit 中，所有不同類型的編解碼器都會出現在下列類別之下：</span><span class="sxs-lookup"><span data-stu-id="43ce1-123">In GraphEdit, all these different types of codecs appear together under the following categories:</span></span>

-   <span data-ttu-id="43ce1-124">音訊壓縮</span><span class="sxs-lookup"><span data-stu-id="43ce1-124">Audio compressor</span></span>
-   <span data-ttu-id="43ce1-125">影片壓縮</span><span class="sxs-lookup"><span data-stu-id="43ce1-125">Video compressor</span></span>
-   <span data-ttu-id="43ce1-126">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="43ce1-126">DirectShow filter</span></span>

<span data-ttu-id="43ce1-127">不過，其中許多編解碼器都是由協力廠商或其他 Microsoft 應用程式或作業系統元件所安裝，而不是供其他的 DirectShow 應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="43ce1-127">Many of these codecs, however, are installed by third parties, or by other Microsoft applications or operating system components, and are not meant for use by other DirectShow applications.</span></span> <span data-ttu-id="43ce1-128">GraphEdit 中顯示的編解碼器清單也取決於主機系統上執行的 Windows 版本，以及已安裝的 DirectShow SDK 版本。</span><span class="sxs-lookup"><span data-stu-id="43ce1-128">The list of codecs visible in GraphEdit also depends on which version of Windows is running on the host system, and which version of the DirectShow SDK is installed.</span></span>

 

 




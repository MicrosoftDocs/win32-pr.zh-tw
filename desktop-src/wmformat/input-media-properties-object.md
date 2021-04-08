---
title: 輸入媒體屬性物件
description: 輸入媒體屬性物件
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- Windows Media Format SDK、輸入媒體屬性物件
- Advanced Systems Format (ASF) 、輸入媒體屬性物件
- ASF (Advanced 系統格式) 、輸入媒體屬性物件
- 物件、輸入媒體屬性物件
- 輸入媒體屬性物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beddda23ab7be86c3cb522edb8e811978c0c9ed9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841880"
---
# <a name="input-media-properties-object"></a><span data-ttu-id="bca59-108">輸入媒體屬性物件</span><span class="sxs-lookup"><span data-stu-id="bca59-108">Input Media Properties Object</span></span>

<span data-ttu-id="bca59-109">寫入器物件所建立的輸入媒體屬性物件支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="bca59-109">An input media properties object created by the writer object supports the following interfaces.</span></span> <span data-ttu-id="bca59-110">這些介面是透過對寫入器物件之其中一個介面的 **QueryInterface** 呼叫來存取。</span><span class="sxs-lookup"><span data-stu-id="bca59-110">These interfaces are accessed by a call to **QueryInterface** on one of the interfaces of the writer object.</span></span>



| <span data-ttu-id="bca59-111">介面</span><span class="sxs-lookup"><span data-stu-id="bca59-111">Interface</span></span>                                        | <span data-ttu-id="bca59-112">描述</span><span class="sxs-lookup"><span data-stu-id="bca59-112">Description</span></span>                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bca59-113">**IWMInputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="bca59-113">**IWMInputMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | <span data-ttu-id="bca59-114">捕獲輸入資料流程的屬性。</span><span class="sxs-lookup"><span data-stu-id="bca59-114">Retrieves the properties of an input stream.</span></span>                                                               |
| [<span data-ttu-id="bca59-115">**IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="bca59-115">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | <span data-ttu-id="bca59-116">用作其他媒體屬性介面的基底介面， (輸入、輸出和影片) 。</span><span class="sxs-lookup"><span data-stu-id="bca59-116">Used as the base interface for the other media-property interfaces (input, output, and video).</span></span>             |
| [<span data-ttu-id="bca59-117">**IWMVideoMediaProps**</span><span class="sxs-lookup"><span data-stu-id="bca59-117">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | <span data-ttu-id="bca59-118">管理影片資料流程的屬性。</span><span class="sxs-lookup"><span data-stu-id="bca59-118">Manages the properties of a video stream.</span></span> <span data-ttu-id="bca59-119">這是選擇性的介面，僅適用于影片串流。</span><span class="sxs-lookup"><span data-stu-id="bca59-119">This is an optional interface, available only for video streams.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bca59-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="bca59-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bca59-121">**物件**</span><span class="sxs-lookup"><span data-stu-id="bca59-121">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="bca59-122">**寫入器物件**</span><span class="sxs-lookup"><span data-stu-id="bca59-122">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 





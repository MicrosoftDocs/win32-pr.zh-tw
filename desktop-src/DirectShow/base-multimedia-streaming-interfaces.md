---
description: 基底多媒體串流介面
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: 基底多媒體串流介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b715a68bd65a2fa3a3923edf10f0e2d1f6c22edb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945718"
---
# <a name="base-multimedia-streaming-interfaces"></a><span data-ttu-id="34a39-103">基底多媒體串流介面</span><span class="sxs-lookup"><span data-stu-id="34a39-103">Base Multimedia Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="34a39-104">這些 Api 已被取代。</span><span class="sxs-lookup"><span data-stu-id="34a39-104">These APIs are deprecated.</span></span> <span data-ttu-id="34a39-105">應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md) 篩選器或執行自訂篩選，以從 DirectShow 篩選圖形取得資料。</span><span class="sxs-lookup"><span data-stu-id="34a39-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="34a39-106">基底多媒體串流介面提供以程式設計方式存取多媒體串流。</span><span class="sxs-lookup"><span data-stu-id="34a39-106">The base multimedia streaming interfaces provide a programmatic way to access multimedia streams.</span></span> <span data-ttu-id="34a39-107">不過，使用基底介面來存取特定類型的資料，可能會限制您對資料的控制量，因此媒體開發人員應建立這些介面的衍生版本，以提供更強大的功能來控制其媒體類型的獨特功能。</span><span class="sxs-lookup"><span data-stu-id="34a39-107">However, using a base interface to access a specific type of data can limit the amount of control you have over the data, so media developers should create derived versions of these interfaces that provide more powerful control over the unique capabilities of their media type.</span></span>



| <span data-ttu-id="34a39-108">介面</span><span class="sxs-lookup"><span data-stu-id="34a39-108">Interface</span></span>                                      | <span data-ttu-id="34a39-109">描述</span><span class="sxs-lookup"><span data-stu-id="34a39-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34a39-110">**IMultiMediaStream**</span><span class="sxs-lookup"><span data-stu-id="34a39-110">**IMultiMediaStream**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | <span data-ttu-id="34a39-111">定義如何存取最高層級的多媒體資料流程物件;此物件包含和提供其他資料流程物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="34a39-111">Defines how to access the highest-level multimedia stream object; this object contains and provides access to other stream objects.</span></span> <span data-ttu-id="34a39-112">[**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) 有列舉或取出特定資料流程的方法，以及檢查資料流程的總時間持續時間和搜尋。</span><span class="sxs-lookup"><span data-stu-id="34a39-112">[**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) has methods that enumerate or retrieve specific streams, as well as checking the stream's total time duration and seeking within the stream.</span></span>                                                                                                       |
| [<span data-ttu-id="34a39-113">**IMediaStream**</span><span class="sxs-lookup"><span data-stu-id="34a39-113">**IMediaStream**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | <span data-ttu-id="34a39-114">定義泛型資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="34a39-114">Defines a generic stream object.</span></span> <span data-ttu-id="34a39-115">您可以使用其方法來取出資料流程的指標、取得資料流程的相關資訊，以及從資料流程資料建立範例。</span><span class="sxs-lookup"><span data-stu-id="34a39-115">Use its methods to retrieve a pointer to the stream, get information about the stream, and create samples from the stream data.</span></span> <span data-ttu-id="34a39-116">您也可以建立共用的資料流程範例，讓多個資料流程可以存取，而不需要複製範例的資料。</span><span class="sxs-lookup"><span data-stu-id="34a39-116">You can also create shared stream samples, which multiple streams can access without duplicating the sample's data.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="34a39-117">**IStreamSample**</span><span class="sxs-lookup"><span data-stu-id="34a39-117">**IStreamSample**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | <span data-ttu-id="34a39-118">控制特定資料流程範例的行為。</span><span class="sxs-lookup"><span data-stu-id="34a39-118">Controls the behavior of a specific stream sample.</span></span> <span data-ttu-id="34a39-119">您可以取出建立範例的資料流程、檢查範例的開始和結束時間和完成狀態，然後在範例本身 (透過 [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) 方法) 來執行使用者定義函數。</span><span class="sxs-lookup"><span data-stu-id="34a39-119">You can retrieve the stream that created the sample, check the sample's start and end times and completion status, and perform a user-defined function on the sample itself (through the [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) method).</span></span> <span data-ttu-id="34a39-120">一般而言，Update 方法會以適當的方式處理範例資料，例如轉譯影片資料或播放音訊資料。</span><span class="sxs-lookup"><span data-stu-id="34a39-120">Typically, the Update method processes the sample data in an appropriate manner, such as rendering video data or playing back audio data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="34a39-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="34a39-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34a39-122">多媒體串流介面的清單</span><span class="sxs-lookup"><span data-stu-id="34a39-122">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 




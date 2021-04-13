---
description: 音訊串流介面
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: 音訊串流介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68210beef0b05fcfc89ae5005c485fbc4b74d40f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510282"
---
# <a name="audio-streaming-interfaces"></a><span data-ttu-id="09beb-103">音訊串流介面</span><span class="sxs-lookup"><span data-stu-id="09beb-103">Audio Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="09beb-104">這些 Api 已被取代。</span><span class="sxs-lookup"><span data-stu-id="09beb-104">These APIs are deprecated.</span></span> <span data-ttu-id="09beb-105">應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md) 篩選器或執行自訂篩選，以從 DirectShow 篩選圖形取得資料。</span><span class="sxs-lookup"><span data-stu-id="09beb-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 



| <span data-ttu-id="09beb-106">介面</span><span class="sxs-lookup"><span data-stu-id="09beb-106">Interface</span></span>                                        | <span data-ttu-id="09beb-107">描述</span><span class="sxs-lookup"><span data-stu-id="09beb-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09beb-108">**IAudioMediaStream**</span><span class="sxs-lookup"><span data-stu-id="09beb-108">**IAudioMediaStream**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | <span data-ttu-id="09beb-109">控制音訊媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="09beb-109">Controls audio media streams.</span></span> <span data-ttu-id="09beb-110">這個介面繼承自 [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) 介面，用來建立一或多個 [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) 物件。</span><span class="sxs-lookup"><span data-stu-id="09beb-110">This interface inherits from the [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) interface and is used to create one or more [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) objects.</span></span> <span data-ttu-id="09beb-111">它也可用來設定和取出資料流程資料的目前格式。</span><span class="sxs-lookup"><span data-stu-id="09beb-111">It is also used to set and retrieve the current format of the stream data.</span></span>                                                                                                            |
| [<span data-ttu-id="09beb-112">**IAudioStreamSample**</span><span class="sxs-lookup"><span data-stu-id="09beb-112">**IAudioStreamSample**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | <span data-ttu-id="09beb-113">從基礎 [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) 資料物件中抓取資訊。</span><span class="sxs-lookup"><span data-stu-id="09beb-113">Retrieves information from the underlying [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) data objects.</span></span>                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="09beb-114">**IMemoryData**</span><span class="sxs-lookup"><span data-stu-id="09beb-114">**IMemoryData**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | <span data-ttu-id="09beb-115">包含的方法可設定和取出音訊資料物件上的記憶體資料。</span><span class="sxs-lookup"><span data-stu-id="09beb-115">Contains methods that set and retrieve memory data on audio data objects.</span></span> <span data-ttu-id="09beb-116">音訊資料物件提供資料流程範例存取的基礎資料。</span><span class="sxs-lookup"><span data-stu-id="09beb-116">Audio data objects provide the underlying data that stream samples access.</span></span> <span data-ttu-id="09beb-117">這個介面提供一種方法來初始化記憶體緩衝區，並在物件中設定實際的音訊資料量。</span><span class="sxs-lookup"><span data-stu-id="09beb-117">This interface provides a way to initialize memory buffers and to set actual amounts of audio data in the objects.</span></span> <span data-ttu-id="09beb-118">此外， [**IMemoryData：： GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) 方法可以用來取出音訊記憶體資料。</span><span class="sxs-lookup"><span data-stu-id="09beb-118">Additionally, the [**IMemoryData::GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) method can be used to retrieve audio memory data.</span></span> |
| [<span data-ttu-id="09beb-119">**IAudioData**</span><span class="sxs-lookup"><span data-stu-id="09beb-119">**IAudioData**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | <span data-ttu-id="09beb-120">提供可讓應用程式設定和取得音訊串流將會參考之基礎音訊資料的方法。</span><span class="sxs-lookup"><span data-stu-id="09beb-120">Provides methods that enable applications to set and get the underlying audio data that audio streams will reference.</span></span> <span data-ttu-id="09beb-121">音訊資料格式設定于 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構中。</span><span class="sxs-lookup"><span data-stu-id="09beb-121">The audio data format is set in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="09beb-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="09beb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09beb-123">多媒體串流介面的清單</span><span class="sxs-lookup"><span data-stu-id="09beb-123">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 

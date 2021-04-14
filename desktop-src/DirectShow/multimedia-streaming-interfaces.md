---
description: 多媒體串流介面
ms.assetid: 53d639e2-8717-4552-b0d3-b8c500bd38a8
title: 多媒體串流介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d654bae73ee822f553a1494e3b374cf35b8ac4a1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104514368"
---
# <a name="multimedia-streaming-interfaces"></a><span data-ttu-id="14992-103">多媒體串流介面</span><span class="sxs-lookup"><span data-stu-id="14992-103">Multimedia Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="14992-104">這些 Api 已被取代。</span><span class="sxs-lookup"><span data-stu-id="14992-104">These APIs are deprecated.</span></span> <span data-ttu-id="14992-105">應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md) 篩選器或執行自訂篩選，以從 DirectShow 篩選圖形取得資料。</span><span class="sxs-lookup"><span data-stu-id="14992-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="14992-106">本節包含所有多媒體串流介面及其方法的參考專案，包括 Microsoft DirectShow 支援的專案。</span><span class="sxs-lookup"><span data-stu-id="14992-106">This section contains reference entries for all the multimedia streaming interfaces and their methods, including those that Microsoft DirectShow supports.</span></span>



| <span data-ttu-id="14992-107">介面</span><span class="sxs-lookup"><span data-stu-id="14992-107">Interface</span></span>                                                  | <span data-ttu-id="14992-108">描述</span><span class="sxs-lookup"><span data-stu-id="14992-108">Description</span></span>                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14992-109">**IAMMediaStream**</span><span class="sxs-lookup"><span data-stu-id="14992-109">**IAMMediaStream**</span></span>](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream)                   | <span data-ttu-id="14992-110">處理在使用多媒體串流的應用程式中，DirectShow 篩選和篩選圖形之間的內部連接。</span><span class="sxs-lookup"><span data-stu-id="14992-110">Handles the internal connections between DirectShow filters and filter graphs in applications that use multimedia streaming.</span></span>                            |
| [<span data-ttu-id="14992-111">**IAMMediaTypeSample**</span><span class="sxs-lookup"><span data-stu-id="14992-111">**IAMMediaTypeSample**</span></span>](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample)           | <span data-ttu-id="14992-112">包含使用任意媒體類型運算元據流範例的方法。</span><span class="sxs-lookup"><span data-stu-id="14992-112">Contains methods for manipulating stream samples with arbitrary media types.</span></span>                                                                            |
| [<span data-ttu-id="14992-113">**IAMMediaTypeStream**</span><span class="sxs-lookup"><span data-stu-id="14992-113">**IAMMediaTypeStream**</span></span>](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream)           | <span data-ttu-id="14992-114">包含用來建立具有任意媒體類型之多媒體資料流程的方法。</span><span class="sxs-lookup"><span data-stu-id="14992-114">Contains methods for creating multimedia streams with arbitrary media types.</span></span>                                                                            |
| [<span data-ttu-id="14992-115">**IAMMultiMediaStream**</span><span class="sxs-lookup"><span data-stu-id="14992-115">**IAMMultiMediaStream**</span></span>](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream)         | <span data-ttu-id="14992-116">將 DirectShow 功能公開給多媒體串流開發人員。</span><span class="sxs-lookup"><span data-stu-id="14992-116">Exposes DirectShow functionality to multimedia stream developers.</span></span>                                                                                       |
| [<span data-ttu-id="14992-117">**IAudioData**</span><span class="sxs-lookup"><span data-stu-id="14992-117">**IAudioData**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                           | <span data-ttu-id="14992-118">提供可讓應用程式設定和取得音訊串流將會參考之基礎音訊資料的方法。</span><span class="sxs-lookup"><span data-stu-id="14992-118">Provides methods that enable applications to set and get the underlying audio data that audio streams will reference.</span></span>                                   |
| [<span data-ttu-id="14992-119">**IAudioMediaStream**</span><span class="sxs-lookup"><span data-stu-id="14992-119">**IAudioMediaStream**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)             | <span data-ttu-id="14992-120">提供可設定和取得資料流程格式的方法，以控制音訊媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="14992-120">Controls audio media streams by providing methods that set and get the stream's format.</span></span>                                                                 |
| [<span data-ttu-id="14992-121">**IAudioStreamSample**</span><span class="sxs-lookup"><span data-stu-id="14992-121">**IAudioStreamSample**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample)           | <span data-ttu-id="14992-122">從基礎 [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) 資料物件中抓取資訊。</span><span class="sxs-lookup"><span data-stu-id="14992-122">Retrieves information from the underlying [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) data objects.</span></span>                                                                |
| [<span data-ttu-id="14992-123">**IDirectDrawMediaStream**</span><span class="sxs-lookup"><span data-stu-id="14992-123">**IDirectDrawMediaStream**</span></span>](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | <span data-ttu-id="14992-124">控制出現在 Microsoft® DirectDraw®表面上的媒體串流。</span><span class="sxs-lookup"><span data-stu-id="14992-124">Controls media streams that appear on Microsoft® DirectDraw® surfaces.</span></span>                                                                                  |
| [<span data-ttu-id="14992-125">**IDirectDrawStreamSample**</span><span class="sxs-lookup"><span data-stu-id="14992-125">**IDirectDrawStreamSample**</span></span>](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | <span data-ttu-id="14992-126">提供方法，這些方法可設定和取出與目前資料流程範例相關聯的 DirectDraw 介面指標。</span><span class="sxs-lookup"><span data-stu-id="14992-126">Provides methods that set and retrieve pointers to the DirectDraw surface associated with the current stream sample.</span></span>                                    |
| [<span data-ttu-id="14992-127">**IMediaStream**</span><span class="sxs-lookup"><span data-stu-id="14992-127">**IMediaStream**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)                       | <span data-ttu-id="14992-128">提供媒體資料流程特性的存取權，例如資料流程的媒體類型和目的識別碼。</span><span class="sxs-lookup"><span data-stu-id="14992-128">Provides access to the characteristics of a media stream, such as the stream's media type and purpose ID.</span></span> <span data-ttu-id="14992-129">它也有建立資料範例的方法。</span><span class="sxs-lookup"><span data-stu-id="14992-129">It also has methods that create data samples.</span></span> |
| [<span data-ttu-id="14992-130">**IMediaStreamFilter**</span><span class="sxs-lookup"><span data-stu-id="14992-130">**IMediaStreamFilter**</span></span>](/previous-versions/windows/desktop/api/amstream/nn-amstream-imediastreamfilter)           | <span data-ttu-id="14992-131">媒體資料流程篩選器支援，由多媒體資料流程物件在內部使用。</span><span class="sxs-lookup"><span data-stu-id="14992-131">Supported by the Media Stream filter, which is used internally by the multimedia stream object.</span></span> <span data-ttu-id="14992-132">.</span><span class="sxs-lookup"><span data-stu-id="14992-132">.</span></span>                                                       |
| [<span data-ttu-id="14992-133">**IMemoryData**</span><span class="sxs-lookup"><span data-stu-id="14992-133">**IMemoryData**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)                         | <span data-ttu-id="14992-134">包含的方法可設定和取出音訊資料物件上的記憶體資料。</span><span class="sxs-lookup"><span data-stu-id="14992-134">Contains methods that set and retrieve memory data on audio data objects.</span></span>                                                                               |
| [<span data-ttu-id="14992-135">**IMultiMediaStream**</span><span class="sxs-lookup"><span data-stu-id="14992-135">**IMultiMediaStream**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)             | <span data-ttu-id="14992-136">提供控制多媒體資料流程的方法，並提供其基礎媒體資料流程的存取權。</span><span class="sxs-lookup"><span data-stu-id="14992-136">Provides methods that control a multimedia stream and provide access to its underlying media streams.</span></span>                                                   |
| [<span data-ttu-id="14992-137">**IStreamSample**</span><span class="sxs-lookup"><span data-stu-id="14992-137">**IStreamSample**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)                     | <span data-ttu-id="14992-138">提供資料流程範例行為的控制權。</span><span class="sxs-lookup"><span data-stu-id="14992-138">Provides control over the behavior of stream samples.</span></span>                                                                                                   |



 

 

 




---
description: 媒體類型
ms.assetid: 690fda6e-dcbd-44dc-968d-cc949126da81
title: '媒體類型 (媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acbfb1b637eef6acb664d3d95a0488f155c6916
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321624"
---
# <a name="media-types-media-foundation"></a><span data-ttu-id="c5427-103">媒體類型 (媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="c5427-103">Media Types (Media Foundation)</span></span>

<span data-ttu-id="c5427-104">*媒體類型* 是描述媒體資料流程格式的方式。</span><span class="sxs-lookup"><span data-stu-id="c5427-104">A *media type* is a way to describe the format of a media stream.</span></span> <span data-ttu-id="c5427-105">在媒體基礎中，媒體類型會以 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="c5427-105">In Media Foundation, media types are represented by the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface.</span></span> <span data-ttu-id="c5427-106">應用程式會使用媒體類型來探索媒體檔案或媒體資料流程的格式。</span><span class="sxs-lookup"><span data-stu-id="c5427-106">Applications use media types to discover the format of a media file or media stream.</span></span> <span data-ttu-id="c5427-107">媒體基礎管線中的物件會使用媒體類型來協調其傳遞或接收的格式。</span><span class="sxs-lookup"><span data-stu-id="c5427-107">Objects in the Media Foundation pipeline use media types to negotiate the formats they will deliver or receive.</span></span>

<span data-ttu-id="c5427-108">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="c5427-108">This section contains the following topics.</span></span>



| <span data-ttu-id="c5427-109">主題</span><span class="sxs-lookup"><span data-stu-id="c5427-109">Topic</span></span>                                                                    | <span data-ttu-id="c5427-110">描述</span><span class="sxs-lookup"><span data-stu-id="c5427-110">Description</span></span>                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="c5427-111">關於媒體類型</span><span class="sxs-lookup"><span data-stu-id="c5427-111">About Media Types</span></span>](about-media-types.md)                               | <span data-ttu-id="c5427-112">媒體基礎媒體類型的一般總覽。</span><span class="sxs-lookup"><span data-stu-id="c5427-112">General overview of media types in Media Foundation.</span></span>                             |
| [<span data-ttu-id="c5427-113">媒體類型 Guid</span><span class="sxs-lookup"><span data-stu-id="c5427-113">Media Type GUIDs</span></span>](media-type-guids.md)                                 | <span data-ttu-id="c5427-114">列出主要類型和子類型的已定義 Guid。</span><span class="sxs-lookup"><span data-stu-id="c5427-114">Lists the defined GUIDs for major types and subtypes.</span></span>                            |
| [<span data-ttu-id="c5427-115">音訊媒體類型</span><span class="sxs-lookup"><span data-stu-id="c5427-115">Audio Media Types</span></span>](audio-media-types.md)                               | <span data-ttu-id="c5427-116">如何建立音訊格式的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c5427-116">How to create media types for audio formats.</span></span>                                     |
| [<span data-ttu-id="c5427-117">影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="c5427-117">Video Media Types</span></span>](video-media-types.md)                               | <span data-ttu-id="c5427-118">如何建立影片格式的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c5427-118">How to create media types for video formats.</span></span>                                     |
| [<span data-ttu-id="c5427-119">完成和部分媒體類型</span><span class="sxs-lookup"><span data-stu-id="c5427-119">Complete and Partial Media Types</span></span>](complete-and-partial-media-types.md) | <span data-ttu-id="c5427-120">描述完整媒體類型與部分媒體類型之間的差異。</span><span class="sxs-lookup"><span data-stu-id="c5427-120">Describes the difference between complete media types and partial media types.</span></span>   |
| [<span data-ttu-id="c5427-121">媒體類型轉換</span><span class="sxs-lookup"><span data-stu-id="c5427-121">Media Type Conversions</span></span>](media-type-conversions.md)                     | <span data-ttu-id="c5427-122">如何在媒體基礎媒體類型與較舊的格式結構之間轉換。</span><span class="sxs-lookup"><span data-stu-id="c5427-122">How to convert between Media Foundation media types and older format structures.</span></span> |
| [<span data-ttu-id="c5427-123">媒體類型 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="c5427-123">Media Type Helper Functions</span></span>](media-type-helper-functions.md)           | <span data-ttu-id="c5427-124">可操作或從媒體類型取得資訊的函式清單。</span><span class="sxs-lookup"><span data-stu-id="c5427-124">A list of functions that manipulate or get information from a media type.</span></span>        |
| [<span data-ttu-id="c5427-125">媒體類型的偵錯工具代碼</span><span class="sxs-lookup"><span data-stu-id="c5427-125">Media Type Debugging Code</span></span>](media-type-debugging-code.md)               | <span data-ttu-id="c5427-126">示範如何在偵錯工具中查看媒體類型的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="c5427-126">Example code that shows how to view a media type while debugging.</span></span>                |



 

## <a name="related-topics"></a><span data-ttu-id="c5427-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5427-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5427-128">媒體基礎基本</span><span class="sxs-lookup"><span data-stu-id="c5427-128">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> <dt>

[<span data-ttu-id="c5427-129">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="c5427-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




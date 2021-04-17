---
title: 設定 Web 資料流程
description: 設定 Web 資料流程
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- 資料流程，設定 Web 資料流程
- 編解碼器，設定 Web 串流
- Web 串流，設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c91c36788b858b2378ebf46b553f076c5ec490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301851"
---
# <a name="configuring-web-streams"></a><span data-ttu-id="64d72-106">設定 Web 資料流程</span><span class="sxs-lookup"><span data-stu-id="64d72-106">Configuring Web Streams</span></span>

<span data-ttu-id="64d72-107">Web 串流是一種特殊類型的檔案傳輸資料流程，用來在單一資料流程中傳遞與網站相關聯的檔案。</span><span class="sxs-lookup"><span data-stu-id="64d72-107">Web streams are a specialized type of file transfer stream used to deliver the files associated with a Web site in a single stream.</span></span> <span data-ttu-id="64d72-108">下表摘要說明 Web 串流設定。</span><span class="sxs-lookup"><span data-stu-id="64d72-108">Web stream configuration is summarized in the following table.</span></span>



| <span data-ttu-id="64d72-109">設定</span><span class="sxs-lookup"><span data-stu-id="64d72-109">Setting</span></span>                                            | <span data-ttu-id="64d72-110">Description</span><span class="sxs-lookup"><span data-stu-id="64d72-110">Description</span></span>                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="64d72-111">**WM \_ 媒體 \_ 類型。 majortype**</span><span class="sxs-lookup"><span data-stu-id="64d72-111">**WM\_MEDIA\_TYPE.majortype**</span></span>                      | <span data-ttu-id="64d72-112">設定為 WMMEDIATYPE \_ FileTransfer。</span><span class="sxs-lookup"><span data-stu-id="64d72-112">Set to WMMEDIATYPE\_FileTransfer.</span></span>                                                 |
| <span data-ttu-id="64d72-113">**WM \_ 媒體 \_ 類型。子類型**</span><span class="sxs-lookup"><span data-stu-id="64d72-113">**WM\_MEDIA\_TYPE.subtype**</span></span>                        | <span data-ttu-id="64d72-114">設定為 WMMEDIASUBTYPE \_ WebStream。</span><span class="sxs-lookup"><span data-stu-id="64d72-114">Set to WMMEDIASUBTYPE\_WebStream.</span></span>                                                 |
| <span data-ttu-id="64d72-115">**WM \_ 媒體 \_ 類型。 bFixedSizeSamples**</span><span class="sxs-lookup"><span data-stu-id="64d72-115">**WM\_MEDIA\_TYPE.bFixedSizeSamples**</span></span>              | <span data-ttu-id="64d72-116">設定為 False。</span><span class="sxs-lookup"><span data-stu-id="64d72-116">Set to False.</span></span>                                                                     |
| <span data-ttu-id="64d72-117">**WM \_ 媒體 \_ 類型。 bTemporalCompression**</span><span class="sxs-lookup"><span data-stu-id="64d72-117">**WM\_MEDIA\_TYPE.bTemporalCompression**</span></span>           | <span data-ttu-id="64d72-118">設定為 [True]。</span><span class="sxs-lookup"><span data-stu-id="64d72-118">Set to True.</span></span>                                                                      |
| <span data-ttu-id="64d72-119">**WM \_ 媒體 \_ 類型。 lSampleSize**</span><span class="sxs-lookup"><span data-stu-id="64d72-119">**WM\_MEDIA\_TYPE.lSampleSize**</span></span>                    | <span data-ttu-id="64d72-120">設定為0。</span><span class="sxs-lookup"><span data-stu-id="64d72-120">Set to 0.</span></span>                                                                         |
| <span data-ttu-id="64d72-121">**WM \_ 媒體 \_ 類型。 formattype**</span><span class="sxs-lookup"><span data-stu-id="64d72-121">**WM\_MEDIA\_TYPE.formattype**</span></span>                     | <span data-ttu-id="64d72-122">設定為 WMFORMAT \_ WebStream。</span><span class="sxs-lookup"><span data-stu-id="64d72-122">Set to WMFORMAT\_WebStream.</span></span>                                                       |
| <span data-ttu-id="64d72-123">**WM \_ 媒體 \_ 類型。 pUnk**</span><span class="sxs-lookup"><span data-stu-id="64d72-123">**WM\_MEDIA\_TYPE.pUnk**</span></span>                           | <span data-ttu-id="64d72-124">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="64d72-124">Set to **NULL**.</span></span>                                                                  |
| <span data-ttu-id="64d72-125">**WM \_ 媒體 \_ 類型。 cbFormat**</span><span class="sxs-lookup"><span data-stu-id="64d72-125">**WM\_MEDIA\_TYPE.cbFormat**</span></span>                       | <span data-ttu-id="64d72-126">設定為 `sizeof(WMT_WEBSTREAM_FORMAT)`。</span><span class="sxs-lookup"><span data-stu-id="64d72-126">Set to `sizeof(WMT_WEBSTREAM_FORMAT)`.</span></span>                                            |
| <span data-ttu-id="64d72-127">**WM \_ 媒體 \_ 類型。 pbFormat**</span><span class="sxs-lookup"><span data-stu-id="64d72-127">**WM\_MEDIA\_TYPE.pbFormat**</span></span>                       | <span data-ttu-id="64d72-128">設定為正確設定的 **WMT \_ WEBSTREAM \_ 格式** 結構位址。</span><span class="sxs-lookup"><span data-stu-id="64d72-128">Set to the address of a properly configured **WMT\_WEBSTREAM\_FORMAT** structure.</span></span> |
| <span data-ttu-id="64d72-129">**WMT \_ WEBSTREAM \_ FORMAT. cbSampleHeaderFixedData**</span><span class="sxs-lookup"><span data-stu-id="64d72-129">**WMT\_WEBSTREAM\_FORMAT.cbSampleHeaderFixedData**</span></span> | <span data-ttu-id="64d72-130">設定為 `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`。</span><span class="sxs-lookup"><span data-stu-id="64d72-130">Set to `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.</span></span>                                     |
| <span data-ttu-id="64d72-131">**WMT \_ WEBSTREAM \_ FORMAT. wVersion**</span><span class="sxs-lookup"><span data-stu-id="64d72-131">**WMT\_WEBSTREAM\_FORMAT.wVersion**</span></span>                | <span data-ttu-id="64d72-132">設定為 1。</span><span class="sxs-lookup"><span data-stu-id="64d72-132">Set to 1.</span></span>                                                                         |
| <span data-ttu-id="64d72-133">**WMT \_ WEBSTREAM \_ FORMAT. wreserved**</span><span class="sxs-lookup"><span data-stu-id="64d72-133">**WMT\_WEBSTREAM\_FORMAT.wreserved**</span></span>               | <span data-ttu-id="64d72-134">設定為0。</span><span class="sxs-lookup"><span data-stu-id="64d72-134">Set to 0.</span></span>                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="64d72-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="64d72-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64d72-136">**所有資料流程通用的設定**</span><span class="sxs-lookup"><span data-stu-id="64d72-136">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="64d72-137">**設定任意資料流程類型**</span><span class="sxs-lookup"><span data-stu-id="64d72-137">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="64d72-138">**Web 串流**</span><span class="sxs-lookup"><span data-stu-id="64d72-138">**Web Streams**</span></span>](web-streams.md)
</dt> </dl>

 

 





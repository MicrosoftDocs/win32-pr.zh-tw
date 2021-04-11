---
title: 'EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK) '
description: EC \_ WMT \_ 索引 \_ 事件
ms.assetid: 46e6a011-7f25-470b-9e10-fa59f0ddbf22
keywords:
- Windows Media Format SDK，EC_WMT_INDEX_EVENT
- DirectShow，EC_WMT_INDEX_EVENT
- EC_WMT_INDEX_EVENT
- Advanced Systems Format (ASF) ，EC_WMT_INDEX_EVENT
- ASF (Advanced Systems Format) ，EC_WMT_INDEX_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34bca14ed02ac78fcfc77d1b9b716f75115a24f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024423"
---
# <a name="ec_wmt_index_event-windows-media-format-11-sdk"></a><span data-ttu-id="3fdc9-108">EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK) </span><span class="sxs-lookup"><span data-stu-id="3fdc9-108">EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="3fdc9-109">當應用程式使用 ASF 寫入器為 Windows Media 視訊檔案編制索引時，由 Windows Media Format SDK 傳送。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-109">Sent by the Windows Media Format SDK when an application uses the ASF Writer to index Windows Media Video files.</span></span>

<span data-ttu-id="3fdc9-110">參數</span><span class="sxs-lookup"><span data-stu-id="3fdc9-110">Parameters</span></span>

<span data-ttu-id="3fdc9-111">*lParam1*</span><span class="sxs-lookup"><span data-stu-id="3fdc9-111">*lParam1*</span></span>

<span data-ttu-id="3fdc9-112">可以是下列任何一個 **WMT \_ 狀態** 消息。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-112">Can be any one of the following **WMT\_STATUS** messages.</span></span>



| <span data-ttu-id="3fdc9-113">訊息</span><span class="sxs-lookup"><span data-stu-id="3fdc9-113">Message</span></span>              | <span data-ttu-id="3fdc9-114">描述</span><span class="sxs-lookup"><span data-stu-id="3fdc9-114">Description</span></span>                                     |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="3fdc9-115">WMT \_ 已開始</span><span class="sxs-lookup"><span data-stu-id="3fdc9-115">WMT\_STARTED</span></span>         | <span data-ttu-id="3fdc9-116">索引已開始。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-116">Indexing has begun.</span></span> <span data-ttu-id="3fdc9-117">*lParam2* 為零。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-117">*lParam2* is zero.</span></span>          |
| <span data-ttu-id="3fdc9-118">WMT \_ 已關閉</span><span class="sxs-lookup"><span data-stu-id="3fdc9-118">WMT\_CLOSED</span></span>          | <span data-ttu-id="3fdc9-119">索引已完成。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-119">Indexing has been completed.</span></span> <span data-ttu-id="3fdc9-120">*lParam2* 為零。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-120">*lParam2* is zero.</span></span> |
| <span data-ttu-id="3fdc9-121">WMT \_ 索引 \_ 進度</span><span class="sxs-lookup"><span data-stu-id="3fdc9-121">WMT\_INDEX\_PROGRESS</span></span> | <span data-ttu-id="3fdc9-122">正在編制索引。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-122">Indexing is in progress.</span></span>                        |



 

<span data-ttu-id="3fdc9-123">*lParam2*</span><span class="sxs-lookup"><span data-stu-id="3fdc9-123">*lParam2*</span></span>

<span data-ttu-id="3fdc9-124">如果 *lParam1* 是 WMT \_ CLOSED 或 WMT \_ 開始，則 *lParam2* 為零。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-124">If *lParam1* is WMT\_CLOSED or WMT\_STARTED, then *lParam2* is zero.</span></span> <span data-ttu-id="3fdc9-125">如果 *lParam1* 是 WMT \_ INDEX \_ 進度，則 *lParam2* 為 **DWORD** ，會以總下載大小的百分比來表示進度量。</span><span class="sxs-lookup"><span data-stu-id="3fdc9-125">If *lParam1* is WMT\_INDEX\_PROGRESS, then *lParam2* is a **DWORD** that expresses the amount of progress as a percentage of the total download size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fdc9-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="3fdc9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fdc9-127">**DirectShow QASF 參考**</span><span class="sxs-lookup"><span data-stu-id="3fdc9-127">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 





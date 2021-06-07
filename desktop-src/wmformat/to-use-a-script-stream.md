---
title: 使用腳本資料流程
description: 使用腳本資料流程
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Windows Media Format SDK，腳本資料流程
- Advanced Systems Format (ASF) 、腳本資料流程
- ASF (Advanced 系統格式) 、腳本資料流程
- 腳本資料流程，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09782855bd3000d711f134c5889733e49e020c44
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444729"
---
# <a name="to-use-a-script-stream"></a><span data-ttu-id="f2f63-107">使用腳本資料流程</span><span class="sxs-lookup"><span data-stu-id="f2f63-107">To Use a Script Stream</span></span>

<span data-ttu-id="f2f63-108">本節說明如何將腳本資料傳送至寫入器，以便包含在檔案中。</span><span class="sxs-lookup"><span data-stu-id="f2f63-108">This section describes how to send script data to the writer for inclusion in a file.</span></span> <span data-ttu-id="f2f63-109">如需在設定檔中包含腳本資料流程的詳細資訊，請參閱設定 [任意資料流程類型](configuring-arbitrary-stream-types.md)。</span><span class="sxs-lookup"><span data-stu-id="f2f63-109">For information about including script streams in profiles, see [Configuring Arbitrary Stream Types](configuring-arbitrary-stream-types.md).</span></span>

<span data-ttu-id="f2f63-110">每個腳本都包含兩個字串： *類型* 字串和 *引數* 字串。</span><span class="sxs-lookup"><span data-stu-id="f2f63-110">Each script consists of two strings, a *type* string and an *argument* string.</span></span>

<span data-ttu-id="f2f63-111">腳本資料必須先格式化，才能傳送到寫入器。</span><span class="sxs-lookup"><span data-stu-id="f2f63-111">The script data must be formatted before it is sent to the writer.</span></span> <span data-ttu-id="f2f63-112">字串應串連，並以 **null** 字元分隔，並以 **null** 字元結束。</span><span class="sxs-lookup"><span data-stu-id="f2f63-112">The strings should be concatenated, separated by a **NULL** character, and terminated with a **NULL** character.</span></span> <span data-ttu-id="f2f63-113">下列範例顯示合法的腳本：</span><span class="sxs-lookup"><span data-stu-id="f2f63-113">The following example shows a legitimate script:</span></span>



| &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |   &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="f2f63-114">U</span><span class="sxs-lookup"><span data-stu-id="f2f63-114">U</span></span>   | <span data-ttu-id="f2f63-115">R</span><span class="sxs-lookup"><span data-stu-id="f2f63-115">R</span></span>   | <span data-ttu-id="f2f63-116">L</span><span class="sxs-lookup"><span data-stu-id="f2f63-116">L</span></span>   | &nbsp; | <span data-ttu-id="f2f63-117">h</span><span class="sxs-lookup"><span data-stu-id="f2f63-117">h</span></span>   | <span data-ttu-id="f2f63-118">t</span><span class="sxs-lookup"><span data-stu-id="f2f63-118">t</span></span>   | <span data-ttu-id="f2f63-119">t</span><span class="sxs-lookup"><span data-stu-id="f2f63-119">t</span></span>   | <span data-ttu-id="f2f63-120">p</span><span class="sxs-lookup"><span data-stu-id="f2f63-120">p</span></span>   | <span data-ttu-id="f2f63-121">:</span><span class="sxs-lookup"><span data-stu-id="f2f63-121">:</span></span>   | /   | /   | <span data-ttu-id="f2f63-122">w</span><span class="sxs-lookup"><span data-stu-id="f2f63-122">w</span></span>   | <span data-ttu-id="f2f63-123">w</span><span class="sxs-lookup"><span data-stu-id="f2f63-123">w</span></span>   | <span data-ttu-id="f2f63-124">w</span><span class="sxs-lookup"><span data-stu-id="f2f63-124">w</span></span>   | <span data-ttu-id="f2f63-125">.</span><span class="sxs-lookup"><span data-stu-id="f2f63-125">.</span></span>   | <span data-ttu-id="f2f63-126">a</span><span class="sxs-lookup"><span data-stu-id="f2f63-126">a</span></span>   | <span data-ttu-id="f2f63-127">d</span><span class="sxs-lookup"><span data-stu-id="f2f63-127">d</span></span>   | <span data-ttu-id="f2f63-128">a</span><span class="sxs-lookup"><span data-stu-id="f2f63-128">a</span></span>   | <span data-ttu-id="f2f63-129">t</span><span class="sxs-lookup"><span data-stu-id="f2f63-129">t</span></span>   | <span data-ttu-id="f2f63-130">u</span><span class="sxs-lookup"><span data-stu-id="f2f63-130">u</span></span>   | <span data-ttu-id="f2f63-131">m</span><span class="sxs-lookup"><span data-stu-id="f2f63-131">m</span></span>   | <span data-ttu-id="f2f63-132">.</span><span class="sxs-lookup"><span data-stu-id="f2f63-132">.</span></span>   | <span data-ttu-id="f2f63-133">c</span><span class="sxs-lookup"><span data-stu-id="f2f63-133">c</span></span>   | <span data-ttu-id="f2f63-134">o</span><span class="sxs-lookup"><span data-stu-id="f2f63-134">o</span></span>   | <span data-ttu-id="f2f63-135">m</span><span class="sxs-lookup"><span data-stu-id="f2f63-135">m</span></span>   | &nbsp; |



 

<span data-ttu-id="f2f63-136">每一對指令碼命令都應該撰寫為寫入器的範例。</span><span class="sxs-lookup"><span data-stu-id="f2f63-136">Each pair of script commands should be written as a sample to the writer.</span></span> <span data-ttu-id="f2f63-137">如需撰寫範例的詳細資訊，請參閱 [撰寫範例](to-write-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="f2f63-137">For more information about writing samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="f2f63-138">當您播放 ASF 檔案時，讀取器 (或同步讀取器會將指令碼命令傳遞至展示時間順序中) 。</span><span class="sxs-lookup"><span data-stu-id="f2f63-138">When the ASF file is played, the script commands will be delivered by the reader (or synchronous reader) in presentation time order.</span></span> <span data-ttu-id="f2f63-139">應用程式必須負責剖析兩個字串，並回應指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="f2f63-139">It is the responsibility of the application to parse the two strings and respond to the script command.</span></span>

> [!Note]  
> <span data-ttu-id="f2f63-140">使用 DRM 加密檔案時，沒有指令碼命令可以有0的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="f2f63-140">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f2f63-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2f63-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2f63-142">**使用指令碼命令**</span><span class="sxs-lookup"><span data-stu-id="f2f63-142">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 





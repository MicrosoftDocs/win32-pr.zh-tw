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
ms.openlocfilehash: 82dee2c4a9789406c21b18c58a5f281a768fc713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311445"
---
# <a name="to-use-a-script-stream"></a><span data-ttu-id="38a7e-107">使用腳本資料流程</span><span class="sxs-lookup"><span data-stu-id="38a7e-107">To Use a Script Stream</span></span>

<span data-ttu-id="38a7e-108">本節說明如何將腳本資料傳送至寫入器，以便包含在檔案中。</span><span class="sxs-lookup"><span data-stu-id="38a7e-108">This section describes how to send script data to the writer for inclusion in a file.</span></span> <span data-ttu-id="38a7e-109">如需在設定檔中包含腳本資料流程的詳細資訊，請參閱設定 [任意資料流程類型](configuring-arbitrary-stream-types.md)。</span><span class="sxs-lookup"><span data-stu-id="38a7e-109">For information about including script streams in profiles, see [Configuring Arbitrary Stream Types](configuring-arbitrary-stream-types.md).</span></span>

<span data-ttu-id="38a7e-110">每個腳本都包含兩個字串： *類型* 字串和 *引數* 字串。</span><span class="sxs-lookup"><span data-stu-id="38a7e-110">Each script consists of two strings, a *type* string and an *argument* string.</span></span>

<span data-ttu-id="38a7e-111">腳本資料必須先格式化，才能傳送到寫入器。</span><span class="sxs-lookup"><span data-stu-id="38a7e-111">The script data must be formatted before it is sent to the writer.</span></span> <span data-ttu-id="38a7e-112">字串應串連，並以 **null** 字元分隔，並以 **null** 字元結束。</span><span class="sxs-lookup"><span data-stu-id="38a7e-112">The strings should be concatenated, separated by a **NULL** character, and terminated with a **NULL** character.</span></span> <span data-ttu-id="38a7e-113">下列範例顯示合法的腳本：</span><span class="sxs-lookup"><span data-stu-id="38a7e-113">The following example shows a legitimate script:</span></span>



|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="38a7e-114">U</span><span class="sxs-lookup"><span data-stu-id="38a7e-114">U</span></span>   | <span data-ttu-id="38a7e-115">R</span><span class="sxs-lookup"><span data-stu-id="38a7e-115">R</span></span>   | <span data-ttu-id="38a7e-116">L</span><span class="sxs-lookup"><span data-stu-id="38a7e-116">L</span></span>   | <span data-ttu-id="38a7e-117">\\0</span><span class="sxs-lookup"><span data-stu-id="38a7e-117">\\0</span></span> | <span data-ttu-id="38a7e-118">h</span><span class="sxs-lookup"><span data-stu-id="38a7e-118">h</span></span>   | <span data-ttu-id="38a7e-119">t</span><span class="sxs-lookup"><span data-stu-id="38a7e-119">t</span></span>   | <span data-ttu-id="38a7e-120">t</span><span class="sxs-lookup"><span data-stu-id="38a7e-120">t</span></span>   | <span data-ttu-id="38a7e-121">p</span><span class="sxs-lookup"><span data-stu-id="38a7e-121">p</span></span>   | <span data-ttu-id="38a7e-122">:</span><span class="sxs-lookup"><span data-stu-id="38a7e-122">:</span></span>   | /   | /   | <span data-ttu-id="38a7e-123">w</span><span class="sxs-lookup"><span data-stu-id="38a7e-123">w</span></span>   | <span data-ttu-id="38a7e-124">w</span><span class="sxs-lookup"><span data-stu-id="38a7e-124">w</span></span>   | <span data-ttu-id="38a7e-125">w</span><span class="sxs-lookup"><span data-stu-id="38a7e-125">w</span></span>   | <span data-ttu-id="38a7e-126">.</span><span class="sxs-lookup"><span data-stu-id="38a7e-126">.</span></span>   | <span data-ttu-id="38a7e-127">a</span><span class="sxs-lookup"><span data-stu-id="38a7e-127">a</span></span>   | <span data-ttu-id="38a7e-128">d</span><span class="sxs-lookup"><span data-stu-id="38a7e-128">d</span></span>   | <span data-ttu-id="38a7e-129">a</span><span class="sxs-lookup"><span data-stu-id="38a7e-129">a</span></span>   | <span data-ttu-id="38a7e-130">t</span><span class="sxs-lookup"><span data-stu-id="38a7e-130">t</span></span>   | <span data-ttu-id="38a7e-131">u</span><span class="sxs-lookup"><span data-stu-id="38a7e-131">u</span></span>   | <span data-ttu-id="38a7e-132">m</span><span class="sxs-lookup"><span data-stu-id="38a7e-132">m</span></span>   | <span data-ttu-id="38a7e-133">.</span><span class="sxs-lookup"><span data-stu-id="38a7e-133">.</span></span>   | <span data-ttu-id="38a7e-134">c</span><span class="sxs-lookup"><span data-stu-id="38a7e-134">c</span></span>   | <span data-ttu-id="38a7e-135">o</span><span class="sxs-lookup"><span data-stu-id="38a7e-135">o</span></span>   | <span data-ttu-id="38a7e-136">m</span><span class="sxs-lookup"><span data-stu-id="38a7e-136">m</span></span>   | <span data-ttu-id="38a7e-137">\\0</span><span class="sxs-lookup"><span data-stu-id="38a7e-137">\\0</span></span> |



 

<span data-ttu-id="38a7e-138">每一對指令碼命令都應該撰寫為寫入器的範例。</span><span class="sxs-lookup"><span data-stu-id="38a7e-138">Each pair of script commands should be written as a sample to the writer.</span></span> <span data-ttu-id="38a7e-139">如需撰寫範例的詳細資訊，請參閱 [撰寫範例](to-write-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="38a7e-139">For more information about writing samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="38a7e-140">當您播放 ASF 檔案時，讀取器 (或同步讀取器會將指令碼命令傳遞至展示時間順序中) 。</span><span class="sxs-lookup"><span data-stu-id="38a7e-140">When the ASF file is played, the script commands will be delivered by the reader (or synchronous reader) in presentation time order.</span></span> <span data-ttu-id="38a7e-141">應用程式必須負責剖析兩個字串，並回應指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="38a7e-141">It is the responsibility of the application to parse the two strings and respond to the script command.</span></span>

> [!Note]  
> <span data-ttu-id="38a7e-142">使用 DRM 加密檔案時，沒有指令碼命令可以有0的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="38a7e-142">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="38a7e-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="38a7e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38a7e-144">**使用指令碼命令**</span><span class="sxs-lookup"><span data-stu-id="38a7e-144">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 





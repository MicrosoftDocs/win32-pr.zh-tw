---
title: IAgentCharacter 準備
description: IAgentCharacter 準備
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eebee8d2ea99c8782e9506e0e4a812cfb277487
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023442"
---
# <a name="iagentcharacterprepare"></a><span data-ttu-id="1c146-103">IAgentCharacter：:P 準備</span><span class="sxs-lookup"><span data-stu-id="1c146-103">IAgentCharacter::Prepare</span></span>

<span data-ttu-id="1c146-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="1c146-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="1c146-105">抓取字元的動畫資料。</span><span class="sxs-lookup"><span data-stu-id="1c146-105">Retrieves animation data for a character.</span></span>

-   <span data-ttu-id="1c146-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="1c146-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="1c146-107">當函式傳回時， *pdwReqID* 會包含要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c146-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="1c146-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span><span class="sxs-lookup"><span data-stu-id="1c146-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span></span>
</dt> <dd>

<span data-ttu-id="1c146-109">值，表示要載入的動畫資料類型，必須是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="1c146-109">A value that indicates the animation data type to load that must be one of the following:</span></span>



| <span data-ttu-id="1c146-110">值</span><span class="sxs-lookup"><span data-stu-id="1c146-110">Value</span></span>                                                           | <span data-ttu-id="1c146-111">描述</span><span class="sxs-lookup"><span data-stu-id="1c146-111">Description</span></span>                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1c146-112">**const 不帶正負號簡短\*\*\*\*準備 \_ 動畫 = 0;**</span><span class="sxs-lookup"><span data-stu-id="1c146-112">**const unsigned short** **PREPARE\_ANIMATION = 0;**</span></span><br/> | <span data-ttu-id="1c146-113">字元的動畫資料。</span><span class="sxs-lookup"><span data-stu-id="1c146-113">A character's animation data.</span></span>                              |
| <span data-ttu-id="1c146-114">**const 不帶正負號簡短\*\*\*\*準備 \_ 狀態 = 1;**</span><span class="sxs-lookup"><span data-stu-id="1c146-114">**const unsigned short** **PREPARE\_STATE = 1;**</span></span><br/>     | <span data-ttu-id="1c146-115">字元的狀態資料。</span><span class="sxs-lookup"><span data-stu-id="1c146-115">A character's state data.</span></span>                                  |
| <span data-ttu-id="1c146-116">**const 不帶正負號簡短\*\*\*\*準備 \_ WAVE = 2**</span><span class="sxs-lookup"><span data-stu-id="1c146-116">**const unsigned short** **PREPARE\_WAVE = 2**</span></span><br/>       | <span data-ttu-id="1c146-117">字元的音效檔 (。WAV 或。LWV 適用于語音輸出的) 。</span><span class="sxs-lookup"><span data-stu-id="1c146-117">A character's sound file (.WAV or .LWV) for spoken output.</span></span> |



 

</dd> <dt>

<span data-ttu-id="1c146-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span><span class="sxs-lookup"><span data-stu-id="1c146-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="1c146-119">動畫或狀態的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c146-119">The name of the animation or state.</span></span>

<span data-ttu-id="1c146-120">動畫名稱是以使用 Microsoft Agent 字元編輯器儲存時為字元所定義的名稱為基礎。</span><span class="sxs-lookup"><span data-stu-id="1c146-120">The animation name is based on that defined for the character when it was saved using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="1c146-121">針對狀態，此值可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="1c146-121">For states, the value can be one of the following:</span></span>



|                      |                                                 |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="1c146-122">**"Gesturing"**</span><span class="sxs-lookup"><span data-stu-id="1c146-122">**"Gesturing"**</span></span>      | <span data-ttu-id="1c146-123">取得所有 **Gesturing** 狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-123">To retrieve all **Gesturing** state animations.</span></span> |
| <span data-ttu-id="1c146-124">**"GesturingDown"**</span><span class="sxs-lookup"><span data-stu-id="1c146-124">**"GesturingDown"**</span></span>  | <span data-ttu-id="1c146-125">取出 **GesturingDown** 動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-125">To retrieve **GesturingDown** animations.</span></span>       |
| <span data-ttu-id="1c146-126">**"GesturingLeft"**</span><span class="sxs-lookup"><span data-stu-id="1c146-126">**"GesturingLeft"**</span></span>  | <span data-ttu-id="1c146-127">取出 **GesturingLeft** 動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-127">To retrieve **GesturingLeft** animations.</span></span>       |
| <span data-ttu-id="1c146-128">**"GesturingRight"**</span><span class="sxs-lookup"><span data-stu-id="1c146-128">**"GesturingRight"**</span></span> | <span data-ttu-id="1c146-129">取出 **GesturingRight** 動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-129">To retrieve **GesturingRight** animations.</span></span>      |
| <span data-ttu-id="1c146-130">**"GesturingUp"**</span><span class="sxs-lookup"><span data-stu-id="1c146-130">**"GesturingUp"**</span></span>    | <span data-ttu-id="1c146-131">取出 **GesturingUp** 動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-131">To retrieve **GesturingUp** animations.</span></span>         |
| <span data-ttu-id="1c146-132">**隱匿**</span><span class="sxs-lookup"><span data-stu-id="1c146-132">**"Hiding"**</span></span>         | <span data-ttu-id="1c146-133">取得 **隱藏** 狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-133">To retrieve the **Hiding** state animations.</span></span>    |
| <span data-ttu-id="1c146-134">**聽覺**</span><span class="sxs-lookup"><span data-stu-id="1c146-134">**"Hearing"**</span></span>        | <span data-ttu-id="1c146-135">取出 **聽力** 狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-135">To retrieve the **Hearing** state animations.</span></span>   |
| <span data-ttu-id="1c146-136">**閒置**</span><span class="sxs-lookup"><span data-stu-id="1c146-136">**"Idling"**</span></span>         | <span data-ttu-id="1c146-137">取得所有 **閒置** 狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-137">To retrieve all **Idling** state animations.</span></span>    |
| <span data-ttu-id="1c146-138">**"IdlingLevel1"**</span><span class="sxs-lookup"><span data-stu-id="1c146-138">**"IdlingLevel1"**</span></span>   | <span data-ttu-id="1c146-139">取得所有 **IdlingLevel1** 動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-139">To retrieve all **IdlingLevel1** animations.</span></span>    |
| <span data-ttu-id="1c146-140">**"IdlingLevel2"**</span><span class="sxs-lookup"><span data-stu-id="1c146-140">**"IdlingLevel2"**</span></span>   | <span data-ttu-id="1c146-141">取得所有 **IdlingLevel2** 動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-141">To retrieve all **IdlingLevel2** animations.</span></span>    |
| <span data-ttu-id="1c146-142">**"IdlingLevel3"**</span><span class="sxs-lookup"><span data-stu-id="1c146-142">**"IdlingLevel3"**</span></span>   | <span data-ttu-id="1c146-143">取得所有 **IdlingLevel3** 動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-143">To retrieve all **IdlingLevel3** animations.</span></span>    |
| <span data-ttu-id="1c146-144">**欣賞**</span><span class="sxs-lookup"><span data-stu-id="1c146-144">**"Listening"**</span></span>      | <span data-ttu-id="1c146-145">以取出 **接聽** 狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-145">To retrieve the **Listening** state animations.</span></span> |
| <span data-ttu-id="1c146-146">**移動**</span><span class="sxs-lookup"><span data-stu-id="1c146-146">**"Moving"**</span></span>         | <span data-ttu-id="1c146-147">取得所有 **移動** 狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-147">To retrieve all **Moving** state animations.</span></span>    |
| <span data-ttu-id="1c146-148">**"MovingDown"**</span><span class="sxs-lookup"><span data-stu-id="1c146-148">**"MovingDown"**</span></span>     | <span data-ttu-id="1c146-149">取得所有 **移動** 動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-149">To retrieve all **Moving** animations.</span></span>          |
| <span data-ttu-id="1c146-150">**"MovingLeft"**</span><span class="sxs-lookup"><span data-stu-id="1c146-150">**"MovingLeft"**</span></span>     | <span data-ttu-id="1c146-151">取得所有 **MovingLeft** 動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-151">To retrieve all **MovingLeft** animations.</span></span>      |
| <span data-ttu-id="1c146-152">**"MovingRight"**</span><span class="sxs-lookup"><span data-stu-id="1c146-152">**"MovingRight"**</span></span>    | <span data-ttu-id="1c146-153">取得所有 **MovingRight** 動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-153">To retrieve all **MovingRight** animations.</span></span>     |
| <span data-ttu-id="1c146-154">**"MovingUp"**</span><span class="sxs-lookup"><span data-stu-id="1c146-154">**"MovingUp"**</span></span>       | <span data-ttu-id="1c146-155">取得所有 **MovingUp** 動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-155">To retrieve all **MovingUp** animations.</span></span>        |
| <span data-ttu-id="1c146-156">**男**</span><span class="sxs-lookup"><span data-stu-id="1c146-156">**"Showing"**</span></span>        | <span data-ttu-id="1c146-157">取得 **顯示** 狀態動畫的。</span><span class="sxs-lookup"><span data-stu-id="1c146-157">To retrieve the **Showing** state animations.</span></span>   |
| <span data-ttu-id="1c146-158">**說話**</span><span class="sxs-lookup"><span data-stu-id="1c146-158">**"Speaking"**</span></span>       | <span data-ttu-id="1c146-159">取得 **說話** 狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-159">To retrieve the **Speaking** state animations.</span></span>  |



 

<span data-ttu-id="1c146-160">出於.WAV 檔，請將 *bszName* 設定為的 URL 或檔案規格。WAV 檔。</span><span class="sxs-lookup"><span data-stu-id="1c146-160">For .WAV files, set *bszName* to the URL or file specification for the .WAV file.</span></span> <span data-ttu-id="1c146-161">如果規格未完成，則會將它解讀為相對於 [**Load**](https://www.bing.com/search?q=**Load**) 方法中所使用的規格。</span><span class="sxs-lookup"><span data-stu-id="1c146-161">If the specification is not complete, it is interpreted as being relative to the specification used in the [**Load**](https://www.bing.com/search?q=**Load**) method.</span></span>

</dd> <dt>

<span data-ttu-id="1c146-162"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span><span class="sxs-lookup"><span data-stu-id="1c146-162"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span></span>
</dt> <dd>

<span data-ttu-id="1c146-163">布林值，指定伺服器是否將 [**準備**](/windows/desktop/lwef/iagentcharacter--prepare) 要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="1c146-163">A Boolean specifying whether the server queues the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request.</span></span> <span data-ttu-id="1c146-164">**True** 會將要求排入佇列，並讓其後的任何動畫要求等到它所指定的動畫資料載入為止。</span><span class="sxs-lookup"><span data-stu-id="1c146-164">**True** queues the request and causes any animation request that follows it to wait until the animation data it specifies is loaded.</span></span> <span data-ttu-id="1c146-165">**False** 會以非同步方式抓取動畫資料。</span><span class="sxs-lookup"><span data-stu-id="1c146-165">**False** retrieves the animation data asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="1c146-166"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="1c146-166"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="1c146-167">接收 [**準備**](/windows/desktop/lwef/iagentcharacter--prepare) 要求識別碼之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="1c146-167">Address of a variable that receives the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="1c146-168">如果您使用 HTTP 通訊協定載入字元 (。ACF 檔) ，您必須先使用「 [**準備**](/windows/desktop/lwef/iagentcharacter--prepare) 」方法來取出動畫資料，然後才能播放動畫。</span><span class="sxs-lookup"><span data-stu-id="1c146-168">If you load a character using the HTTP protocol (an .ACF file), you must use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to retrieve animation data before you can play the animation.</span></span> <span data-ttu-id="1c146-169">如果您使用 UNC 通訊協定將字元載入 (，就不能使用這個方法。ACS 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="1c146-169">You cannot use this method if you loaded the character using the UNC protocol (an .ACS file).</span></span> <span data-ttu-id="1c146-170">如果您使用 UNC 通訊協定 ( 載入該字元，您也無法使用「 **準備** 」來抓取字元的 HTTP 資料。) 的 ACS 字元檔。</span><span class="sxs-lookup"><span data-stu-id="1c146-170">You also cannot retrieve HTTP data for a character using **Prepare** if you loaded that character using the UNC protocol (.ACS character file).</span></span>

<span data-ttu-id="1c146-171">以 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 方法取出的動畫或音效資料會儲存在瀏覽器的快取中。</span><span class="sxs-lookup"><span data-stu-id="1c146-171">Animation or sound data retrieved with the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method is stored in the browser's cache.</span></span> <span data-ttu-id="1c146-172">後續的呼叫將會檢查快取，如果動畫資料已經存在，控制項會直接從快取載入資料。</span><span class="sxs-lookup"><span data-stu-id="1c146-172">Subsequent calls will check the cache, and if the animation data is already there, the control loads the data directly from the cache.</span></span> <span data-ttu-id="1c146-173">載入之後，您可以使用 [**Play**](/windows/desktop/lwef/iagentcharacter--play) 或 [**朗讀**](/windows/desktop/lwef/iagentcharacter--speak) 方法來播放動畫或音效資料。</span><span class="sxs-lookup"><span data-stu-id="1c146-173">Once loaded, the animation or sound data can be played with the [**Play**](/windows/desktop/lwef/iagentcharacter--play) or [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) methods.</span></span>

<span data-ttu-id="1c146-174">您可以使用逗號分隔來指定多個動畫和狀態。</span><span class="sxs-lookup"><span data-stu-id="1c146-174">You can specify multiple animations and states by separating them with commas.</span></span> <span data-ttu-id="1c146-175">不過，您無法在相同的 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 語句中混合類型。</span><span class="sxs-lookup"><span data-stu-id="1c146-175">However, you cannot mix types in the same [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) statement.</span></span>

 


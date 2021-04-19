---
title: " (WMP SDK) 的事件元素"
description: 事件元素會定義在收到標記為事件的指令碼命令時，Windows Media Player 所採取的行為或動作。
ms.assetid: d12af3bd-a63e-4022-aa84-0386eeef1390
keywords:
- 事件元素 Windows Media Player
topic_type:
- apiref
api_name:
- EVENT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befc5f8462f66c1b3fbe37f0acf1a35e7f704fbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989698"
---
# <a name="event-element"></a><span data-ttu-id="f40df-104">EVENT 元素</span><span class="sxs-lookup"><span data-stu-id="f40df-104">EVENT Element</span></span>

<span data-ttu-id="f40df-105">**事件** 元素會定義在收到標記為事件的指令碼命令時，Windows Media Player 所採取的行為或動作。</span><span class="sxs-lookup"><span data-stu-id="f40df-105">The **EVENT** element defines a behavior or action taken by Windows Media Player when it receives a script command labeled as an event.</span></span>

``` syntax
<EVENT   
   NAME = "text string"
   WHENDONE = "RESUME" | "NEXT" | "BREAK"
>
</EVENT>
```

## <a name="attributes"></a><span data-ttu-id="f40df-106">屬性</span><span class="sxs-lookup"><span data-stu-id="f40df-106">Attributes</span></span>

<span data-ttu-id="f40df-107">需要 (**名稱**) </span><span class="sxs-lookup"><span data-stu-id="f40df-107">**NAME** (required)</span></span>

<span data-ttu-id="f40df-108">事件的名稱。</span><span class="sxs-lookup"><span data-stu-id="f40df-108">The name of the event.</span></span>

<span data-ttu-id="f40df-109">**WHENDONE** (必要) </span><span class="sxs-lookup"><span data-stu-id="f40df-109">**WHENDONE** (required)</span></span>

<span data-ttu-id="f40df-110">值，這個值會定義播放參考內容之後的 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="f40df-110">A value that defines what Windows Media Player does after playing the referenced content.</span></span>

<span data-ttu-id="f40df-111">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="f40df-111">The following values are possible.</span></span>



| <span data-ttu-id="f40df-112">值</span><span class="sxs-lookup"><span data-stu-id="f40df-112">Value</span></span>  | <span data-ttu-id="f40df-113">描述</span><span class="sxs-lookup"><span data-stu-id="f40df-113">Description</span></span>                                                                                                                                                                                                                     |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f40df-114">RESUME</span><span class="sxs-lookup"><span data-stu-id="f40df-114">RESUME</span></span> | <span data-ttu-id="f40df-115">目前的專案 (由事件中斷的剪輯，) 繼續播放。</span><span class="sxs-lookup"><span data-stu-id="f40df-115">The current entry (the clip interrupted by the event) resumes playing.</span></span> <span data-ttu-id="f40df-116">如果內容是儲存的內容，它會在停止的相同時間點繼續;如果內容是廣播，則會在目前的位置繼續進行。</span><span class="sxs-lookup"><span data-stu-id="f40df-116">If the content is stored content, it resumes at the same point where it stopped; if the content is broadcast, it resumes at the current position.</span></span>        |
| <span data-ttu-id="f40df-117">NEXT</span><span class="sxs-lookup"><span data-stu-id="f40df-117">NEXT</span></span>   | <span data-ttu-id="f40df-118">下一個 **專案專案** 的播放方式，就像事件尚未發生，且 Windows Media Player 已到達目前剪輯的結尾。</span><span class="sxs-lookup"><span data-stu-id="f40df-118">The next **ENTRY** element plays as if the event had not occurred and Windows Media Player had reached the end of the current clip.</span></span>                                                                                             |
| <span data-ttu-id="f40df-119">BREAK</span><span class="sxs-lookup"><span data-stu-id="f40df-119">BREAK</span></span>  | <span data-ttu-id="f40df-120">如果目前的專案是在 **重複** 迴圈內，則迴圈會結束，就像重複計數已完成一樣。</span><span class="sxs-lookup"><span data-stu-id="f40df-120">If the current entry is within a **REPEAT** loop, the loop terminates as if the repeat count had been completed.</span></span> <span data-ttu-id="f40df-121">否則，Windows Media Player 會跳到播放清單的結尾，如同最後一個專案如往常般完成一樣。</span><span class="sxs-lookup"><span data-stu-id="f40df-121">Otherwise, Windows Media Player jumps to the end of the playlist as if the final entry had completed as usual.</span></span> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="f40df-122">父/子項目</span><span class="sxs-lookup"><span data-stu-id="f40df-122">Parent/Child Elements</span></span>



| <span data-ttu-id="f40df-123">階層</span><span class="sxs-lookup"><span data-stu-id="f40df-123">Hierarchy</span></span>       | <span data-ttu-id="f40df-124">元素</span><span class="sxs-lookup"><span data-stu-id="f40df-124">Elements</span></span>                |
|-----------------|-------------------------|
| <span data-ttu-id="f40df-125">父元素</span><span class="sxs-lookup"><span data-stu-id="f40df-125">Parent elements</span></span> | <span data-ttu-id="f40df-126">**.ASX**</span><span class="sxs-lookup"><span data-stu-id="f40df-126">**ASX**</span></span>                 |
| <span data-ttu-id="f40df-127">子元素</span><span class="sxs-lookup"><span data-stu-id="f40df-127">Child elements</span></span>  | <span data-ttu-id="f40df-128">**ENTRY**、 **ENTRYREF**</span><span class="sxs-lookup"><span data-stu-id="f40df-128">**ENTRY**, **ENTRYREF**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f40df-129">備註</span><span class="sxs-lookup"><span data-stu-id="f40df-129">Remarks</span></span>

<span data-ttu-id="f40df-130">此元素會定義在收到標記為事件的指令碼命令時，Windows Media Player 所採取的行為或動作。</span><span class="sxs-lookup"><span data-stu-id="f40df-130">This element defines a behavior or action taken by Windows Media Player when it receives a script command labeled as an event.</span></span> <span data-ttu-id="f40df-131">事件是內嵌于資料流程的特定類型指令碼命令，會傳送至包含雙字串的 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="f40df-131">An event is a particular type of script command embedded in a stream sent to Windows Media Player that consists of a double string.</span></span> <span data-ttu-id="f40df-132">第一個字串是 "event" 這個字，而第二個字串則是事件名稱。</span><span class="sxs-lookup"><span data-stu-id="f40df-132">The first string is the word "event", and the second string is the event name.</span></span> <span data-ttu-id="f40df-133">第二個字串中的事件名稱必須符合中繼檔中定義的事件名稱。</span><span class="sxs-lookup"><span data-stu-id="f40df-133">The event name in the second string must match the event name defined in the metafile.</span></span> <span data-ttu-id="f40df-134"> (比對不區分大小寫。 ) 事件可以傳送至 Windows Media Player 接收即時串流，或是儲存在以隨選單播串流形式傳遞的 .asf、.wma 或 .wmv 檔案中。</span><span class="sxs-lookup"><span data-stu-id="f40df-134">(The match is not case-sensitive.) Events can be sent to Windows Media Player receiving a real-time stream, or can be saved in an .asf, .wma, or .wmv file that gets delivered as an on-demand unicast stream.</span></span> <span data-ttu-id="f40df-135">當 Windows Media Player 收到指令碼命令時，它會處理事件，如 **事件** 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="f40df-135">When Windows Media Player receives the script command, it processes the event as defined by the **EVENT** element.</span></span>

<span data-ttu-id="f40df-136">這個元素會定義每次 Windows Media Player 收到具有命名事件的指令碼命令時所處理的專案或 **ENTRYREF** **專案** 範圍。</span><span class="sxs-lookup"><span data-stu-id="f40df-136">This element defines a scope of **ENTRY** or **ENTRYREF** elements that are processed whenever Windows Media Player receives the script command with the named event.</span></span> <span data-ttu-id="f40df-137">**ENTRYREF** 可以是指向 ASP 頁面的 URL。</span><span class="sxs-lookup"><span data-stu-id="f40df-137">The **ENTRYREF** can be a URL that points to an ASP page.</span></span> <span data-ttu-id="f40df-138">您可以使用此元素，以近乎即時的方式指定串流切換的行為，而不是使用其他內容片段或 Windows Media 中繼檔的參考，預先撰寫的資料流程變更。</span><span class="sxs-lookup"><span data-stu-id="f40df-138">With this element, you can specify a behavior for stream switching in near real time, as opposed to pre-authored stream changes using references to other pieces of content or Windows Media metafiles.</span></span>

<span data-ttu-id="f40df-139">當您使用 ASP 頁面產生播放清單時，必須指定 *回應* 的值。**ContentType** 屬性和 *回應*。ASP 頁面中的 **expires** 屬性，因為 Windows Media Player 的延遲問題。</span><span class="sxs-lookup"><span data-stu-id="f40df-139">When you use ASP pages to generate playlists, you must specify a value for the *Response*.**ContentType** property and the *Response*.**expires** property in the ASP page because of latency issues with Windows Media Player.</span></span> <span data-ttu-id="f40df-140">*回應*。**ContentType** 必須是有效的 Windows Media 中繼檔副檔名。</span><span class="sxs-lookup"><span data-stu-id="f40df-140">The *Response*.**ContentType** must be a valid file name extension for Windows Media metafiles.</span></span> <span data-ttu-id="f40df-141">有效類型包括 .asf、.asx、.wma、. 地板蠟、.wmv 和. 300k.wvx。</span><span class="sxs-lookup"><span data-stu-id="f40df-141">Valid types include .asf, .asx, .wma, .wax, .wmv, and .wvx.</span></span>

<span data-ttu-id="f40df-142">如需在 ASP 中使用 **回應** 物件的詳細資訊，請參閱 Platform SDK。</span><span class="sxs-lookup"><span data-stu-id="f40df-142">See the Platform SDK for details about using the **Response** object in ASP.</span></span>

<span data-ttu-id="f40df-143">這個元素可以出現在 **ASX** 元素內的任何位置。</span><span class="sxs-lookup"><span data-stu-id="f40df-143">This element can appear anywhere within the **ASX** element.</span></span> <span data-ttu-id="f40df-144">如果 **asx** 專案中有多個 **事件** 元素的 **名稱** 屬性具有相同的值，Windows Media Player 會使用 **ASX** 元素內的第一個相符專案，並忽略所有其他專案。</span><span class="sxs-lookup"><span data-stu-id="f40df-144">If multiple **EVENT** elements within an **ASX** element have identical values for their **NAME** attributes, Windows Media Player uses the first occurrence within the **ASX** element, and ignores all others.</span></span> <span data-ttu-id="f40df-145">當 **事件** 元素有相異的 **名稱** 屬性時，在 **ASX** 元素內的順序並不重要。</span><span class="sxs-lookup"><span data-stu-id="f40df-145">When **EVENT** elements have distinct **NAME** attributes, their order within the **ASX** element does not matter.</span></span>

<span data-ttu-id="f40df-146">Windows Media Player 會捨棄它在處理另一個事件時所收到的事件。</span><span class="sxs-lookup"><span data-stu-id="f40df-146">Windows Media Player discards events it receives while processing another event.</span></span> <span data-ttu-id="f40df-147">不支援事件的嵌套。</span><span class="sxs-lookup"><span data-stu-id="f40df-147">Nesting of events is not supported.</span></span> <span data-ttu-id="f40df-148">當 Windows Media Player 處於預覽模式時，事件內容不受 **PREVIEWDURATION** 元素的限制;即使作用中 **專案專案** 的預覽持續時間在事件結束之前過期，也可以播放事件內容的完整長度。</span><span class="sxs-lookup"><span data-stu-id="f40df-148">When Windows Media Player is in preview mode, event content is not constrained by the **PREVIEWDURATION** element; the full length of event content can play even if the preview duration for the active **ENTRY** element expires prior to the end of the event.</span></span>

## <a name="examples"></a><span data-ttu-id="f40df-149">範例</span><span class="sxs-lookup"><span data-stu-id="f40df-149">Examples</span></span>

<span data-ttu-id="f40df-150">在此範例中，當 Windows Media Player 在其呈現的串流媒體中收到指令碼命令事件和命令字串 "Adlink" 時，它會在播放清單中搜尋 **事件名稱** "Adlink"。</span><span class="sxs-lookup"><span data-stu-id="f40df-150">In this example, when Windows Media Player receives the script command EVENT and command string "Adlink" in the streaming media it is rendering, it searches the playlist for an **EVENTNAME** "Adlink".</span></span> <span data-ttu-id="f40df-151">Windows Media Player 從正在轉譯的資料流程切換，並播放 **事件** 中所參考的內容： " https://example.microsoft.com/adlink.htm "。</span><span class="sxs-lookup"><span data-stu-id="f40df-151">Windows Media Player switches from the stream it is rendering and plays the content referenced in the **EVENT**, "https://example.microsoft.com/adlink.htm".</span></span>

<span data-ttu-id="f40df-152">**專案** 屬性 **CLIENTSKIP** 設定為 [否]，以防止略過 **事件** 剪輯。</span><span class="sxs-lookup"><span data-stu-id="f40df-152">**ENTRY** attribute **CLIENTSKIP** is set to NO to prevent the **EVENT** clip from being skipped.</span></span> <span data-ttu-id="f40df-153">必須加以播放。</span><span class="sxs-lookup"><span data-stu-id="f40df-153">It must be played.</span></span>

<span data-ttu-id="f40df-154">腳本 `WHENDONE="RESUME"` 會指示 Windows Media Player 在 Adlink 完成時，繼續播放先前切換的媒體。</span><span class="sxs-lookup"><span data-stu-id="f40df-154">The script `WHENDONE="RESUME"` instructs Windows Media Player to resume playing the previous media it switched from as soon as Adlink.asf is finished.</span></span>


```XML
<ASX VERSION="3.0">
<ENTRY CLIENTSKIP="NO">
   <REF HREF="https://example.microsoft.com/clip1.asf" />
</ENTRY>
<EVENT NAME="Adlink" WHENDONE="RESUME">
   <ENTRYREF HREF="https://example.microsoft.com/adlink.htm" 
       CLIENTSKIP="NO" />
</EVENT>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="f40df-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="f40df-155">Requirements</span></span>



| <span data-ttu-id="f40df-156">需求</span><span class="sxs-lookup"><span data-stu-id="f40df-156">Requirement</span></span> | <span data-ttu-id="f40df-157">值</span><span class="sxs-lookup"><span data-stu-id="f40df-157">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f40df-158">版本</span><span class="sxs-lookup"><span data-stu-id="f40df-158">Version</span></span><br/> | <span data-ttu-id="f40df-159">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="f40df-159">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f40df-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f40df-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f40df-161">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="f40df-161">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="f40df-162">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="f40df-162">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> <dt>

[<span data-ttu-id="f40df-163">**Windows Media Player 物件模型**</span><span class="sxs-lookup"><span data-stu-id="f40df-163">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 






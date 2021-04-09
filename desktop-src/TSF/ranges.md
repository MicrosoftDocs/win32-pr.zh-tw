---
title: 範圍
description: 範圍
ms.assetid: 7488e29e-3409-4db3-98b4-f3438ad7c94e
keywords:
- 文字服務架構 (TSF) 、範圍
- TSF (文字服務架構) ，範圍
- 文字服務，範圍
- 啟用 TSF 的應用程式，範圍
- 範圍
- 文字服務架構 (TSF) 、錨點
- TSF (文字服務架構) 、錨點
- 文字服務，錨點
- 啟用 TSF 的應用程式，錨點
- 錨點
- 文字服務架構 (TSF) ，複製
- TSF (文字服務架構) ，複製
- 文字服務，複製
- 啟用 TSF 的應用程式，複製
- 克隆
- 文字服務架構 (TSF) ，備份
- TSF (文字服務架構) ，備份
- 文字服務，備份
- 啟用 TSF 的應用程式，備份
- backups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6430f28731f95c0ad9c1beb04b31f0600b8c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932554"
---
# <a name="ranges"></a><span data-ttu-id="be658-123">範圍</span><span class="sxs-lookup"><span data-stu-id="be658-123">Ranges</span></span>

## <a name="anchors"></a><span data-ttu-id="be658-124">錨點</span><span class="sxs-lookup"><span data-stu-id="be658-124">Anchors</span></span>

<span data-ttu-id="be658-125">範圍是由兩個 *錨* 點（開始錨點和結束錨點）所分隔。</span><span class="sxs-lookup"><span data-stu-id="be658-125">A range is delimited by two *anchors*, a start anchor and an end anchor.</span></span> <span data-ttu-id="be658-126">錨點存在於兩個字元之間的虛數中。</span><span class="sxs-lookup"><span data-stu-id="be658-126">An anchor exists in an imaginary slot between two characters.</span></span> <span data-ttu-id="be658-127">[開始] 錨點與錨點後面的文字相關，而端點錨點與錨點前面的文字相關。</span><span class="sxs-lookup"><span data-stu-id="be658-127">The start anchor relates to text that follows the anchor and the end anchor relates to text that precedes the anchor.</span></span> <span data-ttu-id="be658-128">開始和結束錨點都可以存在於相同的位置。</span><span class="sxs-lookup"><span data-stu-id="be658-128">Both the start and end anchors can exist in the same location.</span></span> <span data-ttu-id="be658-129">在此情況下，範圍的長度為零。</span><span class="sxs-lookup"><span data-stu-id="be658-129">In this case, the range has zero length.</span></span>

<span data-ttu-id="be658-130">例如，以下列文字開頭：</span><span class="sxs-lookup"><span data-stu-id="be658-130">For example, start with the following text:</span></span>


```C++
This is text.
```



<span data-ttu-id="be658-131">現在將範圍套用至具有起點和結尾錨點（位於位置0）的這個文字。</span><span class="sxs-lookup"><span data-stu-id="be658-131">Now apply a range to this text with both the start and end anchors at position 0.</span></span> <span data-ttu-id="be658-132">它會以視覺化方式呈現：</span><span class="sxs-lookup"><span data-stu-id="be658-132">It is visually represented as:</span></span>


```C++
<anchor></anchor>This is text.
```



<span data-ttu-id="be658-133">錨點不會佔用文字本身內的任何空間。</span><span class="sxs-lookup"><span data-stu-id="be658-133">The anchors do not take up any space within the text itself.</span></span> <span data-ttu-id="be658-134">這是長度為零的範圍，其文字為空白。</span><span class="sxs-lookup"><span data-stu-id="be658-134">This is a zero-length range and its text is empty.</span></span>

<span data-ttu-id="be658-135">現在將結束錨點 + 3 個位置移位。</span><span class="sxs-lookup"><span data-stu-id="be658-135">Now shift the end anchor +3 positions.</span></span> <span data-ttu-id="be658-136">它會以視覺化方式呈現：</span><span class="sxs-lookup"><span data-stu-id="be658-136">It is visually represented as:</span></span>


```C++
<anchor>Thi</anchor>s is text.
```



<span data-ttu-id="be658-137">開始錨點位於位置0的字元之前，而結束錨點則位於位置3的字元之後，因為結束錨點已移至右邊的3個位置。</span><span class="sxs-lookup"><span data-stu-id="be658-137">The start anchor is positioned just before the character in position 0 and the end anchor is positioned just after the character in position 3 because the end anchor moved to the right 3 places.</span></span> <span data-ttu-id="be658-138">文字範圍現在是 "Thi"。</span><span class="sxs-lookup"><span data-stu-id="be658-138">The range of text is now "Thi".</span></span>

<span data-ttu-id="be658-139">此外，您無法在結束錨點之後進行啟動錨點，也無法在起始錨點前面建立端點錨點。</span><span class="sxs-lookup"><span data-stu-id="be658-139">Additionally, the start anchor cannot be made to follow the end anchor and the end anchor cannot be made to precede the start anchor.</span></span>

## <a name="anchor-gravity"></a><span data-ttu-id="be658-140">錨點引力</span><span class="sxs-lookup"><span data-stu-id="be658-140">Anchor Gravity</span></span>

<span data-ttu-id="be658-141">每個錨點都有一個 *重力* 設定，可決定當文字插入文字資料流程的錨點位置時，錨點的回應方式。</span><span class="sxs-lookup"><span data-stu-id="be658-141">Each anchor has a *gravity* setting that determines how the anchor responds when text is inserted into the text stream at the anchor position.</span></span> <span data-ttu-id="be658-142">在錨點的位置進行插入時，必須在錨點的位置中進行調整。</span><span class="sxs-lookup"><span data-stu-id="be658-142">When an insertion is made at the position of an anchor, an adjustment must be made in the position of the anchor.</span></span> <span data-ttu-id="be658-143">重心會決定如何調整此錨點位置。</span><span class="sxs-lookup"><span data-stu-id="be658-143">The gravity determines how this anchor position adjustment is made.</span></span>

<span data-ttu-id="be658-144">例如：</span><span class="sxs-lookup"><span data-stu-id="be658-144">For example:</span></span>


```C++
It is <anchor></anchor>cold today.
```



<span data-ttu-id="be658-145">如果在範圍位置插入 "非常" 這個字，則開始錨點可以放置在插入的單字之前或之後：</span><span class="sxs-lookup"><span data-stu-id="be658-145">If the word "very " is inserted at the range position, the start anchor can be positioned either before or after the inserted word:</span></span>


```C++
It is <anchor>very </anchor>cold today.
```



<span data-ttu-id="be658-146">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="be658-146">\- Or -</span></span>


```C++
It is very <anchor></anchor>cold today.
```



<span data-ttu-id="be658-147">錨點重力會指定在插入位置時，錨點重新置放的方式。</span><span class="sxs-lookup"><span data-stu-id="be658-147">The anchor gravity specifies how the anchor is repositioned when an insertion is made at its position.</span></span> <span data-ttu-id="be658-148">重心 *可以是回溯或\*\*轉寄*。</span><span class="sxs-lookup"><span data-stu-id="be658-148">The gravity can be either *backward* or *forward*.</span></span>

<span data-ttu-id="be658-149">如果錨點有回溯引力，則在插入時，錨點會向後移動（相對於插入點），使插入的文字在錨點之後：</span><span class="sxs-lookup"><span data-stu-id="be658-149">If the anchor has backward gravity, the anchor moves backward, relative to the insertion point, on insertion so that the inserted text follows the anchor:</span></span>


```C++
It is <anchor>very </anchor>cold today.
```



<span data-ttu-id="be658-150">如果錨點具有向前引力，則錨點會向前移動 (相對於插入點) 插入點，使插入的文字在錨點之前：</span><span class="sxs-lookup"><span data-stu-id="be658-150">If the anchor has forward gravity, the anchor moves forward (relative to the insertion point) on insertion so that the inserted text precedes the anchor:</span></span>


```C++
It is very <anchor></anchor>cold today.
```



## <a name="clones-and-backups"></a><span data-ttu-id="be658-151">複製和備份</span><span class="sxs-lookup"><span data-stu-id="be658-151">Clones and Backups</span></span>

<span data-ttu-id="be658-152">有兩種方式可以建立範圍物件的「複製」。</span><span class="sxs-lookup"><span data-stu-id="be658-152">There are two ways to make a "copy" of a range object.</span></span> <span data-ttu-id="be658-153">第一個是使用 [ITfRange：： clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone)建立範圍的 *複本*。</span><span class="sxs-lookup"><span data-stu-id="be658-153">The first is to make a *clone* of the range using [ITfRange::Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone).</span></span> <span data-ttu-id="be658-154">第二個則是使用 [ITfCoNtext：： CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup)進行範圍 *備份*。</span><span class="sxs-lookup"><span data-stu-id="be658-154">The second is to make a *backup* of the range using [ITfContext::CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup).</span></span>

<span data-ttu-id="be658-155">複製是不包含靜態資料之範圍的複本。</span><span class="sxs-lookup"><span data-stu-id="be658-155">A clone is a copy of a range that does not include static data.</span></span> <span data-ttu-id="be658-156">系統會複製範圍的錨點，但複製仍會涵蓋內容中的文字範圍。</span><span class="sxs-lookup"><span data-stu-id="be658-156">The anchors of the range are copied, but the clone still covers a range of text within the context.</span></span> <span data-ttu-id="be658-157">複製是所有方面的範圍物件。</span><span class="sxs-lookup"><span data-stu-id="be658-157">A clone is a range object in all respects.</span></span> <span data-ttu-id="be658-158">這表示複製範圍的文字和屬性是動態的，如果複製所涵蓋之範圍的文字及/或屬性變更，則會變更。</span><span class="sxs-lookup"><span data-stu-id="be658-158">This means that the text and properties for a cloned range are dynamic and will change if the text and/or properties of the range covered by the clone changes.</span></span>

<span data-ttu-id="be658-159">備份會在備份做為靜態資料時儲存範圍的文字和屬性。</span><span class="sxs-lookup"><span data-stu-id="be658-159">A backup stores the text and properties of a range at the time the backup is made as static data.</span></span> <span data-ttu-id="be658-160">備份也會複製原始範圍，以便追蹤原始範圍的大小和位置變更。</span><span class="sxs-lookup"><span data-stu-id="be658-160">A backup also clones the original range so that changes to the size and position of the original range can be tracked.</span></span> <span data-ttu-id="be658-161">這表示備份範圍的文字和屬性是靜態的，而且如果備份所涵蓋之範圍的文字及/或屬性變更，則不會變更。</span><span class="sxs-lookup"><span data-stu-id="be658-161">This means that the text and properties for a backed up range are static and do not change if the text and/or properties of the range covered by the backup changes.</span></span>

<span data-ttu-id="be658-162">例如，下列範圍 (在內容中 pRange) ：</span><span class="sxs-lookup"><span data-stu-id="be658-162">For example, the following range (pRange) within the context:</span></span>


```C++
"This is some <pRange>text</pRange>."
```



<span data-ttu-id="be658-163">現在，請複製此範圍並進行備份：</span><span class="sxs-lookup"><span data-stu-id="be658-163">Now make a clone and a backup of this range:</span></span>


```C++
ITfRange *pClone;
ITfRangeBackup *pBackup;

pRange->Clone(&pClone);
pContext->CreateRangeBackup(ec, pRange, &pBackup);
```



<span data-ttu-id="be658-164">現在，物件包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="be658-164">Now, the objects contain the following:</span></span>


```C++
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



<span data-ttu-id="be658-165">現在變更 pRange 的文字：</span><span class="sxs-lookup"><span data-stu-id="be658-165">Now change the text of pRange:</span></span>


```C++
WCHAR wsz[] = L"other words";
pRange->SetText(ec, 0, wsz, lstrlenW(wsz));
```



<span data-ttu-id="be658-166">現在，物件包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="be658-166">Now, the objects contain the following:</span></span>


```C++
Context = "This is some other words."
pRange  = "other words"
pClone  = "other words"
pBackup = "text"
```



<span data-ttu-id="be658-167">設定文字會導致內容中的文字變更。</span><span class="sxs-lookup"><span data-stu-id="be658-167">Setting the text caused the text within the context to change.</span></span> <span data-ttu-id="be658-168">它也會造成 pRange 和 pClone 的結束錨點變更。</span><span class="sxs-lookup"><span data-stu-id="be658-168">It also caused the end anchor of pRange and pClone to change.</span></span> <span data-ttu-id="be658-169">pClone 現在包含「其他文字」，因為在範圍內變更文字，而這些變更會由所有範圍追蹤。</span><span class="sxs-lookup"><span data-stu-id="be658-169">pClone now contains "other words" because the text changed within the range and these changes are tracked by all ranges.</span></span> <span data-ttu-id="be658-170">當 pRange 和 pClone 所涵蓋的文字變更時，pClone 的文字也會變更。</span><span class="sxs-lookup"><span data-stu-id="be658-170">When the text covered by both pRange and pClone changed, the text of pClone changed as well.</span></span>

<span data-ttu-id="be658-171">PBackup 中的文字未與原始 pRange 變更，因為備份中) 的 (資料與內容無關，而且會分開儲存。</span><span class="sxs-lookup"><span data-stu-id="be658-171">The text in pBackup has not changed from the original pRange because the data (text and properties) in the backup is unrelated to the context and is stored separately.</span></span> <span data-ttu-id="be658-172">備份中包含的複製實際上會變更，但資料是靜態的。</span><span class="sxs-lookup"><span data-stu-id="be658-172">The clone contained within the backup does actually change, but the data is static.</span></span>

<span data-ttu-id="be658-173">還原備份時，可以將備份套用到備份內的複製或完全不同的範圍。</span><span class="sxs-lookup"><span data-stu-id="be658-173">When restoring a backup, the backup can be applied to the clone within the backup or to a different range entirely.</span></span> <span data-ttu-id="be658-174">若要將備份套用到備份內的複製，請將 **Null** 傳遞至 [ITfRangeBackup：： Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) ，如下列程式碼範例所示：</span><span class="sxs-lookup"><span data-stu-id="be658-174">To apply the backup to the clone within the backup, pass **NULL** to [ITfRangeBackup::Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) as shown in the following code example:</span></span>


```C++
pBackup->Restore(ec, NULL);
```



<span data-ttu-id="be658-175">現在，物件包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="be658-175">Now, the objects contain the following:</span></span>


```C++
Context = "This is some text."
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



<span data-ttu-id="be658-176">若要將備份還原至不同的範圍，請在呼叫 **ITfRangeBackup：： restore** 時傳遞範圍物件的指標。</span><span class="sxs-lookup"><span data-stu-id="be658-176">To restore the backup to a different range, pass a pointer to the range object when calling **ITfRangeBackup::Restore**.</span></span> <span data-ttu-id="be658-177">備份的文字和屬性將會套用至新的範圍。</span><span class="sxs-lookup"><span data-stu-id="be658-177">The backed up text and properties will be applied to the new range.</span></span> <span data-ttu-id="be658-178">例如，在 **還原** 呼叫之前使用上述範例，將會修改 pRange 以示範這一點：</span><span class="sxs-lookup"><span data-stu-id="be658-178">For example, using the example above prior to the **Restore** call, pRange will be modified to demonstrate this:</span></span>


```C++
LONG lShifted;
pRange->ShiftEnd(ec, -2, &lShifted, NULL);
```



<span data-ttu-id="be658-179">現在，物件包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="be658-179">Now, the objects contain the following:</span></span>


```C++
Context = "This is some other words."
pRange  = "other wor"
pClone  = "other words"
pBackup = "text"
```



<span data-ttu-id="be658-180">當 pRange 的結束錨點移至左邊的兩個位置時，pClone 的結束錨點不會變更。</span><span class="sxs-lookup"><span data-stu-id="be658-180">When the end anchor of pRange was shifted to the left two places, the end anchor of pClone did not change.</span></span>

<span data-ttu-id="be658-181">現在使用 pRange 還原備份，並使用下列程式碼範例：</span><span class="sxs-lookup"><span data-stu-id="be658-181">Now restore the backup using pRange with the following code example:</span></span>


```C++
pBackup->Restore(ec, pRange);
```



<span data-ttu-id="be658-182">現在，物件包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="be658-182">Now, the objects contain the following:</span></span>


```C++
Context = "This is some textds."
pRange  = "text"
pClone  = "textds"
pBackup = "text"
```



<span data-ttu-id="be658-183">PRange 所涵蓋的文字已取代為 "text"、pClone 所涵蓋的部分文字已變更，以及 pBackup 變更以符合 pRange。</span><span class="sxs-lookup"><span data-stu-id="be658-183">The text covered by pRange has been replaced with "text", a portion of the text covered by pClone has changed, and pBackup changes to match pRange.</span></span>

 

 





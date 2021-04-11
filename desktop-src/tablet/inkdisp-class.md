---
description: 表示筆墨空間內所收集的筆墨筆劃。
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: 'InkDisp 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDisp
- InkDisp.IInkDisp
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 429cbf85bdc92753cda1e58a0e89086b4b5b8b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689783"
---
# <a name="inkdisp-class"></a><span data-ttu-id="fdc75-103">InkDisp 類別</span><span class="sxs-lookup"><span data-stu-id="fdc75-103">InkDisp class</span></span>

<span data-ttu-id="fdc75-104">表示筆墨空間內所收集的筆墨筆劃。</span><span class="sxs-lookup"><span data-stu-id="fdc75-104">Represents the collected strokes of ink within an ink space.</span></span>

<span data-ttu-id="fdc75-105">**InkDisp** 具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fdc75-105">**InkDisp** has these types of members:</span></span>

-   [<span data-ttu-id="fdc75-106">事件</span><span class="sxs-lookup"><span data-stu-id="fdc75-106">Events</span></span>](#events)
-   [<span data-ttu-id="fdc75-107">介面</span><span class="sxs-lookup"><span data-stu-id="fdc75-107">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="fdc75-108">方法</span><span class="sxs-lookup"><span data-stu-id="fdc75-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="fdc75-109">屬性</span><span class="sxs-lookup"><span data-stu-id="fdc75-109">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="fdc75-110">事件</span><span class="sxs-lookup"><span data-stu-id="fdc75-110">Events</span></span>

<span data-ttu-id="fdc75-111">**InkDisp** 類別具有這些事件。</span><span class="sxs-lookup"><span data-stu-id="fdc75-111">The **InkDisp** class has these events.</span></span>



| <span data-ttu-id="fdc75-112">事件</span><span class="sxs-lookup"><span data-stu-id="fdc75-112">Event</span></span>                                    | <span data-ttu-id="fdc75-113">描述</span><span class="sxs-lookup"><span data-stu-id="fdc75-113">Description</span></span>                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="fdc75-114">**InkAdded**</span><span class="sxs-lookup"><span data-stu-id="fdc75-114">**InkAdded**</span></span>](inkdisp-inkadded.md)     | <span data-ttu-id="fdc75-115">在將筆劃加入至 **InkDisp** 物件時發生。</span><span class="sxs-lookup"><span data-stu-id="fdc75-115">Occurs when a stroke is added to the **InkDisp** object.</span></span><br/>     |
| [<span data-ttu-id="fdc75-116">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="fdc75-116">**InkDeleted**</span></span>](inkdisp-inkdeleted.md) | <span data-ttu-id="fdc75-117">從 **InkDisp** 物件中刪除筆劃時發生。</span><span class="sxs-lookup"><span data-stu-id="fdc75-117">Occurs when a stroke is deleted from the **InkDisp** object.</span></span><br/> |



 

### <a name="interfaces"></a><span data-ttu-id="fdc75-118">介面</span><span class="sxs-lookup"><span data-stu-id="fdc75-118">Interfaces</span></span>

<span data-ttu-id="fdc75-119">**InkDisp** 類別會定義這些介面。</span><span class="sxs-lookup"><span data-stu-id="fdc75-119">The **InkDisp** class defines these interfaces.</span></span>



| <span data-ttu-id="fdc75-120">介面</span><span class="sxs-lookup"><span data-stu-id="fdc75-120">Interface</span></span>    | <span data-ttu-id="fdc75-121">描述</span><span class="sxs-lookup"><span data-stu-id="fdc75-121">Description</span></span>                                                       |
|:-------------|:------------------------------------------------------------------|
| <span data-ttu-id="fdc75-122">**IInkDisp**</span><span class="sxs-lookup"><span data-stu-id="fdc75-122">**IInkDisp**</span></span> | <span data-ttu-id="fdc75-123">這個物件會實 **IInkDisp** COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fdc75-123">This object implements the **IInkDisp** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="fdc75-124">方法</span><span class="sxs-lookup"><span data-stu-id="fdc75-124">Methods</span></span>

<span data-ttu-id="fdc75-125">**InkDisp** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="fdc75-125">The **InkDisp** class has these methods.</span></span>



| <span data-ttu-id="fdc75-126">方法</span><span class="sxs-lookup"><span data-stu-id="fdc75-126">Method</span></span>                                                                   | <span data-ttu-id="fdc75-127">描述</span><span class="sxs-lookup"><span data-stu-id="fdc75-127">Description</span></span>                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fdc75-128">**AddStrokesAtRectangle**</span><span class="sxs-lookup"><span data-stu-id="fdc75-128">**AddStrokesAtRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | <span data-ttu-id="fdc75-129">將筆劃集合插入 **InkDisp** 物件中指定的矩形。</span><span class="sxs-lookup"><span data-stu-id="fdc75-129">Inserts a stroke collection into the **InkDisp** object at the specified rectangle.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="fdc75-130">**CanPaste**</span><span class="sxs-lookup"><span data-stu-id="fdc75-130">**CanPaste**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | <span data-ttu-id="fdc75-131">指出 [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) 是否可轉換為 **InkDisp** 物件。</span><span class="sxs-lookup"><span data-stu-id="fdc75-131">Indicates whether the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) can be converted to an **InkDisp** object.</span></span><br/>                                                                                       |
| [<span data-ttu-id="fdc75-132">**剪輯**</span><span class="sxs-lookup"><span data-stu-id="fdc75-132">**Clip**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | <span data-ttu-id="fdc75-133">移除矩形外筆劃或筆劃集合的部分。</span><span class="sxs-lookup"><span data-stu-id="fdc75-133">Removes portions of a stroke or collection of strokes that are outside a rectangle.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="fdc75-134">**ClipboardCopy**</span><span class="sxs-lookup"><span data-stu-id="fdc75-134">**ClipboardCopy**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | <span data-ttu-id="fdc75-135">將 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="fdc75-135">Copies the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection to the Clipboard.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="fdc75-136">**ClipboardCopyWithRectangle**</span><span class="sxs-lookup"><span data-stu-id="fdc75-136">**ClipboardCopyWithRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | <span data-ttu-id="fdc75-137">將已知矩形內所包含的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="fdc75-137">Copies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects that are contained within the known rectangle to the Clipboard.</span></span><br/>                                                               |
| [<span data-ttu-id="fdc75-138">**ClipboardPaste**</span><span class="sxs-lookup"><span data-stu-id="fdc75-138">**ClipboardPaste**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | <span data-ttu-id="fdc75-139">將 [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) 從剪貼簿複製到 **InkDisp** 物件。</span><span class="sxs-lookup"><span data-stu-id="fdc75-139">Copies the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) from the Clipboard to the **InkDisp** object.</span></span><br/>                                                                                               |
| [<span data-ttu-id="fdc75-140">**克隆**</span><span class="sxs-lookup"><span data-stu-id="fdc75-140">**Clone**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | <span data-ttu-id="fdc75-141">建立重複的 **InkDisp** 物件。</span><span class="sxs-lookup"><span data-stu-id="fdc75-141">Creates a duplicate **InkDisp** object.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="fdc75-142">**CreateStroke**</span><span class="sxs-lookup"><span data-stu-id="fdc75-142">**CreateStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | <span data-ttu-id="fdc75-143">從點或封包資料建立筆劃。</span><span class="sxs-lookup"><span data-stu-id="fdc75-143">Creates a stroke from points or packet data.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="fdc75-144">**CreateStrokes**</span><span class="sxs-lookup"><span data-stu-id="fdc75-144">**CreateStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | <span data-ttu-id="fdc75-145">建立這個 **InkDisp** 物件的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合。</span><span class="sxs-lookup"><span data-stu-id="fdc75-145">Creates an [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection for this **InkDisp** object.</span></span><br/>                                                                                                |
| [<span data-ttu-id="fdc75-146">**DeleteStroke**</span><span class="sxs-lookup"><span data-stu-id="fdc75-146">**DeleteStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | <span data-ttu-id="fdc75-147">從 **InkDisp** 物件中刪除筆劃。</span><span class="sxs-lookup"><span data-stu-id="fdc75-147">Deletes a stroke from the **InkDisp** object.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="fdc75-148">**DeleteStrokes**</span><span class="sxs-lookup"><span data-stu-id="fdc75-148">**DeleteStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | <span data-ttu-id="fdc75-149">從 **InkDisp** 物件中刪除筆劃。</span><span class="sxs-lookup"><span data-stu-id="fdc75-149">Deletes strokes from the **InkDisp** object.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="fdc75-150">**ExtractStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="fdc75-150">**ExtractStrokes Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | <span data-ttu-id="fdc75-151">從 **InkDisp** 物件中解壓縮筆劃，並傳回新的 **InkDisp** 物件，其中包含已解壓縮的筆劃。</span><span class="sxs-lookup"><span data-stu-id="fdc75-151">Extracts strokes from the **InkDisp** object and returns a new **InkDisp** object containing the extracted strokes.</span></span><br/>                                                                       |
| [<span data-ttu-id="fdc75-152">**ExtractWithRectangle 方法**</span><span class="sxs-lookup"><span data-stu-id="fdc75-152">**ExtractWithRectangle Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | <span data-ttu-id="fdc75-153">從現有的 **InkDisp 類別** 物件剪下或複製筆劃，然後將其貼入新的 **InkDisp 類別** 物件，方法是使用已知的矩形來判斷要解壓縮哪些筆觸。</span><span class="sxs-lookup"><span data-stu-id="fdc75-153">Cuts or copies strokes from an existing **InkDisp Class** object and pastes them into a new **InkDisp Class** object, by using the known rectangle to determine which strokes to extract.</span></span><br/> |
| [<span data-ttu-id="fdc75-154">**GetBoundingBox**</span><span class="sxs-lookup"><span data-stu-id="fdc75-154">**GetBoundingBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | <span data-ttu-id="fdc75-155">抓取 **InkDisp** 物件中所有筆劃的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="fdc75-155">Retrieves the bounding box of all of the strokes in the **InkDisp** object.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="fdc75-156">**HitTestCircle**</span><span class="sxs-lookup"><span data-stu-id="fdc75-156">**HitTestCircle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | <span data-ttu-id="fdc75-157">抓取完全在已知圓形內部或交集的 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合。</span><span class="sxs-lookup"><span data-stu-id="fdc75-157">Retrieves the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that are either completely inside or intersected by a known circle.</span></span><br/>                                                  |
| [<span data-ttu-id="fdc75-158">**HitTestWithLasso**</span><span class="sxs-lookup"><span data-stu-id="fdc75-158">**HitTestWithLasso**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | <span data-ttu-id="fdc75-159">抓取折線選取區域內的筆觸。</span><span class="sxs-lookup"><span data-stu-id="fdc75-159">Retrieves the strokes within a polyline selection area.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="fdc75-160">**HitTestWithRectangle**</span><span class="sxs-lookup"><span data-stu-id="fdc75-160">**HitTestWithRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | <span data-ttu-id="fdc75-161">抓取指定矩形內所包含的筆劃。</span><span class="sxs-lookup"><span data-stu-id="fdc75-161">Retrieves the strokes that are contained within a specified rectangle.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="fdc75-162">**載入**</span><span class="sxs-lookup"><span data-stu-id="fdc75-162">**Load**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | <span data-ttu-id="fdc75-163">使用已知的二進位資料填入新的 **InkDisp** 物件。</span><span class="sxs-lookup"><span data-stu-id="fdc75-163">Populates a new **InkDisp** object with known binary data.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="fdc75-164">**NearestPoint**</span><span class="sxs-lookup"><span data-stu-id="fdc75-164">**NearestPoint**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | <span data-ttu-id="fdc75-165">抓取最接近已知點之 **InkDisp** 物件內的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) ，並選擇性地提供其他資訊。</span><span class="sxs-lookup"><span data-stu-id="fdc75-165">Retrieves the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) within the **InkDisp** object that is nearest to a known point, optionally providing additional information.</span></span><br/>                       |
| [<span data-ttu-id="fdc75-166">**儲存**</span><span class="sxs-lookup"><span data-stu-id="fdc75-166">**Save**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | <span data-ttu-id="fdc75-167">將筆墨轉換成指定的格式，並傳回二進位資料。</span><span class="sxs-lookup"><span data-stu-id="fdc75-167">Converts the ink to a specified format and returns the binary data.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="fdc75-168">屬性</span><span class="sxs-lookup"><span data-stu-id="fdc75-168">Properties</span></span>

<span data-ttu-id="fdc75-169">**InkDisp** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fdc75-169">The **InkDisp** class has these properties.</span></span>



| <span data-ttu-id="fdc75-170">屬性</span><span class="sxs-lookup"><span data-stu-id="fdc75-170">Property</span></span>                                                                           | <span data-ttu-id="fdc75-171">存取類型</span><span class="sxs-lookup"><span data-stu-id="fdc75-171">Access type</span></span>           | <span data-ttu-id="fdc75-172">Description</span><span class="sxs-lookup"><span data-stu-id="fdc75-172">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fdc75-173">**CustomStrokes**</span><span class="sxs-lookup"><span data-stu-id="fdc75-173">**CustomStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | <span data-ttu-id="fdc75-174">唯讀</span><span class="sxs-lookup"><span data-stu-id="fdc75-174">Read-only</span></span><br/>  | <span data-ttu-id="fdc75-175">取得要與筆墨一起保存的 [**IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) 集合。</span><span class="sxs-lookup"><span data-stu-id="fdc75-175">Gets the [**IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) collection to be persisted with the ink.</span></span><br/>                             |
| [<span data-ttu-id="fdc75-176">**髒**</span><span class="sxs-lookup"><span data-stu-id="fdc75-176">**Dirty**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | <span data-ttu-id="fdc75-177">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fdc75-177">Read/write</span></span><br/> | <span data-ttu-id="fdc75-178">取得或設定值，這個值會指出自上一次儲存筆墨之後， **InkDisp** 物件是否已修改。</span><span class="sxs-lookup"><span data-stu-id="fdc75-178">Gets or sets the value that indicates whether an **InkDisp** object has been modified since the last time the ink was saved.</span></span><br/> |
| [<span data-ttu-id="fdc75-179">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="fdc75-179">**ExtendedProperties**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | <span data-ttu-id="fdc75-180">唯讀</span><span class="sxs-lookup"><span data-stu-id="fdc75-180">Read-only</span></span><br/>  | <span data-ttu-id="fdc75-181">取得應用程式定義資料的集合。</span><span class="sxs-lookup"><span data-stu-id="fdc75-181">Gets the collection of application-defined data.</span></span><br/>                                                                             |
| [<span data-ttu-id="fdc75-182">**中風**</span><span class="sxs-lookup"><span data-stu-id="fdc75-182">**Strokes**</span></span>](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | <span data-ttu-id="fdc75-183">唯讀</span><span class="sxs-lookup"><span data-stu-id="fdc75-183">Read-only</span></span><br/>  | <span data-ttu-id="fdc75-184">取得 **InkDisp** 物件中所包含的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合。</span><span class="sxs-lookup"><span data-stu-id="fdc75-184">Gets the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection contained in the **InkDisp** object.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="fdc75-185">備註</span><span class="sxs-lookup"><span data-stu-id="fdc75-185">Remarks</span></span>

<span data-ttu-id="fdc75-186">此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。</span><span class="sxs-lookup"><span data-stu-id="fdc75-186">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

> [!Note]  
> <span data-ttu-id="fdc75-187">這個物件的第一個具現化也會使 GDI + 具現化。</span><span class="sxs-lookup"><span data-stu-id="fdc75-187">The first instantiation of this object causes GDI+ to be instantiated as well.</span></span> <span data-ttu-id="fdc75-188">副作用是，如果您在迴圈中使用單一筆墨物件，並在迴圈中建立和終結它，您將會導致 GDI + 的具現化。</span><span class="sxs-lookup"><span data-stu-id="fdc75-188">A side-effect is that if you are using a single ink object in a loop and create and destroy it within the loop, you will cause GDI+ to be instantiated over and over.</span></span> <span data-ttu-id="fdc75-189">這可能會導致應用程式效能降低。</span><span class="sxs-lookup"><span data-stu-id="fdc75-189">This can cause a performance degradation in your application.</span></span> <span data-ttu-id="fdc75-190">若要避免這種情況，請在應用程式使用筆墨時隨時保留筆墨物件的單一實例。</span><span class="sxs-lookup"><span data-stu-id="fdc75-190">To prevent this, keep a single instance of an ink object at all times while your application is using ink.</span></span>

 

<span data-ttu-id="fdc75-191">**InkDisp** 物件是筆劃 (點) 資料的容器。</span><span class="sxs-lookup"><span data-stu-id="fdc75-191">An **InkDisp** object is a container of stroke (point) data.</span></span> <span data-ttu-id="fdc75-192">筆劃資料（或畫筆所收集的點）會放入 **InkDisp** 物件中。</span><span class="sxs-lookup"><span data-stu-id="fdc75-192">The stroke data, or the points collected by the pen, are put into an **InkDisp** object.</span></span> <span data-ttu-id="fdc75-193">[**筆劃**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)屬性包含 **InkDisp** 物件內所有筆劃的資料。</span><span class="sxs-lookup"><span data-stu-id="fdc75-193">The [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property contains the data for all strokes within the **InkDisp** object.</span></span>

<span data-ttu-id="fdc75-194">[**InkCollector**](inkcollector-class.md)物件、 [**InkOverlay**](inkoverlay-class.md)物件和 [InkPicture](inkpicture-control-reference.md)控制項會收集輸入裝置的點，並將它們放入 **InkDisp** 物件中。</span><span class="sxs-lookup"><span data-stu-id="fdc75-194">The [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, and [InkPicture](inkpicture-control-reference.md) control collects points from the input device and puts them into an **InkDisp** object.</span></span> <span data-ttu-id="fdc75-195">這些物件基本上是做為將筆墨分配至一或多個不同 **InkDisp** 物件的來源，這些物件可作為保存分散式筆墨的容器。</span><span class="sxs-lookup"><span data-stu-id="fdc75-195">These objects essentially act as the source that distributes ink into one or many different **InkDisp** objects, which act as containers that hold the distributed ink.</span></span>

<span data-ttu-id="fdc75-196">筆墨空間是 tablet 內容座標所對應的虛擬座標空間。</span><span class="sxs-lookup"><span data-stu-id="fdc75-196">The ink space is a virtual coordinate space to which the coordinates of the tablet context are mapped.</span></span> <span data-ttu-id="fdc75-197">此空間已固定為 HIMETRIC 座標系統。</span><span class="sxs-lookup"><span data-stu-id="fdc75-197">This space is fixed to a HIMETRIC coordinate system.</span></span> <span data-ttu-id="fdc75-198">在筆墨空間座標中，從0到1的移動等於1個 HIMETRIC 單位。</span><span class="sxs-lookup"><span data-stu-id="fdc75-198">In ink space coordinates, a move from 0 to 1 equals 1 HIMETRIC unit.</span></span> <span data-ttu-id="fdc75-199">此對應可讓您輕鬆地建立多個 **InkDisp** 物件的關聯。</span><span class="sxs-lookup"><span data-stu-id="fdc75-199">This mapping makes it easy to relate multiple **InkDisp** objects.</span></span>

<span data-ttu-id="fdc75-200">[**InkRenderer**](inkrenderer-class.md)物件會管理筆墨與顯示視窗之間的對應。</span><span class="sxs-lookup"><span data-stu-id="fdc75-200">The [**InkRenderer**](inkrenderer-class.md) object manages the mappings between ink and the display window.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdc75-201">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdc75-201">Requirements</span></span>



| <span data-ttu-id="fdc75-202">需求</span><span class="sxs-lookup"><span data-stu-id="fdc75-202">Requirement</span></span> | <span data-ttu-id="fdc75-203">值</span><span class="sxs-lookup"><span data-stu-id="fdc75-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc75-204">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fdc75-204">Minimum supported client</span></span><br/> | <span data-ttu-id="fdc75-205">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdc75-205">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fdc75-206">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fdc75-206">Minimum supported server</span></span><br/> | <span data-ttu-id="fdc75-207">都不支援</span><span class="sxs-lookup"><span data-stu-id="fdc75-207">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fdc75-208">標頭</span><span class="sxs-lookup"><span data-stu-id="fdc75-208">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdc75-209"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="fdc75-209"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fdc75-210">程式庫</span><span class="sxs-lookup"><span data-stu-id="fdc75-210">Library</span></span><br/>                  | <dl> <span data-ttu-id="fdc75-211"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdc75-211"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fdc75-212">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdc75-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdc75-213">**IInkStrokeDisp 介面**</span><span class="sxs-lookup"><span data-stu-id="fdc75-213">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

<span data-ttu-id="fdc75-214">[InkStrokes 集合](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fdc75-214">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fdc75-215">**IInkTablet 介面**</span><span class="sxs-lookup"><span data-stu-id="fdc75-215">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 


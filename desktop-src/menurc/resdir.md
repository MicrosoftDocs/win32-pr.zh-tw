---
title: RESDIR 結構
description: 包含資源群組中個別圖示或游標元件的相關資訊。 每個群組元件都有一個 RESDIR 結構。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\resdir.htm
keywords:
- RESDIR 結構功能表和其他資源
topic_type:
- apiref
api_name:
- RESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b854a4af3367131f6a559e1fef5899fae8b81107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968332"
---
# <a name="resdir-structure"></a><span data-ttu-id="46e33-106">RESDIR 結構</span><span class="sxs-lookup"><span data-stu-id="46e33-106">RESDIR structure</span></span>

<span data-ttu-id="46e33-107">包含資源群組中個別圖示或游標元件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="46e33-107">Contains information about an individual icon or cursor component in a resource group.</span></span> <span data-ttu-id="46e33-108">每個群組元件都有一個 **RESDIR** 結構。</span><span class="sxs-lookup"><span data-stu-id="46e33-108">There is one **RESDIR** structure for each group component.</span></span> <span data-ttu-id="46e33-109">此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="46e33-109">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="46e33-110">語法</span><span class="sxs-lookup"><span data-stu-id="46e33-110">Syntax</span></span>


```C++
typedef struct {
  ICONRESDIR Icon;
  CURSORDIR  Cursor;
  CURSORDIR  Planes;
  CURSORDIR  BitCount;
  CURSORDIR  BytesInRes;
  CURSORDIR  IconCursorId;
} RESDIR;
```



## <a name="members"></a><span data-ttu-id="46e33-111">成員</span><span class="sxs-lookup"><span data-stu-id="46e33-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="46e33-112">**圖示**</span><span class="sxs-lookup"><span data-stu-id="46e33-112">**Icon**</span></span>
</dt> <dd>

<span data-ttu-id="46e33-113">類型： **[ **ICONRESDIR**](iconresdir.md)**</span><span class="sxs-lookup"><span data-stu-id="46e33-113">Type: **[**ICONRESDIR**](iconresdir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46e33-114">指定圖示的寬度、高度和色彩計數。</span><span class="sxs-lookup"><span data-stu-id="46e33-114">The width, height, and color count of the indicated icon.</span></span>

</dd> <dt>

<span data-ttu-id="46e33-115">**資料指標**</span><span class="sxs-lookup"><span data-stu-id="46e33-115">**Cursor**</span></span>
</dt> <dd>

<span data-ttu-id="46e33-116">類型： **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="46e33-116">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46e33-117">指定之游標的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="46e33-117">The width and height of the indicated cursor.</span></span>

</dd> <dt>

<span data-ttu-id="46e33-118">**飛機**</span><span class="sxs-lookup"><span data-stu-id="46e33-118">**Planes**</span></span>
</dt> <dd>

<span data-ttu-id="46e33-119">類型： **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="46e33-119">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46e33-120">圖示或游標點陣圖中的色彩平面數目。</span><span class="sxs-lookup"><span data-stu-id="46e33-120">The number of color planes in the icon or cursor bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="46e33-121">**BitCount**</span><span class="sxs-lookup"><span data-stu-id="46e33-121">**BitCount**</span></span>
</dt> <dd>

<span data-ttu-id="46e33-122">類型： **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="46e33-122">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46e33-123">圖示或游標點陣圖中每個圖元的位數。</span><span class="sxs-lookup"><span data-stu-id="46e33-123">The number of bits per pixel in the icon or cursor bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="46e33-124">**BytesInRes**</span><span class="sxs-lookup"><span data-stu-id="46e33-124">**BytesInRes**</span></span>
</dt> <dd>

<span data-ttu-id="46e33-125">類型： **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="46e33-125">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46e33-126">資源的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="46e33-126">The size of the resource, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="46e33-127">**IconCursorId**</span><span class="sxs-lookup"><span data-stu-id="46e33-127">**IconCursorId**</span></span>
</dt> <dd>

<span data-ttu-id="46e33-128">類型： **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="46e33-128">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46e33-129">具有唯一序數識別碼的圖示或游標。</span><span class="sxs-lookup"><span data-stu-id="46e33-129">The icon or cursor with a unique ordinal identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46e33-130">備註</span><span class="sxs-lookup"><span data-stu-id="46e33-130">Remarks</span></span>

<span data-ttu-id="46e33-131">一或多個 **RESDIR** 結構會緊接在 .res 檔中的 [**NEWHEADER**](newheader.md) 結構後面。</span><span class="sxs-lookup"><span data-stu-id="46e33-131">One or more **RESDIR** structures immediately follow the [**NEWHEADER**](newheader.md) structure in the .res file.</span></span> <span data-ttu-id="46e33-132">**NEWHEADER** 結構的 **ResCount** 成員會指定 **RESDIR** 結構的數目。</span><span class="sxs-lookup"><span data-stu-id="46e33-132">The **ResCount** member of the **NEWHEADER** structure specifies the number of **RESDIR** structures.</span></span> <span data-ttu-id="46e33-133">請注意， **RESDIR** 結構是由 [**ICONRESDIR**](iconresdir.md) 結構或 [**CURSORDIR**](cursordir.md) 結構所組成，後面接著 **平面**、 **BitCount**、 **BytesInRes** 和 **IconCursorId** 成員。</span><span class="sxs-lookup"><span data-stu-id="46e33-133">Note that the **RESDIR** structure consists of either an [**ICONRESDIR**](iconresdir.md) structure or a [**CURSORDIR**](cursordir.md) structure followed by the **Planes**, **BitCount**, **BytesInRes**, and **IconCursorId** members.</span></span> <span data-ttu-id="46e33-134">如果 **RESDIR** 結構包含資料指標的相關資訊，則資源編譯器寫入至 [RT 資料 \_ 指標](/windows/desktop/menurc/resource-types)資源的前兩個 **字** 是 [**LOCALHEADER**](localheader.md)結構的 **xHotSpot** 和 **yHotSpot** 成員。</span><span class="sxs-lookup"><span data-stu-id="46e33-134">If the **RESDIR** structure contains information about a cursor, the first two **WORD** s the resource compiler writes to the [RT\_CURSOR](/windows/desktop/menurc/resource-types) resource are the **xHotSpot** and **yHotSpot** members of the [**LOCALHEADER**](localheader.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="46e33-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="46e33-135">Requirements</span></span>



| <span data-ttu-id="46e33-136">需求</span><span class="sxs-lookup"><span data-stu-id="46e33-136">Requirement</span></span> | <span data-ttu-id="46e33-137">值</span><span class="sxs-lookup"><span data-stu-id="46e33-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="46e33-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46e33-138">Minimum supported client</span></span><br/> | <span data-ttu-id="46e33-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46e33-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="46e33-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46e33-140">Minimum supported server</span></span><br/> | <span data-ttu-id="46e33-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46e33-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="46e33-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46e33-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="46e33-143">**參考**</span><span class="sxs-lookup"><span data-stu-id="46e33-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="46e33-144">**CURSORDIR**</span><span class="sxs-lookup"><span data-stu-id="46e33-144">**CURSORDIR**</span></span>](cursordir.md)
</dt> <dt>

[<span data-ttu-id="46e33-145">**ICONRESDIR**</span><span class="sxs-lookup"><span data-stu-id="46e33-145">**ICONRESDIR**</span></span>](iconresdir.md)
</dt> <dt>

[<span data-ttu-id="46e33-146">**LOCALHEADER**</span><span class="sxs-lookup"><span data-stu-id="46e33-146">**LOCALHEADER**</span></span>](localheader.md)
</dt> <dt>

[<span data-ttu-id="46e33-147">**NEWHEADER**</span><span class="sxs-lookup"><span data-stu-id="46e33-147">**NEWHEADER**</span></span>](newheader.md)
</dt> <dt>

<span data-ttu-id="46e33-148">**概念**</span><span class="sxs-lookup"><span data-stu-id="46e33-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="46e33-149">資源</span><span class="sxs-lookup"><span data-stu-id="46e33-149">Resources</span></span>](resources.md)
</dt> </dl>

 


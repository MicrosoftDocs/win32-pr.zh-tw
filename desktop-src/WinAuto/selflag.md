---
title: 'SELFLAG 常數 (Oleacc) '
description: 本主題說明用來指定如何選取可存取物件或取得焦點的常數值。
ms.assetid: 52755540-dcf4-4e0b-bb5c-88b05f134d79
topic_type:
- apiref
api_name:
- SELFLAG_NONE
- SELFLAG_TAKEFOCUS
- SELFLAG_TAKESELECTION
- SELFLAG_EXTENDSELECTION
- SELFLAG_ADDSELECTION
- SELFLAG_REMOVESELECTION
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb49daffd2bb20e705d17aa51c3bff3d9622a6de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989799"
---
# <a name="selflag-constants"></a><span data-ttu-id="79cf8-103">SELFLAG 常數</span><span class="sxs-lookup"><span data-stu-id="79cf8-103">SELFLAG Constants</span></span>

<span data-ttu-id="79cf8-104">本主題說明用來指定如何選取可存取物件或取得焦點的常數值。</span><span class="sxs-lookup"><span data-stu-id="79cf8-104">This topic describes the constant values used to specify how an accessible object becomes selected or takes the focus.</span></span> <span data-ttu-id="79cf8-105">常數定義于 oleacc 中，並與 [**IAccessible：： accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) 方法搭配使用。</span><span class="sxs-lookup"><span data-stu-id="79cf8-105">The constants are defined in oleacc.h and are used with the [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method.</span></span>

<span data-ttu-id="79cf8-106">不允許下列組合：</span><span class="sxs-lookup"><span data-stu-id="79cf8-106">The following combinations are not allowed:</span></span>

-   <span data-ttu-id="79cf8-107">SELFLAG \_ ADDSELECTION \| SELFLAG \_ REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="79cf8-107">SELFLAG\_ADDSELECTION \| SELFLAG\_REMOVESELECTION</span></span>
-   <span data-ttu-id="79cf8-108">SELFLAG \_ ADDSELECTION \| SELFLAG \_ TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="79cf8-108">SELFLAG\_ADDSELECTION \| SELFLAG\_TAKESELECTION</span></span>
-   <span data-ttu-id="79cf8-109">SELFLAG \_ REMOVESELECTION \| SELFLAG \_ TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="79cf8-109">SELFLAG\_REMOVESELECTION \| SELFLAG\_TAKESELECTION</span></span>
-   <span data-ttu-id="79cf8-110">SELFLAG \_ EXTENDSELECTION \| SELFLAG \_ TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="79cf8-110">SELFLAG\_EXTENDSELECTION \| SELFLAG\_TAKESELECTION</span></span>

<span data-ttu-id="79cf8-111">**用戶端注意事項：** Microsoft Active Accessibility 不支援選取 [編輯] 和 [rich edit] 控制項中包含的文字，因為該文字會在物件的 [值] [屬性](value-property.md)中公開為字串。</span><span class="sxs-lookup"><span data-stu-id="79cf8-111">**Note to clients :** Microsoft Active Accessibility does not support the selection of the text contained in edit and rich edit controls because the text is exposed as a string in the object's [Value property](value-property.md).</span></span>

<span data-ttu-id="79cf8-112">如需有關如何執行複雜選取作業的詳細資訊，請參閱 [選取子物件](selecting-child-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="79cf8-112">For information on how to perform complex selection operations, see [Selecting Child Objects](selecting-child-objects.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="79cf8-113">常數/值</span><span class="sxs-lookup"><span data-stu-id="79cf8-113">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="79cf8-114">Description</span><span class="sxs-lookup"><span data-stu-id="79cf8-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl> <span data-ttu-id="79cf8-115"><dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="79cf8-115"><dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="79cf8-116">不執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="79cf8-116">Performs no action.</span></span> <span data-ttu-id="79cf8-117">Microsoft Active Accessibility 不會變更選取範圍或焦點。</span><span class="sxs-lookup"><span data-stu-id="79cf8-117">Microsoft Active Accessibility does not change the selection or focus.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl> <span data-ttu-id="79cf8-118"><dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </span><span class="sxs-lookup"><span data-stu-id="79cf8-118"><dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="79cf8-119">將焦點設定為物件，並使其成為選取錨點。</span><span class="sxs-lookup"><span data-stu-id="79cf8-119">Sets the focus to the object and makes it the selection anchor.</span></span> <span data-ttu-id="79cf8-120">此旗標本身會使用此旗標來變更選取專案。</span><span class="sxs-lookup"><span data-stu-id="79cf8-120">Used by itself, this flag does not alter the selection.</span></span> <span data-ttu-id="79cf8-121">其效果類似于手動移動焦點，方法是按住方向鍵，同時按住 CTRL 鍵 Windows 檔案總管或任意多重選取清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="79cf8-121">The effect is similar to moving the focus manually by pressing an ARROW key while holding down the CTRL key in Windows Explorer or in any multiple-selection list box.</span></span> <br/> <span data-ttu-id="79cf8-122">使用具有 <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>的物件，SELFLAG_TAKEFOCUS 會結合下列值：</span><span class="sxs-lookup"><span data-stu-id="79cf8-122">With objects that have the <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS is combined with the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="79cf8-123">SELFLAG_TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="79cf8-123">SELFLAG_TAKESELECTION</span></span></li>
<li><span data-ttu-id="79cf8-124">SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="79cf8-124">SELFLAG_EXTENDSELECTION</span></span></li>
<li><span data-ttu-id="79cf8-125">SELFLAG_ADDSELECTION</span><span class="sxs-lookup"><span data-stu-id="79cf8-125">SELFLAG_ADDSELECTION</span></span></li>
<li><span data-ttu-id="79cf8-126">SELFLAG_REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="79cf8-126">SELFLAG_REMOVESELECTION</span></span></li>
<li><span data-ttu-id="79cf8-127">SELFLAG_ADDSELECTION |SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="79cf8-127">SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</span></span></li>
<li><span data-ttu-id="79cf8-128">SELFLAG_REMOVESELECTION |SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="79cf8-128">SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</span></span></li>
</ul>
<span data-ttu-id="79cf8-129">如果您使用具有<strong>HWND</strong>的物件上的 SELFLAG_TAKEFOCUS 旗標來呼叫<a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible：： accSelect</strong></a> ，只有當物件的父系已經有焦點時，旗標才會生效。</span><span class="sxs-lookup"><span data-stu-id="79cf8-129">If you call <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible::accSelect</strong></a> with the SELFLAG_TAKEFOCUS flag on an object that has an <strong>HWND</strong>, the flag will take effect only if the object's parent already has the focus.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl> <span data-ttu-id="79cf8-130"><dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0x2</dt> </span><span class="sxs-lookup"><span data-stu-id="79cf8-130"><dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0x2</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="79cf8-131">選取物件，並將選取專案從容器中的所有其他物件中移除。</span><span class="sxs-lookup"><span data-stu-id="79cf8-131">Selects the object and removes the selection from all other objects in the container.</span></span> <br/> <span data-ttu-id="79cf8-132">除非它與 SELFLAG_TAKEFOCUS 合併，否則此旗標不會變更焦點或選取錨點。</span><span class="sxs-lookup"><span data-stu-id="79cf8-132">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="79cf8-133">SELFLAG_TAKESELECTION |SELFLAG_TAKEFOCUS 組合相當於按一下 Windows 檔案總管中的專案。</span><span class="sxs-lookup"><span data-stu-id="79cf8-133">The SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS combination is equivalent to single-clicking an item in Windows Explorer.</span></span><br/> <span data-ttu-id="79cf8-134">此旗標不得與下列旗標結合：</span><span class="sxs-lookup"><span data-stu-id="79cf8-134">This flag must not be combined with the following flags:</span></span><br/>
<ul>
<li><span data-ttu-id="79cf8-135">SELFLAG_ADDSELECTION</span><span class="sxs-lookup"><span data-stu-id="79cf8-135">SELFLAG_ADDSELECTION</span></span></li>
<li><span data-ttu-id="79cf8-136">SELFLAG_REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="79cf8-136">SELFLAG_REMOVESELECTION</span></span></li>
<li><span data-ttu-id="79cf8-137">SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="79cf8-137">SELFLAG_EXTENDSELECTION</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl> <span data-ttu-id="79cf8-138"><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </span><span class="sxs-lookup"><span data-stu-id="79cf8-138"><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="79cf8-139">變更選取範圍，讓選取範圍錨點和此物件之間的所有物件都採用錨點物件的選取狀態。</span><span class="sxs-lookup"><span data-stu-id="79cf8-139">Alters the selection so that all objects between the selection anchor and this object take on the anchor object's selection state.</span></span> <span data-ttu-id="79cf8-140">如果不選取錨點物件，物件會從選取項目移除。</span><span class="sxs-lookup"><span data-stu-id="79cf8-140">If the anchor object is not selected, the objects are removed from the selection.</span></span> <span data-ttu-id="79cf8-141">如果選取錨點物件，則會擴充選取範圍，以包含此物件和之間的所有物件。</span><span class="sxs-lookup"><span data-stu-id="79cf8-141">If the anchor object is selected, the selection is extended to include this object and all the objects in between.</span></span> <span data-ttu-id="79cf8-142">藉由結合此旗標與 SELFLAG_ADDSELECTION 或 SELFLAG_REMOVESELECTION 來設定選取狀態。</span><span class="sxs-lookup"><span data-stu-id="79cf8-142">Set the selection state by combining this flag with SELFLAG_ADDSELECTION or SELFLAG_REMOVESELECTION.</span></span> <br/> <span data-ttu-id="79cf8-143">除非它與 SELFLAG_TAKEFOCUS 合併，否則此旗標不會變更焦點或選取錨點。</span><span class="sxs-lookup"><span data-stu-id="79cf8-143">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="79cf8-144">SELFLAG_EXTENDSELECTION |SELFLAG_TAKEFOCUS 組合相當於以手動方式將專案新增至選取範圍，方法是按住 SHIFT 鍵，然後按一下 Windows 檔案總管中未選取的物件。</span><span class="sxs-lookup"><span data-stu-id="79cf8-144">The SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combination is equivalent to adding an item to a selection manually by holding down the SHIFT key and clicking an unselected object in Windows Explorer.</span></span><br/> <span data-ttu-id="79cf8-145">此旗標不會與 SELFLAG_TAKESELECTION 結合。</span><span class="sxs-lookup"><span data-stu-id="79cf8-145">This flag is not combined with SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl> <span data-ttu-id="79cf8-146"><dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </span><span class="sxs-lookup"><span data-stu-id="79cf8-146"><dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="79cf8-147">將物件加入至目前的選取專案;可能的結果是非連續的選取專案。</span><span class="sxs-lookup"><span data-stu-id="79cf8-147">Adds the object to the current selection; possible result is a noncontiguous selection.</span></span> <br/> <span data-ttu-id="79cf8-148">除非它與 SELFLAG_TAKEFOCUS 合併，否則此旗標不會變更焦點或選取錨點。</span><span class="sxs-lookup"><span data-stu-id="79cf8-148">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="79cf8-149">SELFLAG_ADDSELECTION |SELFLAG_TAKEFOCUS 組合相當於以手動方式將專案新增至選取範圍，方法是按住 CTRL 鍵，然後按一下 Windows 檔案總管中未選取的物件。</span><span class="sxs-lookup"><span data-stu-id="79cf8-149">The SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combination is equivalent to adding an item to a selection manually by holding down the CTRL key and clicking an unselected object in Windows Explorer.</span></span><br/> <span data-ttu-id="79cf8-150">此旗標不會與 SELFLAG_REMOVESELECTION 或 SELFLAG_TAKESELECTION 合併。</span><span class="sxs-lookup"><span data-stu-id="79cf8-150">This flag is not combined with SELFLAG_REMOVESELECTION or SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl> <span data-ttu-id="79cf8-151"><dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </span><span class="sxs-lookup"><span data-stu-id="79cf8-151"><dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="79cf8-152">從目前的選取範圍中移除物件;可能的結果是非連續的選取專案。</span><span class="sxs-lookup"><span data-stu-id="79cf8-152">Removes the object from the current selection; possible result is a noncontiguous selection.</span></span> <br/> <span data-ttu-id="79cf8-153">除非它與 SELFLAG_TAKEFOCUS 合併，否則此旗標不會變更焦點或選取錨點。</span><span class="sxs-lookup"><span data-stu-id="79cf8-153">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="79cf8-154">SELFLAG_REMOVESELECTION |SELFLAG_TAKEFOCUS 組合相當於手動移除選取專案中的專案，方法是按住 CTRL 鍵，同時按一下 Windows 檔案總管中選取的物件。</span><span class="sxs-lookup"><span data-stu-id="79cf8-154">The SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS combination is equivalent to removing an item from a selection manually, by holding down the CTRL key while clicking a selected object in Windows Explorer.</span></span><br/> <span data-ttu-id="79cf8-155">此旗標不會與 SELFLAG_ADDSELECTION 或 SELFLAG_TAKESELECTION 合併。</span><span class="sxs-lookup"><span data-stu-id="79cf8-155">This flag is not combined with SELFLAG_ADDSELECTION or SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="79cf8-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="79cf8-156">Requirements</span></span>



| <span data-ttu-id="79cf8-157">需求</span><span class="sxs-lookup"><span data-stu-id="79cf8-157">Requirement</span></span> | <span data-ttu-id="79cf8-158">值</span><span class="sxs-lookup"><span data-stu-id="79cf8-158">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="79cf8-159">標頭</span><span class="sxs-lookup"><span data-stu-id="79cf8-159">Header</span></span><br/> | <dl> <span data-ttu-id="79cf8-160"><dt>Oleacc。h</dt></span><span class="sxs-lookup"><span data-stu-id="79cf8-160"><dt>Oleacc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79cf8-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79cf8-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79cf8-162">**IAccessible：： accSelect**</span><span class="sxs-lookup"><span data-stu-id="79cf8-162">**IAccessible::accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[<span data-ttu-id="79cf8-163">選取子物件</span><span class="sxs-lookup"><span data-stu-id="79cf8-163">Selecting Child Objects</span></span>](selecting-child-objects.md)
</dt> </dl>

 

 






---
description: IExtender 介面會提供一組新增至控制項介面的基本屬性。 程式設計人員可以使用這些屬性，就像是控制項的一部分一樣。
ms.assetid: 901873bd-af6a-415e-865f-21769367c99f
title: IExtender 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender
- IExtender.Align
- IExtender.get_Align
- IExtender.put_Align
- IExtender.Enabled
- IExtender.get_Enabled
- IExtender.put_Enabled
- IExtender.Height
- IExtender.get_Height
- IExtender.put_Height
- IExtender.Left
- IExtender.get_Left
- IExtender.put_Left
- IExtender.TabStop
- IExtender.get_TabStop
- IExtender.put_TabStop
- IExtender.Top
- IExtender.get_Top
- IExtender.put_Top
- IExtender.Visible
- IExtender.get_Visible
- IExtender.put_Visible
- IExtender.Width
- IExtender.get_Width
- IExtender.put_Width
- IExtender.Name
- IExtender.get_Name
- IExtender.Parent
- IExtender.get_Parent
- IExtender.Hwnd
- IExtender.get_Hwnd
- IExtender.Container
- IExtender.get_Container
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: fd600de816889e1c644a0e6074d9b8a97e0ec80c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975963"
---
# <a name="iextender-interface"></a><span data-ttu-id="2ee20-104">IExtender 介面</span><span class="sxs-lookup"><span data-stu-id="2ee20-104">IExtender interface</span></span>

<span data-ttu-id="2ee20-105">**IExtender** 介面會提供一組新增至控制項介面的基本屬性。</span><span class="sxs-lookup"><span data-stu-id="2ee20-105">The **IExtender** interface provides a set of basic properties that are added to the interface of a control.</span></span> <span data-ttu-id="2ee20-106">程式設計人員可以使用這些屬性，就像是控制項的一部分一樣。</span><span class="sxs-lookup"><span data-stu-id="2ee20-106">Programmers can use these properties as if they were part of the control.</span></span>

## <a name="members"></a><span data-ttu-id="2ee20-107">成員</span><span class="sxs-lookup"><span data-stu-id="2ee20-107">Members</span></span>

<span data-ttu-id="2ee20-108">**IExtender** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="2ee20-108">The **IExtender** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2ee20-109">**IExtender** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2ee20-109">**IExtender** also has these types of members:</span></span>

-   [<span data-ttu-id="2ee20-110">方法</span><span class="sxs-lookup"><span data-stu-id="2ee20-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="2ee20-111">屬性</span><span class="sxs-lookup"><span data-stu-id="2ee20-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2ee20-112">方法</span><span class="sxs-lookup"><span data-stu-id="2ee20-112">Methods</span></span>

<span data-ttu-id="2ee20-113">**IExtender** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2ee20-113">The **IExtender** interface has these methods.</span></span>



| <span data-ttu-id="2ee20-114">方法</span><span class="sxs-lookup"><span data-stu-id="2ee20-114">Method</span></span>                         | <span data-ttu-id="2ee20-115">描述</span><span class="sxs-lookup"><span data-stu-id="2ee20-115">Description</span></span>                                    |
|:-------------------------------|:-----------------------------------------------|
| [<span data-ttu-id="2ee20-116">**移動**</span><span class="sxs-lookup"><span data-stu-id="2ee20-116">**Move**</span></span>](iextender-move.md) | <span data-ttu-id="2ee20-117">移動 MDIForm、表單或控制項。</span><span class="sxs-lookup"><span data-stu-id="2ee20-117">Moves an MDIForm, form, or control.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2ee20-118">屬性</span><span class="sxs-lookup"><span data-stu-id="2ee20-118">Properties</span></span>

<span data-ttu-id="2ee20-119">**IExtender** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2ee20-119">The **IExtender** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="2ee20-120">屬性</span><span class="sxs-lookup"><span data-stu-id="2ee20-120">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="2ee20-121">存取類型</span><span class="sxs-lookup"><span data-stu-id="2ee20-121">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="2ee20-122">Description</span><span class="sxs-lookup"><span data-stu-id="2ee20-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="2ee20-123">對齊</span><span class="sxs-lookup"><span data-stu-id="2ee20-123">Align</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="2ee20-124">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2ee20-124">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="2ee20-125">傳回或設定值，這個值會決定物件在表單上的任何位置，或是顯示在表單的頂端、底部、左方或右方時，會自動調整大小以符合表單的寬度。</span><span class="sxs-lookup"><span data-stu-id="2ee20-125">Returns or sets a value that determines whether an object is displayed in any size anywhere on a form or whether it is displayed at the top, bottom, left, or right of the form and is automatically sized to fit the width of the form.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2ee20-126">常數</span><span class="sxs-lookup"><span data-stu-id="2ee20-126">Constant</span></span></th>
<th><span data-ttu-id="2ee20-127">描述</span><span class="sxs-lookup"><span data-stu-id="2ee20-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ee20-128">vbAlignNone 0</span><span class="sxs-lookup"><span data-stu-id="2ee20-128">vbAlignNone 0</span></span></td>
<td><span data-ttu-id="2ee20-129">非 MDI 格式的 (預設值) 無：大小和位置可以在設計階段或在程式碼中設定。</span><span class="sxs-lookup"><span data-stu-id="2ee20-129">(Default in a non-MDI form) None—size and location can be set at design time or in code.</span></span> <span data-ttu-id="2ee20-130">如果物件是在 MDI 表單上，則會忽略此設定。</span><span class="sxs-lookup"><span data-stu-id="2ee20-130">The setting is ignored if the object is on an MDI form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ee20-131">vbAlignTop 1</span><span class="sxs-lookup"><span data-stu-id="2ee20-131">vbAlignTop 1</span></span></td>
<td><span data-ttu-id="2ee20-132"> (MDI 表單中的預設值) Top-物件位於表單頂端，而其寬度等於表單的 ScaleWidth 屬性設定。</span><span class="sxs-lookup"><span data-stu-id="2ee20-132">(Default in an MDI form) Top—the object is at the top of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ee20-133">vbAlignBottom 2</span><span class="sxs-lookup"><span data-stu-id="2ee20-133">vbAlignBottom 2</span></span></td>
<td><span data-ttu-id="2ee20-134">底部：物件位於表單底部，其寬度等於表單的 [ScaleWidth] 屬性設定。</span><span class="sxs-lookup"><span data-stu-id="2ee20-134">Bottom—the object is at the bottom of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ee20-135">vbAlignLeft 3</span><span class="sxs-lookup"><span data-stu-id="2ee20-135">vbAlignLeft 3</span></span></td>
<td><span data-ttu-id="2ee20-136">左方：物件位於表單的左邊，而其寬度等於表單的 ScaleWidth 屬性設定。</span><span class="sxs-lookup"><span data-stu-id="2ee20-136">Left—the object is at the left of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ee20-137">vbAlignRight 4</span><span class="sxs-lookup"><span data-stu-id="2ee20-137">vbAlignRight 4</span></span></td>
<td><span data-ttu-id="2ee20-138">Right：物件位於表單的右邊，而且其寬度等於表單的 ScaleWidth 屬性設定。</span><span class="sxs-lookup"><span data-stu-id="2ee20-138">Right—the object is at the right of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="2ee20-139">容器</span><span class="sxs-lookup"><span data-stu-id="2ee20-139">Container</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-140">唯讀</span><span class="sxs-lookup"><span data-stu-id="2ee20-140">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-141">傳回表單上控制項的容器。</span><span class="sxs-lookup"><span data-stu-id="2ee20-141">Returns the container of a control on a form.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="2ee20-142">已啟用</span><span class="sxs-lookup"><span data-stu-id="2ee20-142">Enabled</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-143">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2ee20-143">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-144">傳回或設定值，這個值會決定表單或控制項是否可以回應使用者產生的事件。</span><span class="sxs-lookup"><span data-stu-id="2ee20-144">Returns or sets a value that determines whether a form or control can respond to user-generated events.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="2ee20-145">高度</span><span class="sxs-lookup"><span data-stu-id="2ee20-145">Height</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-146">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2ee20-146">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-147">傳回或設定物件的高度。</span><span class="sxs-lookup"><span data-stu-id="2ee20-147">Returns or sets the height of an object.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="2ee20-148">Hwnd</span><span class="sxs-lookup"><span data-stu-id="2ee20-148">Hwnd</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-149">唯讀</span><span class="sxs-lookup"><span data-stu-id="2ee20-149">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-150">傳回表單或控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2ee20-150">Returns a handle to a form or control.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="2ee20-151">Left</span><span class="sxs-lookup"><span data-stu-id="2ee20-151">Left</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-152">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2ee20-152">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-153">傳回或設定物件的內部左邊緣和其容器左邊緣之間的距離。</span><span class="sxs-lookup"><span data-stu-id="2ee20-153">Returns or sets the distance between the internal left edge of an object and the left edge of its container.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="2ee20-154">Name</span><span class="sxs-lookup"><span data-stu-id="2ee20-154">Name</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-155">唯讀</span><span class="sxs-lookup"><span data-stu-id="2ee20-155">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-156">傳回程序代碼中用來識別表單、控制項或資料存取物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ee20-156">Returns the name used in code to identify a form, control, or data access object.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="2ee20-157">父代</span><span class="sxs-lookup"><span data-stu-id="2ee20-157">Parent</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-158">唯讀</span><span class="sxs-lookup"><span data-stu-id="2ee20-158">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-159">傳回包含控制項或另一個物件或集合的表單、物件或集合。</span><span class="sxs-lookup"><span data-stu-id="2ee20-159">Returns the form, object, or collection that contains a control or another object or collection.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="2ee20-160">TabStop</span><span class="sxs-lookup"><span data-stu-id="2ee20-160">TabStop</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-161">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2ee20-161">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-162">傳回或設定值，這個值表示使用者是否可以使用 <strong>Tab</strong> 鍵將焦點提供給物件。</span><span class="sxs-lookup"><span data-stu-id="2ee20-162">Returns or sets a value that indicates whether a user can use the <strong>Tab</strong> key to give the focus to an object.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="2ee20-163">頁首</span><span class="sxs-lookup"><span data-stu-id="2ee20-163">Top</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-164">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2ee20-164">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-165">傳回或設定物件的內部上邊緣和其容器的上邊緣之間的距離。</span><span class="sxs-lookup"><span data-stu-id="2ee20-165">Returns or sets the distance between the internal top edge of an object and the top edge of its container.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="2ee20-166">可見</span><span class="sxs-lookup"><span data-stu-id="2ee20-166">Visible</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-167">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2ee20-167">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-168">傳回或設定值，這個值表示物件是否為可見或隱藏。</span><span class="sxs-lookup"><span data-stu-id="2ee20-168">Returns or sets a value that indicates whether an object is visible or hidden.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="2ee20-169">寬度</span><span class="sxs-lookup"><span data-stu-id="2ee20-169">Width</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-170">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2ee20-170">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="2ee20-171">傳回或設定物件的寬度。</span><span class="sxs-lookup"><span data-stu-id="2ee20-171">Returns or sets the width of an object.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="2ee20-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ee20-172">Requirements</span></span>



| <span data-ttu-id="2ee20-173">需求</span><span class="sxs-lookup"><span data-stu-id="2ee20-173">Requirement</span></span> | <span data-ttu-id="2ee20-174">值</span><span class="sxs-lookup"><span data-stu-id="2ee20-174">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee20-175">DLL</span><span class="sxs-lookup"><span data-stu-id="2ee20-175">DLL</span></span><br/> | <dl> <span data-ttu-id="2ee20-176"><dt>Ole2disp.dll;</dt><dt>Oleaut32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ee20-176"><dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt></span></span> </dl> |



 

 

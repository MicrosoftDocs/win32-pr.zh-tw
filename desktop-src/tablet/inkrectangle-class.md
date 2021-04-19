---
description: 表示對矩形的存取。
ms.assetid: 78e6c29c-0f43-46a5-9d30-948de5f369c8
title: 'InkRectangle 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRectangle
- InkRectangle.IInkRectangle
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: d643696fe19523bac93ebca71cf885cd93b8570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988475"
---
# <a name="inkrectangle-class"></a><span data-ttu-id="37ee5-103">InkRectangle 類別</span><span class="sxs-lookup"><span data-stu-id="37ee5-103">InkRectangle class</span></span>

<span data-ttu-id="37ee5-104">表示對矩形的存取。</span><span class="sxs-lookup"><span data-stu-id="37ee5-104">Represents access to a rectangle.</span></span>

<span data-ttu-id="37ee5-105">**InkRectangle** 具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="37ee5-105">**InkRectangle** has these types of members:</span></span>

-   [<span data-ttu-id="37ee5-106">介面</span><span class="sxs-lookup"><span data-stu-id="37ee5-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="37ee5-107">方法</span><span class="sxs-lookup"><span data-stu-id="37ee5-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="37ee5-108">屬性</span><span class="sxs-lookup"><span data-stu-id="37ee5-108">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="37ee5-109">介面</span><span class="sxs-lookup"><span data-stu-id="37ee5-109">Interfaces</span></span>

<span data-ttu-id="37ee5-110">**InkRectangle** 類別會定義這些介面。</span><span class="sxs-lookup"><span data-stu-id="37ee5-110">The **InkRectangle** class defines these interfaces.</span></span>



| <span data-ttu-id="37ee5-111">介面</span><span class="sxs-lookup"><span data-stu-id="37ee5-111">Interface</span></span>         | <span data-ttu-id="37ee5-112">描述</span><span class="sxs-lookup"><span data-stu-id="37ee5-112">Description</span></span>                                                            |
|:------------------|:-----------------------------------------------------------------------|
| <span data-ttu-id="37ee5-113">**IInkRectangle**</span><span class="sxs-lookup"><span data-stu-id="37ee5-113">**IInkRectangle**</span></span> | <span data-ttu-id="37ee5-114">這個物件會實 **IInkRectangle** COM 介面。</span><span class="sxs-lookup"><span data-stu-id="37ee5-114">This object implements the **IInkRectangle** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="37ee5-115">方法</span><span class="sxs-lookup"><span data-stu-id="37ee5-115">Methods</span></span>

<span data-ttu-id="37ee5-116">**InkRectangle** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="37ee5-116">The **InkRectangle** class has these methods.</span></span>



| <span data-ttu-id="37ee5-117">方法</span><span class="sxs-lookup"><span data-stu-id="37ee5-117">Method</span></span>                                            | <span data-ttu-id="37ee5-118">描述</span><span class="sxs-lookup"><span data-stu-id="37ee5-118">Description</span></span>                                                                        |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="37ee5-119">**GetRectangle**</span><span class="sxs-lookup"><span data-stu-id="37ee5-119">**GetRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-getrectangle) | <span data-ttu-id="37ee5-120">在單一呼叫中抓取 **InkRectangle** 物件的元素。</span><span class="sxs-lookup"><span data-stu-id="37ee5-120">Retrieves the elements of the **InkRectangle** object in a single call.</span></span><br/> |
| [<span data-ttu-id="37ee5-121">**SetRectangle**</span><span class="sxs-lookup"><span data-stu-id="37ee5-121">**SetRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-setrectangle) | <span data-ttu-id="37ee5-122">在單一呼叫中修改 **InkRectangle** 物件的元素。</span><span class="sxs-lookup"><span data-stu-id="37ee5-122">Modifies the elements of the **InkRectangle** object in a single call.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="37ee5-123">屬性</span><span class="sxs-lookup"><span data-stu-id="37ee5-123">Properties</span></span>

<span data-ttu-id="37ee5-124">**InkRectangle** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="37ee5-124">The **InkRectangle** class has these properties.</span></span>



| <span data-ttu-id="37ee5-125">屬性</span><span class="sxs-lookup"><span data-stu-id="37ee5-125">Property</span></span>                                         | <span data-ttu-id="37ee5-126">存取類型</span><span class="sxs-lookup"><span data-stu-id="37ee5-126">Access type</span></span>           | <span data-ttu-id="37ee5-127">Description</span><span class="sxs-lookup"><span data-stu-id="37ee5-127">Description</span></span>                                                        |
|:-------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="37ee5-128">**下層**</span><span class="sxs-lookup"><span data-stu-id="37ee5-128">**Bottom**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom)<br/> | <span data-ttu-id="37ee5-129">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="37ee5-129">Read/write</span></span><br/> | <span data-ttu-id="37ee5-130">取得或設定矩形的底部位置。</span><span class="sxs-lookup"><span data-stu-id="37ee5-130">Gets or sets the bottom position of the rectangle.</span></span><br/>      |
| [<span data-ttu-id="37ee5-131">**資料**</span><span class="sxs-lookup"><span data-stu-id="37ee5-131">**Data**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_data)<br/>     | <span data-ttu-id="37ee5-132">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="37ee5-132">Read/write</span></span><br/> | <span data-ttu-id="37ee5-133">取得或設定只有)  (c + + 的矩形結構存取權。</span><span class="sxs-lookup"><span data-stu-id="37ee5-133">Gets or sets access to the rectangle struct (C++ only).</span></span><br/> |
| [<span data-ttu-id="37ee5-134">**離開**</span><span class="sxs-lookup"><span data-stu-id="37ee5-134">**Left**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left)<br/>     | <span data-ttu-id="37ee5-135">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="37ee5-135">Read/write</span></span><br/> | <span data-ttu-id="37ee5-136">取得或設定矩形的左邊位置。</span><span class="sxs-lookup"><span data-stu-id="37ee5-136">Gets or sets the left position of the rectangle.</span></span><br/>        |
| [<span data-ttu-id="37ee5-137">**對**</span><span class="sxs-lookup"><span data-stu-id="37ee5-137">**Right**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right)<br/>   | <span data-ttu-id="37ee5-138">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="37ee5-138">Read/write</span></span><br/> | <span data-ttu-id="37ee5-139">取得或設定矩形的右邊位置。</span><span class="sxs-lookup"><span data-stu-id="37ee5-139">Gets or sets the right position of the rectangle.</span></span><br/>       |
| [<span data-ttu-id="37ee5-140">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="37ee5-140">**Top**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top)<br/>       | <span data-ttu-id="37ee5-141">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="37ee5-141">Read/write</span></span><br/> | <span data-ttu-id="37ee5-142">取得或設定矩形的上方位置。</span><span class="sxs-lookup"><span data-stu-id="37ee5-142">Gets or sets the top position of the rectangle.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="37ee5-143">備註</span><span class="sxs-lookup"><span data-stu-id="37ee5-143">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="37ee5-144">如果某個點位於 [**左側**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left)或 [**頂端**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top)，或是在全部四邊內，就會在 **InkRectangle** 中。</span><span class="sxs-lookup"><span data-stu-id="37ee5-144">A point is within an **InkRectangle** if it lies on the [**Left**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left) or [**Top**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top) side or is within all four sides.</span></span> <span data-ttu-id="37ee5-145">[**右邊**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right)或 [**下**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom)一端的點會被視為矩形外部。</span><span class="sxs-lookup"><span data-stu-id="37ee5-145">A point on the [**Right**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right) or [**Bottom**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom) side is considered outside the rectangle.</span></span>

 

<span data-ttu-id="37ee5-146">您可以藉由呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化此物件。</span><span class="sxs-lookup"><span data-stu-id="37ee5-146">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method.</span></span>

> [!Note]  
> <span data-ttu-id="37ee5-147">如果 **InkRectangle** 大於 \_ (2 ^ 31-1 個維度中) 的最大值，則無法使用。</span><span class="sxs-lookup"><span data-stu-id="37ee5-147">An **InkRectangle** cannot be used if it is larger than LONG\_MAX (2^31 - 1) in either dimension.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="37ee5-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="37ee5-148">Requirements</span></span>



| <span data-ttu-id="37ee5-149">需求</span><span class="sxs-lookup"><span data-stu-id="37ee5-149">Requirement</span></span> | <span data-ttu-id="37ee5-150">值</span><span class="sxs-lookup"><span data-stu-id="37ee5-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37ee5-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37ee5-151">Minimum supported client</span></span><br/> | <span data-ttu-id="37ee5-152">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37ee5-152">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="37ee5-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37ee5-153">Minimum supported server</span></span><br/> | <span data-ttu-id="37ee5-154">都不支援</span><span class="sxs-lookup"><span data-stu-id="37ee5-154">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="37ee5-155">標頭</span><span class="sxs-lookup"><span data-stu-id="37ee5-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="37ee5-156"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="37ee5-156"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="37ee5-157">程式庫</span><span class="sxs-lookup"><span data-stu-id="37ee5-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="37ee5-158"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37ee5-158"><dt>InkObj.dll</dt></span></span> </dl>                               |



 


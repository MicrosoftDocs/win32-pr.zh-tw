---
description: 代表3x3 矩陣，後者又表示仿射轉換。
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: 'InkTransform 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkTransform
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 61641f0fed8ec98321e155f82ff9a35150e7fdcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980711"
---
# <a name="inktransform-class"></a><span data-ttu-id="bf235-103">InkTransform 類別</span><span class="sxs-lookup"><span data-stu-id="bf235-103">InkTransform class</span></span>

<span data-ttu-id="bf235-104">代表3x3 矩陣，後者又表示仿射轉換。</span><span class="sxs-lookup"><span data-stu-id="bf235-104">Represents a 3x3 matrix that, in turn, represents an affine transformation.</span></span>

<span data-ttu-id="bf235-105">**InkTransform** 具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bf235-105">**InkTransform** has these types of members:</span></span>

-   [<span data-ttu-id="bf235-106">方法</span><span class="sxs-lookup"><span data-stu-id="bf235-106">Methods</span></span>](#methods)
-   [<span data-ttu-id="bf235-107">屬性</span><span class="sxs-lookup"><span data-stu-id="bf235-107">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bf235-108">方法</span><span class="sxs-lookup"><span data-stu-id="bf235-108">Methods</span></span>

<span data-ttu-id="bf235-109">**InkTransform** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="bf235-109">The **InkTransform** class has these methods.</span></span>



| <span data-ttu-id="bf235-110">方法</span><span class="sxs-lookup"><span data-stu-id="bf235-110">Method</span></span>                                                  | <span data-ttu-id="bf235-111">描述</span><span class="sxs-lookup"><span data-stu-id="bf235-111">Description</span></span>                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf235-112">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="bf235-112">**GetTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | <span data-ttu-id="bf235-113">將 **InkTransform** 抓取為6個浮點數。</span><span class="sxs-lookup"><span data-stu-id="bf235-113">Retrieves the **InkTransform** as 6 floats.</span></span><br/>                                                                      |
| [<span data-ttu-id="bf235-114">**反映**</span><span class="sxs-lookup"><span data-stu-id="bf235-114">**Reflect**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | <span data-ttu-id="bf235-115">以水準或垂直方向反映轉換。</span><span class="sxs-lookup"><span data-stu-id="bf235-115">Reflects the transform in either the horizontal or vertical directions.</span></span><br/>                                          |
| [<span data-ttu-id="bf235-116">**重設**</span><span class="sxs-lookup"><span data-stu-id="bf235-116">**Reset**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | <span data-ttu-id="bf235-117">將轉換重設為其原始狀態。</span><span class="sxs-lookup"><span data-stu-id="bf235-117">Resets the transform to its original state.</span></span><br/>                                                                      |
| [<span data-ttu-id="bf235-118">**旋轉**</span><span class="sxs-lookup"><span data-stu-id="bf235-118">**Rotate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | <span data-ttu-id="bf235-119">以度為單位的角度旋轉轉換，並選擇性地指定旋轉的中心點。</span><span class="sxs-lookup"><span data-stu-id="bf235-119">Rotates the transform by an angle measured in degrees, and optionally specifies a center point for the rotation.</span></span><br/> |
| [<span data-ttu-id="bf235-120">**ScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="bf235-120">**ScaleTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | <span data-ttu-id="bf235-121">依 X 和 Y 因數調整轉換。</span><span class="sxs-lookup"><span data-stu-id="bf235-121">Scales the transform by X and Y factors.</span></span><br/>                                                                         |
| [<span data-ttu-id="bf235-122">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="bf235-122">**SetTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | <span data-ttu-id="bf235-123">使用6個浮點數修改 **InkTransform** 。</span><span class="sxs-lookup"><span data-stu-id="bf235-123">Modifies the **InkTransform** using 6 floats.</span></span><br/>                                                                    |
| [<span data-ttu-id="bf235-124">**剪切**</span><span class="sxs-lookup"><span data-stu-id="bf235-124">**Shear**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | <span data-ttu-id="bf235-125">套用具有指定水準和垂直因數的切變。</span><span class="sxs-lookup"><span data-stu-id="bf235-125">Applies a shear with the specified horizontal and vertical factors.</span></span><br/>                                              |
| [<span data-ttu-id="bf235-126">**翻譯**</span><span class="sxs-lookup"><span data-stu-id="bf235-126">**Translate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | <span data-ttu-id="bf235-127">依指定的水準和垂直元件移動轉換。</span><span class="sxs-lookup"><span data-stu-id="bf235-127">Moves the transform by the specified horizontal and vertical components.</span></span><br/>                                         |



 

### <a name="properties"></a><span data-ttu-id="bf235-128">屬性</span><span class="sxs-lookup"><span data-stu-id="bf235-128">Properties</span></span>

<span data-ttu-id="bf235-129">**InkTransform** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bf235-129">The **InkTransform** class has these properties.</span></span>



| <span data-ttu-id="bf235-130">屬性</span><span class="sxs-lookup"><span data-stu-id="bf235-130">Property</span></span>                                     | <span data-ttu-id="bf235-131">存取類型</span><span class="sxs-lookup"><span data-stu-id="bf235-131">Access type</span></span>           | <span data-ttu-id="bf235-132">Description</span><span class="sxs-lookup"><span data-stu-id="bf235-132">Description</span></span>                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf235-133">**資料**</span><span class="sxs-lookup"><span data-stu-id="bf235-133">**Data**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | <span data-ttu-id="bf235-134">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bf235-134">Read/write</span></span><br/> | <span data-ttu-id="bf235-135">取得或設定 WIN32 XFORM 結構的自動化版本。</span><span class="sxs-lookup"><span data-stu-id="bf235-135">Gets or sets the Automation version of the WIN32 XFORM struct.</span></span><br/>                            |
| [<span data-ttu-id="bf235-136">**eDx**</span><span class="sxs-lookup"><span data-stu-id="bf235-136">**eDx**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | <span data-ttu-id="bf235-137">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bf235-137">Read/write</span></span><br/> | <span data-ttu-id="bf235-138">取得或設定指定第三列第一個資料行中之元素的實數。</span><span class="sxs-lookup"><span data-stu-id="bf235-138">Gets or sets the real number that specifies the element in the third row, first column.</span></span><br/>   |
| [<span data-ttu-id="bf235-139">**艾迪**</span><span class="sxs-lookup"><span data-stu-id="bf235-139">**eDy**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | <span data-ttu-id="bf235-140">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bf235-140">Read/write</span></span><br/> | <span data-ttu-id="bf235-141">取得或設定指定第三列第二個數據行中之元素的實數。</span><span class="sxs-lookup"><span data-stu-id="bf235-141">Gets or sets the real number that specifies the element in the third row, second column.</span></span><br/>  |
| [<span data-ttu-id="bf235-142">**eM11**</span><span class="sxs-lookup"><span data-stu-id="bf235-142">**eM11**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | <span data-ttu-id="bf235-143">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bf235-143">Read/write</span></span><br/> | <span data-ttu-id="bf235-144">取得或設定指定第一個資料列第一個資料行中之元素的實數。</span><span class="sxs-lookup"><span data-stu-id="bf235-144">Gets or sets the real number that specifies the element in the first row, first column.</span></span><br/>   |
| [<span data-ttu-id="bf235-145">**eM12**</span><span class="sxs-lookup"><span data-stu-id="bf235-145">**eM12**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | <span data-ttu-id="bf235-146">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bf235-146">Read/write</span></span><br/> | <span data-ttu-id="bf235-147">取得或設定指定第一個資料列第二個數據行中之元素的實數。</span><span class="sxs-lookup"><span data-stu-id="bf235-147">Gets or sets the real number that specifies the element in the first row, second column.</span></span><br/>  |
| [<span data-ttu-id="bf235-148">**eM21**</span><span class="sxs-lookup"><span data-stu-id="bf235-148">**eM21**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | <span data-ttu-id="bf235-149">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bf235-149">Read/write</span></span><br/> | <span data-ttu-id="bf235-150">取得或設定指定第二個數據列第一個資料行中之元素的實數。</span><span class="sxs-lookup"><span data-stu-id="bf235-150">Gets or sets the real number that specifies the element in the second row, first column.</span></span><br/>  |
| [<span data-ttu-id="bf235-151">**eM22**</span><span class="sxs-lookup"><span data-stu-id="bf235-151">**eM22**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | <span data-ttu-id="bf235-152">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bf235-152">Read/write</span></span><br/> | <span data-ttu-id="bf235-153">取得或設定指定第二個數據列第二個數據行中之元素的實數。</span><span class="sxs-lookup"><span data-stu-id="bf235-153">Gets or sets the real number that specifies the element in the second row, second column.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bf235-154">備註</span><span class="sxs-lookup"><span data-stu-id="bf235-154">Remarks</span></span>

<span data-ttu-id="bf235-155">此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。</span><span class="sxs-lookup"><span data-stu-id="bf235-155">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="bf235-156">此物件在3x3 矩陣中只會儲存九個數字的六個，因為表示仿射轉換的所有3x3 矩陣都有相同的第三個數據行 (0、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="bf235-156">The object stores only six of the nine numbers in a 3x3 matrix because all 3x3 matrices that represent affine transformations have the same third column (0, 0, 1).</span></span> <span data-ttu-id="bf235-157">接著，這個物件會用來描述轉換作業，例如移動、剪下、縮放或旋轉 [**InkRenderer**](inkrenderer-class.md) 物件、 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件或 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合。</span><span class="sxs-lookup"><span data-stu-id="bf235-157">This object in turn is used to describe transformation operations such as moving, shearing, scaling, or rotating in an [**InkRenderer**](inkrenderer-class.md) object, [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object, or [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

> [!Note]  
> <span data-ttu-id="bf235-158">**InkTransform** 物件與 [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform)結構相互關聯。</span><span class="sxs-lookup"><span data-stu-id="bf235-158">The **InkTransform** object correlates to the [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bf235-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf235-159">Requirements</span></span>



| <span data-ttu-id="bf235-160">需求</span><span class="sxs-lookup"><span data-stu-id="bf235-160">Requirement</span></span> | <span data-ttu-id="bf235-161">值</span><span class="sxs-lookup"><span data-stu-id="bf235-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf235-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf235-162">Minimum supported client</span></span><br/> | <span data-ttu-id="bf235-163">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf235-163">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="bf235-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf235-164">Minimum supported server</span></span><br/> | <span data-ttu-id="bf235-165">都不支援</span><span class="sxs-lookup"><span data-stu-id="bf235-165">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="bf235-166">標頭</span><span class="sxs-lookup"><span data-stu-id="bf235-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf235-167"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="bf235-167"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bf235-168">程式庫</span><span class="sxs-lookup"><span data-stu-id="bf235-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf235-169"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf235-169"><dt>InkObj.dll</dt></span></span> </dl>                               |



 


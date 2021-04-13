---
title: 值對應注釋
description: 值對應注釋
ms.assetid: f7c9304a-0eed-4a73-ab06-56723f3cfa5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d21b04374344475689989c2570af6975dc97c13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104560894"
---
# <a name="value-map-annotation"></a><span data-ttu-id="75e6e-103">值對應注釋</span><span class="sxs-lookup"><span data-stu-id="75e6e-103">Value Map Annotation</span></span>

<span data-ttu-id="75e6e-104">使用值對應注釋，您可以使用對應字串來指出清單視圖或樹狀檢視中專案的影像索引如何對應至其角色或狀態。</span><span class="sxs-lookup"><span data-stu-id="75e6e-104">With value map annotation, you can use a mapping string to indicate how the image index of an item in a list view or tree view corresponds to its role or state.</span></span> <span data-ttu-id="75e6e-105">例如，對應字串可能表示清單視圖的影像索引0對應到核取方塊的角色，而影像索引1則對應到選項按鈕的角色。</span><span class="sxs-lookup"><span data-stu-id="75e6e-105">For example, a mapping string may indicate that a list view's image index 0 maps to a role of check box, while image index 1 maps to a role of radio button.</span></span>

<span data-ttu-id="75e6e-106">您也可以使用「值對應注釋」來指定對應至滑杆上數值的字串。</span><span class="sxs-lookup"><span data-stu-id="75e6e-106">You can also use value map annotation to specify strings that map to the numeric values on a slider.</span></span>

## <a name="when-to-use-this-technique"></a><span data-ttu-id="75e6e-107">使用這項技術的時機</span><span class="sxs-lookup"><span data-stu-id="75e6e-107">When to Use This Technique</span></span>

<span data-ttu-id="75e6e-108">在下列情況下，請考慮使用值對應注釋。</span><span class="sxs-lookup"><span data-stu-id="75e6e-108">Consider using Value Map Annotation in the following situations.</span></span>

-   <span data-ttu-id="75e6e-109">當主控描繪的清單視圖或樹狀檢視合併使用影像時，您想要根據該影像提供自訂的可存取描述 ([**description**](description-property.md) 屬性) 。</span><span class="sxs-lookup"><span data-stu-id="75e6e-109">When an owner-drawn list view or tree view incorporates the use of images, and you want to provide a custom accessible description ([**Description**](description-property.md) property) based on that image.</span></span> <span data-ttu-id="75e6e-110">下圖顯示一個範例。</span><span class="sxs-lookup"><span data-stu-id="75e6e-110">The following illustration shows an example.</span></span>

    ![[開始] 功能表的圖例，其中圖示提供視覺線索給內容](images/iconlist.gif)

-   <span data-ttu-id="75e6e-112">當主控描繪的清單視圖或樹狀檢視控制項合併使用影像，使樹狀目錄或清單專案的作用像是簡單控制項（通常是核取方塊或選項按鈕），而您想要將影像對應至角色。</span><span class="sxs-lookup"><span data-stu-id="75e6e-112">When an owner-drawn list view or tree view control incorporates the use of images to make the tree or list items act like simple controls, typically checkboxes or radio buttons, and you want to map the image to a role.</span></span> <span data-ttu-id="75e6e-113">下列螢幕擷取畫面顯示範例。</span><span class="sxs-lookup"><span data-stu-id="75e6e-113">The following screen shot shows an example.</span></span>

    ![internet explorer 選項設定核取方塊和選項按鈕值的螢幕擷取畫面](images/customlist.gif)

-   <span data-ttu-id="75e6e-115">使用滑杆來選取可以描述為簡單整數以外的值時，如下列螢幕擷取畫面所示，其中的螢幕解析度設定會以字串描述。</span><span class="sxs-lookup"><span data-stu-id="75e6e-115">When a slider is used to select a value that can be described as something other than a simple integer, as in the following screen shot, where the screen resolution setting is described by a string.</span></span>

    ![用來設定螢幕解析度之滑杆的螢幕擷取畫面](images/slider.gif)

<span data-ttu-id="75e6e-117">使用值對應注釋，對應字串會指出清單或樹狀結構的影像索引如何對應至其角色或狀態。</span><span class="sxs-lookup"><span data-stu-id="75e6e-117">With value map annotation, a mapping string indicates how the list's or tree's image index corresponds to its role or state.</span></span> <span data-ttu-id="75e6e-118">或者，它可以指出滑杆的數值如何對應至字串。</span><span class="sxs-lookup"><span data-stu-id="75e6e-118">Or, it can indicate how a slider's numeric value corresponds to a string.</span></span> <span data-ttu-id="75e6e-119">例如，對應字串可能表示清單視圖的影像索引0對應到核取方塊的角色，而影像索引1則對應到選項按鈕的角色。</span><span class="sxs-lookup"><span data-stu-id="75e6e-119">For example, a mapping string may indicate that a list view's image index 0 maps to a role of check box and image index 1 maps to a role of radio button.</span></span> <span data-ttu-id="75e6e-120">使用 [**IAccPropServices：： SetHwndPropStr ()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) 將對應字串附加至控制項。</span><span class="sxs-lookup"><span data-stu-id="75e6e-120">Use [**IAccPropServices::SetHwndPropStr()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) to attach the mapping string to the control.</span></span>

<span data-ttu-id="75e6e-121">由於需要控制項專屬知識才能支援值對應，因此支援值對應注釋的控制項和屬性數目有限，包括滑杆值對應、清單視圖和樹狀檢視。</span><span class="sxs-lookup"><span data-stu-id="75e6e-121">Because control-specific knowledge is required to support value mapping, there are a limited number of controls and properties that support value map annotation, including slider value maps, list views, and tree views.</span></span>

## <a name="slider-value-map"></a><span data-ttu-id="75e6e-122">滑杆值對應</span><span class="sxs-lookup"><span data-stu-id="75e6e-122">Slider Value Map</span></span>

<span data-ttu-id="75e6e-123">**PROPID \_ACC \_ VALUEMAP** 包含從內部滑杆位置到人們可讀取字串的對應。</span><span class="sxs-lookup"><span data-stu-id="75e6e-123">**PROPID\_ACC\_VALUEMAP** contains a mapping from internal slider positions to human-readable strings.</span></span> <span data-ttu-id="75e6e-124">Oleacc.dll 滑杆 proxy 支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="75e6e-124">This property is supported by the Oleacc.dll slider proxy.</span></span> <span data-ttu-id="75e6e-125">如果在值對應中找到目前的滑杆值，對應的字串就會公開為值，而不是預設的百分比字串 (例如 "50" ) 。</span><span class="sxs-lookup"><span data-stu-id="75e6e-125">If the current slider value is found in the value map, the corresponding string will be exposed as the value instead of the default percentage string (for example, "50").</span></span>

## <a name="list-view-and-tree-view"></a><span data-ttu-id="75e6e-126">清單視圖和樹狀檢視</span><span class="sxs-lookup"><span data-stu-id="75e6e-126">List View and Tree View</span></span>

<span data-ttu-id="75e6e-127">**PROPID \_ACC \_ ROLEMAP**、 **PROPID \_ ACC \_ STATEMAP** 和 **PROPID \_ ACC \_ DESCRIPTONMAP** 提供從狀態映射索引到角色和狀態值的對應。</span><span class="sxs-lookup"><span data-stu-id="75e6e-127">**PROPID\_ACC\_ROLEMAP**, **PROPID\_ACC\_STATEMAP**, and **PROPID\_ACC\_DESCRIPTONMAP** provide mappings from state image indexes to role and state values.</span></span> <span data-ttu-id="75e6e-128">這些對應可讓這些映射索引對應到適當的角色 (通常是 [**角色 \_ 系統 \_ 選項按鈕**](object-roles.md) 或 [**角色 \_ 系統 \_ CHECKBUTTON**](object-roles.md)) 和其他狀態位 (通常會 [**\_ \_ 檢查) 狀態系統**](object-state-constants.md) 。</span><span class="sxs-lookup"><span data-stu-id="75e6e-128">These maps allow those image indexes to be mapped to appropriate roles (usually [**ROLE\_SYSTEM\_RADIOBUTTON**](object-roles.md) or [**ROLE\_SYSTEM\_CHECKBUTTON**](object-roles.md)) and additional state bits (usually [**STATE\_SYSTEM\_CHECKED**](object-state-constants.md)).</span></span>

<span data-ttu-id="75e6e-129">如需值對應注釋的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="75e6e-129">For more information about value map annotation, see the following topics:</span></span>

-   [<span data-ttu-id="75e6e-130">使用值對應注釋</span><span class="sxs-lookup"><span data-stu-id="75e6e-130">Using Value Map Annotation</span></span>](using-value-map-annotation.md)
-   [<span data-ttu-id="75e6e-131">值對應注釋範例</span><span class="sxs-lookup"><span data-stu-id="75e6e-131">Value Map Annotation Sample</span></span>](value-map-annotation-sample.md)

## <a name="annotation-map-format"></a><span data-ttu-id="75e6e-132">注釋地圖格式</span><span class="sxs-lookup"><span data-stu-id="75e6e-132">Annotation Map Format</span></span>

<span data-ttu-id="75e6e-133">下表描述批註對應中包含的欄位。</span><span class="sxs-lookup"><span data-stu-id="75e6e-133">The following table describes the fields that are included in an annotation map.</span></span>



| <span data-ttu-id="75e6e-134">欄位</span><span class="sxs-lookup"><span data-stu-id="75e6e-134">Field</span></span>               | <span data-ttu-id="75e6e-135">描述</span><span class="sxs-lookup"><span data-stu-id="75e6e-135">Description</span></span>                                                                                                                                                                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75e6e-136">的</span><span class="sxs-lookup"><span data-stu-id="75e6e-136">'A'</span></span>                 | <span data-ttu-id="75e6e-137">表示使用特定的編碼配置。</span><span class="sxs-lookup"><span data-stu-id="75e6e-137">Indicates that a particular coding scheme is used.</span></span> <span data-ttu-id="75e6e-138">未來的編碼配置可能會支援其他首碼。</span><span class="sxs-lookup"><span data-stu-id="75e6e-138">Additional prefixes may be supported for future encoding schemes.</span></span>                                                                                                                                                          |
| <span data-ttu-id="75e6e-139">分隔符號</span><span class="sxs-lookup"><span data-stu-id="75e6e-139">Delimiter character</span></span> | <span data-ttu-id="75e6e-140">通常會使用冒號 (： ) ，但可以是 **Null** 或空白以外的另一個字元。</span><span class="sxs-lookup"><span data-stu-id="75e6e-140">Usually a colon (:) is used, but can be another character except for **NULL** or an empty space.</span></span> <span data-ttu-id="75e6e-141">因為此字元將作為其餘欄位的分隔符號，所以不能當做地圖中值的一部分使用。</span><span class="sxs-lookup"><span data-stu-id="75e6e-141">Because this character will be used as a delimiter for the remaining fields, it may not be used as part of a value in the map.</span></span>                                               |
| <span data-ttu-id="75e6e-142">0、1或2</span><span class="sxs-lookup"><span data-stu-id="75e6e-142">0, 1, or 2</span></span>          | <span data-ttu-id="75e6e-143">值，指出正在使用的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="75e6e-143">A value that indicates which key is being used.</span></span> <span data-ttu-id="75e6e-144">針對樹狀檢視和清單視圖角色和狀態對應，此索引鍵可以是 0 (映射索引) 、1 (狀態影像索引) ，或 2 (重迭影像索引) 。</span><span class="sxs-lookup"><span data-stu-id="75e6e-144">For Tree View and List View role and state maps, this key can be 0 (image index), 1 (state image index), or 2 (overlay image index).</span></span> <span data-ttu-id="75e6e-145">針對滑杆和其他不提供按鍵選擇的控制項，此值必須為0。</span><span class="sxs-lookup"><span data-stu-id="75e6e-145">For sliders and other controls that do not offer a choice of keys, this value must be 0.</span></span> |
| <span data-ttu-id="75e6e-146">分隔符號</span><span class="sxs-lookup"><span data-stu-id="75e6e-146">Delimiter character</span></span> | <span data-ttu-id="75e6e-147">:</span><span class="sxs-lookup"><span data-stu-id="75e6e-147">:</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="75e6e-148">索引鍵/值組</span><span class="sxs-lookup"><span data-stu-id="75e6e-148">Key value pairs</span></span>     | <span data-ttu-id="75e6e-149">每個配對都包含一個金鑰字串和一個分隔符號。</span><span class="sxs-lookup"><span data-stu-id="75e6e-149">Each pair consists of a key string and a delimiter character.</span></span> <span data-ttu-id="75e6e-150">索引鍵字串是一個數位，而且可能是以十進位或十六進位 (開頭為 "0x" 前置詞) 格式。</span><span class="sxs-lookup"><span data-stu-id="75e6e-150">The key string is a number and may be in decimal or hexadecimal (with a leading "0x" prefix) format.</span></span>                                                                                                            |
| <span data-ttu-id="75e6e-151">值字串</span><span class="sxs-lookup"><span data-stu-id="75e6e-151">Value string</span></span>        | <span data-ttu-id="75e6e-152">如果是值對應，這就是字串。</span><span class="sxs-lookup"><span data-stu-id="75e6e-152">For value maps, this is a string.</span></span> <span data-ttu-id="75e6e-153">針對角色和狀態對應，這是數位 (十進位或十六進位) 。</span><span class="sxs-lookup"><span data-stu-id="75e6e-153">For role and state maps, this is a number (decimal or hexadecimal).</span></span>                                                                                                                                                                         |
| <span data-ttu-id="75e6e-154">分隔符號</span><span class="sxs-lookup"><span data-stu-id="75e6e-154">Delimiter character</span></span> | <span data-ttu-id="75e6e-155">:</span><span class="sxs-lookup"><span data-stu-id="75e6e-155">:</span></span>                                                                                                                                                                                                                                                                             |



 

<span data-ttu-id="75e6e-156">例如，地圖看起來可能如下所示：</span><span class="sxs-lookup"><span data-stu-id="75e6e-156">For example, a map may look like the following:</span></span>


```C++
A:0:0:Cold:1:Warm:3:Hot:
```



<span data-ttu-id="75e6e-157">將此值對應套用至滑杆控制項時，當滑杆位於位置1時，將會公開 "暖" 值。</span><span class="sxs-lookup"><span data-stu-id="75e6e-157">When this value map is applied to a slider control, a value of "Warm" will be exposed when the slider is at position 1.</span></span> <span data-ttu-id="75e6e-158">因為這個範例不包含值2，所以會公開該位置的預設值。</span><span class="sxs-lookup"><span data-stu-id="75e6e-158">Because value 2 is not included in this example, the default value for that position will be exposed.</span></span> <span data-ttu-id="75e6e-159">若為滑杆，預設值會是百分比值，例如33。</span><span class="sxs-lookup"><span data-stu-id="75e6e-159">For a slider, the default would be a percentage value, such as 33.</span></span>

 

 





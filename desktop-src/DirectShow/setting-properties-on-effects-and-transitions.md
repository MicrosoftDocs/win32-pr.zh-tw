---
description: 設定效果和轉換的屬性
ms.assetid: ce773140-7e50-4b72-8cb5-e34cba51644d
title: 設定效果和轉換的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ddd129eb9d4ab24ebef6f5c760a4211f26c9a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972915"
---
# <a name="setting-properties-on-effects-and-transitions"></a><span data-ttu-id="1ab29-103">設定效果和轉換的屬性</span><span class="sxs-lookup"><span data-stu-id="1ab29-103">Setting Properties on Effects and Transitions</span></span>

<span data-ttu-id="1ab29-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="1ab29-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="1ab29-105">許多 [DirectShow 編輯服務](directshow-editing-services.md) 效果和轉換都支援控制其行為的屬性。</span><span class="sxs-lookup"><span data-stu-id="1ab29-105">Many [DirectShow Editing Services](directshow-editing-services.md) effects and transitions support properties that control their behavior.</span></span> <span data-ttu-id="1ab29-106">應用程式可以使用 [**IPropertySetter**](ipropertysetter.md) 介面來設定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1ab29-106">An application can set the value of a property using the [**IPropertySetter**](ipropertysetter.md) interface.</span></span> <span data-ttu-id="1ab29-107">基礎效果或轉換物件必須支援 **IDispatch** 來設定屬性。</span><span class="sxs-lookup"><span data-stu-id="1ab29-107">The underlying effect or transition object must support **IDispatch** for setting the properties.</span></span> <span data-ttu-id="1ab29-108">使用影片效果和轉換，應用程式可以設定一段時間後會變更的值範圍。</span><span class="sxs-lookup"><span data-stu-id="1ab29-108">With video effects and transitions, the application can set a range of values that change over time.</span></span> <span data-ttu-id="1ab29-109"> (例如，您可以設定抹除轉換，以在整個框架中來回移動。 ) 有音訊效果時，屬性的值為靜態，且不會隨著時間而變更。</span><span class="sxs-lookup"><span data-stu-id="1ab29-109">(For example, you can set a wipe transition to move back and forth across the frame.) With audio effects, the value of the property is static and cannot change over time.</span></span> <span data-ttu-id="1ab29-110">唯一的例外是 [音量信封](volume-envelope-effect.md) 效果，其支援磁片區層級的動態屬性。</span><span class="sxs-lookup"><span data-stu-id="1ab29-110">The only exception is the [Volume Envelope](volume-envelope-effect.md) effect, which supports a dynamic property for the volume level.</span></span>

<span data-ttu-id="1ab29-111">若要設定屬性，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="1ab29-111">To set a property, perform the following steps.</span></span>

1.  <span data-ttu-id="1ab29-112">建立屬性 setter (CLSID PropertySetter) 的實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1ab29-112">Create an instance of the property setter (CLSID\_PropertySetter).</span></span>
2.  <span data-ttu-id="1ab29-113">以屬性資料填入 [**DEXTER \_ PARAM**](dexter-param.md) 和 [**DEXTER \_ 值**](dexter-value.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="1ab29-113">Fill [**DEXTER\_PARAM**](dexter-param.md) and [**DEXTER\_VALUE**](dexter-value.md) structures with the property data.</span></span> <span data-ttu-id="1ab29-114">以下將討論這些結構。</span><span class="sxs-lookup"><span data-stu-id="1ab29-114">These structures are discussed below.</span></span>
3.  <span data-ttu-id="1ab29-115">將 [**DEXTER \_ PARAM**](dexter-param.md) 和 [**DEXTER \_ 值**](dexter-value.md) 結構傳遞至 [**IPropertySetter：： AddProp**](ipropertysetter-addprop.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="1ab29-115">Pass the [**DEXTER\_PARAM**](dexter-param.md) and [**DEXTER\_VALUE**](dexter-value.md) structures to the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method.</span></span>
4.  <span data-ttu-id="1ab29-116">針對您要設定的每個屬性重複步驟2和3。</span><span class="sxs-lookup"><span data-stu-id="1ab29-116">Repeat steps 2 and 3 for each property you want to set.</span></span>
5.  <span data-ttu-id="1ab29-117">將 [**IPropertySetter**](ipropertysetter.md) 介面指標傳遞至 [**IAMTimelineObj：： SetPropertySetter**](iamtimelineobj-setpropertysetter.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="1ab29-117">Pass the [**IPropertySetter**](ipropertysetter.md) interface pointer to the [**IAMTimelineObj::SetPropertySetter**](iamtimelineobj-setpropertysetter.md) method.</span></span>

<span data-ttu-id="1ab29-118">[**DEXTER \_ PARAM**](dexter-param.md)結構會指定所要設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="1ab29-118">The [**DEXTER\_PARAM**](dexter-param.md) structure specifies which property is being set.</span></span> <span data-ttu-id="1ab29-119">它包含下列成員。</span><span class="sxs-lookup"><span data-stu-id="1ab29-119">It contains the following members.</span></span>

-   <span data-ttu-id="1ab29-120">**名稱**：屬性的名稱</span><span class="sxs-lookup"><span data-stu-id="1ab29-120">**Name**: Name of the property</span></span>
-   <span data-ttu-id="1ab29-121">**dispID**： Reserved，必須為零</span><span class="sxs-lookup"><span data-stu-id="1ab29-121">**dispID**: Reserved, must be zero</span></span>
-   <span data-ttu-id="1ab29-122">值 **：值** 數目</span><span class="sxs-lookup"><span data-stu-id="1ab29-122">**nValues**: Number of values</span></span>

<span data-ttu-id="1ab29-123">DEXTER \_ 值結構會指定屬性在指定時間的值。</span><span class="sxs-lookup"><span data-stu-id="1ab29-123">The DEXTER\_VALUE structure specifies the value of a property at a given time.</span></span> <span data-ttu-id="1ab29-124">它包含下列成員。</span><span class="sxs-lookup"><span data-stu-id="1ab29-124">It contains the following members.</span></span>

-   <span data-ttu-id="1ab29-125">**v**：為屬性指定新值的 VARIANT 類型。</span><span class="sxs-lookup"><span data-stu-id="1ab29-125">**v**: VARIANT type that specifies a new value for the property.</span></span> <span data-ttu-id="1ab29-126">這個變異的 **vt** 成員定義了屬性的資料型別。</span><span class="sxs-lookup"><span data-stu-id="1ab29-126">The **vt** member of this VARIANT defines the data type of the property.</span></span> <span data-ttu-id="1ab29-127">如需 **VARIANT** 型別的詳細資訊，請參閱 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="1ab29-127">For more information on the **VARIANT** type, see the Windows SDK.</span></span>
-   <span data-ttu-id="1ab29-128">**rt**：屬性會假設此值（相對於效果或轉換的開始時間）的參考時間。</span><span class="sxs-lookup"><span data-stu-id="1ab29-128">**rt**: Reference time when the property assumes this value, relative to the starting time of the effect or transition.</span></span> <span data-ttu-id="1ab29-129">效果或轉換的開始時間相對於其父物件的開始時間。</span><span class="sxs-lookup"><span data-stu-id="1ab29-129">The start time of the effect or transition is relative to the start time of its parent object.</span></span>
-   <span data-ttu-id="1ab29-130">**dwInterp**：指定屬性如何從先前值變更為新值的旗標。</span><span class="sxs-lookup"><span data-stu-id="1ab29-130">**dwInterp**: Flag that specifies how the property changes from the previous value to the new value.</span></span> <span data-ttu-id="1ab29-131">使用 DEXTERF \_ 跳躍旗標，屬性會在指定的時間立即跳到新值。</span><span class="sxs-lookup"><span data-stu-id="1ab29-131">With the DEXTERF\_JUMP flag, the property jumps instantly to the new value at the specified time.</span></span> <span data-ttu-id="1ab29-132">使用 DEXTERF \_ 插補旗標，屬性會以線性方式從先前的值插入。</span><span class="sxs-lookup"><span data-stu-id="1ab29-132">With the DEXTERF\_INTERPOLATE flag, the property is interpolated linearly from the previous value.</span></span>

<span data-ttu-id="1ab29-133">如果您將 **vt** 成員設定為 vt \_ BSTR，屬性 setter 會進行任何必要的轉換。</span><span class="sxs-lookup"><span data-stu-id="1ab29-133">If you set the **vt** member to VT\_BSTR, the property setter makes any necessary conversions.</span></span> <span data-ttu-id="1ab29-134">若為浮點值，請在小數點之前加上前置零。</span><span class="sxs-lookup"><span data-stu-id="1ab29-134">For floating-point values, include the leading zero before the decimal place.</span></span> <span data-ttu-id="1ab29-135">例如，0.3，而不是. 3。</span><span class="sxs-lookup"><span data-stu-id="1ab29-135">For example, 0.3, not .3.</span></span>

> [!Note]  
> <span data-ttu-id="1ab29-136">應用程式應該避免依賴從 **BSTR** 轉換成數值。</span><span class="sxs-lookup"><span data-stu-id="1ab29-136">Applications should avoid relying on the conversion from **BSTR** s to numeric values.</span></span> <span data-ttu-id="1ab29-137">如果屬性具有數值，則可以使用適當的數值 **VARIANT** 類型。</span><span class="sxs-lookup"><span data-stu-id="1ab29-137">If the property has a numeric value, use the appropriate numeric **VARIANT** type is possible.</span></span>

 

<span data-ttu-id="1ab29-138">屬性的值可能會隨著時間而變更，因此 [**IPropertySetter：： AddProp**](ipropertysetter-addprop.md) 方法會採用單一 [**DEXTER \_ 參數**](dexter-param.md) 結構和 [**DEXTER \_ 值**](dexter-value.md) 結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="1ab29-138">The value of a property can change over time, so the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method takes a single [**DEXTER\_PARAM**](dexter-param.md) structure and a pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span> <span data-ttu-id="1ab29-139">陣列會為屬性定義一組以時間為基礎的值。</span><span class="sxs-lookup"><span data-stu-id="1ab29-139">The array defines a set of time-based values for the property.</span></span> <span data-ttu-id="1ab29-140">陣列的成員必須是遞增的時間順序，而且 DEXTER PARAM 結構 **的次序成員** \_ 必須等於陣列的長度。</span><span class="sxs-lookup"><span data-stu-id="1ab29-140">The members of the array must be in ascending time order, and the **nValues** member of the DEXTER\_PARAM structure must equal the length of the array.</span></span>

<span data-ttu-id="1ab29-141">下列程式碼範例會建立適用于 [SMPTE](smpte-wipe-transition.md) 抹除轉換的屬性資料。</span><span class="sxs-lookup"><span data-stu-id="1ab29-141">The following code example creates property data for the [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span> <span data-ttu-id="1ab29-142">它會將抹除碼設定為120，以建立 oval 抹除。</span><span class="sxs-lookup"><span data-stu-id="1ab29-142">It sets the wipe code to 120, which creates an oval wipe.</span></span> <span data-ttu-id="1ab29-143">它會將參考時間設定為零，表示轉換開始。</span><span class="sxs-lookup"><span data-stu-id="1ab29-143">It sets the reference time to zero, indicating the start of the transition.</span></span>


```C++
IPropertySetter     *pProp;   // Property setter
IAMTimelineObj      *pTransObj;  // Transition object
// Create an SMPTE Wipe transition object. (Not shown)

hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER,
    IID_IPropertySetter, (void**) &pProp);

// Error checking is omitted for clarity...

DEXTER_PARAM param;
DEXTER_VALUE *pValue = (DEXTER_VALUE*)CoTaskMemAlloc(sizeof(DEXTER_VALUE));

// Initialize the parameter. 
param.Name = SysAllocString(L"MaskNum");
param.dispID = 0;
param.nValues = 1;

// Initialize the value.
pValue->v.vt = VT_I4;
pValue->v.lVal = 120; // Oval
pValue->rt = 0;
pValue->dwInterp = DEXTERF_JUMP;

pProp->AddProp(param, pValue);

// Free allocated resources.
SysFreeString(param.Name);
VariantClear(&(pValue->v));
CoTaskMemFree(pValue);

// Set the property on the transition.
pTransObj->SetPropertySetter(pProp);
pProp->Release();
```



<span data-ttu-id="1ab29-144">**動態變更屬性**</span><span class="sxs-lookup"><span data-stu-id="1ab29-144">**Dynamically Changing Properties**</span></span>

<span data-ttu-id="1ab29-145">轉譯影片編輯專案之後，就可以在圖形執行時修改效果或轉換物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="1ab29-145">After you render a video editing project, it is possible to modify an effect or transition object's properties while the graph is running.</span></span> <span data-ttu-id="1ab29-146">不過，只有當您在應用程式呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md)之前設定該物件的屬性時，才有可能這樣做。</span><span class="sxs-lookup"><span data-stu-id="1ab29-146">However, this is possible only if you set properties on that object before the application called [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span> <span data-ttu-id="1ab29-147">若是如此，您可以在效果或轉換上呼叫 [**IAMTimelineObj：： GetPropertySetter**](iamtimelineobj-getpropertysetter.md) 、清除或修改屬性，變更將會在圖形執行時動態發生。</span><span class="sxs-lookup"><span data-stu-id="1ab29-147">If so, you can call [**IAMTimelineObj::GetPropertySetter**](iamtimelineobj-getpropertysetter.md) on the effect or transition, clear or modify the properties, and the changes will happen dynamically as the graph is running.</span></span> <span data-ttu-id="1ab29-148">發生變更時可能會有視覺異常，因此建議僅供預覽。</span><span class="sxs-lookup"><span data-stu-id="1ab29-148">There may be visual anomalies while the change occurs, so this is recommended only for preview.</span></span> <span data-ttu-id="1ab29-149">當您將專案寫入檔案時，請勿變更屬性。</span><span class="sxs-lookup"><span data-stu-id="1ab29-149">Do not change the properties while you are writing the project to a file.</span></span>

<span data-ttu-id="1ab29-150">如果您在呼叫 **ConnectFrontEnd** 之前未在效果或轉換物件上設定任何屬性，您就無法在圖形執行時將屬性加入其中。</span><span class="sxs-lookup"><span data-stu-id="1ab29-150">If you did not set any properties on the effect or transition object before you called **ConnectFrontEnd**, you cannot add properties to it while the graph is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ab29-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="1ab29-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ab29-152">使用效果和轉換</span><span class="sxs-lookup"><span data-stu-id="1ab29-152">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 




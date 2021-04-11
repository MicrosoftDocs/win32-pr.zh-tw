---
description: 影片色彩來源
ms.assetid: e6addd55-06ca-4d4b-b2b0-fde281fab244
title: 影片色彩來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e9c751d74a78b027d50f033acb3709d18fe8f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193521"
---
# <a name="video-color-source"></a><span data-ttu-id="aec43-103">影片色彩來源</span><span class="sxs-lookup"><span data-stu-id="aec43-103">Video Color Source</span></span>

> [!Note]  
> <span data-ttu-id="aec43-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="aec43-104">\[Deprecated.</span></span> <span data-ttu-id="aec43-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="aec43-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="aec43-106">影片色彩來源會建立純色的連續影片影像。</span><span class="sxs-lookup"><span data-stu-id="aec43-106">The Video Color Source creates a continuous video image of a solid color.</span></span>

<span data-ttu-id="aec43-107">類別識別碼 (CLSID) ： **{0CFDD070-581A-11D2-9EE6-006008039E37}**</span><span class="sxs-lookup"><span data-stu-id="aec43-107">Class ID (CLSID): **{0CFDD070-581A-11D2-9EE6-006008039E37}**</span></span>

<span data-ttu-id="aec43-108">CLSID 變數名稱： **clsid \_ ColorSource**</span><span class="sxs-lookup"><span data-stu-id="aec43-108">CLSID Variable Name: **CLSID\_ColorSource**</span></span>

<span data-ttu-id="aec43-109">屬性</span><span class="sxs-lookup"><span data-stu-id="aec43-109">Properties</span></span>



| <span data-ttu-id="aec43-110">屬性</span><span class="sxs-lookup"><span data-stu-id="aec43-110">Property</span></span> | <span data-ttu-id="aec43-111">類型</span><span class="sxs-lookup"><span data-stu-id="aec43-111">Type</span></span>      | <span data-ttu-id="aec43-112">預設</span><span class="sxs-lookup"><span data-stu-id="aec43-112">Default</span></span> | <span data-ttu-id="aec43-113">描述</span><span class="sxs-lookup"><span data-stu-id="aec43-113">Description</span></span>                                   |
|----------|-----------|---------|-----------------------------------------------|
| <span data-ttu-id="aec43-114">色彩</span><span class="sxs-lookup"><span data-stu-id="aec43-114">"Color"</span></span>  | <span data-ttu-id="aec43-115">**Dword**</span><span class="sxs-lookup"><span data-stu-id="aec43-115">**DWORD**</span></span> | <span data-ttu-id="aec43-116">0</span><span class="sxs-lookup"><span data-stu-id="aec43-116">0</span></span>       | <span data-ttu-id="aec43-117">指定要產生的色彩。</span><span class="sxs-lookup"><span data-stu-id="aec43-117">Specifies the color to generate.</span></span> <span data-ttu-id="aec43-118">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="aec43-118">See Remarks.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="aec43-119">備註</span><span class="sxs-lookup"><span data-stu-id="aec43-119">Remarks</span></span>

<span data-ttu-id="aec43-120">影片色彩來源與來源物件搭配使用。</span><span class="sxs-lookup"><span data-stu-id="aec43-120">The Video Color Source is used with source objects.</span></span> <span data-ttu-id="aec43-121">首先，建立新的來源物件。</span><span class="sxs-lookup"><span data-stu-id="aec43-121">First, create a new source object.</span></span> <span data-ttu-id="aec43-122">然後藉 \_ 由呼叫 [**IAMTimelineObj：： SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) 方法，將來源物件的子物件 GUID 設定為 CLSID ColorSource。</span><span class="sxs-lookup"><span data-stu-id="aec43-122">Then set the source object's subobject GUID to CLSID\_ColorSource, by calling the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="aec43-123">若要設定色彩，請建立 [屬性 Setter](property-setter.md) 物件，並在時間零套用 "color" 屬性。</span><span class="sxs-lookup"><span data-stu-id="aec43-123">To set the color, create a [Property Setter](property-setter.md) object and apply the "Color" property at time zero.</span></span> <span data-ttu-id="aec43-124">這個屬性的值是 *0xAARRGGBB* 格式的十六進位數位，其中 *AA* 是 Alpha 值、 *RR* 是紅色值、 *GG* 是綠色值，而 *BB* 是藍色值。</span><span class="sxs-lookup"><span data-stu-id="aec43-124">The value of this property is a hexadecimal number with the format *0xAARRGGBB*, where *AA* is the alpha value, *RR* is the red value, *GG* is the green value, and *BB* is the blue value.</span></span> <span data-ttu-id="aec43-125">Alpha 值的範圍從 0x00 (透明) 到 0xFF (不透明) 。</span><span class="sxs-lookup"><span data-stu-id="aec43-125">Alpha values range from 0x00 (transparent) to 0xFF (opaque).</span></span> <span data-ttu-id="aec43-126">屬性是靜態的，且必須套用於時為零。</span><span class="sxs-lookup"><span data-stu-id="aec43-126">The property is static and must be applied at time zero.</span></span>

<span data-ttu-id="aec43-127">如果您未指定 Alpha 值，則預設為零 (透明) 。</span><span class="sxs-lookup"><span data-stu-id="aec43-127">If you do not specify the alpha value, it defaults to zero (transparent).</span></span> <span data-ttu-id="aec43-128">在32位顏色的影片專案中，這會導致使用 Alpha 的轉換或效果，以完全透明的方式將影片色彩來源轉譯。</span><span class="sxs-lookup"><span data-stu-id="aec43-128">In a 32-bit-color video project, this will cause transitions or effects that use alpha to render the Video Color Source as completely transparent.</span></span> <span data-ttu-id="aec43-129">為了安全起見，請一律指定 Alpha。</span><span class="sxs-lookup"><span data-stu-id="aec43-129">To be safe, always specify the alpha.</span></span> <span data-ttu-id="aec43-130">例如，不透明的黑色是 **0xFF000000**。</span><span class="sxs-lookup"><span data-stu-id="aec43-130">For example, opaque black is **0xFF000000**.</span></span>

<span data-ttu-id="aec43-131">下列程式碼範例顯示如何使用這個物件。</span><span class="sxs-lookup"><span data-stu-id="aec43-131">The following code example shows how to use this object.</span></span> <span data-ttu-id="aec43-132">如需使用 [**IPropertySetter**](ipropertysetter.md)的詳細資訊，請參閱 [設定效果和轉換的屬性](setting-properties-on-effects-and-transitions.md)：</span><span class="sxs-lookup"><span data-stu-id="aec43-132">For more information about using [**IPropertySetter**](ipropertysetter.md), see [Setting Properties on Effects and Transitions](setting-properties-on-effects-and-transitions.md):</span></span>


```C++
DWORD           dwYellow = 0xFFFF00;
IAMTimelineObj  *pSource = NULL;

// Create the source.
HRESULT hr = pTimeline->CreateEmptyNode(&pSource, TIMELINE_MAJOR_TYPE_SOURCE);
if (SUCCEEDED(hr))
{
    hr = pSource->SetStartStop(0, 50000000);
}

if (SUCCEEDED(hr))
{
    hr = pSource->SetSubObjectGUID(CLSID_ColorSource);
}

// Create a property setter.
if (SUCCEEDED(hr))
{
    IPropertySetter *pProp = NULL;
    
    hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pProp));

    if SUCCEEDED(hr))
    {
        // Set the color.    
        DEXTER_PARAM param;
        DEXTER_VALUE val;

        param.Name = SysAllocString(OLESTR("Color"));
        param.dispID = 0;
        param.nValues = 1;

        if (param.Name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            val.v.vt = VT_I4;
            val.v.lVal = dwYellow;
            val.rt = 0;  // Time must be zero.
            val.dwInterp = DEXTERF_JUMP;

            hr = pProp->AddProp(param, &val);
            
            SysFreeString(param.Name);
        }

        if (SUCCEEDED(hr))
        {
            hr = pSource->SetPropertySetter(pProp); 
        }
        pProp->Release();
    }
}
```



<span data-ttu-id="aec43-133">下列範例顯示在上一個範例中建立之物件的 XML 標記法。</span><span class="sxs-lookup"><span data-stu-id="aec43-133">The following example shows the XML representation of the object created in the previous example.</span></span> <span data-ttu-id="aec43-134">在此情況下， [**param**](param-element.md) 元素不支援 [**at**](at-element.md) 或 [**線性**](linear-element.md) 元素，因為物件不支援動態屬性：</span><span class="sxs-lookup"><span data-stu-id="aec43-134">In this case the [**param**](param-element.md) element does not support [**at**](at-element.md) or [**linear**](linear-element.md) elements, because the object does not support dynamic properties:</span></span>


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 




---
title: 3D 查閱資料表效果
description: 3D 查閱資料表是一般用途的效果，可透過預先計算效果將所有輸入值子集的輸入對應到輸出的方式，來封裝任何 1 1 圖像效果。
ms.assetid: 2f0b4b6d-f371-101c-918a-bf564778e593
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d0c6c5df1aa873d3458345d77a46f6f3fdae40b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844424"
---
# <a name="3d-lookup-table-effect"></a><span data-ttu-id="a6012-103">3D 查閱資料表效果</span><span class="sxs-lookup"><span data-stu-id="a6012-103">3D lookup table effect</span></span>

<span data-ttu-id="a6012-104">3D 查閱資料表是一般用途的效果，可透過預先計算效果將所有輸入值子集的輸入對應到輸出的方式，來封裝任何1:1 圖像效果。</span><span class="sxs-lookup"><span data-stu-id="a6012-104">A 3D look-up table is a general-purpose effect that is used to encapsulate any 1:1 imaging effect by pre-computing how the effect maps inputs to outputs for a subset of all input values.</span></span>

<span data-ttu-id="a6012-105"> (LUT) 效果的3D 查閱資料表效果會使用影像的 RGB 色彩值來為3D 材質編制索引，其中紋理包含任意效果管線的預先計算輸出值，藉以修改輸入影像。</span><span class="sxs-lookup"><span data-stu-id="a6012-105">The 3D Lookup Table (LUT) effect modifies an input image by using the image's RGB color value to index a 3D texture, where the texture contains a precomputed output value of an arbitrary effect pipeline.</span></span>

<span data-ttu-id="a6012-106">3D LUT 必須載入 GPU 材質資源才能轉譯，而這可能會耗用大量資源，視材質和裝置功能的大小而定。</span><span class="sxs-lookup"><span data-stu-id="a6012-106">The 3D LUT must be loaded into a GPU texture resource in order to be rendered, and this can be expensive depending on the size of the texture and the device capabilities.</span></span> <span data-ttu-id="a6012-107">應用程式開發人員可以使用 [**ID2D1LookupTable3D**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d) D2D 資源指定何時支付此成本。</span><span class="sxs-lookup"><span data-stu-id="a6012-107">Application developers can specify when to pay this cost using the [**ID2D1LookupTable3D**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d) D2D resource.</span></span> <span data-ttu-id="a6012-108">**ID2D1LookupTable3D** 具有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="a6012-108">**ID2D1LookupTable3D** has the following attributes:</span></span>

-   <span data-ttu-id="a6012-109">提供 3D LUT 的 GPU 資源的抽象化標記法。</span><span class="sxs-lookup"><span data-stu-id="a6012-109">Provides an abstracted representation of 3D LUT's GPU resource.</span></span>
-   <span data-ttu-id="a6012-110">視裝置功能而定，將會建立2D 或3D 材質，並填入提供的 LUT 資料。</span><span class="sxs-lookup"><span data-stu-id="a6012-110">Depending on the device capabilities, either a 2D or 3D texture will be created and filled with the provided LUT data.</span></span>
-   <span data-ttu-id="a6012-111">可以傳遞至 3D LUT 效果的屬性以進行呈現。</span><span class="sxs-lookup"><span data-stu-id="a6012-111">Can be passed to the 3D LUT effect's property for rendering.</span></span>

<span data-ttu-id="a6012-112">這項效果的 CLSID 是 CLSID \_ D2D1LookupTable3D。</span><span class="sxs-lookup"><span data-stu-id="a6012-112">The CLSID for this effect is CLSID\_D2D1LookupTable3D.</span></span>

-   [<span data-ttu-id="a6012-113">範例影像</span><span class="sxs-lookup"><span data-stu-id="a6012-113">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="a6012-114">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="a6012-114">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="a6012-115">效果屬性</span><span class="sxs-lookup"><span data-stu-id="a6012-115">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="a6012-116">需求</span><span class="sxs-lookup"><span data-stu-id="a6012-116">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a6012-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="a6012-117">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="a6012-118">範例影像</span><span class="sxs-lookup"><span data-stu-id="a6012-118">Example image</span></span>

![效果輸出的範例](images/3dlookuptable-effect.png)

## <a name="sample-code"></a><span data-ttu-id="a6012-120">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="a6012-120">Sample code</span></span>

```cpp
//
    // 1. Generate the lookup table data and create an ID2D1LookupTable3D.
    //
 
    // Create a 16x16x16 LUT of arbitrary data type T.
    UINT extents[] = { 16, 16, 16 };
    UINT cElements = extents[0] * extents[1] * extents[2] * 4;
    UINT cbElements = cElements * formatSize;
 
    // Compute the step size in each direction to vary the RGB 
    // channels uniformly over the range [0, 1]
    float steps[] = 
    { 
        1.0f / static_cast<float>(extents[0] - 1),
        1.0f / static_cast<float>(extents[1] - 1),
        1.0f / static_cast<float>(extents[2] - 1),
    };
 
    CArray<BYTE> lutData;
    IFR(lutData.Resize(cbElements));
 
    T* pData = reinterpret_cast<T *>(lutData.GetData());
    T oneValue = ConvertValue<T>(1.0f);
    
    // Generate the LUT by applying an imaging pipeline to RGB values.
    for (UINT iR = 0; iR < extents[2]; iR++)
    {
        for (UINT iG = 0; iG < extents[1]; iG++)
        {
            for (UINT iB = 0; iB < extents[0]; iB++)
            {
                T outputColor[3];
                ApplyPipeline(iR * steps[2], iG * steps[1], iB * steps[0], &outputColor);
 
                pData[0] = outColor[0];
                pData[1] = outColor[1];
                pData[2] = outColor[2];
 
                // Set opaque alpha in the output
                pData[3] = oneValue;
 
                // Advance the pointer
                pData += sizeof(T) * 4;
            }
        }
    }
    
    // Compute the strides of the LUT data.
    UINT strides[2];
    IFR(UIntMult(sizeof(T) * 4, extents[0], &strides[0]));
    IFR(UIntMult(strides[0], extents[1], &strides[1]));
    
    D2D1_BUFFER_PRECISION precision = GetBufferPrecision<T>();
 
    // Create an ID2D1LookupTable3D from the LUT data.
    CComPtr<ID2D1LookupTable3D> sp3dLut;
    IFR(_spEffectContext1->CreateLookupTable3D(
        precision,
        extents,
        lutData.GetData(),
        lutData.GetCount(),
        strides,
        &sp3dLut
        )); 
 
    //
    // 2. To apply the lookup table to an input image, create a LookupTable3D effect
    //    and pass the ID2D1LookupTable3D to the effect as a property.
    //
 
    // Create a 3D LUT effect to render our LUT.
    CComPtr<ID2D1Effect> sp3dLutEffect;
    IFR(pEffectContext->CreateEffect(CLSID_D2D1LookupTable3D, &sp3dLutEffect)); 
 
    // Set the LUT as a property on the effect.
    IFR(sp3dLutEffect->SetValue(D2D1_LOOKUPTABLE3D_PROP_LUT, _spLut));
```

## <a name="effect-properties"></a><span data-ttu-id="a6012-121">效果屬性</span><span class="sxs-lookup"><span data-stu-id="a6012-121">Effect properties</span></span>

<span data-ttu-id="a6012-122">3D 查閱資料表效果的屬性是由 [**D2D1 \_ LOOKUPTABLE3D \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_lookuptable3d_prop) 屬性列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="a6012-122">The properties for the 3D lookup table effect are defined by the [**D2D1\_LOOKUPTABLE3D\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_lookuptable3d_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6012-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6012-123">Requirements</span></span>



| <span data-ttu-id="a6012-124">需求</span><span class="sxs-lookup"><span data-stu-id="a6012-124">Requirement</span></span> | <span data-ttu-id="a6012-125">值</span><span class="sxs-lookup"><span data-stu-id="a6012-125">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="a6012-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6012-126">Minimum supported client</span></span> | <span data-ttu-id="a6012-127">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6012-127">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="a6012-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6012-128">Minimum supported server</span></span> | <span data-ttu-id="a6012-129">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6012-129">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="a6012-130">標頭</span><span class="sxs-lookup"><span data-stu-id="a6012-130">Header</span></span>                   | <span data-ttu-id="a6012-131">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="a6012-131">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="a6012-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="a6012-132">Library</span></span>                  | <span data-ttu-id="a6012-133">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="a6012-133">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="a6012-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="a6012-134">Related topics</span></span>

* [<span data-ttu-id="a6012-135">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="a6012-135">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

---
title: 塔效果
description: 您可以使用此效果來輸出影像的一部分，但是將區域保留在部分外部，以用於後續作業。
ms.assetid: D35E32CB-4DF7-408F-A717-1E421DDC8763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f9e1d4c6df0698d47a35eb2cbdaf670b98ed125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466320"
---
# <a name="atlas-effect"></a><span data-ttu-id="14c13-103">塔效果</span><span class="sxs-lookup"><span data-stu-id="14c13-103">Atlas effect</span></span>

<span data-ttu-id="14c13-104">您可以使用此效果來輸出影像的一部分，但是將區域保留在部分外部，以用於後續作業。</span><span class="sxs-lookup"><span data-stu-id="14c13-104">You can use this effect to output a portion of an image but retain the region outside of the portion for use in subsequent operations.</span></span>

<span data-ttu-id="14c13-105">這項效果的 CLSID 是 CLSID \_ D2D1Atlas。</span><span class="sxs-lookup"><span data-stu-id="14c13-105">The CLSID for this effect is CLSID\_D2D1Atlas.</span></span>

<span data-ttu-id="14c13-106">如果您想要載入由許多較小的影像組成的大型影像，例如 sprite 的各種框架，則塔效果相當有用。</span><span class="sxs-lookup"><span data-stu-id="14c13-106">The atlas effect is useful if you want to load a large image made up of many smaller images, such as various frames of a sprite.</span></span>

<span data-ttu-id="14c13-107">若要建立輸出效果：</span><span class="sxs-lookup"><span data-stu-id="14c13-107">To create the output the effect:</span></span>

1.  <span data-ttu-id="14c13-108">將輸入裁剪至指定的 *InputRect* 屬性。</span><span class="sxs-lookup"><span data-stu-id="14c13-108">Crops the input to the given *InputRect* property.</span></span>
2.  <span data-ttu-id="14c13-109">將結果的原點轉譯為 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="14c13-109">Translates the origin of the result to (0,0).</span></span>

> [!Note]  
> <span data-ttu-id="14c13-110">只有當兩個矩形之間的圖元在輸入上為透明黑色時， *InputPaddingRect* 屬性才應該較大。</span><span class="sxs-lookup"><span data-stu-id="14c13-110">The *InputPaddingRect* property should only be larger if and only if the pixels between the two rectangles are transparent black on the input.</span></span> <span data-ttu-id="14c13-111">這可能會導致 Direct2D 更能以最佳方式執行圖形。</span><span class="sxs-lookup"><span data-stu-id="14c13-111">This may result in Direct2D executing the graph more optimally.</span></span>

 

<span data-ttu-id="14c13-112">以下是效果的範例。</span><span class="sxs-lookup"><span data-stu-id="14c13-112">Here is an example of the effect.</span></span> <span data-ttu-id="14c13-113">此映射很小，而且很簡單，可供說明之用。</span><span class="sxs-lookup"><span data-stu-id="14c13-113">This image is small and simple for illustration purposes.</span></span>

![輸入影像。](images/atlas.png)

<span data-ttu-id="14c13-115">上述影像是效果的輸入。</span><span class="sxs-lookup"><span data-stu-id="14c13-115">The preceding image is the input to the effect.</span></span> <span data-ttu-id="14c13-116">此處的程式碼會建立一個塔效果、設定輸入、設定輸入矩形，然後繪製輸出。</span><span class="sxs-lookup"><span data-stu-id="14c13-116">The code here creates an atlas effect, sets the input, sets the input rectangle, and then draws the output.</span></span>


```C++
ComPtr<ID2D1Effect> atlasEffect;

// Create the Atlas Effect.
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Atlas, &atlasEffect));

// Set the input.
atlasEffect->SetInputEffect(0, inputImage.Get());

// The images here are 150 x 150 pixels.
float size = 150.0f;

// Compensate for the padding between images.
float padding = 10.0f;

// The input rectangle.  150 x 150 pixels with 10 pixel padding
D2D1_Vector_4F inputRect = D2D1::Vector4F(size + (padding * 2), padding, size, size);

DX::ThrowIfFailed(atlasEffect->SetValue(D2D1_ATLAS_PROP_INPUT_RECT, inputRect));

// Draw the image
m_d2dContext->DrawImage(atlasEffect.Get());
```



<span data-ttu-id="14c13-117">上述程式碼會選取位於第二個三角形周圍的矩形。</span><span class="sxs-lookup"><span data-stu-id="14c13-117">The preceding code selects a rectangle that is around the second triangle.</span></span> <span data-ttu-id="14c13-118">它周圍的填補會被忽略。</span><span class="sxs-lookup"><span data-stu-id="14c13-118">The padding around it is ignored.</span></span> <span data-ttu-id="14c13-119">以下是產生的影像。</span><span class="sxs-lookup"><span data-stu-id="14c13-119">Here is the resulting image.</span></span>

![輸出影像。](images/atlas2.png)

> [!Note]  
> <span data-ttu-id="14c13-121">這種情況下，您可以選擇指定 *InputPaddingRect* ，因為填補是透明的黑色。</span><span class="sxs-lookup"><span data-stu-id="14c13-121">This is a situation where you may choose to specify a *InputPaddingRect* because the padding is transparent black.</span></span> <span data-ttu-id="14c13-122">矩形會是 `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);` 。</span><span class="sxs-lookup"><span data-stu-id="14c13-122">The rectangle would be `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);`.</span></span>

 

## <a name="effect-properties"></a><span data-ttu-id="14c13-123">效果屬性</span><span class="sxs-lookup"><span data-stu-id="14c13-123">Effect properties</span></span>



| <span data-ttu-id="14c13-124">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="14c13-124">Display name and index enumeration</span></span>                                             | <span data-ttu-id="14c13-125">Description</span><span class="sxs-lookup"><span data-stu-id="14c13-125">Description</span></span>                                                                                                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14c13-126">InputRect</span><span class="sxs-lookup"><span data-stu-id="14c13-126">InputRect</span></span><br/> <span data-ttu-id="14c13-127">D2D1 \_ 塔 \_ 的 \_ 輸入 \_ 矩形</span><span class="sxs-lookup"><span data-stu-id="14c13-127">D2D1\_ATLAS\_PROP\_INPUT\_RECT</span></span><br/>                 | <span data-ttu-id="14c13-128">傳遞給下一個效果的影像部分。</span><span class="sxs-lookup"><span data-stu-id="14c13-128">The portion of the image passed to the next effect.</span></span><br/> <span data-ttu-id="14c13-129">類型為 D2D1 \_ VECTOR \_ 4F。</span><span class="sxs-lookup"><span data-stu-id="14c13-129">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="14c13-130">預設值為 (-FLT \_ max、-FLT \_ MAX、FLT \_ max、FLT \_ max) 。</span><span class="sxs-lookup"><span data-stu-id="14c13-130">Default value is (-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX).</span></span> <br/> |
| <span data-ttu-id="14c13-131">InputPaddingRect</span><span class="sxs-lookup"><span data-stu-id="14c13-131">InputPaddingRect</span></span><br/> <span data-ttu-id="14c13-132">D2D1 \_ 塔 \_ 的 \_ 輸入 \_ 填補 \_ 矩形</span><span class="sxs-lookup"><span data-stu-id="14c13-132">D2D1\_ATLAS\_PROP\_INPUT\_PADDING\_RECT</span></span><br/> | <span data-ttu-id="14c13-133">針對輸出矩形取樣的大小上限。</span><span class="sxs-lookup"><span data-stu-id="14c13-133">The maximum size sampled for the output rectangle.</span></span><br/> <span data-ttu-id="14c13-134">類型為 D2D1 \_ VECTOR \_ 4F。</span><span class="sxs-lookup"><span data-stu-id="14c13-134">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="14c13-135">預設值為 (-FLT \_ max、-FLT \_ MAX、FLT \_ max、FLT \_ max) 。</span><span class="sxs-lookup"><span data-stu-id="14c13-135">Default value is (-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX).</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="14c13-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="14c13-136">Requirements</span></span>



| <span data-ttu-id="14c13-137">需求</span><span class="sxs-lookup"><span data-stu-id="14c13-137">Requirement</span></span> | <span data-ttu-id="14c13-138">值</span><span class="sxs-lookup"><span data-stu-id="14c13-138">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="14c13-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14c13-139">Minimum supported client</span></span> | <span data-ttu-id="14c13-140">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14c13-140">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="14c13-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14c13-141">Minimum supported server</span></span> | <span data-ttu-id="14c13-142">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14c13-142">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="14c13-143">標頭</span><span class="sxs-lookup"><span data-stu-id="14c13-143">Header</span></span>                   | <span data-ttu-id="14c13-144">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="14c13-144">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="14c13-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="14c13-145">Library</span></span>                  | <span data-ttu-id="14c13-146">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="14c13-146">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="14c13-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="14c13-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14c13-148">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="14c13-148">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


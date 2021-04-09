---
title: DPI 補償效果
description: 使用 DPI 補償效果，自動調整輸入點陣圖以符合內容的 DPI。 這適用于建立或載入點陣圖與螢幕不同 DPI 的情況。
ms.assetid: EA8AD89B-A710-468F-A6F3-474DA29586F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a0477d2a57f39738fa9b1ce16c97995c60cf96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844423"
---
# <a name="dpi-compensation-effect"></a><span data-ttu-id="540e1-104">DPI 補償效果</span><span class="sxs-lookup"><span data-stu-id="540e1-104">DPI compensation effect</span></span>

<span data-ttu-id="540e1-105">使用 DPI 補償效果，自動調整輸入點陣圖以符合內容的 DPI。</span><span class="sxs-lookup"><span data-stu-id="540e1-105">Use the DPI compensation effect to automatically adjust an input bitmap to match the DPI of the context.</span></span> <span data-ttu-id="540e1-106">這適用于建立或載入點陣圖與螢幕不同 DPI 的情況。</span><span class="sxs-lookup"><span data-stu-id="540e1-106">This is useful for situations where a bitmap is created or loaded at a different DPI than the screen.</span></span>

<span data-ttu-id="540e1-107">這項效果的 CLSID 是 CLSID \_ D2D1DpiCompensation。</span><span class="sxs-lookup"><span data-stu-id="540e1-107">The CLSID for this effect is CLSID\_D2D1DpiCompensation.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="540e1-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="540e1-108">Effect properties</span></span>



| <span data-ttu-id="540e1-109">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="540e1-109">Display name and index enumeration</span></span>                                                       | <span data-ttu-id="540e1-110">Description</span><span class="sxs-lookup"><span data-stu-id="540e1-110">Description</span></span>                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="540e1-111">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="540e1-111">InterpolationMode</span></span><br/> <span data-ttu-id="540e1-112">D2D1 \_ DPICOMPENSATION \_ 的 \_ 內插補點 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="540e1-112">D2D1\_DPICOMPENSATION\_PROP\_INTERPOLATION\_MODE</span></span><br/> | <span data-ttu-id="540e1-113">效果用來調整影像的插補模式。</span><span class="sxs-lookup"><span data-stu-id="540e1-113">The interpolation mode the effect uses to scale the image.</span></span><br/> <span data-ttu-id="540e1-114">此類型為 D2D1 \_ DPICOMPENSATION \_ 插補 \_ 模式。</span><span class="sxs-lookup"><span data-stu-id="540e1-114">The type is D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE.</span></span><br/> <span data-ttu-id="540e1-115">預設值為 D2D1 \_ DPICOMPENSATION \_ 插補 \_ 模式 \_ 線性。</span><span class="sxs-lookup"><span data-stu-id="540e1-115">The default value is D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_LINEAR .</span></span><br/>                  |
| <span data-ttu-id="540e1-116">BorderMode</span><span class="sxs-lookup"><span data-stu-id="540e1-116">BorderMode</span></span><br/> <span data-ttu-id="540e1-117">D2D1 \_ DPICOMPENSATION \_ 的 \_ 樣式框線 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="540e1-117">D2D1\_DPICOMPENSATION\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="540e1-118">用來計算影像（軟或硬）框線的模式。</span><span class="sxs-lookup"><span data-stu-id="540e1-118">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="540e1-119">如需詳細資訊，請參閱 [框線模式](https://www.bing.com/search?q=Border+modes) 。</span><span class="sxs-lookup"><span data-stu-id="540e1-119">See [Border modes](https://www.bing.com/search?q=Border+modes) for more info.</span></span> <br/> <span data-ttu-id="540e1-120">此類型為 D2D1 \_ 框線 \_ 模式。</span><span class="sxs-lookup"><span data-stu-id="540e1-120">The type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="540e1-121">預設值為 [D2D1 \_ 框線 \_ 模式] \_ 。</span><span class="sxs-lookup"><span data-stu-id="540e1-121">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/> |
| <span data-ttu-id="540e1-122">InputDpi</span><span class="sxs-lookup"><span data-stu-id="540e1-122">InputDpi</span></span><br/> <span data-ttu-id="540e1-123">D2D1 \_ DPICOMPENSATION \_ 的 \_ 輸入 \_ DPI</span><span class="sxs-lookup"><span data-stu-id="540e1-123">D2D1\_DPICOMPENSATION\_PROP\_INPUT\_DPI</span></span><br/>                   | <span data-ttu-id="540e1-124">輸入影像的 DPI。</span><span class="sxs-lookup"><span data-stu-id="540e1-124">The DPI of the input image.</span></span><br/> <span data-ttu-id="540e1-125">此類型為 FLOAT。</span><span class="sxs-lookup"><span data-stu-id="540e1-125">The type is FLOAT.</span></span><br/> <span data-ttu-id="540e1-126">預設值為 96.0 f。</span><span class="sxs-lookup"><span data-stu-id="540e1-126">The default value is 96.0f.</span></span><br/>                                                                                                                                    |



 

## <a name="interpolation-modes"></a><span data-ttu-id="540e1-127">插補模式</span><span class="sxs-lookup"><span data-stu-id="540e1-127">Interpolation modes</span></span>



| <span data-ttu-id="540e1-128">列舉型別</span><span class="sxs-lookup"><span data-stu-id="540e1-128">Enumeration</span></span>                                                       | <span data-ttu-id="540e1-129">描述</span><span class="sxs-lookup"><span data-stu-id="540e1-129">Description</span></span>                                                                                                                                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="540e1-130">\_ \_ \_ \_ 最接近 \_ 鄰近的 D2D1 DPICOMPENSATION 插補模式</span><span class="sxs-lookup"><span data-stu-id="540e1-130">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="540e1-131">範例最接近的單一點，並使用該點。</span><span class="sxs-lookup"><span data-stu-id="540e1-131">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="540e1-132">這個模式會使用較少的處理時間，但會輸出最低品質的影像。</span><span class="sxs-lookup"><span data-stu-id="540e1-132">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="540e1-133">D2D1 \_ DPICOMPENSATION \_ 插補 \_ 模式 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="540e1-133">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="540e1-134">使用四個點取樣和線性插補。</span><span class="sxs-lookup"><span data-stu-id="540e1-134">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="540e1-135">這個模式所使用的處理時間比最近的鄰近模式更多，但會輸出較高品質的影像。</span><span class="sxs-lookup"><span data-stu-id="540e1-135">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="540e1-136">D2D1 \_ DPICOMPENSATION \_ 插補 \_ 模式 \_ 立方</span><span class="sxs-lookup"><span data-stu-id="540e1-136">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="540e1-137">使用16個範例三核心來進行插補。</span><span class="sxs-lookup"><span data-stu-id="540e1-137">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="540e1-138">這個模式會使用大部分的處理時間，但會輸出較高品質的影像。</span><span class="sxs-lookup"><span data-stu-id="540e1-138">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="540e1-139">D2D1 \_ DPICOMPENSATION \_ 插補 \_ 模式 \_ 多 \_ 樣本 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="540e1-139">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="540e1-140">使用單一圖元內的4個線性樣本來取得良好的邊緣消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="540e1-140">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="540e1-141">這種模式適合用來在具有少量圖元的影像上相應減少量。</span><span class="sxs-lookup"><span data-stu-id="540e1-141">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="540e1-142">D2D1 \_ DPICOMPENSATION \_ 插補 \_ 模式 \_ 各向異性</span><span class="sxs-lookup"><span data-stu-id="540e1-142">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="540e1-143">根據點陣圖的轉換圖形，使用非等向篩選來取樣模式。</span><span class="sxs-lookup"><span data-stu-id="540e1-143">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="540e1-144">D2D1 \_ DPICOMPENSATION \_ 插補 \_ 模式 \_ 高 \_ 品質 \_ 三次</span><span class="sxs-lookup"><span data-stu-id="540e1-144">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="540e1-145">如果 downscaling 與轉換矩陣有關，則使用可變大小的高品質三核心來執行預先縮小的影像。</span><span class="sxs-lookup"><span data-stu-id="540e1-145">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="540e1-146">然後使用三次插補模式來進行最終輸出。</span><span class="sxs-lookup"><span data-stu-id="540e1-146">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="540e1-147">如果您未選取模式，效果會預設為 D2D1 \_ DPICOMPENSTION \_ 插補 \_ 模式 \_ 線性。</span><span class="sxs-lookup"><span data-stu-id="540e1-147">If you don't select a mode, the effect defaults to D2D1\_DPICOMPENSTION\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

## <a name="border-modes"></a><span data-ttu-id="540e1-148">框線模式</span><span class="sxs-lookup"><span data-stu-id="540e1-148">Border modes</span></span>



| <span data-ttu-id="540e1-149">Name</span><span class="sxs-lookup"><span data-stu-id="540e1-149">Name</span></span>                     | <span data-ttu-id="540e1-150">描述</span><span class="sxs-lookup"><span data-stu-id="540e1-150">Description</span></span>                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="540e1-151">D2D1 \_ 框線 \_ 模式 \_ 軟</span><span class="sxs-lookup"><span data-stu-id="540e1-151">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="540e1-152">輸入界限之外的圖元是由 [鏡像框線效果](border.md)所產生。</span><span class="sxs-lookup"><span data-stu-id="540e1-152">Pixels outside of the input boundaries are generated by the [mirror border effect](border.md).</span></span> <br/> |
| <span data-ttu-id="540e1-153">D2D1 \_ 框線 \_ 模式 \_ 硬性</span><span class="sxs-lookup"><span data-stu-id="540e1-153">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="540e1-154">輸入界限之外的圖元是透明的黑色。</span><span class="sxs-lookup"><span data-stu-id="540e1-154">Pixels outside of the input boundaries are transparent black.</span></span><br/>                                    |



 

## <a name="requirements"></a><span data-ttu-id="540e1-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="540e1-155">Requirements</span></span>



| <span data-ttu-id="540e1-156">需求</span><span class="sxs-lookup"><span data-stu-id="540e1-156">Requirement</span></span> | <span data-ttu-id="540e1-157">值</span><span class="sxs-lookup"><span data-stu-id="540e1-157">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="540e1-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="540e1-158">Minimum supported client</span></span> | <span data-ttu-id="540e1-159">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="540e1-159">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="540e1-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="540e1-160">Minimum supported server</span></span> | <span data-ttu-id="540e1-161">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="540e1-161">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="540e1-162">標頭</span><span class="sxs-lookup"><span data-stu-id="540e1-162">Header</span></span>                   | <span data-ttu-id="540e1-163">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="540e1-163">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="540e1-164">程式庫</span><span class="sxs-lookup"><span data-stu-id="540e1-164">Library</span></span>                  | <span data-ttu-id="540e1-165">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="540e1-165">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="540e1-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="540e1-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="540e1-167">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="540e1-167">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


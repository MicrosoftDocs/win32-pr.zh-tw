---
title: 'glPushAttrib 函式 (Gl) '
description: 推送屬性堆疊。
ms.assetid: 3c7b93cc-2112-4771-b422-a244821447e5
keywords:
- glPushAttrib 函式 OpenGL
topic_type:
- apiref
api_name:
- glPushAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bc15b85ddca3bdbe5f6774b5368c6f0cde8dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024779"
---
# <a name="glpushattrib-function"></a><span data-ttu-id="7b920-104">glPushAttrib 函式</span><span class="sxs-lookup"><span data-stu-id="7b920-104">glPushAttrib function</span></span>

<span data-ttu-id="7b920-105">推送屬性堆疊。</span><span class="sxs-lookup"><span data-stu-id="7b920-105">Pushes the attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b920-106">語法</span><span class="sxs-lookup"><span data-stu-id="7b920-106">Syntax</span></span>


```C++
void WINAPI glPushAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="7b920-107">參數</span><span class="sxs-lookup"><span data-stu-id="7b920-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b920-108">*面具*</span><span class="sxs-lookup"><span data-stu-id="7b920-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="7b920-109">表示要儲存哪些屬性的遮罩。</span><span class="sxs-lookup"><span data-stu-id="7b920-109">A mask that indicates which attributes to save.</span></span> <span data-ttu-id="7b920-110">符號遮罩常數和其相關聯的 OpenGL 狀態如下 (縮排的段落會列出哪些屬性會儲存) ：</span><span class="sxs-lookup"><span data-stu-id="7b920-110">The symbolic mask constants and their associated OpenGL state are as follows (the indented paragraphs list which attributes are saved):</span></span>

<dl> <dt>

<span data-ttu-id="7b920-111"><span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>GL \_ ACCUM \_ 緩衝區 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-111"><span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>GL\_ACCUM\_BUFFER\_BIT</span></span> 
</dt> <dd>

<span data-ttu-id="7b920-112">累積緩衝區清除值</span><span class="sxs-lookup"><span data-stu-id="7b920-112">Accumulation buffer clear value</span></span>

</dd> <dt>

<span data-ttu-id="7b920-113"><span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>GL \_ 色彩 \_ 緩衝區 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-113"><span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>GL\_COLOR\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-114">GL \_ ALPHA \_ 測試啟用位</span><span class="sxs-lookup"><span data-stu-id="7b920-114">GL\_ALPHA\_TEST enable bit</span></span>

<span data-ttu-id="7b920-115">Alpha 測試函數和參考值</span><span class="sxs-lookup"><span data-stu-id="7b920-115">Alpha test function and reference value</span></span>

<span data-ttu-id="7b920-116">GL \_ BLEND 啟用位</span><span class="sxs-lookup"><span data-stu-id="7b920-116">GL\_BLEND enable bit</span></span>

<span data-ttu-id="7b920-117">混合來源和目的地函數</span><span class="sxs-lookup"><span data-stu-id="7b920-117">Blending source and destination functions</span></span>

<span data-ttu-id="7b920-118">GL \_ 遞色啟用位</span><span class="sxs-lookup"><span data-stu-id="7b920-118">GL\_DITHER enable bit</span></span>

<span data-ttu-id="7b920-119">GL \_ 描繪 \_ 緩衝區設定</span><span class="sxs-lookup"><span data-stu-id="7b920-119">GL\_DRAW\_BUFFER setting</span></span>

<span data-ttu-id="7b920-120">GL \_ 邏輯 \_ OP 啟用位</span><span class="sxs-lookup"><span data-stu-id="7b920-120">GL\_LOGIC\_OP enable bit</span></span>

<span data-ttu-id="7b920-121">邏輯 op 函數</span><span class="sxs-lookup"><span data-stu-id="7b920-121">Logic op function</span></span>

<span data-ttu-id="7b920-122">色彩模式和索引模式清除值</span><span class="sxs-lookup"><span data-stu-id="7b920-122">Color-mode and index-mode clear values</span></span>

<span data-ttu-id="7b920-123">色彩模式和索引模式 writemasks</span><span class="sxs-lookup"><span data-stu-id="7b920-123">Color-mode and index-mode writemasks</span></span>

</dd> <dt>

<span data-ttu-id="7b920-124"><span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>GL \_ 目前 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-124"><span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>GL\_CURRENT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-125">目前的 RGBA 色彩</span><span class="sxs-lookup"><span data-stu-id="7b920-125">Current RGBA color</span></span>

<span data-ttu-id="7b920-126">目前的色彩索引</span><span class="sxs-lookup"><span data-stu-id="7b920-126">Current color index</span></span>

<span data-ttu-id="7b920-127">目前的一般向量</span><span class="sxs-lookup"><span data-stu-id="7b920-127">Current normal vector</span></span>

<span data-ttu-id="7b920-128">目前的材質座標</span><span class="sxs-lookup"><span data-stu-id="7b920-128">Current texture coordinates</span></span>

<span data-ttu-id="7b920-129">目前的點陣位置 GL \_ 目前的 \_ 點陣 \_ 位置 \_ 有效旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-129">Current raster position GL\_CURRENT\_RASTER\_POSITION\_VALID flag</span></span>

<span data-ttu-id="7b920-130">與目前點陣位置相關聯的 RGBA 色彩</span><span class="sxs-lookup"><span data-stu-id="7b920-130">RGBA color associated with current raster position</span></span>

<span data-ttu-id="7b920-131">與目前點陣位置相關聯的色彩索引</span><span class="sxs-lookup"><span data-stu-id="7b920-131">Color index associated with current raster position</span></span>

<span data-ttu-id="7b920-132">與目前點陣位置相關聯的材質座標</span><span class="sxs-lookup"><span data-stu-id="7b920-132">Texture coordinates associated with current raster position</span></span>

<span data-ttu-id="7b920-133">GL \_ EDGE \_ 旗標旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-133">GL\_EDGE\_FLAG flag</span></span>

</dd> <dt>

<span data-ttu-id="7b920-134"><span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>GL \_ 深度 \_ 緩衝區 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-134"><span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>GL\_DEPTH\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-135">GL \_ 深度 \_ 測試啟用位</span><span class="sxs-lookup"><span data-stu-id="7b920-135">GL\_DEPTH\_TEST enable bit</span></span>

<span data-ttu-id="7b920-136">深度緩衝區測試函式</span><span class="sxs-lookup"><span data-stu-id="7b920-136">Depth buffer test function</span></span>

<span data-ttu-id="7b920-137">深度緩衝區清除值</span><span class="sxs-lookup"><span data-stu-id="7b920-137">Depth buffer clear value</span></span>

<span data-ttu-id="7b920-138">GL \_ 深度 \_ WRITEMASK 啟用位</span><span class="sxs-lookup"><span data-stu-id="7b920-138">GL\_DEPTH\_WRITEMASK enable bit</span></span>

</dd> <dt>

<span data-ttu-id="7b920-139"><span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>GL \_ 啟用 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-139"><span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>GL\_ENABLE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-140">GL \_ ALPHA \_ 測試旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-140">GL\_ALPHA\_TEST flag</span></span>

<span data-ttu-id="7b920-141">GL \_ 自動 \_ 正常旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-141">GL\_AUTO\_NORMAL flag</span></span>

<span data-ttu-id="7b920-142">GL \_ BLEND 旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-142">GL\_BLEND flag</span></span>

<span data-ttu-id="7b920-143">啟用使用者可定義裁剪平面的位</span><span class="sxs-lookup"><span data-stu-id="7b920-143">Enable bits for the user-definable clipping planes</span></span>

<span data-ttu-id="7b920-144">GL \_ 色彩 \_ 材質</span><span class="sxs-lookup"><span data-stu-id="7b920-144">GL\_COLOR\_MATERIAL</span></span>

<span data-ttu-id="7b920-145">GL \_ 挑選 \_ 臉部旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-145">GL\_CULL\_FACE flag</span></span>

<span data-ttu-id="7b920-146">GL \_ 深度 \_ 測試旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-146">GL\_DEPTH\_TEST flag</span></span>

<span data-ttu-id="7b920-147">GL \_ 遞色旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-147">GL\_DITHER flag</span></span>

<span data-ttu-id="7b920-148">GL \_ 霧化旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-148">GL\_FOG flag</span></span>

<span data-ttu-id="7b920-149">GL \_ 燈 0 <= *i* < GL \_ 最大 \_ 燈</span><span class="sxs-lookup"><span data-stu-id="7b920-149">GL\_LIGHT *i* where 0 <= *i* < GL\_MAX\_LIGHTS</span></span>

<span data-ttu-id="7b920-150">GL \_ 照明旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-150">GL\_LIGHTING flag</span></span>

<span data-ttu-id="7b920-151">GL \_ 行 \_ 平滑旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-151">GL\_LINE\_SMOOTH flag</span></span>

<span data-ttu-id="7b920-152">GL \_ 線 \_ STIPPLE 旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-152">GL\_LINE\_STIPPLE flag</span></span>

<span data-ttu-id="7b920-153">GL \_ 色彩 \_ 邏輯 \_ OP 旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-153">GL\_COLOR\_LOGIC\_OP flag</span></span>

<span data-ttu-id="7b920-154">GL \_ 索引 \_ 邏輯 \_ OP 旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-154">GL\_INDEX\_LOGIC\_OP flag</span></span>

<span data-ttu-id="7b920-155">GL \_ MAP1 \_ x，其中 x 是地圖類型</span><span class="sxs-lookup"><span data-stu-id="7b920-155">GL\_MAP1\_x where x is a map type</span></span>

<span data-ttu-id="7b920-156">GL \_ list.map2 \_ x，其中 x 是地圖類型</span><span class="sxs-lookup"><span data-stu-id="7b920-156">GL\_MAP2\_x where x is a map type</span></span>

<span data-ttu-id="7b920-157">GL \_ 標準化旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-157">GL\_NORMALIZE flag</span></span>

<span data-ttu-id="7b920-158">GL \_ 點 \_ 平滑旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-158">GL\_POINT\_SMOOTH flag</span></span>

<span data-ttu-id="7b920-159">GL \_ 多邊形 \_ 位移 \_ 線旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-159">GL\_POLYGON\_OFFSET\_LINE flag</span></span>

<span data-ttu-id="7b920-160">GL \_ 多邊形 \_ 位移 \_ 填滿旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-160">GL\_POLYGON\_OFFSET\_FILL flag</span></span>

<span data-ttu-id="7b920-161">GL \_ 多邊形 \_ 位移 \_ 點旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-161">GL\_POLYGON\_OFFSET\_POINT flag</span></span>

<span data-ttu-id="7b920-162">GL \_ 多邊形 \_ 平滑旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-162">GL\_POLYGON\_SMOOTH flag</span></span>

<span data-ttu-id="7b920-163">GL \_ 多邊形 \_ STIPPLE 旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-163">GL\_POLYGON\_STIPPLE flag</span></span>

<span data-ttu-id="7b920-164">GL \_ 剪式 \_ 測試旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-164">GL\_SCISSOR\_TEST flag</span></span>

<span data-ttu-id="7b920-165">GL \_ 樣板 \_ 測試旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-165">GL\_STENCIL\_TEST flag</span></span>

<span data-ttu-id="7b920-166">GL \_ 材質 \_ 1d 旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-166">GL\_TEXTURE\_1D flag</span></span>

<span data-ttu-id="7b920-167">GL \_ 材質 \_ 2d 旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-167">GL\_TEXTURE\_2D flag</span></span>

<span data-ttu-id="7b920-168">旗標 GL \_ 材質 \_ GEN x， \_ 其中 x 是 S、T、R 或 Q</span><span class="sxs-lookup"><span data-stu-id="7b920-168">Flags GL\_TEXTURE\_GEN\_x where x is S, T, R, or Q</span></span>

</dd> <dt>

<span data-ttu-id="7b920-169"><span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>GL \_ EVAL \_ BIT</span><span class="sxs-lookup"><span data-stu-id="7b920-169"><span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>GL\_EVAL\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-170">GL \_ MAP1 \_ x 啟用 bits，其中 x 是地圖類型</span><span class="sxs-lookup"><span data-stu-id="7b920-170">GL\_MAP1\_x enable bits, where x is a map type</span></span>

<span data-ttu-id="7b920-171">GL \_ list.map2 \_ x 啟用 bits，其中 x 是地圖類型</span><span class="sxs-lookup"><span data-stu-id="7b920-171">GL\_MAP2\_x enable bits, where x is a map type</span></span>

<span data-ttu-id="7b920-172">立體格線端點和部門</span><span class="sxs-lookup"><span data-stu-id="7b920-172">1-D grid endpoints and divisions</span></span>

<span data-ttu-id="7b920-173">2d 格線端點和部門</span><span class="sxs-lookup"><span data-stu-id="7b920-173">2-D grid endpoints and divisions</span></span>

<span data-ttu-id="7b920-174">GL \_ AUTO \_ 正常啟用位</span><span class="sxs-lookup"><span data-stu-id="7b920-174">GL\_AUTO\_NORMAL enable bit</span></span>

</dd> <dt>

<span data-ttu-id="7b920-175"><span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>GL \_ 霧化 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-175"><span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>GL\_FOG\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-176">GL \_ 霧化啟用旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-176">GL\_FOG enable flag</span></span>

<span data-ttu-id="7b920-177">霧化色彩</span><span class="sxs-lookup"><span data-stu-id="7b920-177">Fog color</span></span>

<span data-ttu-id="7b920-178">霧化密度</span><span class="sxs-lookup"><span data-stu-id="7b920-178">Fog density</span></span>

<span data-ttu-id="7b920-179">線性霧化開始</span><span class="sxs-lookup"><span data-stu-id="7b920-179">Linear fog start</span></span>

<span data-ttu-id="7b920-180">線性霧化結束</span><span class="sxs-lookup"><span data-stu-id="7b920-180">Linear fog end</span></span>

<span data-ttu-id="7b920-181">霧化索引</span><span class="sxs-lookup"><span data-stu-id="7b920-181">Fog index</span></span>

<span data-ttu-id="7b920-182">GL \_ 霧化 \_ 模式值</span><span class="sxs-lookup"><span data-stu-id="7b920-182">GL\_FOG\_MODE value</span></span>

</dd> <dt>

<span data-ttu-id="7b920-183"><span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>GL \_ 提示 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-183"><span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>GL\_HINT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-184">GL \_ 透視圖 \_ 校正 \_ 提示設定</span><span class="sxs-lookup"><span data-stu-id="7b920-184">GL\_PERSPECTIVE\_CORRECTION\_HINT setting</span></span>

<span data-ttu-id="7b920-185">GL \_ 點 \_ 平滑 \_ 提示設定</span><span class="sxs-lookup"><span data-stu-id="7b920-185">GL\_POINT\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="7b920-186">GL \_ LINE \_ 平滑 \_ 提示設定</span><span class="sxs-lookup"><span data-stu-id="7b920-186">GL\_LINE\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="7b920-187">GL \_ 多邊形 \_ 平滑 \_ 提示設定</span><span class="sxs-lookup"><span data-stu-id="7b920-187">GL\_POLYGON\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="7b920-188">GL \_ 霧化 \_ 提示設定</span><span class="sxs-lookup"><span data-stu-id="7b920-188">GL\_FOG\_HINT setting</span></span>

</dd> <dt>

<span data-ttu-id="7b920-189"><span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>GL \_ 照明 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-189"><span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>GL\_LIGHTING\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-190">GL \_ 色彩 \_ 材質啟用位</span><span class="sxs-lookup"><span data-stu-id="7b920-190">GL\_COLOR\_MATERIAL enable bit</span></span>

<span data-ttu-id="7b920-191">GL \_ 色 \_ 材質 \_ 臉部值</span><span class="sxs-lookup"><span data-stu-id="7b920-191">GL\_COLOR\_MATERIAL\_FACE value</span></span>

<span data-ttu-id="7b920-192">追蹤目前色彩的色彩材質參數</span><span class="sxs-lookup"><span data-stu-id="7b920-192">Color material parameters that are tracking the current color</span></span>

<span data-ttu-id="7b920-193">環境場景色彩</span><span class="sxs-lookup"><span data-stu-id="7b920-193">Ambient scene color</span></span>

<span data-ttu-id="7b920-194">GL \_ LIGHT \_ 模型 \_ 本機 \_ 檢視器值</span><span class="sxs-lookup"><span data-stu-id="7b920-194">GL\_LIGHT\_MODEL\_LOCAL\_VIEWER value</span></span>

<span data-ttu-id="7b920-195">GL \_ LIGHT \_ 模型 \_ 雙 \_ 側設定</span><span class="sxs-lookup"><span data-stu-id="7b920-195">GL\_LIGHT\_MODEL\_TWO\_SIDE setting</span></span>

<span data-ttu-id="7b920-196">GL \_ 照明啟用位</span><span class="sxs-lookup"><span data-stu-id="7b920-196">GL\_LIGHTING enable bit</span></span>

<span data-ttu-id="7b920-197">為每個光線啟用位</span><span class="sxs-lookup"><span data-stu-id="7b920-197">Enable bit for each light</span></span>

<span data-ttu-id="7b920-198">每個光線的環境、擴散和反射濃度</span><span class="sxs-lookup"><span data-stu-id="7b920-198">Ambient, diffuse, and specular intensity for each light</span></span>

<span data-ttu-id="7b920-199">每個光線的方向、位置、指數和截止角度</span><span class="sxs-lookup"><span data-stu-id="7b920-199">Direction, position, exponent, and cutoff angle for each light</span></span>

<span data-ttu-id="7b920-200">每個光線的常數、線性和二次衰減因素</span><span class="sxs-lookup"><span data-stu-id="7b920-200">Constant, linear, and quadratic attenuation factors for each light</span></span>

<span data-ttu-id="7b920-201">每個材質的環境、擴散、反射和放射色彩</span><span class="sxs-lookup"><span data-stu-id="7b920-201">Ambient, diffuse, specular, and emissive color for each material</span></span>

<span data-ttu-id="7b920-202">每個材質的環境、擴散和反射色彩索引</span><span class="sxs-lookup"><span data-stu-id="7b920-202">Ambient, diffuse, and specular color indexes for each material</span></span>

<span data-ttu-id="7b920-203">每個材質 GL \_ 陰影 \_ 模型設定的反射指數</span><span class="sxs-lookup"><span data-stu-id="7b920-203">Specular exponent for each material GL\_SHADE\_MODEL setting</span></span>

</dd> <dt>

<span data-ttu-id="7b920-204"><span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>GL \_ 行 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-204"><span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>GL\_LINE\_BIT</span></span> 
</dt> <dd>

<span data-ttu-id="7b920-205">GL \_ 行 \_ 平滑旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-205">GL\_LINE\_SMOOTH flag</span></span>

<span data-ttu-id="7b920-206">GL \_ LINE \_ STIPPLE enable bit</span><span class="sxs-lookup"><span data-stu-id="7b920-206">GL\_LINE\_STIPPLE enable bit</span></span>

<span data-ttu-id="7b920-207">Line stipple pattern 和 repeat 計數器</span><span class="sxs-lookup"><span data-stu-id="7b920-207">Line stipple pattern and repeat counter</span></span>

<span data-ttu-id="7b920-208">線條寬度</span><span class="sxs-lookup"><span data-stu-id="7b920-208">Line width</span></span>

</dd> <dt>

<span data-ttu-id="7b920-209"><span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>GL \_ 清單 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-209"><span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>GL\_LIST\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-210">GL \_ 清單 \_ 基礎設定</span><span class="sxs-lookup"><span data-stu-id="7b920-210">GL\_LIST\_BASE setting</span></span>

</dd> <dt>

<span data-ttu-id="7b920-211"><span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>GL \_ 圖元 \_ 模式 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-211"><span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>GL\_PIXEL\_MODE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-212">GL \_ red \_ 偏差和 gl \_ red \_ SCALE 設定</span><span class="sxs-lookup"><span data-stu-id="7b920-212">GL\_RED\_BIAS and GL\_RED\_SCALE settings</span></span>

<span data-ttu-id="7b920-213">GL \_ 綠 \_ 偏差和 gl \_ 綠色 \_ 刻度值</span><span class="sxs-lookup"><span data-stu-id="7b920-213">GL\_GREEN\_BIAS and GL\_GREEN\_SCALE values</span></span>

<span data-ttu-id="7b920-214">GL \_ 藍色 \_ 偏差和 gl \_ 藍色 \_ 調整</span><span class="sxs-lookup"><span data-stu-id="7b920-214">GL\_BLUE\_BIAS and GL\_BLUE\_SCALE</span></span>

<span data-ttu-id="7b920-215">GL \_ Alpha \_ 偏差和 gl \_ Alpha \_ 刻度</span><span class="sxs-lookup"><span data-stu-id="7b920-215">GL\_ALPHA\_BIAS and GL\_ALPHA\_SCALE</span></span>

<span data-ttu-id="7b920-216">GL \_ 深度 \_ 偏差和 gl \_ 深度 \_ 調整</span><span class="sxs-lookup"><span data-stu-id="7b920-216">GL\_DEPTH\_BIAS and GL\_DEPTH\_SCALE</span></span>

<span data-ttu-id="7b920-217">GL \_ 索引 \_ 位移和 gl \_ 索引 \_ 移位值</span><span class="sxs-lookup"><span data-stu-id="7b920-217">GL\_INDEX\_OFFSET and GL\_INDEX\_SHIFT values</span></span>

<span data-ttu-id="7b920-218">GL \_ 地圖 \_ 色彩和 gl \_ 地圖樣板 \_ 旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-218">GL\_MAP\_COLOR and GL\_MAP\_STENCIL flags</span></span>

<span data-ttu-id="7b920-219">GL \_ zoom \_ X 和 gl \_ zoom 縮放 \_ Y 因素</span><span class="sxs-lookup"><span data-stu-id="7b920-219">GL\_ZOOM\_X and GL\_ZOOM\_Y factors</span></span>

<span data-ttu-id="7b920-220">GL \_ 讀取 \_ 緩衝區設定</span><span class="sxs-lookup"><span data-stu-id="7b920-220">GL\_READ\_BUFFER setting</span></span>

</dd> <dt>

<span data-ttu-id="7b920-221"><span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>GL \_ 點 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-221"><span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>GL\_POINT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-222">GL \_ 點 \_ 平滑旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-222">GL\_POINT\_SMOOTH flag</span></span>

<span data-ttu-id="7b920-223">點大小</span><span class="sxs-lookup"><span data-stu-id="7b920-223">Point size</span></span>

</dd> <dt>

<span data-ttu-id="7b920-224"><span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>GL \_ 多邊形 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-224"><span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>GL\_POLYGON\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-225">GL \_ 精選 \_ 臉部啟用位</span><span class="sxs-lookup"><span data-stu-id="7b920-225">GL\_CULL\_FACE enable bit</span></span>

<span data-ttu-id="7b920-226">GL \_ 挑選 \_ 臉部 \_ 模式值</span><span class="sxs-lookup"><span data-stu-id="7b920-226">GL\_CULL\_FACE\_MODE value</span></span>

<span data-ttu-id="7b920-227">GL \_ 正面 \_ 臉部指標</span><span class="sxs-lookup"><span data-stu-id="7b920-227">GL\_FRONT\_FACE indicator</span></span>

<span data-ttu-id="7b920-228">GL \_ 多邊形 \_ 模式設定</span><span class="sxs-lookup"><span data-stu-id="7b920-228">GL\_POLYGON\_MODE setting</span></span>

<span data-ttu-id="7b920-229">GL \_ 多邊形 \_ 平滑旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-229">GL\_POLYGON\_SMOOTH flag</span></span>

<span data-ttu-id="7b920-230">GL \_ 多邊形 \_ STIPPLE 啟用位</span><span class="sxs-lookup"><span data-stu-id="7b920-230">GL\_POLYGON\_STIPPLE enable bit</span></span>

<span data-ttu-id="7b920-231">GL \_ 多邊形 \_ 位移 \_ 填滿旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-231">GL\_POLYGON\_OFFSET\_FILL flag</span></span>

<span data-ttu-id="7b920-232">GL \_ 多邊形 \_ 位移 \_ 線旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-232">GL\_POLYGON\_OFFSET\_LINE flag</span></span>

<span data-ttu-id="7b920-233">GL \_ 多邊形 \_ 位移 \_ 點旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-233">GL\_POLYGON\_OFFSET\_POINT flag</span></span>

<span data-ttu-id="7b920-234">GL \_ 多邊形 \_ 位移 \_ 因數</span><span class="sxs-lookup"><span data-stu-id="7b920-234">GL\_POLYGON\_OFFSET\_FACTOR</span></span>

<span data-ttu-id="7b920-235">GL \_ 多邊形 \_ 位移 \_ 單位</span><span class="sxs-lookup"><span data-stu-id="7b920-235">GL\_POLYGON\_OFFSET\_UNITS</span></span>

</dd> <dt>

<span data-ttu-id="7b920-236"><span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>GL \_ 多邊形 \_ STIPPLE \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-236"><span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>GL\_POLYGON\_STIPPLE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-237">多邊形 stipple 影像</span><span class="sxs-lookup"><span data-stu-id="7b920-237">Polygon stipple image</span></span>

</dd> <dt>

<span data-ttu-id="7b920-238"><span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>GL \_ 剪式 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-238"><span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>GL\_SCISSOR\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-239">GL \_ 剪式 \_ 測試旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-239">GL\_SCISSOR\_TEST flag</span></span>

<span data-ttu-id="7b920-240">剪式方塊</span><span class="sxs-lookup"><span data-stu-id="7b920-240">Scissor box</span></span>

</dd> <dt>

<span data-ttu-id="7b920-241"><span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>GL \_ 樣板 \_ 緩衝區 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-241"><span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>GL\_STENCIL\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-242">GL \_ 樣板 \_ 測試啟用位</span><span class="sxs-lookup"><span data-stu-id="7b920-242">GL\_STENCIL\_TEST enable bit</span></span>

<span data-ttu-id="7b920-243">樣板函數和參考值</span><span class="sxs-lookup"><span data-stu-id="7b920-243">Stencil function and reference value</span></span>

<span data-ttu-id="7b920-244">樣板值遮罩</span><span class="sxs-lookup"><span data-stu-id="7b920-244">Stencil value mask</span></span>

<span data-ttu-id="7b920-245">樣板失敗、傳遞和深度緩衝區傳遞動作</span><span class="sxs-lookup"><span data-stu-id="7b920-245">Stencil fail, pass, and depth buffer pass actions</span></span>

<span data-ttu-id="7b920-246">樣板緩衝區清除值</span><span class="sxs-lookup"><span data-stu-id="7b920-246">Stencil buffer clear value</span></span>

<span data-ttu-id="7b920-247">樣板緩衝區 writemask</span><span class="sxs-lookup"><span data-stu-id="7b920-247">Stencil buffer writemask</span></span>

</dd> <dt>

<span data-ttu-id="7b920-248"><span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>GL \_ 材質 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-248"><span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>GL\_TEXTURE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-249">啟用四個材質座標的位</span><span class="sxs-lookup"><span data-stu-id="7b920-249">Enable bits for the four texture coordinates</span></span>

<span data-ttu-id="7b920-250">每個材質影像的框線色彩</span><span class="sxs-lookup"><span data-stu-id="7b920-250">Border color for each texture image</span></span>

<span data-ttu-id="7b920-251">每個材質影像的縮制函式</span><span class="sxs-lookup"><span data-stu-id="7b920-251">Minification function for each texture image</span></span>

<span data-ttu-id="7b920-252">每個材質影像的縮放功能</span><span class="sxs-lookup"><span data-stu-id="7b920-252">Magnification function for each texture image</span></span>

<span data-ttu-id="7b920-253">每個材質影像的材質座標和換行模式</span><span class="sxs-lookup"><span data-stu-id="7b920-253">Texture coordinates and wrap mode for each texture image</span></span>

<span data-ttu-id="7b920-254">每個材質環境的色彩和模式</span><span class="sxs-lookup"><span data-stu-id="7b920-254">Color and mode for each texture environment</span></span>

<span data-ttu-id="7b920-255">啟用 bits GL \_ 紋理 \_ GEN \_ *x*;*x* 是 S、T、R 和 Q</span><span class="sxs-lookup"><span data-stu-id="7b920-255">Enable bits GL\_TEXTURE\_GEN\_*x*; *x* is S, T, R, and Q</span></span>

<span data-ttu-id="7b920-256">\_ \_ \_ S、T、R 和 Q 的 GL 材質 GEN 模式設定</span><span class="sxs-lookup"><span data-stu-id="7b920-256">GL\_TEXTURE\_GEN\_MODE setting for S, T, R, and Q</span></span>

<span data-ttu-id="7b920-257">S、T、R 和 Q 的 glTexGen 平面方程式</span><span class="sxs-lookup"><span data-stu-id="7b920-257">glTexGen plane equations for S, T, R, and Q</span></span>

</dd> <dt>

<span data-ttu-id="7b920-258"><span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>GL \_ 轉換 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-258"><span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>GL\_TRANSFORM\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-259">六個裁剪平面的係數</span><span class="sxs-lookup"><span data-stu-id="7b920-259">Coefficients of the six clipping planes</span></span>

<span data-ttu-id="7b920-260">啟用使用者可定義裁剪平面的位</span><span class="sxs-lookup"><span data-stu-id="7b920-260">Enable bits for the user-definable clipping planes</span></span>

<span data-ttu-id="7b920-261">GL \_ 矩陣 \_ 模式值</span><span class="sxs-lookup"><span data-stu-id="7b920-261">GL\_MATRIX\_MODE value</span></span>

<span data-ttu-id="7b920-262">GL \_ 標準化旗標</span><span class="sxs-lookup"><span data-stu-id="7b920-262">GL\_NORMALIZE flag</span></span>

</dd> <dt>

<span data-ttu-id="7b920-263"><span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>GL \_ 區 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7b920-263"><span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>GL\_VIEWPORT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7b920-264">深度範圍 (近和遠) </span><span class="sxs-lookup"><span data-stu-id="7b920-264">Depth range (near and far)</span></span>

<span data-ttu-id="7b920-265">視口原點和範圍</span><span class="sxs-lookup"><span data-stu-id="7b920-265">Viewport origin and extent</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b920-266">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b920-266">Return value</span></span>

<span data-ttu-id="7b920-267">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7b920-267">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7b920-268">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="7b920-268">Error codes</span></span>

<span data-ttu-id="7b920-269">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7b920-269">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7b920-270">Name</span><span class="sxs-lookup"><span data-stu-id="7b920-270">Name</span></span>                                                                                                  | <span data-ttu-id="7b920-271">意義</span><span class="sxs-lookup"><span data-stu-id="7b920-271">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7b920-272"><dt>**GL \_ 堆疊 \_ 溢位**</dt></span><span class="sxs-lookup"><span data-stu-id="7b920-272"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="7b920-273">當屬性堆疊已滿時，就會呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="7b920-273">The function was called while the attribute stack was full.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="7b920-274"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="7b920-274"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7b920-275">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="7b920-275">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7b920-276">備註</span><span class="sxs-lookup"><span data-stu-id="7b920-276">Remarks</span></span>

<span data-ttu-id="7b920-277">**GlPushAttrib** 函式會採用一個引數，此遮罩會指出要在屬性堆疊上儲存的狀態變數群組。</span><span class="sxs-lookup"><span data-stu-id="7b920-277">The **glPushAttrib** function takes one argument, a mask that indicates which groups of state variables to save on the attribute stack.</span></span> <span data-ttu-id="7b920-278">符號常數用來設定遮罩中的位。</span><span class="sxs-lookup"><span data-stu-id="7b920-278">Symbolic constants are used to set bits in the mask.</span></span> <span data-ttu-id="7b920-279">Mask 參數通常是藉由將邏輯 **OR** 運算套用至這些常數中的數個來構成。</span><span class="sxs-lookup"><span data-stu-id="7b920-279">The mask parameter is typically constructed by applying the logical **OR** operation to several of these constants.</span></span> <span data-ttu-id="7b920-280">您可以使用特殊遮罩 GL \_ 所有的 \_ ATTRIB \_ 位來儲存所有可堆疊的狀態。</span><span class="sxs-lookup"><span data-stu-id="7b920-280">You can use the special mask GL\_ALL\_ATTRIB\_BITS to save all stackable states.</span></span>

<span data-ttu-id="7b920-281">[**GlPopAttrib**](glpopattrib.md)函式會還原使用 last **glPushAttrib** 命令所儲存之狀態變數的值。</span><span class="sxs-lookup"><span data-stu-id="7b920-281">The [**glPopAttrib**](glpopattrib.md) function restores the values of the state variables saved with the last **glPushAttrib** command.</span></span> <span data-ttu-id="7b920-282">未儲存的會保持不變。</span><span class="sxs-lookup"><span data-stu-id="7b920-282">Those not saved are left unchanged.</span></span>

<span data-ttu-id="7b920-283">將屬性推送至完整堆疊，或從空白堆疊取出屬性是錯誤的。</span><span class="sxs-lookup"><span data-stu-id="7b920-283">It is an error to push attributes onto a full stack, or to pop attributes off an empty stack.</span></span> <span data-ttu-id="7b920-284">在任一種情況下，都會設定錯誤旗標，且不會對 OpenGL 狀態進行其他變更。</span><span class="sxs-lookup"><span data-stu-id="7b920-284">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="7b920-285">一開始，屬性堆疊是空的。</span><span class="sxs-lookup"><span data-stu-id="7b920-285">Initially, the attribute stack is empty.</span></span>

<span data-ttu-id="7b920-286">並非所有 OpenGL 狀態的值都可以儲存在屬性堆疊上。</span><span class="sxs-lookup"><span data-stu-id="7b920-286">Not all values for the OpenGL state can be saved on the attribute stack.</span></span> <span data-ttu-id="7b920-287">例如，您無法儲存圖元 pack 和解除封裝狀態、轉譯模式狀態，以及選取和意見反應狀態。</span><span class="sxs-lookup"><span data-stu-id="7b920-287">For example, you cannot save pixel pack and unpack state, render mode state, and select and feedback state.</span></span>

<span data-ttu-id="7b920-288">屬性堆疊的深度取決於執行，但必須至少為16。</span><span class="sxs-lookup"><span data-stu-id="7b920-288">The depth of the attribute stack depends on the implementation, but it must be at least 16.</span></span>

<span data-ttu-id="7b920-289">下列函式會取出 **glPushAttrib** 和 [**glPopAttrib**](glpopattrib.md)的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="7b920-289">The following functions retrieve information related to **glPushAttrib** and [**glPopAttrib**](glpopattrib.md):</span></span>

<span data-ttu-id="7b920-290">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ ATTRIB \_ STACK \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="7b920-290">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="7b920-291">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 最大 \_ ATTRIB 參數 \_ 堆疊 \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="7b920-291">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="7b920-292">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b920-292">Requirements</span></span>



| <span data-ttu-id="7b920-293">需求</span><span class="sxs-lookup"><span data-stu-id="7b920-293">Requirement</span></span> | <span data-ttu-id="7b920-294">值</span><span class="sxs-lookup"><span data-stu-id="7b920-294">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b920-295">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b920-295">Minimum supported client</span></span><br/> | <span data-ttu-id="7b920-296">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b920-296">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7b920-297">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b920-297">Minimum supported server</span></span><br/> | <span data-ttu-id="7b920-298">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b920-298">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7b920-299">標頭</span><span class="sxs-lookup"><span data-stu-id="7b920-299">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b920-300"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="7b920-300"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7b920-301">程式庫</span><span class="sxs-lookup"><span data-stu-id="7b920-301">Library</span></span><br/>                  | <dl> <span data-ttu-id="7b920-302"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b920-302"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7b920-303">DLL</span><span class="sxs-lookup"><span data-stu-id="7b920-303">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b920-304"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b920-304"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b920-305">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b920-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b920-306">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7b920-306">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7b920-307">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="7b920-307">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7b920-308">**glGet**</span><span class="sxs-lookup"><span data-stu-id="7b920-308">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="7b920-309">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="7b920-309">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="7b920-310">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="7b920-310">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="7b920-311">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="7b920-311">**glGetLight**</span></span>](glgetlight.md)
</dt> <dt>

[<span data-ttu-id="7b920-312">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="7b920-312">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="7b920-313">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="7b920-313">**glGetMaterial**</span></span>](glgetmaterial.md)
</dt> <dt>

[<span data-ttu-id="7b920-314">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="7b920-314">**glGetPixelMap**</span></span>](glgetpixelmap.md)
</dt> <dt>

[<span data-ttu-id="7b920-315">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="7b920-315">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="7b920-316">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="7b920-316">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="7b920-317">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="7b920-317">**glGetTexEnv**</span></span>](glgettexenv.md)
</dt> <dt>

[<span data-ttu-id="7b920-318">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="7b920-318">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="7b920-319">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="7b920-319">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="7b920-320">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="7b920-320">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="7b920-321">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="7b920-321">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="7b920-322">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7b920-322">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 






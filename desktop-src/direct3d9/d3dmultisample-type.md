---
description: 定義裝置可套用的完整場景取樣層級。
ms.assetid: 1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8
title: 'D3DMULTISAMPLE_TYPE 列舉 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMULTISAMPLE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: da8f9c1c8bb3aa74c0ab22a5cc701e7d835898de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323003"
---
# <a name="d3dmultisample_type-enumeration"></a><span data-ttu-id="5c257-103">D3DMULTISAMPLE \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="5c257-103">D3DMULTISAMPLE\_TYPE enumeration</span></span>

<span data-ttu-id="5c257-104">定義裝置可套用的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="5c257-104">Defines the levels of full-scene multisampling that the device can apply.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c257-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c257-105">Syntax</span></span>


```C++
typedef enum D3DMULTISAMPLE_TYPE { 
  D3DMULTISAMPLE_NONE          = 0,
  D3DMULTISAMPLE_NONMASKABLE   = 1,
  D3DMULTISAMPLE_2_SAMPLES     = 2,
  D3DMULTISAMPLE_3_SAMPLES     = 3,
  D3DMULTISAMPLE_4_SAMPLES     = 4,
  D3DMULTISAMPLE_5_SAMPLES     = 5,
  D3DMULTISAMPLE_6_SAMPLES     = 6,
  D3DMULTISAMPLE_7_SAMPLES     = 7,
  D3DMULTISAMPLE_8_SAMPLES     = 8,
  D3DMULTISAMPLE_9_SAMPLES     = 9,
  D3DMULTISAMPLE_10_SAMPLES    = 10,
  D3DMULTISAMPLE_11_SAMPLES    = 11,
  D3DMULTISAMPLE_12_SAMPLES    = 12,
  D3DMULTISAMPLE_13_SAMPLES    = 13,
  D3DMULTISAMPLE_14_SAMPLES    = 14,
  D3DMULTISAMPLE_15_SAMPLES    = 15,
  D3DMULTISAMPLE_16_SAMPLES    = 16,
  D3DMULTISAMPLE_FORCE_DWORD   = 0xffffffff
} D3DMULTISAMPLE_TYPE, *LPD3DMULTISAMPLE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="5c257-106">常數</span><span class="sxs-lookup"><span data-stu-id="5c257-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5c257-107"><span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE \_ 無**</span><span class="sxs-lookup"><span data-stu-id="5c257-107"><span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-108">沒有任何層級的完整場景取樣可供使用。</span><span class="sxs-lookup"><span data-stu-id="5c257-108">No level of full-scene multisampling is available.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-109"><span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE \_ NONMASKABLE**</span><span class="sxs-lookup"><span data-stu-id="5c257-109"><span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE\_NONMASKABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="5c257-110">啟用高採樣品質值。</span><span class="sxs-lookup"><span data-stu-id="5c257-110">Enables the multisample quality value.</span></span> <span data-ttu-id="5c257-111">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="5c257-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-112"><span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**D3DMULTISAMPLE \_ 2 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="5c257-112"><span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**D3DMULTISAMPLE\_2\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-113">可用的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="5c257-113">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-114"><span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**D3DMULTISAMPLE \_ 3 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="5c257-114"><span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**D3DMULTISAMPLE\_3\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-115">可用的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="5c257-115">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-116"><span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**D3DMULTISAMPLE \_ 4 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="5c257-116"><span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**D3DMULTISAMPLE\_4\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-117">可用的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="5c257-117">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-118"><span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**D3DMULTISAMPLE \_ 5 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="5c257-118"><span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**D3DMULTISAMPLE\_5\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-119">可用的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="5c257-119">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-120"><span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**D3DMULTISAMPLE \_ 6 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="5c257-120"><span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**D3DMULTISAMPLE\_6\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-121">可用的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="5c257-121">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-122"><span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**D3DMULTISAMPLE \_ 7 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="5c257-122"><span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**D3DMULTISAMPLE\_7\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-123">可用的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="5c257-123">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-124"><span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**D3DMULTISAMPLE \_ 8 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="5c257-124"><span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**D3DMULTISAMPLE\_8\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-125">可用的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="5c257-125">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-126"><span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**D3DMULTISAMPLE \_ 9 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="5c257-126"><span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**D3DMULTISAMPLE\_9\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-127">可用的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="5c257-127">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-128"><span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**D3DMULTISAMPLE \_ 10 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="5c257-128"><span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**D3DMULTISAMPLE\_10\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-129">可用的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="5c257-129">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-130"><span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**D3DMULTISAMPLE \_ 11 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="5c257-130"><span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**D3DMULTISAMPLE\_11\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-131">可用的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="5c257-131">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-132"><span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**D3DMULTISAMPLE \_ 12 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="5c257-132"><span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**D3DMULTISAMPLE\_12\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-133">可用的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="5c257-133">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-134"><span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**D3DMULTISAMPLE \_ 13 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="5c257-134"><span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**D3DMULTISAMPLE\_13\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-135">可用的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="5c257-135">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-136"><span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**D3DMULTISAMPLE \_ 14 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="5c257-136"><span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**D3DMULTISAMPLE\_14\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-137">可用的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="5c257-137">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-138"><span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**D3DMULTISAMPLE \_ 15 個 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="5c257-138"><span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**D3DMULTISAMPLE\_15\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-139">可用的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="5c257-139">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-140"><span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**D3DMULTISAMPLE \_ 16 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="5c257-140"><span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**D3DMULTISAMPLE\_16\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-141">可用的完整場景取樣層級。</span><span class="sxs-lookup"><span data-stu-id="5c257-141">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-142"><span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="5c257-142"><span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="5c257-143">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="5c257-143">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="5c257-144">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="5c257-144">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="5c257-145">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="5c257-145">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c257-146">備註</span><span class="sxs-lookup"><span data-stu-id="5c257-146">Remarks</span></span>

<span data-ttu-id="5c257-147">除了在 [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) time 啟用完整場景的取樣，將會有呈現狀態，可在更細微的層級上開啟和關閉各種層面。</span><span class="sxs-lookup"><span data-stu-id="5c257-147">In addition to enabling full-scene multisampling at [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) time, there will be render states that turn various aspects on and off at fine-grained levels.</span></span>

<span data-ttu-id="5c257-148">只有在使用 D3DSWAPEFFECT 捨棄交換效果所建立或重設的交換鏈上，才會對取樣器有效 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5c257-148">Multisampling is valid only on a swap chain that is being created or reset with the D3DSWAPEFFECT\_DISCARD swap effect.</span></span>

<span data-ttu-id="5c257-149">您可以使用下列方法中) 的參數 (或子參數來設定 [多級鋸齒消除鋸齒] 值。</span><span class="sxs-lookup"><span data-stu-id="5c257-149">The multisample antialiasing value can be set with the parameters (or sub-parameters) in the following methods.</span></span>



| <span data-ttu-id="5c257-150">方法</span><span class="sxs-lookup"><span data-stu-id="5c257-150">Method</span></span>                                                                                             | <span data-ttu-id="5c257-151">參數</span><span class="sxs-lookup"><span data-stu-id="5c257-151">Parameters</span></span>                         | <span data-ttu-id="5c257-152">子參數</span><span class="sxs-lookup"><span data-stu-id="5c257-152">Sub-parameters</span></span>                     |
|----------------------------------------------------------------------------------------------------|------------------------------------|------------------------------------|
| [<span data-ttu-id="5c257-153">**IDirect3D9::CheckDeviceMultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="5c257-153">**IDirect3D9::CheckDeviceMultiSampleType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)           | <span data-ttu-id="5c257-154">MultiSampleType 和 pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="5c257-154">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="5c257-155">**IDirect3D9::CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="5c257-155">**IDirect3D9::CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)                                       | <span data-ttu-id="5c257-156">pPresentationParameters</span><span class="sxs-lookup"><span data-stu-id="5c257-156">pPresentationParameters</span></span>            | <span data-ttu-id="5c257-157">MultiSampleType 和 pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="5c257-157">MultiSampleType and pQualityLevels</span></span> |
| [<span data-ttu-id="5c257-158">**IDirect3DDevice9::CreateAdditionalSwapChain**</span><span class="sxs-lookup"><span data-stu-id="5c257-158">**IDirect3DDevice9::CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) | <span data-ttu-id="5c257-159">pPresentationParameters</span><span class="sxs-lookup"><span data-stu-id="5c257-159">pPresentationParameters</span></span>            | <span data-ttu-id="5c257-160">MultiSampleType 和 pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="5c257-160">MultiSampleType and pQualityLevels</span></span> |
| [<span data-ttu-id="5c257-161">**IDirect3DDevice9::CreateDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="5c257-161">**IDirect3DDevice9::CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) | <span data-ttu-id="5c257-162">MultiSampleType 和 pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="5c257-162">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="5c257-163">**IDirect3DDevice9::CreateRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="5c257-163">**IDirect3DDevice9::CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)               | <span data-ttu-id="5c257-164">MultiSampleType 和 pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="5c257-164">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="5c257-165">**IDirect3DDevice9::Reset**</span><span class="sxs-lookup"><span data-stu-id="5c257-165">**IDirect3DDevice9::Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)                                         | <span data-ttu-id="5c257-166">pPresentationParameters</span><span class="sxs-lookup"><span data-stu-id="5c257-166">pPresentationParameters</span></span>            | <span data-ttu-id="5c257-167">MultiSampleType 和 pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="5c257-167">MultiSampleType and pQualityLevels</span></span> |



 

<span data-ttu-id="5c257-168">從一個多型型別切換成另一個，以提升消除鋸齒的品質，並不是很好的作法。</span><span class="sxs-lookup"><span data-stu-id="5c257-168">It is not good practice to switch from one multisample type to another to raise the quality of the antialiasing.</span></span>

<span data-ttu-id="5c257-169">D3DMULTISAMPLE \_ NONE 可啟用除了捨棄、鎖定等以外的交換效果。</span><span class="sxs-lookup"><span data-stu-id="5c257-169">D3DMULTISAMPLE\_NONE enables swap effects other than discarding, locking, and so on.</span></span>

<span data-ttu-id="5c257-170">顯示裝置是否支援遮罩取樣 (多樣本轉譯目標格式的多個範例以及消除鋸齒支援) 或單純的不可遮罩的取樣 (只有消除鋸齒支援) ，裝置的驅動程式會提供 D3DMULTISAMPLE \_ NONMASKABLE 多樣本類型的品質層級數目。</span><span class="sxs-lookup"><span data-stu-id="5c257-170">Whether the display device supports maskable multisampling (more than one sample for a multiple-sample render-target format plus antialias support) or just non-maskable multisampling (only antialias support), the driver for the device provides the number of quality levels for the D3DMULTISAMPLE\_NONMASKABLE multiple-sample type.</span></span> <span data-ttu-id="5c257-171">只使用取樣以進行消除鋸齒的應用程式只需要查詢驅動程式支援的不可遮罩多個樣本品質層級數目。</span><span class="sxs-lookup"><span data-stu-id="5c257-171">Applications that just use multisampling for antialiasing purposes only need to query for the number of non-maskable multiple-sample quality levels that the driver supports.</span></span>

<span data-ttu-id="5c257-172">您可以使用 [**IDirect3D9：： CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)的 pQualityLevels 參數來取得裝置支援的品質等級。</span><span class="sxs-lookup"><span data-stu-id="5c257-172">The quality levels supported by the device can be obtained with the pQualityLevels parameter of [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span></span> <span data-ttu-id="5c257-173">應用程式所使用的品質層級會使用 [**IDirect3DDevice9：： CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) 和 [**IDirect3DDevice9：： CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)的 MultiSampleQuality 參數來設定。</span><span class="sxs-lookup"><span data-stu-id="5c257-173">Quality levels used by the application are set with the MultiSampleQuality parameter of [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) and [**IDirect3DDevice9::CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget).</span></span>

<span data-ttu-id="5c257-174">如需 \_ 遮罩取樣的討論，請參閱 D3DRS MULTISAMPLEMASK。</span><span class="sxs-lookup"><span data-stu-id="5c257-174">See D3DRS\_MULTISAMPLEMASK for discussion of maskable multisampling.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c257-175">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c257-175">Requirements</span></span>



| <span data-ttu-id="5c257-176">需求</span><span class="sxs-lookup"><span data-stu-id="5c257-176">Requirement</span></span> | <span data-ttu-id="5c257-177">值</span><span class="sxs-lookup"><span data-stu-id="5c257-177">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c257-178">標頭</span><span class="sxs-lookup"><span data-stu-id="5c257-178">Header</span></span><br/> | <dl> <span data-ttu-id="5c257-179"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c257-179"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c257-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c257-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c257-181">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="5c257-181">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="5c257-182">**D3DPRESENT \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="5c257-182">**D3DPRESENT\_PARAMETERS**</span></span>](d3dpresent-parameters.md)
</dt> <dt>

[<span data-ttu-id="5c257-183">**D3DSURFACE \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="5c257-183">**D3DSURFACE\_DESC**</span></span>](d3dsurface-desc.md)
</dt> </dl>

 

 

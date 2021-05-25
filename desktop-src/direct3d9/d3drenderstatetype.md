---
description: 轉譯狀態會定義各種頂點和圖元處理的設定狀態。
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: 'D3DRENDERSTATETYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRENDERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0a7ad803535032705e6e1bb5456109486c59d190
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343063"
---
# <a name="d3drenderstatetype-enumeration"></a><span data-ttu-id="73bf3-103">D3DRENDERSTATETYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="73bf3-103">D3DRENDERSTATETYPE enumeration</span></span>

<span data-ttu-id="73bf3-104">轉譯狀態會定義各種頂點和圖元處理的設定狀態。</span><span class="sxs-lookup"><span data-stu-id="73bf3-104">Render states define set-up states for all kinds of vertex and pixel processing.</span></span> <span data-ttu-id="73bf3-105">某些轉譯狀態會設定頂點處理，而某些設定圖元處理 (查看 [ (Direct3D 9) ](render-states.md)) 的轉譯狀態。</span><span class="sxs-lookup"><span data-stu-id="73bf3-105">Some render states set up vertex processing, and some set up pixel processing (see [Render States (Direct3D 9)](render-states.md)).</span></span> <span data-ttu-id="73bf3-106">您可以使用 stateblocks 來儲存和還原轉譯狀態 (請參閱 [ (Direct3D 9) ) 的狀態欄塊儲存和還原狀態 ](state-blocks-save-and-restore-state.md) 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-106">Render states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="73bf3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="73bf3-107">Syntax</span></span>


```C++
typedef enum D3DRENDERSTATETYPE { 
  D3DRS_ZENABLE                     = 7,
  D3DRS_FILLMODE                    = 8,
  D3DRS_SHADEMODE                   = 9,
  D3DRS_ZWRITEENABLE                = 14,
  D3DRS_ALPHATESTENABLE             = 15,
  D3DRS_LASTPIXEL                   = 16,
  D3DRS_SRCBLEND                    = 19,
  D3DRS_DESTBLEND                   = 20,
  D3DRS_CULLMODE                    = 22,
  D3DRS_ZFUNC                       = 23,
  D3DRS_ALPHAREF                    = 24,
  D3DRS_ALPHAFUNC                   = 25,
  D3DRS_DITHERENABLE                = 26,
  D3DRS_ALPHABLENDENABLE            = 27,
  D3DRS_FOGENABLE                   = 28,
  D3DRS_SPECULARENABLE              = 29,
  D3DRS_FOGCOLOR                    = 34,
  D3DRS_FOGTABLEMODE                = 35,
  D3DRS_FOGSTART                    = 36,
  D3DRS_FOGEND                      = 37,
  D3DRS_FOGDENSITY                  = 38,
  D3DRS_RANGEFOGENABLE              = 48,
  D3DRS_STENCILENABLE               = 52,
  D3DRS_STENCILFAIL                 = 53,
  D3DRS_STENCILZFAIL                = 54,
  D3DRS_STENCILPASS                 = 55,
  D3DRS_STENCILFUNC                 = 56,
  D3DRS_STENCILREF                  = 57,
  D3DRS_STENCILMASK                 = 58,
  D3DRS_STENCILWRITEMASK            = 59,
  D3DRS_TEXTUREFACTOR               = 60,
  D3DRS_WRAP0                       = 128,
  D3DRS_WRAP1                       = 129,
  D3DRS_WRAP2                       = 130,
  D3DRS_WRAP3                       = 131,
  D3DRS_WRAP4                       = 132,
  D3DRS_WRAP5                       = 133,
  D3DRS_WRAP6                       = 134,
  D3DRS_WRAP7                       = 135,
  D3DRS_CLIPPING                    = 136,
  D3DRS_LIGHTING                    = 137,
  D3DRS_AMBIENT                     = 139,
  D3DRS_FOGVERTEXMODE               = 140,
  D3DRS_COLORVERTEX                 = 141,
  D3DRS_LOCALVIEWER                 = 142,
  D3DRS_NORMALIZENORMALS            = 143,
  D3DRS_DIFFUSEMATERIALSOURCE       = 145,
  D3DRS_SPECULARMATERIALSOURCE      = 146,
  D3DRS_AMBIENTMATERIALSOURCE       = 147,
  D3DRS_EMISSIVEMATERIALSOURCE      = 148,
  D3DRS_VERTEXBLEND                 = 151,
  D3DRS_CLIPPLANEENABLE             = 152,
  D3DRS_POINTSIZE                   = 154,
  D3DRS_POINTSIZE_MIN               = 155,
  D3DRS_POINTSPRITEENABLE           = 156,
  D3DRS_POINTSCALEENABLE            = 157,
  D3DRS_POINTSCALE_A                = 158,
  D3DRS_POINTSCALE_B                = 159,
  D3DRS_POINTSCALE_C                = 160,
  D3DRS_MULTISAMPLEANTIALIAS        = 161,
  D3DRS_MULTISAMPLEMASK             = 162,
  D3DRS_PATCHEDGESTYLE              = 163,
  D3DRS_DEBUGMONITORTOKEN           = 165,
  D3DRS_POINTSIZE_MAX               = 166,
  D3DRS_INDEXEDVERTEXBLENDENABLE    = 167,
  D3DRS_COLORWRITEENABLE            = 168,
  D3DRS_TWEENFACTOR                 = 170,
  D3DRS_BLENDOP                     = 171,
  D3DRS_POSITIONDEGREE              = 172,
  D3DRS_NORMALDEGREE                = 173,
  D3DRS_SCISSORTESTENABLE           = 174,
  D3DRS_SLOPESCALEDEPTHBIAS         = 175,
  D3DRS_ANTIALIASEDLINEENABLE       = 176,
  D3DRS_MINTESSELLATIONLEVEL        = 178,
  D3DRS_MAXTESSELLATIONLEVEL        = 179,
  D3DRS_ADAPTIVETESS_X              = 180,
  D3DRS_ADAPTIVETESS_Y              = 181,
  D3DRS_ADAPTIVETESS_Z              = 182,
  D3DRS_ADAPTIVETESS_W              = 183,
  D3DRS_ENABLEADAPTIVETESSELLATION  = 184,
  D3DRS_TWOSIDEDSTENCILMODE         = 185,
  D3DRS_CCW_STENCILFAIL             = 186,
  D3DRS_CCW_STENCILZFAIL            = 187,
  D3DRS_CCW_STENCILPASS             = 188,
  D3DRS_CCW_STENCILFUNC             = 189,
  D3DRS_COLORWRITEENABLE1           = 190,
  D3DRS_COLORWRITEENABLE2           = 191,
  D3DRS_COLORWRITEENABLE3           = 192,
  D3DRS_BLENDFACTOR                 = 193,
  D3DRS_SRGBWRITEENABLE             = 194,
  D3DRS_DEPTHBIAS                   = 195,
  D3DRS_WRAP8                       = 198,
  D3DRS_WRAP9                       = 199,
  D3DRS_WRAP10                      = 200,
  D3DRS_WRAP11                      = 201,
  D3DRS_WRAP12                      = 202,
  D3DRS_WRAP13                      = 203,
  D3DRS_WRAP14                      = 204,
  D3DRS_WRAP15                      = 205,
  D3DRS_SEPARATEALPHABLENDENABLE    = 206,
  D3DRS_SRCBLENDALPHA               = 207,
  D3DRS_DESTBLENDALPHA              = 208,
  D3DRS_BLENDOPALPHA                = 209,
  D3DRS_FORCE_DWORD                 = 0x7fffffff
} D3DRENDERSTATETYPE, *LPD3DRENDERSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="73bf3-108">常數</span><span class="sxs-lookup"><span data-stu-id="73bf3-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="73bf3-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ ZENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS\_ZENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-110">深度緩衝處理狀態，作為 [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) 列舉型別的其中一個成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-110">Depth-buffering state as one member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumerated type.</span></span> <span data-ttu-id="73bf3-111">將此狀態設定為 D3DZB \_ TRUE，以啟用 z 緩衝、D3DZB \_ USEW 來啟用 w 緩衝，或 D3DZB \_ FALSE 以停用深度緩衝。</span><span class="sxs-lookup"><span data-stu-id="73bf3-111">Set this state to D3DZB\_TRUE to enable z-buffering, D3DZB\_USEW to enable w-buffering, or D3DZB\_FALSE to disable depth buffering.</span></span>

<span data-ttu-id="73bf3-112">\_如果已將 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)結構的 EnableAutoDepthStencil 成員設為 **TRUE**，則此呈現狀態的預設值為 D3DZB TRUE， \_ 否則為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="73bf3-112">The default value for this render state is D3DZB\_TRUE if a depth stencil was created along with the swap chain by setting the EnableAutoDepthStencil member of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure to **TRUE**, and D3DZB\_FALSE otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ FILLMODE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS\_FILLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-114">[**D3DFILLMODE**](./d3dfillmode.md)列舉型別的一或多個成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-114">One or more members of the [**D3DFILLMODE**](./d3dfillmode.md) enumerated type.</span></span> <span data-ttu-id="73bf3-115">預設值為 D3DFILL \_ 固態。</span><span class="sxs-lookup"><span data-stu-id="73bf3-115">The default value is D3DFILL\_SOLID.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ SHADEMODE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS\_SHADEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-117">[**D3DSHADEMODE**](./d3dshademode.md)列舉型別的一或多個成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-117">One or more members of the [**D3DSHADEMODE**](./d3dshademode.md) enumerated type.</span></span> <span data-ttu-id="73bf3-118">預設值為 D3DSHADE \_ GOURAUD。</span><span class="sxs-lookup"><span data-stu-id="73bf3-118">The default value is D3DSHADE\_GOURAUD.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ ZWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS\_ZWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-120">**TRUE** 表示讓應用程式寫入深度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="73bf3-120">**TRUE** to enable the application to write to the depth buffer.</span></span> <span data-ttu-id="73bf3-121">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-121">The default value is **TRUE**.</span></span> <span data-ttu-id="73bf3-122">此成員可讓應用程式防止系統以新的深度值更新深度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="73bf3-122">This member enables an application to prevent the system from updating the depth buffer with new depth values.</span></span> <span data-ttu-id="73bf3-123">如果 **為 FALSE**，則會根據轉譯狀態 D3DRS \_ ZFUNC （假設深度緩衝處理已發生）進行深度比較，但不會將深度值寫入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="73bf3-123">If **FALSE**, depth comparisons are still made according to the render state D3DRS\_ZFUNC, assuming that depth buffering is taking place, but depth values are not written to the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ ALPHATESTENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS\_ALPHATESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-125">**TRUE** 表示啟用每圖元 Alpha 測試。</span><span class="sxs-lookup"><span data-stu-id="73bf3-125">**TRUE** to enable per pixel alpha testing.</span></span> <span data-ttu-id="73bf3-126">如果測試通過，則會由框架緩衝區來處理圖元。</span><span class="sxs-lookup"><span data-stu-id="73bf3-126">If the test passes, the pixel is processed by the frame buffer.</span></span> <span data-ttu-id="73bf3-127">否則，就會略過圖元的所有框架緩衝區處理。</span><span class="sxs-lookup"><span data-stu-id="73bf3-127">Otherwise, all frame-buffer processing is skipped for the pixel.</span></span>

<span data-ttu-id="73bf3-128">使用 D3DRS ALPHAFUNC 轉譯狀態所提供的比較函式，藉由比較輸入的 Alpha 值與參考 Alpha 值來完成測試 \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-128">The test is done by comparing the incoming alpha value with the reference alpha value, using the comparison function provided by the D3DRS\_ALPHAFUNC render state.</span></span> <span data-ttu-id="73bf3-129">參考 Alpha 值是由針對 D3DRS ALPHAREF 所設定的值所決定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-129">The reference alpha value is determined by the value set for D3DRS\_ALPHAREF.</span></span> <span data-ttu-id="73bf3-130">如需詳細資訊，請參閱 [ (Direct3D 9 的 Alpha 測試狀態) ](alpha-testing-state.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-130">For more information, see [Alpha Testing State (Direct3D 9)](alpha-testing-state.md).</span></span>

<span data-ttu-id="73bf3-131">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-131">The default value of this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ LASTPIXEL**</span><span class="sxs-lookup"><span data-stu-id="73bf3-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS\_LASTPIXEL**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-133">預設值為 **TRUE**，可讓您繪製線條中的最後一個圖元。</span><span class="sxs-lookup"><span data-stu-id="73bf3-133">The default value is **TRUE**, which enables drawing of the last pixel in a line.</span></span> <span data-ttu-id="73bf3-134">若要防止繪製最後一個圖元，請將此值設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-134">To prevent drawing of the last pixel, set this value to **FALSE**.</span></span> <span data-ttu-id="73bf3-135">如需詳細資訊，請參閱 [ (Direct3D 9) 的大綱和填滿狀態 ](outline-and-fill-state.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-135">For more information, see [Outline and Fill State (Direct3D 9)](outline-and-fill-state.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ SRCBLEND**</span><span class="sxs-lookup"><span data-stu-id="73bf3-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS\_SRCBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-137">[**D3DBLEND**](./d3dblend.md)列舉型別的其中一個成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-137">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="73bf3-138">預設值為 D3DBLEND \_ 一個。</span><span class="sxs-lookup"><span data-stu-id="73bf3-138">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ DESTBLEND**</span><span class="sxs-lookup"><span data-stu-id="73bf3-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS\_DESTBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-140">[**D3DBLEND**](./d3dblend.md)列舉型別的其中一個成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-140">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="73bf3-141">預設值為 D3DBLEND \_ 零。</span><span class="sxs-lookup"><span data-stu-id="73bf3-141">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS \_ CULLMODE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS\_CULLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-143">指定回溯三角形的挑選方式（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="73bf3-143">Specifies how back-facing triangles are culled, if at all.</span></span> <span data-ttu-id="73bf3-144">這可以設定為 [**D3DCULL**](./d3dcull.md) 列舉型別的其中一個成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-144">This can be set to one member of the [**D3DCULL**](./d3dcull.md) enumerated type.</span></span> <span data-ttu-id="73bf3-145">預設值為 D3DCULL \_ CCW。</span><span class="sxs-lookup"><span data-stu-id="73bf3-145">The default value is D3DCULL\_CCW.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS \_ ZFUNC**</span><span class="sxs-lookup"><span data-stu-id="73bf3-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS\_ZFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-147">[**D3DCMPFUNC**](./d3dcmpfunc.md)列舉型別的其中一個成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-147">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="73bf3-148">預設值為 D3DCMP \_ LESSEQUAL。</span><span class="sxs-lookup"><span data-stu-id="73bf3-148">The default value is D3DCMP\_LESSEQUAL.</span></span> <span data-ttu-id="73bf3-149">此成員可讓應用程式根據與相機之間的距離來接受或拒絕圖元。</span><span class="sxs-lookup"><span data-stu-id="73bf3-149">This member enables an application to accept or reject a pixel, based on its distance from the camera.</span></span>

<span data-ttu-id="73bf3-150">圖元的深度值會與深度緩衝區值進行比較。</span><span class="sxs-lookup"><span data-stu-id="73bf3-150">The depth value of the pixel is compared with the depth-buffer value.</span></span> <span data-ttu-id="73bf3-151">如果圖元的深度值通過比較函數，則會寫入圖元。</span><span class="sxs-lookup"><span data-stu-id="73bf3-151">If the depth value of the pixel passes the comparison function, the pixel is written.</span></span>

<span data-ttu-id="73bf3-152">只有當轉譯狀態為 **TRUE** 時，才會將 depth 值寫入深度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="73bf3-152">The depth value is written to the depth buffer only if the render state is **TRUE**.</span></span>

<span data-ttu-id="73bf3-153">如果深度測試失敗，軟體 rasterizers 和許多硬體加速器的運作速度會更快，因為不需要在圖元呈現時篩選和 lambert 材質。</span><span class="sxs-lookup"><span data-stu-id="73bf3-153">Software rasterizers and many hardware accelerators work faster if the depth test fails, because there is no need to filter and modulate the texture if the pixel is not going to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ ALPHAREF**</span><span class="sxs-lookup"><span data-stu-id="73bf3-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS\_ALPHAREF**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-155">值，指定在啟用 Alpha 測試時測試圖元的參考 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-155">Value that specifies a reference alpha value against which pixels are tested when alpha testing is enabled.</span></span> <span data-ttu-id="73bf3-156">這是8位值，放在 DWORD 轉譯狀態值的低8位中。</span><span class="sxs-lookup"><span data-stu-id="73bf3-156">This is an 8-bit value placed in the low 8 bits of the DWORD render-state value.</span></span> <span data-ttu-id="73bf3-157">值的範圍可以從0x00000000 到0x000000FF。</span><span class="sxs-lookup"><span data-stu-id="73bf3-157">Values can range from 0x00000000 through 0x000000FF.</span></span> <span data-ttu-id="73bf3-158">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-158">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ ALPHAFUNC**</span><span class="sxs-lookup"><span data-stu-id="73bf3-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS\_ALPHAFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-160">[**D3DCMPFUNC**](./d3dcmpfunc.md)列舉型別的其中一個成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-160">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="73bf3-161">預設值為 [永遠 D3DCMP] \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-161">The default value is D3DCMP\_ALWAYS.</span></span> <span data-ttu-id="73bf3-162">此成員可讓應用程式根據其 Alpha 值來接受或拒絕圖元。</span><span class="sxs-lookup"><span data-stu-id="73bf3-162">This member enables an application to accept or reject a pixel, based on its alpha value.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ DITHERENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS\_DITHERENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-164">**TRUE** 表示啟用遞色。</span><span class="sxs-lookup"><span data-stu-id="73bf3-164">**TRUE** to enable dithering.</span></span> <span data-ttu-id="73bf3-165">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-165">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ ALPHABLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS\_ALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-167">**TRUE** 表示啟用 Alpha 混合透明度。</span><span class="sxs-lookup"><span data-stu-id="73bf3-167">**TRUE** to enable alpha-blended transparency.</span></span> <span data-ttu-id="73bf3-168">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-168">The default value is **FALSE**.</span></span>

<span data-ttu-id="73bf3-169">Alpha 混色的類型取決於 D3DRS \_ SRCBLEND 和 D3DRS \_ DESTBLEND 轉譯狀態。</span><span class="sxs-lookup"><span data-stu-id="73bf3-169">The type of alpha blending is determined by the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ FOGENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS\_FOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-171">**TRUE** 表示啟用霧化混色。</span><span class="sxs-lookup"><span data-stu-id="73bf3-171">**TRUE** to enable fog blending.</span></span> <span data-ttu-id="73bf3-172">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-172">The default value is **FALSE**.</span></span> <span data-ttu-id="73bf3-173">如需使用霧化混合的詳細資訊，請參閱 [霧化](fog.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-173">For more information about using fog blending, see [Fog](fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ SPECULARENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS\_SPECULARENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-175">**TRUE** 表示啟用高光。</span><span class="sxs-lookup"><span data-stu-id="73bf3-175">**TRUE** to enable specular highlights.</span></span> <span data-ttu-id="73bf3-176">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-176">The default value is **FALSE**.</span></span>

<span data-ttu-id="73bf3-177">高光的計算方式，就像物件的每個頂點都在物件的原點一樣。</span><span class="sxs-lookup"><span data-stu-id="73bf3-177">Specular highlights are calculated as though every vertex in the object being lit is at the object's origin.</span></span> <span data-ttu-id="73bf3-178">只要物件是以原點建立模型，而且從光線到物件的距離相對較大，這就會提供預期的結果。</span><span class="sxs-lookup"><span data-stu-id="73bf3-178">This gives the expected results as long as the object is modeled around the origin and the distance from the light to the object is relatively large.</span></span> <span data-ttu-id="73bf3-179">在其他情況下，結果會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="73bf3-179">In other cases, the results as undefined.</span></span>

<span data-ttu-id="73bf3-180">當這個成員設定為 **TRUE** 時，會在紋理重迭之後，但在 Alpha 混合之前，將反射色彩新增至基底色彩。</span><span class="sxs-lookup"><span data-stu-id="73bf3-180">When this member is set to **TRUE**, the specular color is added to the base color after the texture cascade but before alpha blending.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS \_ FOGCOLOR**</span><span class="sxs-lookup"><span data-stu-id="73bf3-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS\_FOGCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-182">型別為 [**D3DCOLOR**](d3dcolor.md)的值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-182">Value whose type is [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="73bf3-183">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-183">The default value is 0.</span></span> <span data-ttu-id="73bf3-184">如需有關霧化色彩的詳細資訊，請參閱 [ (Direct3D 9) 的霧化色彩 ](fog-color.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-184">For more information about fog color, see [Fog Color (Direct3D 9)](fog-color.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ FOGTABLEMODE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS\_FOGTABLEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-186">要用於圖元霧化的霧化公式。</span><span class="sxs-lookup"><span data-stu-id="73bf3-186">The fog formula to be used for pixel fog.</span></span> <span data-ttu-id="73bf3-187">設定為 [**D3DFOGMODE**](./d3dfogmode.md) 列舉型別的其中一個成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-187">Set to one of the members of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="73bf3-188">預設值為 [無] D3DFOG \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-188">The default value is D3DFOG\_NONE.</span></span> <span data-ttu-id="73bf3-189">如需圖元霧化的詳細資訊，請參閱 [ (Direct3D 9) 的圖元霧化 ](pixel-fog.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-189">For more information about pixel fog, see [Pixel Fog (Direct3D 9)](pixel-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS \_ FOGSTART**</span><span class="sxs-lookup"><span data-stu-id="73bf3-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS\_FOGSTART**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-191">圖元或頂點霧化效果開始于線性霧化模式的深度。</span><span class="sxs-lookup"><span data-stu-id="73bf3-191">Depth at which pixel or vertex fog effects begin for linear fog mode.</span></span> <span data-ttu-id="73bf3-192">預設值為 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-192">The default value is 0.0f.</span></span> <span data-ttu-id="73bf3-193">深度會在世界空間中指定，用於頂點霧化以及裝置空間 \[ 0.0、1.0 \] 或世界空間，以進行圖元霧化。</span><span class="sxs-lookup"><span data-stu-id="73bf3-193">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="73bf3-194">針對圖元霧化，當系統使用 z 進行霧化計算，而當系統使用眼睛相關的霧化 (w-霧) 時，這些值就會在裝置空間中。</span><span class="sxs-lookup"><span data-stu-id="73bf3-194">For pixel fog, these values are in device space when the system uses z for fog calculations and world-world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="73bf3-195">如需詳細資訊，請參閱 [ (Direct3D 9 的霧化參數) ](fog-parameters.md) 和 [眼睛相關的 Vs. Z 深度](pixel-fog.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-195">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="73bf3-196">此呈現狀態的值為浮點值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-196">Values for this render state are floating-point values.</span></span> <span data-ttu-id="73bf3-197">因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="73bf3-197">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span data-ttu-id="73bf3-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS \_ FOGEND**</span><span class="sxs-lookup"><span data-stu-id="73bf3-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS\_FOGEND**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-199">線性霧化模式的圖元或頂點霧化效果結束的深度。</span><span class="sxs-lookup"><span data-stu-id="73bf3-199">Depth at which pixel or vertex fog effects end for linear fog mode.</span></span> <span data-ttu-id="73bf3-200">預設值為 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-200">The default value is 1.0f.</span></span> <span data-ttu-id="73bf3-201">深度會在世界空間中指定，用於頂點霧化以及裝置空間 \[ 0.0、1.0 \] 或世界空間，以進行圖元霧化。</span><span class="sxs-lookup"><span data-stu-id="73bf3-201">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="73bf3-202">若為圖元霧化，當系統使用 z 進行霧化計算，而當系統使用眼睛相關的霧化 (w-霧化) 時，這些值就會在裝置空間中。</span><span class="sxs-lookup"><span data-stu-id="73bf3-202">For pixel fog, these values are in device space when the system uses z for fog calculations and in world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="73bf3-203">如需詳細資訊，請參閱 [ (Direct3D 9 的霧化參數) ](fog-parameters.md) 和 [眼睛相關的 Vs. Z 深度](pixel-fog.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-203">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="73bf3-204">此呈現狀態的值為浮點值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-204">Values for this render state are floating-point values.</span></span> <span data-ttu-id="73bf3-205">因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="73bf3-205">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span data-ttu-id="73bf3-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS \_ FOGDENSITY**</span><span class="sxs-lookup"><span data-stu-id="73bf3-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS\_FOGDENSITY**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-207">在指數霧化模式中使用之圖元或頂點霧化的霧化密度 (D3DFOG \_ EXP 和 D3DFOG \_ EXP2) 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-207">Fog density for pixel or vertex fog used in the exponential fog modes (D3DFOG\_EXP and D3DFOG\_EXP2).</span></span> <span data-ttu-id="73bf3-208">有效的密度值範圍從0.0 到1.0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-208">Valid density values range from 0.0 through 1.0.</span></span> <span data-ttu-id="73bf3-209">預設值為 1.0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-209">The default value is 1.0.</span></span> <span data-ttu-id="73bf3-210">如需詳細資訊，請參閱 [ (Direct3D 9) 的霧化參數 ](fog-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-210">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

<span data-ttu-id="73bf3-211">此呈現狀態的值為浮點值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-211">Values for this render state are floating-point values.</span></span> <span data-ttu-id="73bf3-212">因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="73bf3-212">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span data-ttu-id="73bf3-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ RANGEFOGENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS\_RANGEFOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-214">**TRUE** 表示啟用以範圍為基礎的頂點霧化。</span><span class="sxs-lookup"><span data-stu-id="73bf3-214">**TRUE** to enable range-based vertex fog.</span></span> <span data-ttu-id="73bf3-215">預設值為 **FALSE**，在這種情況下，系統會使用深度型的霧化。</span><span class="sxs-lookup"><span data-stu-id="73bf3-215">The default value is **FALSE**, in which case the system uses depth-based fog.</span></span> <span data-ttu-id="73bf3-216">在以範圍為基礎的霧化中，從檢視器物件的距離會用來計算霧化效果，而不是物件的深度 (也就是在場景中的 z 座標) 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-216">In range-based fog, the distance of an object from the viewer is used to compute fog effects, not the depth of the object (that is, the z-coordinate) in the scene.</span></span> <span data-ttu-id="73bf3-217">在以範圍為基礎的霧化中，所有的霧化方法都會正常運作，不同之處在于它們會在計算中使用範圍而非深度。</span><span class="sxs-lookup"><span data-stu-id="73bf3-217">In range-based fog, all fog methods work as usual, except that they use range instead of depth in the computations.</span></span>

<span data-ttu-id="73bf3-218">範圍是用於霧化計算的正確因素，但通常會使用深度，因為範圍是計算和深度的耗用時間，通常已可供使用。</span><span class="sxs-lookup"><span data-stu-id="73bf3-218">Range is the correct factor to use for fog computations, but depth is commonly used instead because range is time-consuming to compute and depth is generally already available.</span></span> <span data-ttu-id="73bf3-219">使用深度來計算霧化有不想要的效果，讓周邊物件的 fogginess 隨著檢視器的眼睛變化而變更，在此情況下，深度變更和範圍會維持不變。</span><span class="sxs-lookup"><span data-stu-id="73bf3-219">Using depth to calculate fog has the undesirable effect of having the fogginess of peripheral objects change as the viewer's eye moves - in this case, the depth changes and the range remains constant.</span></span>

<span data-ttu-id="73bf3-220">因為目前沒有硬體支援每個圖元範圍的霧化，所以範圍更正只會提供給頂點霧化。</span><span class="sxs-lookup"><span data-stu-id="73bf3-220">Because no hardware currently supports per-pixel range-based fog, range correction is offered only for vertex fog.</span></span>

<span data-ttu-id="73bf3-221">如需詳細資訊，請參閱 [ (Direct3D 9) 的頂點霧化 ](vertex-fog.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-221">For more information, see [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS \_ STENCILENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS\_STENCILENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-223">**TRUE** 表示啟用 stenciling，否則為 **FALSE** 以停用 stenciling。</span><span class="sxs-lookup"><span data-stu-id="73bf3-223">**TRUE** to enable stenciling, or **FALSE** to disable stenciling.</span></span> <span data-ttu-id="73bf3-224">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-224">The default value is **FALSE**.</span></span> <span data-ttu-id="73bf3-225">如需詳細資訊，請參閱 [ (Direct3D 9) 的樣板緩衝區技術 ](stencil-buffer-techniques.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-225">For more information, see [Stencil Buffer Techniques (Direct3D 9)](stencil-buffer-techniques.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ STENCILFAIL**</span><span class="sxs-lookup"><span data-stu-id="73bf3-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-227">樣板測試失敗時要執行的樣板作業。</span><span class="sxs-lookup"><span data-stu-id="73bf3-227">Stencil operation to perform if the stencil test fails.</span></span> <span data-ttu-id="73bf3-228">值是來自 [**D3DSTENCILOP**](./d3dstencilop.md) 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="73bf3-228">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="73bf3-229">預設值為 [保留] D3DSTENCILOP \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-229">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ STENCILZFAIL**</span><span class="sxs-lookup"><span data-stu-id="73bf3-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-231">樣板測試通過時要執行的樣板作業，而且 (z 測試) 的深度測試失敗。</span><span class="sxs-lookup"><span data-stu-id="73bf3-231">Stencil operation to perform if the stencil test passes and the depth test (z-test) fails.</span></span> <span data-ttu-id="73bf3-232">值是來自 [**D3DSTENCILOP**](./d3dstencilop.md) 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="73bf3-232">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="73bf3-233">預設值為 [保留] D3DSTENCILOP \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-233">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ STENCILPASS**</span><span class="sxs-lookup"><span data-stu-id="73bf3-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-235">當樣板和深度 (z) 測試都通過時，要執行的樣板作業。</span><span class="sxs-lookup"><span data-stu-id="73bf3-235">Stencil operation to perform if both the stencil and the depth (z) tests pass.</span></span> <span data-ttu-id="73bf3-236">值是來自 [**D3DSTENCILOP**](./d3dstencilop.md) 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="73bf3-236">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="73bf3-237">預設值為 [保留] D3DSTENCILOP \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-237">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ STENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="73bf3-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-239">樣板測試的比較函數。</span><span class="sxs-lookup"><span data-stu-id="73bf3-239">Comparison function for the stencil test.</span></span> <span data-ttu-id="73bf3-240">值是來自 [**D3DCMPFUNC**](./d3dcmpfunc.md) 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="73bf3-240">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="73bf3-241">預設值為 [永遠 D3DCMP] \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-241">The default value is D3DCMP\_ALWAYS.</span></span>

<span data-ttu-id="73bf3-242">比較函數是用來比較參考值與樣板緩衝區專案。</span><span class="sxs-lookup"><span data-stu-id="73bf3-242">The comparison function is used to compare the reference value to a stencil buffer entry.</span></span> <span data-ttu-id="73bf3-243">這項比較只適用于在樣板遮罩中設定的參考值和樣板緩衝區專案中的位， (由 D3DRS STENCILMASK 轉譯 \_ 狀態) 設定。</span><span class="sxs-lookup"><span data-stu-id="73bf3-243">This comparison applies only to the bits in the reference value and stencil buffer entry that are set in the stencil mask (set by the D3DRS\_STENCILMASK render state).</span></span> <span data-ttu-id="73bf3-244">若 **為 TRUE**，則樣板測試會通過。</span><span class="sxs-lookup"><span data-stu-id="73bf3-244">If **TRUE**, the stencil test passes.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ STENCILREF**</span><span class="sxs-lookup"><span data-stu-id="73bf3-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS\_STENCILREF**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-246">樣板測試的 int 參考值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-246">An int reference value for the stencil test.</span></span> <span data-ttu-id="73bf3-247">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-247">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ STENCILMASK**</span><span class="sxs-lookup"><span data-stu-id="73bf3-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS\_STENCILMASK**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-249">遮罩會套用至參考值和每個樣板緩衝區專案，以判斷樣板測試的有效位。</span><span class="sxs-lookup"><span data-stu-id="73bf3-249">Mask applied to the reference value and each stencil buffer entry to determine the significant bits for the stencil test.</span></span> <span data-ttu-id="73bf3-250">預設遮罩為0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="73bf3-250">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS \_ STENCILWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="73bf3-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS\_STENCILWRITEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-252">寫入遮罩會套用至寫入至樣板緩衝區的值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-252">Write mask applied to values written into the stencil buffer.</span></span> <span data-ttu-id="73bf3-253">預設遮罩為0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="73bf3-253">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ TEXTUREFACTOR**</span><span class="sxs-lookup"><span data-stu-id="73bf3-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS\_TEXTUREFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-255">用於多紋理混合的色彩，與 D3DTA \_ TFACTOR 材質混合引數或 D3DTOP \_ BLENDFACTORALPHA 材質混合作業。</span><span class="sxs-lookup"><span data-stu-id="73bf3-255">Color used for multiple-texture blending with the D3DTA\_TFACTOR texture-blending argument or the D3DTOP\_BLENDFACTORALPHA texture-blending operation.</span></span> <span data-ttu-id="73bf3-256">相關聯的值是 [**D3DCOLOR**](d3dcolor.md) 變數。</span><span class="sxs-lookup"><span data-stu-id="73bf3-256">The associated value is a [**D3DCOLOR**](d3dcolor.md) variable.</span></span> <span data-ttu-id="73bf3-257">預設值為不透明的白色 (0xFFFFFFFF) 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-257">The default value is opaque white (0xFFFFFFFF).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**</span><span class="sxs-lookup"><span data-stu-id="73bf3-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS\_WRAP0**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-259">多組紋理座標的材質換行行為。</span><span class="sxs-lookup"><span data-stu-id="73bf3-259">Texture-wrapping behavior for multiple sets of texture coordinates.</span></span> <span data-ttu-id="73bf3-260">此轉譯狀態的有效值可以是 D3DWRAPCOORD \_ 0 (或 D3DWRAP \_ U) 、D3DWRAPCOORD \_ 1 (或 D3DWRAP \_ V) 、D3DWRAPCOORD \_ 2 (或 D3DWRAP \_ W) ，以及 D3DWRAPCOORD \_ 3 旗標的任意組合。</span><span class="sxs-lookup"><span data-stu-id="73bf3-260">Valid values for this render state can be any combination of the D3DWRAPCOORD\_0 (or D3DWRAP\_U), D3DWRAPCOORD\_1 (or D3DWRAP\_V), D3DWRAPCOORD\_2 (or D3DWRAP\_W), and D3DWRAPCOORD\_3 flags.</span></span> <span data-ttu-id="73bf3-261">這些會導致系統將第一個、第二、第三和第四個維度的方向（有時稱為 s、t、r 和 q 指示）包裝給指定的材質。</span><span class="sxs-lookup"><span data-stu-id="73bf3-261">These cause the system to wrap in the direction of the first, second, third, and fourth dimensions, sometimes referred to as the s, t, r, and q directions, for a given texture.</span></span> <span data-ttu-id="73bf3-262">此轉譯狀態的預設值為 0 (在) 的所有方向停用換行。</span><span class="sxs-lookup"><span data-stu-id="73bf3-262">The default value for this render state is 0 (wrapping disabled in all directions).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**</span><span class="sxs-lookup"><span data-stu-id="73bf3-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS\_WRAP1**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-264">請參閱 D3DRS \_ WRAP0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-264">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**</span><span class="sxs-lookup"><span data-stu-id="73bf3-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS\_WRAP2**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-266">請參閱 D3DRS \_ WRAP0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-266">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS \_ WRAP3**</span><span class="sxs-lookup"><span data-stu-id="73bf3-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS\_WRAP3**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-268">請參閱 D3DRS \_ WRAP0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-268">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**</span><span class="sxs-lookup"><span data-stu-id="73bf3-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS\_WRAP4**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-270">請參閱 D3DRS \_ WRAP0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-270">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS \_ WRAP5**</span><span class="sxs-lookup"><span data-stu-id="73bf3-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS\_WRAP5**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-272">請參閱 D3DRS \_ WRAP0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-272">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS \_ WRAP6**</span><span class="sxs-lookup"><span data-stu-id="73bf3-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS\_WRAP6**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-274">請參閱 D3DRS \_ WRAP0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-274">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS \_ WRAP7**</span><span class="sxs-lookup"><span data-stu-id="73bf3-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS\_WRAP7**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-276">請參閱 D3DRS \_ WRAP0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-276">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS \_ 剪切**</span><span class="sxs-lookup"><span data-stu-id="73bf3-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS\_CLIPPING**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-278">**TRUE** 表示要啟用 Direct3D 的基本剪輯，或使用 **FALSE** 來停用它。</span><span class="sxs-lookup"><span data-stu-id="73bf3-278">**TRUE** to enable primitive clipping by Direct3D, or **FALSE** to disable it.</span></span> <span data-ttu-id="73bf3-279">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-279">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**D3DRS \_ 光源**</span><span class="sxs-lookup"><span data-stu-id="73bf3-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**D3DRS\_LIGHTING**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-281">**TRUE** 表示啟用 Direct3D 光源，或 **FALSE** 表示停用它。</span><span class="sxs-lookup"><span data-stu-id="73bf3-281">**TRUE** to enable Direct3D lighting, or **FALSE** to disable it.</span></span> <span data-ttu-id="73bf3-282">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-282">The default value is **TRUE**.</span></span> <span data-ttu-id="73bf3-283">只有包含頂點標準的頂點會正確地發亮;未包含一般的頂點會在所有光源計算中採用0的點乘積。</span><span class="sxs-lookup"><span data-stu-id="73bf3-283">Only vertices that include a vertex normal are properly lit; vertices that do not contain a normal employ a dot product of 0 in all lighting calculations.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS \_ 環境**</span><span class="sxs-lookup"><span data-stu-id="73bf3-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS\_AMBIENT**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-285">環境淺色色彩。</span><span class="sxs-lookup"><span data-stu-id="73bf3-285">Ambient light color.</span></span> <span data-ttu-id="73bf3-286">此值的類型為 [**D3DCOLOR**](d3dcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-286">This value is of type [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="73bf3-287">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-287">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS \_ FOGVERTEXMODE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS\_FOGVERTEXMODE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-289">要用於頂點模糊的霧化公式。</span><span class="sxs-lookup"><span data-stu-id="73bf3-289">Fog formula to be used for vertex fog.</span></span> <span data-ttu-id="73bf3-290">設定為 [**D3DFOGMODE**](./d3dfogmode.md) 列舉型別的其中一個成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-290">Set to one member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="73bf3-291">預設值為 [無] D3DFOG \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-291">The default value is D3DFOG\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ COLORVERTEX**</span><span class="sxs-lookup"><span data-stu-id="73bf3-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS\_COLORVERTEX**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-293">**TRUE** 表示啟用每個頂點的色彩，或使用 **FALSE** 來停用它。</span><span class="sxs-lookup"><span data-stu-id="73bf3-293">**TRUE** to enable per-vertex color or **FALSE** to disable it.</span></span> <span data-ttu-id="73bf3-294">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-294">The default value is **TRUE**.</span></span> <span data-ttu-id="73bf3-295">啟用每個頂點色彩可讓系統在其光源計算中包含為個別頂點定義的色彩。</span><span class="sxs-lookup"><span data-stu-id="73bf3-295">Enabling per-vertex color allows the system to include the color defined for individual vertices in its lighting calculations.</span></span>

<span data-ttu-id="73bf3-296">如需詳細資訊，請參閱下列呈現狀態：</span><span class="sxs-lookup"><span data-stu-id="73bf3-296">For more information, see the following render states:</span></span>

-   <span data-ttu-id="73bf3-297">D3DRS \_ DIFFUSEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="73bf3-297">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>
-   <span data-ttu-id="73bf3-298">D3DRS \_ SPECULARMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="73bf3-298">D3DRS\_SPECULARMATERIALSOURCE</span></span>
-   <span data-ttu-id="73bf3-299">D3DRS \_ AMBIENTMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="73bf3-299">D3DRS\_AMBIENTMATERIALSOURCE</span></span>
-   <span data-ttu-id="73bf3-300">D3DRS \_ EMISSIVEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="73bf3-300">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ LOCALVIEWER**</span><span class="sxs-lookup"><span data-stu-id="73bf3-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS\_LOCALVIEWER**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-302">**TRUE** 表示啟用相機相關的高光，或為 **FALSE** 表示使用正向反射醒目顯示。</span><span class="sxs-lookup"><span data-stu-id="73bf3-302">**TRUE** to enable camera-relative specular highlights, or **FALSE** to use orthogonal specular highlights.</span></span> <span data-ttu-id="73bf3-303">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-303">The default value is **TRUE**.</span></span> <span data-ttu-id="73bf3-304">使用正向投射的應用程式應指定 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-304">Applications that use orthogonal projection should specify **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ NORMALIZENORMALS**</span><span class="sxs-lookup"><span data-stu-id="73bf3-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS\_NORMALIZENORMALS**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-306">**TRUE** 表示啟用頂點法線的自動正規化，或 **FALSE** 表示停用。</span><span class="sxs-lookup"><span data-stu-id="73bf3-306">**TRUE** to enable automatic normalization of vertex normals, or **FALSE** to disable it.</span></span> <span data-ttu-id="73bf3-307">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-307">The default value is **FALSE**.</span></span> <span data-ttu-id="73bf3-308">啟用此功能會讓系統在將頂點轉換成相機空間之後，將頂點的頂點法線正規化，而這可能會耗費大量運算時間。</span><span class="sxs-lookup"><span data-stu-id="73bf3-308">Enabling this feature causes the system to normalize the vertex normals for vertices after transforming them to camera space, which can be computationally time-consuming.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ DIFFUSEMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS\_DIFFUSEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-310">光源計算的擴散色彩來源。</span><span class="sxs-lookup"><span data-stu-id="73bf3-310">Diffuse color source for lighting calculations.</span></span> <span data-ttu-id="73bf3-311">有效的值是 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 列舉型別的成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-311">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="73bf3-312">預設值為 D3DMCS \_ COLOR1。</span><span class="sxs-lookup"><span data-stu-id="73bf3-312">The default value is D3DMCS\_COLOR1.</span></span> <span data-ttu-id="73bf3-313">只有當 D3DRS \_ COLORVERTEX 轉譯狀態設為 **TRUE** 時，才會使用此呈現狀態的值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-313">The value for this render state is used only if the D3DRS\_COLORVERTEX render state is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ SPECULARMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS\_SPECULARMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-315">光源計算的反射色彩來源。</span><span class="sxs-lookup"><span data-stu-id="73bf3-315">Specular color source for lighting calculations.</span></span> <span data-ttu-id="73bf3-316">有效的值是 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 列舉型別的成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-316">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="73bf3-317">預設值為 D3DMCS \_ COLOR2。</span><span class="sxs-lookup"><span data-stu-id="73bf3-317">The default value is D3DMCS\_COLOR2.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ AMBIENTMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS\_AMBIENTMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-319">光源計算的環境色彩來源。</span><span class="sxs-lookup"><span data-stu-id="73bf3-319">Ambient color source for lighting calculations.</span></span> <span data-ttu-id="73bf3-320">有效的值是 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 列舉型別的成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-320">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="73bf3-321">預設值為 [D3DMCS \_ 材質]。</span><span class="sxs-lookup"><span data-stu-id="73bf3-321">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ EMISSIVEMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS\_EMISSIVEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-323">光源計算的放射色彩來源。</span><span class="sxs-lookup"><span data-stu-id="73bf3-323">Emissive color source for lighting calculations.</span></span> <span data-ttu-id="73bf3-324">有效的值是 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 列舉型別的成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-324">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="73bf3-325">預設值為 [D3DMCS \_ 材質]。</span><span class="sxs-lookup"><span data-stu-id="73bf3-325">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS \_ VERTEXBLEND**</span><span class="sxs-lookup"><span data-stu-id="73bf3-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS\_VERTEXBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-327">用來執行幾何混合的矩陣數目（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="73bf3-327">Number of matrices to use to perform geometry blending, if any.</span></span> <span data-ttu-id="73bf3-328">有效的值是 [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) 列舉型別的成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-328">Valid values are members of the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="73bf3-329">預設值為 [停用] D3DVBF \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-329">The default value is D3DVBF\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS \_ CLIPPLANEENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS\_CLIPPLANEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-331">啟用或停用使用者定義裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="73bf3-331">Enables or disables user-defined clipping planes.</span></span> <span data-ttu-id="73bf3-332">有效值為任何 DWORD，其中每個位的狀態 (設定或未設定) 切換對應使用者定義裁剪平面的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="73bf3-332">Valid values are any DWORD in which the status of each bit (set or not set) toggles the activation state of a corresponding user-defined clipping plane.</span></span> <span data-ttu-id="73bf3-333">最不重要的位 (位 0) 控制位於索引0的第一個裁剪平面，而後續的位則控制較高索引的裁剪平面啟用。</span><span class="sxs-lookup"><span data-stu-id="73bf3-333">The least significant bit (bit 0) controls the first clipping plane at index 0, and subsequent bits control the activation of clipping planes at higher indexes.</span></span> <span data-ttu-id="73bf3-334">如果設定了位，系統會在場景轉譯期間套用適當的裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="73bf3-334">If a bit is set, the system applies the appropriate clipping plane during scene rendering.</span></span> <span data-ttu-id="73bf3-335">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-335">The default value is 0.</span></span>

<span data-ttu-id="73bf3-336">系統會定義 [**D3DCLIPPLANEn**](d3dclipplanen.md) 宏，以提供便利的方式來啟用裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="73bf3-336">The [**D3DCLIPPLANEn**](d3dclipplanen.md) macros are defined to provide a convenient way to enable clipping planes.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS \_ dialog**</span><span class="sxs-lookup"><span data-stu-id="73bf3-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS\_POINTSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-338">浮點值，如果未指定每個頂點的點大小，則指定用於點大小計算的大小。</span><span class="sxs-lookup"><span data-stu-id="73bf3-338">A float value that specifies the size to use for point size computation in cases where point size is not specified for each vertex.</span></span> <span data-ttu-id="73bf3-339">當頂點包含點大小時，不會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-339">This value is not used when the vertex contains point size.</span></span> <span data-ttu-id="73bf3-340">如果 D3DRS POINTSCALEENABLE 為 FALSE，則此值為螢幕空間單位 \_ ; 否則，此值會在全球空間單位中。 </span><span class="sxs-lookup"><span data-stu-id="73bf3-340">This value is in screen space units if D3DRS\_POINTSCALEENABLE is **FALSE**; otherwise this value is in world space units.</span></span> <span data-ttu-id="73bf3-341">預設值是驅動程式傳回的值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-341">The default value is the value a driver returns.</span></span> <span data-ttu-id="73bf3-342">如果驅動程式傳回0或1，則預設值為64，這可允許軟體點大小模擬。</span><span class="sxs-lookup"><span data-stu-id="73bf3-342">If a driver returns 0 or 1, the default value is 64, which allows software point size emulation.</span></span> <span data-ttu-id="73bf3-343">因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="73bf3-343">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span data-ttu-id="73bf3-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ dialog \_ MIN**</span><span class="sxs-lookup"><span data-stu-id="73bf3-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS\_POINTSIZE\_MIN**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-345">指定點基本的最小大小的 float 值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-345">A float value that specifies the minimum size of point primitives.</span></span> <span data-ttu-id="73bf3-346">在轉譯期間，點基本類型會壓制為此大小。</span><span class="sxs-lookup"><span data-stu-id="73bf3-346">Point primitives are clamped to this size during rendering.</span></span> <span data-ttu-id="73bf3-347">將此值設定為小於1.0 的值，會在點未涵蓋圖元中心時捨棄點，並停用消除鋸齒，或在啟用消除鋸齒功能時以降低濃度呈現消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="73bf3-347">Setting this to values smaller than 1.0 results in points dropping out when the point does not cover a pixel center and antialiasing is disabled or being rendered with reduced intensity when antialiasing is enabled.</span></span> <span data-ttu-id="73bf3-348">預設值為 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-348">The default value is 1.0f.</span></span> <span data-ttu-id="73bf3-349">此值的範圍大於或等於 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-349">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="73bf3-350">因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="73bf3-350">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span data-ttu-id="73bf3-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS \_ POINTSPRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS\_POINTSPRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-352">bool 值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-352">bool value.</span></span> <span data-ttu-id="73bf3-353">若 **為 TRUE**，則會設定點基本的材質座標，以便在每個點上對應完整紋理。</span><span class="sxs-lookup"><span data-stu-id="73bf3-353">When **TRUE**, texture coordinates of point primitives are set so that full textures are mapped on each point.</span></span> <span data-ttu-id="73bf3-354">若為 **FALSE**，則會將頂點材質座標用於整個點。</span><span class="sxs-lookup"><span data-stu-id="73bf3-354">When **FALSE**, the vertex texture coordinates are used for the entire point.</span></span> <span data-ttu-id="73bf3-355">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-355">The default value is **FALSE**.</span></span> <span data-ttu-id="73bf3-356">您可以將 D3DRS \_ POINTSCALEENABLE 設定為 **FALSE** ，並將 D3DRS dialog 設定為 \_ 1.0 （這是預設值），以達到 DirectX 7 樣式的單一圖元點。</span><span class="sxs-lookup"><span data-stu-id="73bf3-356">You can achieve DirectX 7 style single-pixel points by setting D3DRS\_POINTSCALEENABLE to **FALSE** and D3DRS\_POINTSIZE to 1.0, which are the default values.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ POINTSCALEENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS\_POINTSCALEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-358">此為布林值，可控制點基本的大小計算。</span><span class="sxs-lookup"><span data-stu-id="73bf3-358">bool value that controls computation of size for point primitives.</span></span> <span data-ttu-id="73bf3-359">若 **為 TRUE**，則會將點大小解釋為相機空間值，並以距離函式和等距至區 y 軸縮放比例進行調整，以計算最終的螢幕空間大小。</span><span class="sxs-lookup"><span data-stu-id="73bf3-359">When **TRUE**, the point size is interpreted as a camera space value and is scaled by the distance function and the frustum to viewport y-axis scaling to compute the final screen-space point size.</span></span> <span data-ttu-id="73bf3-360">若 **為 FALSE**，則會將點大小轉譯為螢幕空間，並直接使用。</span><span class="sxs-lookup"><span data-stu-id="73bf3-360">When **FALSE**, the point size is interpreted as screen space and used directly.</span></span> <span data-ttu-id="73bf3-361">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-361">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ POINTSCALE \_**</span><span class="sxs-lookup"><span data-stu-id="73bf3-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS\_POINTSCALE\_A**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-363">浮點值，可控制點基本的距離型大小衰減。</span><span class="sxs-lookup"><span data-stu-id="73bf3-363">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="73bf3-364">只有在 D3DRS \_ POINTSCALEENABLE 為 **TRUE** 時才會啟用。</span><span class="sxs-lookup"><span data-stu-id="73bf3-364">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="73bf3-365">預設值為 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-365">The default value is 1.0f.</span></span> <span data-ttu-id="73bf3-366">此值的範圍大於或等於 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-366">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="73bf3-367">因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="73bf3-367">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span data-ttu-id="73bf3-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ POINTSCALE \_ B**</span><span class="sxs-lookup"><span data-stu-id="73bf3-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS\_POINTSCALE\_B**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-369">浮點值，可控制點基本的距離型大小衰減。</span><span class="sxs-lookup"><span data-stu-id="73bf3-369">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="73bf3-370">只有在 D3DRS \_ POINTSCALEENABLE 為 **TRUE** 時才會啟用。</span><span class="sxs-lookup"><span data-stu-id="73bf3-370">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="73bf3-371">預設值為 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-371">The default value is 0.0f.</span></span> <span data-ttu-id="73bf3-372">此值的範圍大於或等於 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-372">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="73bf3-373">因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="73bf3-373">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span data-ttu-id="73bf3-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ POINTSCALE \_ C**</span><span class="sxs-lookup"><span data-stu-id="73bf3-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS\_POINTSCALE\_C**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-375">浮點值，可控制點基本的距離型大小衰減。</span><span class="sxs-lookup"><span data-stu-id="73bf3-375">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="73bf3-376">只有在 D3DRS \_ POINTSCALEENABLE 為 **TRUE** 時才會啟用。</span><span class="sxs-lookup"><span data-stu-id="73bf3-376">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="73bf3-377">預設值為 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-377">The default value is 0.0f.</span></span> <span data-ttu-id="73bf3-378">此值的範圍大於或等於 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-378">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="73bf3-379">因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="73bf3-379">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span data-ttu-id="73bf3-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ MULTISAMPLEANTIALIAS**</span><span class="sxs-lookup"><span data-stu-id="73bf3-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS\_MULTISAMPLEANTIALIAS**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-381">此為布林值，可決定使用多型呈現目標緩衝區時，如何計算個別樣本。</span><span class="sxs-lookup"><span data-stu-id="73bf3-381">bool value that determines how individual samples are computed when using a multisample render-target buffer.</span></span> <span data-ttu-id="73bf3-382">如果設定為 **TRUE**，則會計算多個範例，以便在每個多個範例的不同取樣位置取樣，以執行完整場景消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="73bf3-382">When set to **TRUE**, the multiple samples are computed so that full-scene antialiasing is performed by sampling at different sample positions for each multiple sample.</span></span> <span data-ttu-id="73bf3-383">當設定為 **FALSE** 時，會使用相同的樣本值寫入多個範例，在圖元中心進行取樣，以允許非反鋸齒的轉譯成多層式緩衝區。</span><span class="sxs-lookup"><span data-stu-id="73bf3-383">When set to **FALSE**, the multiple samples are all written with the same sample value, sampled at the pixel center, which allows non-antialiased rendering to a multisample buffer.</span></span> <span data-ttu-id="73bf3-384">轉譯為單一範例緩衝區時，此轉譯狀態不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="73bf3-384">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="73bf3-385">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-385">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ MULTISAMPLEMASK**</span><span class="sxs-lookup"><span data-stu-id="73bf3-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS\_MULTISAMPLEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-387">這個遮罩中的每個位（從最 (LSB) 的最小位開始）會控制多取樣轉譯目標中其中一個範例的修改。</span><span class="sxs-lookup"><span data-stu-id="73bf3-387">Each bit in this mask, starting at the least significant bit (LSB), controls modification of one of the samples in a multisample render target.</span></span> <span data-ttu-id="73bf3-388">因此，對於8樣本轉譯目標，低位元組包含八個範例的每個寫入。</span><span class="sxs-lookup"><span data-stu-id="73bf3-388">Thus, for an 8-sample render target, the low byte contains the eight write enables for each of the eight samples.</span></span> <span data-ttu-id="73bf3-389">轉譯為單一範例緩衝區時，此轉譯狀態不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="73bf3-389">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="73bf3-390">預設值為 0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="73bf3-390">The default value is 0xFFFFFFFF.</span></span>

<span data-ttu-id="73bf3-391">此轉譯狀態可讓您使用多重取樣緩衝區做為累積緩衝區，並在每次傳遞更新範例子集的情況下進行 multipass 轉譯。</span><span class="sxs-lookup"><span data-stu-id="73bf3-391">This render state enables use of a multisample buffer as an accumulation buffer, doing multipass rendering of geometry where each pass updates a subset of samples.</span></span>

<span data-ttu-id="73bf3-392">如果已啟用 n 個 multisamples 和 k 個樣本，則轉譯影像的結果濃度應該是 k/n。</span><span class="sxs-lookup"><span data-stu-id="73bf3-392">If there are n multisamples and k enabled samples, the resulting intensity of the rendered image should be k/n.</span></span> <span data-ttu-id="73bf3-393">每個圖元的每個元件 RGB 都是由 k/n 組成。</span><span class="sxs-lookup"><span data-stu-id="73bf3-393">Each component RGB of every pixel is factored by k/n.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ PATCHEDGESTYLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS\_PATCHEDGESTYLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-395">設定修補程式邊緣是否會使用 float 樣式鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="73bf3-395">Sets whether patch edges will use float style tessellation.</span></span> <span data-ttu-id="73bf3-396">可能的值是由 [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) 列舉類型所定義。</span><span class="sxs-lookup"><span data-stu-id="73bf3-396">Possible values are defined by the [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) enumerated type.</span></span> <span data-ttu-id="73bf3-397">預設值為 D3DPATCHEDGE \_ 離散。</span><span class="sxs-lookup"><span data-stu-id="73bf3-397">The default value is D3DPATCHEDGE\_DISCRETE.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS \_ DEBUGMONITORTOKEN**</span><span class="sxs-lookup"><span data-stu-id="73bf3-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS\_DEBUGMONITORTOKEN**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-399">僅針對監視進行設定。</span><span class="sxs-lookup"><span data-stu-id="73bf3-399">Set only for debugging the monitor.</span></span> <span data-ttu-id="73bf3-400">可能的值是由 [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) 列舉類型所定義。</span><span class="sxs-lookup"><span data-stu-id="73bf3-400">Possible values are defined by the [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) enumerated type.</span></span> <span data-ttu-id="73bf3-401">請注意，如果 \_ 設定了 D3DRS DEBUGMONITORTOKEN，則會將呼叫視為將權杖傳遞至「偵錯工具」監視。</span><span class="sxs-lookup"><span data-stu-id="73bf3-401">Note that if D3DRS\_DEBUGMONITORTOKEN is set, the call is treated as passing a token to the debug monitor.</span></span> <span data-ttu-id="73bf3-402">例如，如果 \_ 將 D3DDMT ENABLE 或 D3DDMT \_ DISABLE 傳遞至 D3DRS \_ DEBUGMONITORTOKEN-其他標記值會傳入，則偵錯工具的 (啟用或停用) 狀態仍會保存。</span><span class="sxs-lookup"><span data-stu-id="73bf3-402">For example, if - after passing D3DDMT\_ENABLE or D3DDMT\_DISABLE to D3DRS\_DEBUGMONITORTOKEN - other token values are passed in, the state (enabled or disabled) of the debug monitor will still persist.</span></span>

<span data-ttu-id="73bf3-403">此狀態只適用于偵錯工具組建。</span><span class="sxs-lookup"><span data-stu-id="73bf3-403">This state is only useful for debug builds.</span></span> <span data-ttu-id="73bf3-404">Debug monitor 預設為啟用 D3DDMT \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-404">The debug monitor defaults to D3DDMT\_ENABLE.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ dialog \_ MAX**</span><span class="sxs-lookup"><span data-stu-id="73bf3-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS\_POINTSIZE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-406">浮點數值，指定要壓制點 sprite 的最大大小。</span><span class="sxs-lookup"><span data-stu-id="73bf3-406">A float value that specifies the maximum size to which point sprites will be clamped.</span></span> <span data-ttu-id="73bf3-407">值必須小於或等於 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 的 MaxPointSize 成員，且大於或等於 D3DRS \_ dialog \_ MIN。</span><span class="sxs-lookup"><span data-stu-id="73bf3-407">The value must be less than or equal to the MaxPointSize member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) and greater than or equal to D3DRS\_POINTSIZE\_MIN.</span></span> <span data-ttu-id="73bf3-408">預設值為64.0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-408">The default value is 64.0.</span></span> <span data-ttu-id="73bf3-409">因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="73bf3-409">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span data-ttu-id="73bf3-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ INDEXEDVERTEXBLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS\_INDEXEDVERTEXBLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-411">啟用或停用索引頂點混合的 bool 值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-411">bool value that enables or disables indexed vertex blending.</span></span> <span data-ttu-id="73bf3-412">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-412">The default value is **FALSE**.</span></span> <span data-ttu-id="73bf3-413">如果設定為 **TRUE**，則會啟用索引頂點混色。</span><span class="sxs-lookup"><span data-stu-id="73bf3-413">When set to **TRUE**, indexed vertex blending is enabled.</span></span> <span data-ttu-id="73bf3-414">當設定為 **FALSE** 時，就會停用索引頂點的混合。</span><span class="sxs-lookup"><span data-stu-id="73bf3-414">When set to **FALSE**, indexed vertex blending is disabled.</span></span> <span data-ttu-id="73bf3-415">如果已啟用此轉譯狀態，則使用者必須傳遞矩陣索引做為每個頂點的封裝 DWORDwith。</span><span class="sxs-lookup"><span data-stu-id="73bf3-415">If this render state is enabled, the user must pass matrix indices as a packed DWORDwith every vertex.</span></span> <span data-ttu-id="73bf3-416">當轉譯狀態已停用，而且透過 D3DRS VERTEXBLEND 狀態啟用了頂點混色時 \_ ，它相當於在每個頂點中具有矩陣索引0、1、2、3。</span><span class="sxs-lookup"><span data-stu-id="73bf3-416">When the render state is disabled and vertex blending is enabled through the D3DRS\_VERTEXBLEND state, it is equivalent to having matrix indices 0, 1, 2, 3 in every vertex.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ COLORWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS\_COLORWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-418">UINT 值，可針對轉譯目標色彩緩衝區啟用每個通道的寫入。</span><span class="sxs-lookup"><span data-stu-id="73bf3-418">UINT value that enables a per-channel write for the render-target color buffer.</span></span> <span data-ttu-id="73bf3-419">設定的位會導致在3D 轉譯期間更新顏色通道。</span><span class="sxs-lookup"><span data-stu-id="73bf3-419">A set bit results in the color channel being updated during 3D rendering.</span></span> <span data-ttu-id="73bf3-420">明確的一點會導致色彩頻道不受影響。</span><span class="sxs-lookup"><span data-stu-id="73bf3-420">A clear bit results in the color channel being unaffected.</span></span> <span data-ttu-id="73bf3-421">如果在 \_ 裝置 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 PrimitiveMiscCaps 成員中設定 D3DPMISCCAPS COLORWRITEENABLE 功能位，則可以使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="73bf3-421">This functionality is available if the D3DPMISCCAPS\_COLORWRITEENABLE capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="73bf3-422">此呈現狀態不會影響清除作業。</span><span class="sxs-lookup"><span data-stu-id="73bf3-422">This render state does not affect the clear operation.</span></span> <span data-ttu-id="73bf3-423">預設值為0x0000000F。</span><span class="sxs-lookup"><span data-stu-id="73bf3-423">The default value is 0x0000000F.</span></span>

<span data-ttu-id="73bf3-424">此轉譯狀態的有效值可以是 D3DCOLORWRITEENABLE \_ ALPHA、D3DCOLORWRITEENABLE \_ BLUE、D3DCOLORWRITEENABLE \_ 綠或 D3DCOLORWRITEENABLE \_ RED 旗標的任何組合。</span><span class="sxs-lookup"><span data-stu-id="73bf3-424">Valid values for this render state can be any combination of the D3DCOLORWRITEENABLE\_ALPHA, D3DCOLORWRITEENABLE\_BLUE, D3DCOLORWRITEENABLE\_GREEN, or D3DCOLORWRITEENABLE\_RED flags.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ TWEENFACTOR**</span><span class="sxs-lookup"><span data-stu-id="73bf3-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS\_TWEENFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-426">控制補間因數的浮點值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-426">A float value that controls the tween factor.</span></span> <span data-ttu-id="73bf3-427">預設值為 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-427">The default value is 0.0f.</span></span> <span data-ttu-id="73bf3-428">因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="73bf3-428">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span data-ttu-id="73bf3-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS \_ BLENDOP**</span><span class="sxs-lookup"><span data-stu-id="73bf3-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS\_BLENDOP**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-430">當 Alpha 混色轉譯狀態（D3DRS \_ ALPHABLENDENABLE）設為 **TRUE** 時，用來選取所套用算數運算的值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-430">Value used to select the arithmetic operation applied when the alpha blending render state, D3DRS\_ALPHABLENDENABLE, is set to **TRUE**.</span></span> <span data-ttu-id="73bf3-431">有效的值是由 [**D3DBLENDOP**](./d3dblendop.md) 列舉類型所定義。</span><span class="sxs-lookup"><span data-stu-id="73bf3-431">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="73bf3-432">預設值為 D3DBLENDOP \_ ADD。</span><span class="sxs-lookup"><span data-stu-id="73bf3-432">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="73bf3-433">如果 \_ 不支援 D3DPMISCCAPS BLENDOP 裝置功能，則 \_ 會執行 D3DBLENDOP ADD。</span><span class="sxs-lookup"><span data-stu-id="73bf3-433">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ POSITIONDEGREE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS\_POSITIONDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-435">N-修補位置插補程度。</span><span class="sxs-lookup"><span data-stu-id="73bf3-435">N-patch position interpolation degree.</span></span> <span data-ttu-id="73bf3-436">值可以是 D3DDEGREE \_ 三 (預設) 或 D3DDEGREE \_ 線性。</span><span class="sxs-lookup"><span data-stu-id="73bf3-436">The values can be D3DDEGREE\_CUBIC (default) or D3DDEGREE\_LINEAR.</span></span> <span data-ttu-id="73bf3-437">如需詳細資訊，請參閱 [**D3DDEGREETYPE**](./d3ddegreetype.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-437">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ NORMALDEGREE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS\_NORMALDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-439">N-修補正常插補的程度。</span><span class="sxs-lookup"><span data-stu-id="73bf3-439">N-patch normal interpolation degree.</span></span> <span data-ttu-id="73bf3-440">值可以是 D3DDEGREE \_ 線性 (預設) 或 D3DDEGREE \_ 二次。</span><span class="sxs-lookup"><span data-stu-id="73bf3-440">The values can be D3DDEGREE\_LINEAR (default) or D3DDEGREE\_QUADRATIC.</span></span> <span data-ttu-id="73bf3-441">如需詳細資訊，請參閱 [**D3DDEGREETYPE**](./d3ddegreetype.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-441">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ SCISSORTESTENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS\_SCISSORTESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-443">**TRUE** 表示啟用剪式測試，而 **FALSE** 則會停用。</span><span class="sxs-lookup"><span data-stu-id="73bf3-443">**TRUE** to enable scissor testing and **FALSE** to disable it.</span></span> <span data-ttu-id="73bf3-444">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-444">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ SLOPESCALEDEPTHBIAS**</span><span class="sxs-lookup"><span data-stu-id="73bf3-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS\_SLOPESCALEDEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-446">用來決定要將多少偏差套用至共同平面基本專案，以減少 z 減少。</span><span class="sxs-lookup"><span data-stu-id="73bf3-446">Used to determine how much bias can be applied to co-planar primitives to reduce z-fighting.</span></span> <span data-ttu-id="73bf3-447">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-447">The default value is 0.</span></span>

<span data-ttu-id="73bf3-448">偏差 = (max \* D3DRS \_ SLOPESCALEDEPTHBIAS) + D3DRS \_ DEPTHBIAS。</span><span class="sxs-lookup"><span data-stu-id="73bf3-448">bias = (max \* D3DRS\_SLOPESCALEDEPTHBIAS) + D3DRS\_DEPTHBIAS.</span></span>

<span data-ttu-id="73bf3-449">其中 max 是所呈現三角形的最大深度斜率。</span><span class="sxs-lookup"><span data-stu-id="73bf3-449">where max is the maximum depth slope of the triangle being rendered.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS\_ANTIALIASEDLINEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-451">**TRUE** 表示啟用行消除鋸齒， **FALSE** 可停用行消除鋸齒功能。</span><span class="sxs-lookup"><span data-stu-id="73bf3-451">**TRUE** to enable line antialiasing, **FALSE** to disable line antialiasing.</span></span> <span data-ttu-id="73bf3-452">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-452">The default value is **FALSE**.</span></span>

<span data-ttu-id="73bf3-453">當轉譯為多取樣轉譯目標時， \_ 會忽略 D3DRS ANTIALIASEDLINEENABLE，並將所有的行呈現為別名。</span><span class="sxs-lookup"><span data-stu-id="73bf3-453">When rendering to a multisample render target, D3DRS\_ANTIALIASEDLINEENABLE is ignored and all lines are rendered aliased.</span></span> <span data-ttu-id="73bf3-454">在多重取樣轉譯目標中使用 [**ID3DXLine**](id3dxline.md) 來呈現反鋸齒線條。</span><span class="sxs-lookup"><span data-stu-id="73bf3-454">Use [**ID3DXLine**](id3dxline.md) for antialiased line rendering in a multisample render target.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ MINTESSELLATIONLEVEL**</span><span class="sxs-lookup"><span data-stu-id="73bf3-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS\_MINTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-456">最小鑲嵌層級。</span><span class="sxs-lookup"><span data-stu-id="73bf3-456">Minimum tessellation level.</span></span> <span data-ttu-id="73bf3-457">預設值為 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-457">The default value is 1.0f.</span></span> <span data-ttu-id="73bf3-458">請參閱 [鑲嵌式 (Direct3D 9) ](tessellation.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-458">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ MAXTESSELLATIONLEVEL**</span><span class="sxs-lookup"><span data-stu-id="73bf3-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS\_MAXTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-460">最大鑲嵌層級。</span><span class="sxs-lookup"><span data-stu-id="73bf3-460">Maximum tessellation level.</span></span> <span data-ttu-id="73bf3-461">預設值為 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-461">The default value is 1.0f.</span></span> <span data-ttu-id="73bf3-462">請參閱 [鑲嵌式 (Direct3D 9) ](tessellation.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-462">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ ADAPTIVETESS \_ X**</span><span class="sxs-lookup"><span data-stu-id="73bf3-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS\_ADAPTIVETESS\_X**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-464">以 x 方向 tessellate 的自我調整數量。</span><span class="sxs-lookup"><span data-stu-id="73bf3-464">Amount to adaptively tessellate, in the x direction.</span></span> <span data-ttu-id="73bf3-465">預設值為 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-465">Default value is 0.0f.</span></span> <span data-ttu-id="73bf3-466">請參閱 [適應性鑲嵌](tessellation.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-466">See [Adaptive Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ ADAPTIVETESS \_ Y**</span><span class="sxs-lookup"><span data-stu-id="73bf3-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS\_ADAPTIVETESS\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-468">以 y 方向 tessellate 的數量。</span><span class="sxs-lookup"><span data-stu-id="73bf3-468">Amount to adaptively tessellate, in the y direction.</span></span> <span data-ttu-id="73bf3-469">預設值為 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-469">Default value is 0.0f.</span></span> <span data-ttu-id="73bf3-470">請參閱 [適應性 \_ 鑲嵌](tessellation.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-470">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ ADAPTIVETESS \_ Z**</span><span class="sxs-lookup"><span data-stu-id="73bf3-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS\_ADAPTIVETESS\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-472">依 z 方向的 tessellate 量。</span><span class="sxs-lookup"><span data-stu-id="73bf3-472">Amount to adaptively tessellate, in the z direction.</span></span> <span data-ttu-id="73bf3-473">預設值為 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-473">Default value is 1.0f.</span></span> <span data-ttu-id="73bf3-474">請參閱 [適應性 \_ 鑲嵌](tessellation.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-474">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ ADAPTIVETESS \_ W**</span><span class="sxs-lookup"><span data-stu-id="73bf3-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS\_ADAPTIVETESS\_W**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-476">依 w 方向的 tessellate 量。</span><span class="sxs-lookup"><span data-stu-id="73bf3-476">Amount to adaptively tessellate, in the w direction.</span></span> <span data-ttu-id="73bf3-477">預設值為 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-477">Default value is 0.0f.</span></span> <span data-ttu-id="73bf3-478">請參閱 [適應性 \_ 鑲嵌](tessellation.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-478">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ ENABLEADAPTIVETESSELLATION**</span><span class="sxs-lookup"><span data-stu-id="73bf3-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS\_ENABLEADAPTIVETESSELLATION**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-480">**TRUE** 表示啟用調適型鑲嵌， **FALSE** 則停用。</span><span class="sxs-lookup"><span data-stu-id="73bf3-480">**TRUE** to enable adaptive tessellation, **FALSE** to disable it.</span></span> <span data-ttu-id="73bf3-481">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-481">The default value is **FALSE**.</span></span> <span data-ttu-id="73bf3-482">請參閱 [適應性 \_ 鑲嵌](tessellation.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-482">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ TWOSIDEDSTENCILMODE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS\_TWOSIDEDSTENCILMODE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-484">**TRUE** 會啟用雙面 Stenciling， **FALSE** 會停用它。</span><span class="sxs-lookup"><span data-stu-id="73bf3-484">**TRUE** enables two-sided stenciling, **FALSE** disables it.</span></span> <span data-ttu-id="73bf3-485">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-485">The default value is **FALSE**.</span></span> <span data-ttu-id="73bf3-486">應用程式應該將 D3DRS \_ CULLMODE 設定為 D3DCULL \_ NONE，以啟用雙面樣板模式。</span><span class="sxs-lookup"><span data-stu-id="73bf3-486">The application should set D3DRS\_CULLMODE to D3DCULL\_NONE to enable two-sided stencil mode.</span></span> <span data-ttu-id="73bf3-487">如果三角形的纏繞順序是順時針的， \_ 則 \* 會使用 D3DRS 樣板作業。</span><span class="sxs-lookup"><span data-stu-id="73bf3-487">If the triangle winding order is clockwise, the D3DRS\_STENCIL\* operations will be used.</span></span> <span data-ttu-id="73bf3-488">如果是逆時針順序，則 \_ 會使用 D3DRS CCW \_ 樣板 \* 作業。</span><span class="sxs-lookup"><span data-stu-id="73bf3-488">If the winding order is counterclockwise, the D3DRS\_CCW\_STENCIL\* operations will be used.</span></span>

<span data-ttu-id="73bf3-489">若要查看是否支援雙面樣板，請檢查 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) for D3DSTENCILCAPS TWOSIDED 的 StencilCaps 成員 \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-489">To see if two-sided stencil is supported, check the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) for D3DSTENCILCAPS\_TWOSIDED.</span></span> <span data-ttu-id="73bf3-490">另請參閱 [D3DSTENCILCAPS](d3dstencilcaps.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-490">See also [D3DSTENCILCAPS](d3dstencilcaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ STENCILFAIL**</span><span class="sxs-lookup"><span data-stu-id="73bf3-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS\_CCW\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-492">如果 CCW 樣板測試失敗，則為要執行的樣板運算。</span><span class="sxs-lookup"><span data-stu-id="73bf3-492">Stencil operation to perform if CCW stencil test fails.</span></span> <span data-ttu-id="73bf3-493">值是來自 [**D3DSTENCILOP**](./d3dstencilop.md) 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="73bf3-493">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="73bf3-494">預設值為 [保留] D3DSTENCILOP \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-494">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ STENCILZFAIL**</span><span class="sxs-lookup"><span data-stu-id="73bf3-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS\_CCW\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-496">如果 CCW 樣板測試通過和 z 測試失敗，要執行的樣板作業。</span><span class="sxs-lookup"><span data-stu-id="73bf3-496">Stencil operation to perform if CCW stencil test passes and z-test fails.</span></span> <span data-ttu-id="73bf3-497">值是來自 [**D3DSTENCILOP**](./d3dstencilop.md) 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="73bf3-497">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="73bf3-498">預設值為 [保留] D3DSTENCILOP \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-498">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ STENCILPASS**</span><span class="sxs-lookup"><span data-stu-id="73bf3-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS\_CCW\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-500">當 CCW 樣板和 z 測試都通過時，要執行的樣板作業。</span><span class="sxs-lookup"><span data-stu-id="73bf3-500">Stencil operation to perform if both CCW stencil and z-tests pass.</span></span> <span data-ttu-id="73bf3-501">值是來自 [**D3DSTENCILOP**](./d3dstencilop.md) 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="73bf3-501">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="73bf3-502">預設值為 [保留] D3DSTENCILOP \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-502">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ STENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="73bf3-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS\_CCW\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-504">比較函數。</span><span class="sxs-lookup"><span data-stu-id="73bf3-504">The comparison function.</span></span> <span data-ttu-id="73bf3-505">如果 ( (ref & mask) 樣板函式 (樣板 & mask) ) 為 **TRUE**，則會通過 CCW 樣板測試。</span><span class="sxs-lookup"><span data-stu-id="73bf3-505">CCW stencil test passes if ((ref & mask) stencil function (stencil & mask)) is **TRUE**.</span></span> <span data-ttu-id="73bf3-506">值是來自 [**D3DCMPFUNC**](./d3dcmpfunc.md) 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="73bf3-506">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="73bf3-507">預設值為 [永遠 D3DCMP] \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-507">The default value is D3DCMP\_ALWAYS.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**</span><span class="sxs-lookup"><span data-stu-id="73bf3-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS\_COLORWRITEENABLE1**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-509">裝置的其他 ColorWriteEnable 值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-509">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="73bf3-510">請參閱 D3DRS \_ COLORWRITEENABLE。</span><span class="sxs-lookup"><span data-stu-id="73bf3-510">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="73bf3-511">如果在 \_ 裝置 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 PrimitiveMiscCaps 成員中設定 D3DPMISCCAPS INDEPENDENTWRITEMASKS 功能位，則可以使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="73bf3-511">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="73bf3-512">預設值為0x0000000f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-512">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**</span><span class="sxs-lookup"><span data-stu-id="73bf3-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS\_COLORWRITEENABLE2**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-514">裝置的其他 ColorWriteEnable 值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-514">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="73bf3-515">請參閱 D3DRS \_ COLORWRITEENABLE。</span><span class="sxs-lookup"><span data-stu-id="73bf3-515">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="73bf3-516">如果在 \_ 裝置 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 PrimitiveMiscCaps 成員中設定 D3DPMISCCAPS INDEPENDENTWRITEMASKS 功能位，則可以使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="73bf3-516">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="73bf3-517">預設值為0x0000000f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-517">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**</span><span class="sxs-lookup"><span data-stu-id="73bf3-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS\_COLORWRITEENABLE3**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-519">裝置的其他 ColorWriteEnable 值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-519">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="73bf3-520">請參閱 D3DRS \_ COLORWRITEENABLE。</span><span class="sxs-lookup"><span data-stu-id="73bf3-520">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="73bf3-521">如果在 \_ 裝置 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 PrimitiveMiscCaps 成員中設定 D3DPMISCCAPS INDEPENDENTWRITEMASKS 功能位，則可以使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="73bf3-521">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="73bf3-522">預設值為0x0000000f。</span><span class="sxs-lookup"><span data-stu-id="73bf3-522">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ BLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="73bf3-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-524">[**D3DCOLOR**](d3dcolor.md) 用於 Alpha 混合期間的常數 blend 因素。</span><span class="sxs-lookup"><span data-stu-id="73bf3-524">[**D3DCOLOR**](d3dcolor.md) used for a constant blend-factor during alpha blending.</span></span> <span data-ttu-id="73bf3-525">如果 D3DPBLENDCAPS \_ BLENDFACTOR 功能位是在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 的 SrcBlendCaps 成員或 **DestBlendCaps** 的 D3DCAPS9 成員中設定，就可以使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="73bf3-525">This functionality is available if the D3DPBLENDCAPS\_BLENDFACTOR capabilities bit is set in the SrcBlendCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) or the DestBlendCaps member of **D3DCAPS9**.</span></span> <span data-ttu-id="73bf3-526">請參閱 [**D3DRENDERSTATETYPE**]()。</span><span class="sxs-lookup"><span data-stu-id="73bf3-526">See [**D3DRENDERSTATETYPE**]().</span></span> <span data-ttu-id="73bf3-527">預設值為0xffffffff。</span><span class="sxs-lookup"><span data-stu-id="73bf3-527">The default value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ SRGBWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS\_SRGBWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-529">啟用轉譯目標寫入，以將 gamma 更正為 sRGB。</span><span class="sxs-lookup"><span data-stu-id="73bf3-529">Enable render-target writes to be gamma corrected to sRGB.</span></span> <span data-ttu-id="73bf3-530">格式必須公開 D3DUSAGE \_ SRGBWRITE。</span><span class="sxs-lookup"><span data-stu-id="73bf3-530">The format must expose D3DUSAGE\_SRGBWRITE.</span></span> <span data-ttu-id="73bf3-531">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-531">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ DEPTHBIAS**</span><span class="sxs-lookup"><span data-stu-id="73bf3-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS\_DEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-533">用來比較深度值的浮點值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-533">A floating-point value that is used for comparison of depth values.</span></span> <span data-ttu-id="73bf3-534">請參閱 [ (Direct3D 9) 的深度偏差 ](depth-bias.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-534">See [Depth Bias (Direct3D 9)](depth-bias.md).</span></span> <span data-ttu-id="73bf3-535">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-535">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**</span><span class="sxs-lookup"><span data-stu-id="73bf3-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS\_WRAP8**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-537">請參閱 D3DRS \_ WRAP0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-537">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**</span><span class="sxs-lookup"><span data-stu-id="73bf3-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS\_WRAP9**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-539">請參閱 D3DRS \_ WRAP0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-539">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**</span><span class="sxs-lookup"><span data-stu-id="73bf3-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS\_WRAP10**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-541">請參閱 D3DRS \_ WRAP0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-541">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**</span><span class="sxs-lookup"><span data-stu-id="73bf3-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS\_WRAP11**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-543">請參閱 D3DRS \_ WRAP0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-543">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**</span><span class="sxs-lookup"><span data-stu-id="73bf3-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS\_WRAP12**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-545">請參閱 D3DRS \_ WRAP0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-545">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**</span><span class="sxs-lookup"><span data-stu-id="73bf3-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS\_WRAP13**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-547">請參閱 D3DRS \_ WRAP0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-547">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**</span><span class="sxs-lookup"><span data-stu-id="73bf3-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS\_WRAP14**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-549">請參閱 D3DRS \_ WRAP0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-549">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**</span><span class="sxs-lookup"><span data-stu-id="73bf3-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS\_WRAP15**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-551">請參閱 D3DRS \_ WRAP0。</span><span class="sxs-lookup"><span data-stu-id="73bf3-551">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ SEPARATEALPHABLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="73bf3-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS\_SEPARATEALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-553">**TRUE** 會啟用 Alpha 色板的不同 blend 模式。</span><span class="sxs-lookup"><span data-stu-id="73bf3-553">**TRUE** enables the separate blend mode for the alpha channel.</span></span> <span data-ttu-id="73bf3-554">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73bf3-554">The default value is **FALSE**.</span></span>

<span data-ttu-id="73bf3-555">當設定為 **FALSE** 時，會強制將套用至 Alpha 的轉譯目標混色因數和作業與針對色彩定義的相同。</span><span class="sxs-lookup"><span data-stu-id="73bf3-555">When set to **FALSE**, the render-target blending factors and operations applied to alpha are forced to be the same as those defined for color.</span></span> <span data-ttu-id="73bf3-556">在未設定 cap D3DPMISCCAPS SEPARATEALPHABLEND 的實執行上，此模式實際上會寫死為 **FALSE** \_ 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-556">This mode is effectively hardwired to **FALSE** on implementations that don't set the cap D3DPMISCCAPS\_SEPARATEALPHABLEND.</span></span> <span data-ttu-id="73bf3-557">請參閱 [D3DPMISCCAPS](d3dpmisccaps.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-557">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

<span data-ttu-id="73bf3-558">個別 Alpha 混色的類型取決於 D3DRS \_ SRCBLENDALPHA 和 D3DRS \_ DESTBLENDALPHA 轉譯狀態。</span><span class="sxs-lookup"><span data-stu-id="73bf3-558">The type of separate alpha blending is determined by the D3DRS\_SRCBLENDALPHA and D3DRS\_DESTBLENDALPHA render states.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ SRCBLENDALPHA**</span><span class="sxs-lookup"><span data-stu-id="73bf3-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS\_SRCBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-560">[**D3DBLEND**](./d3dblend.md)列舉型別的其中一個成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-560">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="73bf3-561">除非 D3DRS \_ SEPARATEALPHABLENDENABLE 為 **TRUE**，否則會忽略此值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-561">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="73bf3-562">預設值為 D3DBLEND \_ 一個。</span><span class="sxs-lookup"><span data-stu-id="73bf3-562">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ DESTBLENDALPHA**</span><span class="sxs-lookup"><span data-stu-id="73bf3-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS\_DESTBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-564">[**D3DBLEND**](./d3dblend.md)列舉型別的其中一個成員。</span><span class="sxs-lookup"><span data-stu-id="73bf3-564">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="73bf3-565">除非 D3DRS \_ SEPARATEALPHABLENDENABLE 為 **TRUE**，否則會忽略此值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-565">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="73bf3-566">預設值為 D3DBLEND \_ 零。</span><span class="sxs-lookup"><span data-stu-id="73bf3-566">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ BLENDOPALPHA**</span><span class="sxs-lookup"><span data-stu-id="73bf3-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS\_BLENDOPALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-568">當轉譯狀態（D3DRS \_ SEPARATEALPHABLENDENABLE）設為 **TRUE** 時，用來選取套用至個別 Alpha 混色之算數運算的值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-568">Value used to select the arithmetic operation applied to separate alpha blending when the render state, D3DRS\_SEPARATEALPHABLENDENABLE, is set to **TRUE**.</span></span>

<span data-ttu-id="73bf3-569">有效的值是由 [**D3DBLENDOP**](./d3dblendop.md) 列舉類型所定義。</span><span class="sxs-lookup"><span data-stu-id="73bf3-569">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="73bf3-570">預設值為 D3DBLENDOP \_ ADD。</span><span class="sxs-lookup"><span data-stu-id="73bf3-570">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="73bf3-571">如果 \_ 不支援 D3DPMISCCAPS BLENDOP 裝置功能，則 \_ 會執行 D3DBLENDOP ADD。</span><span class="sxs-lookup"><span data-stu-id="73bf3-571">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span> <span data-ttu-id="73bf3-572">請參閱 [D3DPMISCCAPS](d3dpmisccaps.md)。</span><span class="sxs-lookup"><span data-stu-id="73bf3-572">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bf3-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="73bf3-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="73bf3-574">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="73bf3-574">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="73bf3-575">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="73bf3-575">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="73bf3-576">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="73bf3-576">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73bf3-577">備註</span><span class="sxs-lookup"><span data-stu-id="73bf3-577">Remarks</span></span>



| <span data-ttu-id="73bf3-578">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="73bf3-578">Render states</span></span>        |   <span data-ttu-id="73bf3-579">紋理取樣器</span><span class="sxs-lookup"><span data-stu-id="73bf3-579">Texture sampler</span></span>                 |
|----------------------|--------------------|
| <span data-ttu-id="73bf3-580">ps \_ 1 \_ 1 到 ps \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="73bf3-580">ps\_1\_1 to ps\_1\_3</span></span> | <span data-ttu-id="73bf3-581">4紋理取樣器</span><span class="sxs-lookup"><span data-stu-id="73bf3-581">4 texture samplers</span></span> |



 

<span data-ttu-id="73bf3-582">Direct3D 定義了 D3DRENDERSTATE \_ WRAPBIAS 常數，方便讓應用程式根據紋理座標集的以零為起始的整數來啟用或停用材質換行 (而不是明確地使用其中一個 D3DRS \_ WRAP n 狀態值) 。</span><span class="sxs-lookup"><span data-stu-id="73bf3-582">Direct3D defines the D3DRENDERSTATE\_WRAPBIAS constant as a convenience for applications to enable or disable texture wrapping, based on the zero-based integer of a texture coordinate set (rather than explicitly using one of the D3DRS\_WRAP n state values).</span></span> <span data-ttu-id="73bf3-583">將 D3DRENDERSTATE \_ WRAPBIAS 值新增至材質座標集的以零為起始的索引，以計算 \_ 對應至該索引的 D3DRS 換行 n 值，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="73bf3-583">Add the D3DRENDERSTATE\_WRAPBIAS value to the zero-based index of a texture coordinate set to calculate the D3DRS\_WRAP n value that corresponds to that index, as shown in the following example.</span></span>


```
// Enable U/V wrapping for textures that use the texture 
// coordinate set at the index within the dwIndex variable
    
HRESULT hr = pd3dDevice->SetRenderState(
dwIndex + D3DRENDERSTATE_WRAPBIAS,  
D3DWRAPCOORD_0 | D3DWRAPCOORD_1);
     
// If dwIndex is 3, the value that results from 
// the addition equals D3DRS_WRAP3 (131)
```



## <a name="requirements"></a><span data-ttu-id="73bf3-584">規格需求</span><span class="sxs-lookup"><span data-stu-id="73bf3-584">Requirements</span></span>



| <span data-ttu-id="73bf3-585">需求</span><span class="sxs-lookup"><span data-stu-id="73bf3-585">Requirement</span></span> | <span data-ttu-id="73bf3-586">值</span><span class="sxs-lookup"><span data-stu-id="73bf3-586">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73bf3-587">標頭</span><span class="sxs-lookup"><span data-stu-id="73bf3-587">Header</span></span><br/> | <dl> <span data-ttu-id="73bf3-588"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="73bf3-588"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73bf3-589">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73bf3-589">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73bf3-590">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="73bf3-590">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="73bf3-591">**IDirect3DDevice9::GetRenderState**</span><span class="sxs-lookup"><span data-stu-id="73bf3-591">**IDirect3DDevice9::GetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[<span data-ttu-id="73bf3-592">**IDirect3DDevice9::SetRenderState**</span><span class="sxs-lookup"><span data-stu-id="73bf3-592">**IDirect3DDevice9::SetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 

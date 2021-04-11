---
description: 材質階段狀態會定義多 blender 材質作業。
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: 'D3DTEXTURESTAGESTATETYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURESTAGESTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0530f428c9ebf89607fa89509c65ddd336fee293
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196223"
---
# <a name="d3dtexturestagestatetype-enumeration"></a><span data-ttu-id="c791b-103">D3DTEXTURESTAGESTATETYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="c791b-103">D3DTEXTURESTAGESTATETYPE enumeration</span></span>

<span data-ttu-id="c791b-104">材質階段狀態會定義多 blender 材質作業。</span><span class="sxs-lookup"><span data-stu-id="c791b-104">Texture stage states define multi-blender texture operations.</span></span> <span data-ttu-id="c791b-105">某些取樣器狀態會設定頂點處理，以及某些設定的圖元處理。</span><span class="sxs-lookup"><span data-stu-id="c791b-105">Some sampler states set up vertex processing, and some set up pixel processing.</span></span> <span data-ttu-id="c791b-106">您可以使用 stateblocks 來儲存和還原材質階段狀態 (請參閱 [ (Direct3D 9) ) 的狀態欄塊儲存和還原狀態 ](state-blocks-save-and-restore-state.md) 。</span><span class="sxs-lookup"><span data-stu-id="c791b-106">Texture stage states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="c791b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c791b-107">Syntax</span></span>


```C++
typedef enum D3DTEXTURESTAGESTATETYPE { 
  D3DTSS_COLOROP                = 1,
  D3DTSS_COLORARG1              = 2,
  D3DTSS_COLORARG2              = 3,
  D3DTSS_ALPHAOP                = 4,
  D3DTSS_ALPHAARG1              = 5,
  D3DTSS_ALPHAARG2              = 6,
  D3DTSS_BUMPENVMAT00           = 7,
  D3DTSS_BUMPENVMAT01           = 8,
  D3DTSS_BUMPENVMAT10           = 9,
  D3DTSS_BUMPENVMAT11           = 10,
  D3DTSS_TEXCOORDINDEX          = 11,
  D3DTSS_BUMPENVLSCALE          = 22,
  D3DTSS_BUMPENVLOFFSET         = 23,
  D3DTSS_TEXTURETRANSFORMFLAGS  = 24,
  D3DTSS_COLORARG0              = 26,
  D3DTSS_ALPHAARG0              = 27,
  D3DTSS_RESULTARG              = 28,
  D3DTSS_CONSTANT               = 32,
  D3DTSS_FORCE_DWORD            = 0x7fffffff
} D3DTEXTURESTAGESTATETYPE, *LPD3DTEXTURESTAGESTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="c791b-108">常數</span><span class="sxs-lookup"><span data-stu-id="c791b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c791b-109"><span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS \_ COLOROP**</span><span class="sxs-lookup"><span data-stu-id="c791b-109"><span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS\_COLOROP**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-110">材質階段狀態是由 [**D3DTEXTUREOP**](./d3dtextureop.md) 列舉型別之一成員所識別的材質色彩混合作業。</span><span class="sxs-lookup"><span data-stu-id="c791b-110">Texture-stage state is a texture color blending operation identified by one member of the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span> <span data-ttu-id="c791b-111">第一個材質階段的預設值 (階段 0) 是 D3DTOP \_ lambert; 針對所有其他階段，預設值為 D3DTOP \_ DISABLE。</span><span class="sxs-lookup"><span data-stu-id="c791b-111">The default value for the first texture stage (stage 0) is D3DTOP\_MODULATE; for all other stages the default is D3DTOP\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="c791b-112"><span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS \_ COLORARG1**</span><span class="sxs-lookup"><span data-stu-id="c791b-112"><span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS\_COLORARG1**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-113">材質階段狀態是階段的第一個色彩引數，由其中一個 [D3DTA](d3dta.md)來識別。</span><span class="sxs-lookup"><span data-stu-id="c791b-113">Texture-stage state is the first color argument for the stage, identified by one of the [D3DTA](d3dta.md).</span></span> <span data-ttu-id="c791b-114">預設引數為 D3DTA \_ 材質。</span><span class="sxs-lookup"><span data-stu-id="c791b-114">The default argument is D3DTA\_TEXTURE.</span></span>

<span data-ttu-id="c791b-115">指定 D3DTA \_ TEMP 以選取用於讀取或寫入的臨時暫存器色彩。</span><span class="sxs-lookup"><span data-stu-id="c791b-115">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="c791b-116">\_如果 \_ 有 D3DPMISCCAPS TSSARGTEMP 裝置功能，則支援 D3DTA TEMP。</span><span class="sxs-lookup"><span data-stu-id="c791b-116">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="c791b-117">註冊的預設值是 (0.0、0.0、0.0、0.0) 。</span><span class="sxs-lookup"><span data-stu-id="c791b-117">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="c791b-118"><span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS \_ COLORARG2**</span><span class="sxs-lookup"><span data-stu-id="c791b-118"><span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS\_COLORARG2**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-119">材質階段狀態是階段的第二個色彩引數，由 [D3DTA](d3dta.md)識別。</span><span class="sxs-lookup"><span data-stu-id="c791b-119">Texture-stage state is the second color argument for the stage, identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="c791b-120">預設引數為 D3DTA \_ CURRENT。</span><span class="sxs-lookup"><span data-stu-id="c791b-120">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="c791b-121">指定 D3DTA \_ TEMP 以選取用於讀取或寫入的臨時暫存器色彩。</span><span class="sxs-lookup"><span data-stu-id="c791b-121">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="c791b-122">\_如果 \_ 有 D3DPMISCCAPS TSSARGTEMP 裝置功能，則支援 D3DTA TEMP。</span><span class="sxs-lookup"><span data-stu-id="c791b-122">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="c791b-123">註冊的預設值是 (0.0、0.0、0.0、0.0) </span><span class="sxs-lookup"><span data-stu-id="c791b-123">The default value for the register is (0.0, 0.0, 0.0, 0.0)</span></span>

</dd> <dt>

<span data-ttu-id="c791b-124"><span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS \_ ALPHAOP**</span><span class="sxs-lookup"><span data-stu-id="c791b-124"><span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS\_ALPHAOP**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-125">材質階段狀態是由 [**D3DTEXTUREOP**](./d3dtextureop.md) 列舉型別之一成員所識別的材質 Alpha 混色運算。</span><span class="sxs-lookup"><span data-stu-id="c791b-125">Texture-stage state is a texture alpha blending operation identified by one member of the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span> <span data-ttu-id="c791b-126">第一個材質階段的預設值 (階段 0) 是 D3DTOP \_ SELECTARG1，而針對所有其他階段，預設值為 D3DTOP \_ DISABLE。</span><span class="sxs-lookup"><span data-stu-id="c791b-126">The default value for the first texture stage (stage 0) is D3DTOP\_SELECTARG1, and for all other stages the default is D3DTOP\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="c791b-127"><span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS \_ ALPHAARG1**</span><span class="sxs-lookup"><span data-stu-id="c791b-127"><span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS\_ALPHAARG1**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-128">材質階段狀態是此階段的第一個 Alpha 引數，由 [D3DTA](d3dta.md)所識別。</span><span class="sxs-lookup"><span data-stu-id="c791b-128">Texture-stage state is the first alpha argument for the stage, identified by by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="c791b-129">預設引數為 D3DTA \_ 材質。</span><span class="sxs-lookup"><span data-stu-id="c791b-129">The default argument is D3DTA\_TEXTURE.</span></span> <span data-ttu-id="c791b-130">如果未針對這個階段設定材質，則預設引數為 D3DTA \_ 擴散。</span><span class="sxs-lookup"><span data-stu-id="c791b-130">If no texture is set for this stage, the default argument is D3DTA\_DIFFUSE.</span></span> <span data-ttu-id="c791b-131">指定 D3DTA \_ TEMP 以選取用於讀取或寫入的臨時暫存器色彩。</span><span class="sxs-lookup"><span data-stu-id="c791b-131">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="c791b-132">\_如果 \_ 有 D3DPMISCCAPS TSSARGTEMP 裝置功能，則支援 D3DTA TEMP。</span><span class="sxs-lookup"><span data-stu-id="c791b-132">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="c791b-133">註冊的預設值是 (0.0、0.0、0.0、0.0) 。</span><span class="sxs-lookup"><span data-stu-id="c791b-133">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="c791b-134"><span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS \_ ALPHAARG2**</span><span class="sxs-lookup"><span data-stu-id="c791b-134"><span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS\_ALPHAARG2**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-135">材質階段狀態是階段的第二個 Alpha 引數，由 [D3DTA](d3dta.md)所識別。</span><span class="sxs-lookup"><span data-stu-id="c791b-135">Texture-stage state is the second alpha argument for the stage, identified by by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="c791b-136">預設引數為 D3DTA \_ CURRENT。</span><span class="sxs-lookup"><span data-stu-id="c791b-136">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="c791b-137">指定 D3DTA \_ TEMP 以選取用於讀取或寫入的臨時暫存器色彩。</span><span class="sxs-lookup"><span data-stu-id="c791b-137">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="c791b-138">\_如果 \_ 有 D3DPMISCCAPS TSSARGTEMP 裝置功能，則支援 D3DTA TEMP。</span><span class="sxs-lookup"><span data-stu-id="c791b-138">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="c791b-139">註冊的預設值是 (0.0、0.0、0.0、0.0) 。</span><span class="sxs-lookup"><span data-stu-id="c791b-139">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="c791b-140"><span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS \_ BUMPENVMAT00**</span><span class="sxs-lookup"><span data-stu-id="c791b-140"><span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS\_BUMPENVMAT00**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-141">材質階段狀態是浮動 \[ \] \[ \] 對應矩陣中 0 0 係數的浮點值。</span><span class="sxs-lookup"><span data-stu-id="c791b-141">Texture-stage state is a floating-point value for the \[0\]\[0\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="c791b-142">預設值為 0.0。</span><span class="sxs-lookup"><span data-stu-id="c791b-142">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="c791b-143"><span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS \_ BUMPENVMAT01**</span><span class="sxs-lookup"><span data-stu-id="c791b-143"><span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS\_BUMPENVMAT01**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-144">材質階段狀態是浮動 \[ \] \[ \] 對應矩陣中 0 1 係數的浮點值。</span><span class="sxs-lookup"><span data-stu-id="c791b-144">Texture-stage state is a floating-point value for the \[0\]\[1\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="c791b-145">預設值為 0.0。</span><span class="sxs-lookup"><span data-stu-id="c791b-145">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="c791b-146"><span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS \_ BUMPENVMAT10**</span><span class="sxs-lookup"><span data-stu-id="c791b-146"><span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS\_BUMPENVMAT10**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-147">材質階段狀態是浮動 \[ \] \[ \] 對應矩陣中的 1 0 係數的浮點值。</span><span class="sxs-lookup"><span data-stu-id="c791b-147">Texture-stage state is a floating-point value for the \[1\]\[0\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="c791b-148">預設值為 0.0。</span><span class="sxs-lookup"><span data-stu-id="c791b-148">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="c791b-149"><span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS \_ BUMPENVMAT11**</span><span class="sxs-lookup"><span data-stu-id="c791b-149"><span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS\_BUMPENVMAT11**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-150">材質階段狀態是浮動 \[ \] \[ \] 對應矩陣中1個係數的浮點值。</span><span class="sxs-lookup"><span data-stu-id="c791b-150">Texture-stage state is a floating-point value for the \[1\]\[1\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="c791b-151">預設值為 0.0。</span><span class="sxs-lookup"><span data-stu-id="c791b-151">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="c791b-152"><span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS \_ TEXCOORDINDEX**</span><span class="sxs-lookup"><span data-stu-id="c791b-152"><span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS\_TEXCOORDINDEX**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-153">要搭配此材質階段使用之材質座標集的索引。</span><span class="sxs-lookup"><span data-stu-id="c791b-153">Index of the texture coordinate set to use with this texture stage.</span></span> <span data-ttu-id="c791b-154">您最多可以為每個頂點指定八組紋理座標。</span><span class="sxs-lookup"><span data-stu-id="c791b-154">You can specify up to eight sets of texture coordinates per vertex.</span></span> <span data-ttu-id="c791b-155">如果頂點未在指定的索引中包含一組紋理座標，系統就會預設為您和 v 座標 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="c791b-155">If a vertex does not include a set of texture coordinates at the specified index, the system defaults to the u and v coordinates (0,0).</span></span>

<span data-ttu-id="c791b-156">使用頂點著色器進行轉譯時，每個階段的材質座標索引都必須設定為其預設值。</span><span class="sxs-lookup"><span data-stu-id="c791b-156">When rendering using vertex shaders, each stage's texture coordinate index must be set to its default value.</span></span> <span data-ttu-id="c791b-157">每個階段的預設索引等於階段索引。</span><span class="sxs-lookup"><span data-stu-id="c791b-157">The default index for each stage is equal to the stage index.</span></span> <span data-ttu-id="c791b-158">針對這個紋理階段使用的每個頂點，將此狀態設定為以零為基底的座標集索引。</span><span class="sxs-lookup"><span data-stu-id="c791b-158">Set this state to the zero-based index of the coordinate set for each vertex that this texture stage uses.</span></span>

<span data-ttu-id="c791b-159">此外，應用程式也可以包含要設定之索引的邏輯 OR，其中一個常數會要求 Direct3D 自動產生材質轉換的輸入材質座標。</span><span class="sxs-lookup"><span data-stu-id="c791b-159">Additionally, applications can include, as logical OR with the index being set, one of the constants to request that Direct3D automatically generate the input texture coordinates for a texture transformation.</span></span> <span data-ttu-id="c791b-160">如需所有常數的清單，請參閱 [D3DTSS \_ TCI](d3dtss-tci.md)。</span><span class="sxs-lookup"><span data-stu-id="c791b-160">For a list of all the constants, see [D3DTSS\_TCI](d3dtss-tci.md).</span></span>

<span data-ttu-id="c791b-161">除了 D3DTSS \_ TCI \_ PASSTHRU （解析為零）之外，如果有下列任何值包含在要設定的索引中，系統會嚴格地使用索引來判斷材質包裝模式。</span><span class="sxs-lookup"><span data-stu-id="c791b-161">With the exception of D3DTSS\_TCI\_PASSTHRU, which resolves to zero, if any of the following values is included with the index being set, the system uses the index strictly to determine texture wrapping mode.</span></span> <span data-ttu-id="c791b-162">這些旗標最適合用來執行環境對應。</span><span class="sxs-lookup"><span data-stu-id="c791b-162">These flags are most useful when performing environment mapping.</span></span>

</dd> <dt>

<span data-ttu-id="c791b-163"><span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS \_ BUMPENVLSCALE**</span><span class="sxs-lookup"><span data-stu-id="c791b-163"><span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS\_BUMPENVLSCALE**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-164">凹凸地圖亮度的浮點刻度值。</span><span class="sxs-lookup"><span data-stu-id="c791b-164">Floating-point scale value for bump-map luminance.</span></span> <span data-ttu-id="c791b-165">預設值為 0.0。</span><span class="sxs-lookup"><span data-stu-id="c791b-165">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="c791b-166"><span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS \_ BUMPENVLOFFSET**</span><span class="sxs-lookup"><span data-stu-id="c791b-166"><span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS\_BUMPENVLOFFSET**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-167">凹凸地圖亮度的浮點位移值。</span><span class="sxs-lookup"><span data-stu-id="c791b-167">Floating-point offset value for bump-map luminance.</span></span> <span data-ttu-id="c791b-168">預設值為 0.0。</span><span class="sxs-lookup"><span data-stu-id="c791b-168">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="c791b-169"><span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS \_ TEXTURETRANSFORMFLAGS**</span><span class="sxs-lookup"><span data-stu-id="c791b-169"><span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS\_TEXTURETRANSFORMFLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-170">[**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md)列舉型別的成員，可控制此材質階段之材質座標的轉換。</span><span class="sxs-lookup"><span data-stu-id="c791b-170">Member of the [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) enumerated type that controls the transformation of texture coordinates for this texture stage.</span></span> <span data-ttu-id="c791b-171">預設值為 [停用] D3DTTFF \_ 。</span><span class="sxs-lookup"><span data-stu-id="c791b-171">The default value is D3DTTFF\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="c791b-172"><span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS \_ COLORARG0**</span><span class="sxs-lookup"><span data-stu-id="c791b-172"><span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS\_COLORARG0**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-173">Triadic 作業的第三個色彩運算元的設定 (乘、加入和線性插補) （由 [D3DTA](d3dta.md)所識別）。</span><span class="sxs-lookup"><span data-stu-id="c791b-173">Settings for the third color operand for triadic operations (multiply, add, and linearly interpolate), identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="c791b-174">如果 \_ 有 D3DTEXOPCAPS MULTIPLYADD 或 D3DTEXOPCAPS LERP 裝置功能，則支援此設定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c791b-174">This setting is supported if the D3DTEXOPCAPS\_MULTIPLYADD or D3DTEXOPCAPS\_LERP device capabilities are present.</span></span> <span data-ttu-id="c791b-175">預設引數為 D3DTA \_ CURRENT。</span><span class="sxs-lookup"><span data-stu-id="c791b-175">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="c791b-176">指定 D3DTA \_ TEMP 以選取用於讀取或寫入的臨時暫存器色彩。</span><span class="sxs-lookup"><span data-stu-id="c791b-176">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="c791b-177">\_如果 \_ 有 D3DPMISCCAPS TSSARGTEMP 裝置功能，則支援 D3DTA TEMP。</span><span class="sxs-lookup"><span data-stu-id="c791b-177">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="c791b-178">註冊的預設值是 (0.0、0.0、0.0、0.0) 。</span><span class="sxs-lookup"><span data-stu-id="c791b-178">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="c791b-179"><span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS \_ ALPHAARG0**</span><span class="sxs-lookup"><span data-stu-id="c791b-179"><span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS\_ALPHAARG0**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-180">Triadic 作業之 Alpha 通道選取器運算元的設定 (乘以、加入和線性插補) ，由 [D3DTA](d3dta.md)所識別。</span><span class="sxs-lookup"><span data-stu-id="c791b-180">Settings for the alpha channel selector operand for triadic operations (multiply, add, and linearly interpolate), identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="c791b-181">如果 \_ 有 D3DTEXOPCAPS MULTIPLYADD 或 D3DTEXOPCAPS LERP 裝置功能，則支援此設定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c791b-181">This setting is supported if the D3DTEXOPCAPS\_MULTIPLYADD or D3DTEXOPCAPS\_LERP device capabilities are present.</span></span> <span data-ttu-id="c791b-182">預設引數為 D3DTA \_ CURRENT。</span><span class="sxs-lookup"><span data-stu-id="c791b-182">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="c791b-183">指定 D3DTA \_ TEMP 以選取用於讀取或寫入的臨時暫存器色彩。</span><span class="sxs-lookup"><span data-stu-id="c791b-183">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="c791b-184">\_如果 \_ 有 D3DPMISCCAPS TSSARGTEMP 裝置功能，則支援 D3DTA TEMP。</span><span class="sxs-lookup"><span data-stu-id="c791b-184">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="c791b-185">預設引數是 (0.0、0.0、0.0、0.0) 。</span><span class="sxs-lookup"><span data-stu-id="c791b-185">The default argument is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="c791b-186"><span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS \_ RESULTARG**</span><span class="sxs-lookup"><span data-stu-id="c791b-186"><span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS\_RESULTARG**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-187">設定為針對此階段的結果選取目的地註冊，由 [D3DTA](d3dta.md)識別。</span><span class="sxs-lookup"><span data-stu-id="c791b-187">Setting to select destination register for the result of this stage, identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="c791b-188">您可以將此值設定為 D3DTA \_ 目前 (預設值) 或 D3DTA \_ TEMP，也就是可讀入後續階段做為輸入引數的單一臨時暫存器。</span><span class="sxs-lookup"><span data-stu-id="c791b-188">This value can be set to D3DTA\_CURRENT (the default value) or to D3DTA\_TEMP, which is a single temporary register that can be read into subsequent stages as an input argument.</span></span> <span data-ttu-id="c791b-189">傳遞至霧化 blender 和框架緩衝區的最終色彩是取自 D3DTA \_ CURRENT，因此最後一個作用中的材質階段狀態必須設定為 [寫入至最新狀態]。</span><span class="sxs-lookup"><span data-stu-id="c791b-189">The final color passed to the fog blender and frame buffer is taken from D3DTA\_CURRENT, so the last active texture stage state must be set to write to current.</span></span> <span data-ttu-id="c791b-190">如果 \_ 有 D3DPMISCCAPS TSSARGTEMP 裝置功能，則支援此設定。</span><span class="sxs-lookup"><span data-stu-id="c791b-190">This setting is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span>

</dd> <dt>

<span data-ttu-id="c791b-191"><span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS \_ 常數**</span><span class="sxs-lookup"><span data-stu-id="c791b-191"><span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS\_CONSTANT**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-192">每個階段的常數色彩。</span><span class="sxs-lookup"><span data-stu-id="c791b-192">Per-stage constant color.</span></span> <span data-ttu-id="c791b-193">若要查看裝置是否支援每一階段的常數色彩，請參閱 \_ [D3DPMISCCAPS](d3dpmisccaps.md)中的 D3DPMISCCAPS PERSTAGECONSTANT 常數。</span><span class="sxs-lookup"><span data-stu-id="c791b-193">To see if a device supports a per-stage constant color, see the D3DPMISCCAPS\_PERSTAGECONSTANT constant in [D3DPMISCCAPS](d3dpmisccaps.md).</span></span> <span data-ttu-id="c791b-194">\_D3DTA 常數會使用 D3DTSS 常數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c791b-194">D3DTSS\_CONSTANT is used by D3DTA\_CONSTANT.</span></span> <span data-ttu-id="c791b-195">請參閱 [D3DTA](d3dta.md)。</span><span class="sxs-lookup"><span data-stu-id="c791b-195">See [D3DTA](d3dta.md).</span></span>

</dd> <dt>

<span data-ttu-id="c791b-196"><span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c791b-196"><span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c791b-197">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="c791b-197">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="c791b-198">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="c791b-198">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="c791b-199">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="c791b-199">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c791b-200">備註</span><span class="sxs-lookup"><span data-stu-id="c791b-200">Remarks</span></span>

<span data-ttu-id="c791b-201">此列舉類型的成員會搭配 [**IDirect3DDevice9：： GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) 和 [**IDirect3DDevice9：： SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) 方法使用，以抓取並設定材質狀態值。</span><span class="sxs-lookup"><span data-stu-id="c791b-201">Members of this enumerated type are used with the [**IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) and [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) methods to retrieve and set texture state values.</span></span>

<span data-ttu-id="c791b-202">D3DTSS \_ BUMPENVMAT00、D3DTSS \_ BUMPENVMAT01、D3DTSS \_ BUMPENVMAT10 和 D3DTSS \_ BUMPENVMAT11 凸塊對應矩陣係數的有效值範圍大於或等於-8.0 且小於8.0。</span><span class="sxs-lookup"><span data-stu-id="c791b-202">The valid range of values for the D3DTSS\_BUMPENVMAT00, D3DTSS\_BUMPENVMAT01, D3DTSS\_BUMPENVMAT10, and D3DTSS\_BUMPENVMAT11 bump-mapping matrix coefficients is greater than or equal to -8.0 and less than 8.0.</span></span> <span data-ttu-id="c791b-203">以數學標記法表示的這個範圍是 (-8.0，8.0) 。</span><span class="sxs-lookup"><span data-stu-id="c791b-203">This range, expressed in mathematical notation is (-8.0,8.0).</span></span>

## <a name="requirements"></a><span data-ttu-id="c791b-204">規格需求</span><span class="sxs-lookup"><span data-stu-id="c791b-204">Requirements</span></span>



| <span data-ttu-id="c791b-205">需求</span><span class="sxs-lookup"><span data-stu-id="c791b-205">Requirement</span></span> | <span data-ttu-id="c791b-206">值</span><span class="sxs-lookup"><span data-stu-id="c791b-206">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c791b-207">標頭</span><span class="sxs-lookup"><span data-stu-id="c791b-207">Header</span></span><br/> | <dl> <span data-ttu-id="c791b-208"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="c791b-208"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c791b-209">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c791b-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c791b-210">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="c791b-210">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="c791b-211">**IDirect3DDevice9::GetTextureStageState**</span><span class="sxs-lookup"><span data-stu-id="c791b-211">**IDirect3DDevice9::GetTextureStageState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[<span data-ttu-id="c791b-212">**IDirect3DDevice9::SetTextureStageState**</span><span class="sxs-lookup"><span data-stu-id="c791b-212">**IDirect3DDevice9::SetTextureStageState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 

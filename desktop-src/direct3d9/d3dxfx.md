---
description: 儲存和建立效果的選項。
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1e5e57b5fac94c1fb24d35cf1826057b75c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108425"
---
# <a name="d3dxfx"></a><span data-ttu-id="d208f-103">D3DXFX</span><span class="sxs-lookup"><span data-stu-id="d208f-103">D3DXFX</span></span>

<span data-ttu-id="d208f-104">儲存和建立效果的選項。</span><span class="sxs-lookup"><span data-stu-id="d208f-104">Options for saving and creating effects.</span></span>

<span data-ttu-id="d208f-105">下表中的常數定義于 d3dx9effect 中。</span><span class="sxs-lookup"><span data-stu-id="d208f-105">The constants in the following table are defined in d3dx9effect.h.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d208f-106">效果狀態儲存和還原旗標</span><span class="sxs-lookup"><span data-stu-id="d208f-106">Effect State Save and Restore Flags</span></span></td>
<td><span data-ttu-id="d208f-107">Description</span><span class="sxs-lookup"><span data-stu-id="d208f-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d208f-108">D3DXFX_DONOTSAVESTATE</span><span class="sxs-lookup"><span data-stu-id="d208f-108">D3DXFX_DONOTSAVESTATE</span></span></td>
<td><span data-ttu-id="d208f-109">呼叫<a href="id3dxeffect--end.md"><strong>End</strong></a>時呼叫<a href="id3dxeffect--begin.md"><strong>Begin</strong></a>或還原時，不會儲存任何狀態。</span><span class="sxs-lookup"><span data-stu-id="d208f-109">No state is saved when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> or restored when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d208f-110">D3DXFX_DONOTSAVESAMPLERSTATE</span><span class="sxs-lookup"><span data-stu-id="d208f-110">D3DXFX_DONOTSAVESAMPLERSTATE</span></span></td>
<td><span data-ttu-id="d208f-111">當呼叫<a href="id3dxeffect--end.md"><strong>End</strong></a>時，stateblock 會儲存<a href="id3dxeffect--begin.md"><strong>開始</strong></a>和還原狀態的狀態。</span><span class="sxs-lookup"><span data-stu-id="d208f-111">A stateblock saves state when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d208f-112">D3DXFX_DONOTSAVESHADERSTATE</span><span class="sxs-lookup"><span data-stu-id="d208f-112">D3DXFX_DONOTSAVESHADERSTATE</span></span></td>
<td><span data-ttu-id="d208f-113">Stateblock 會將狀態 (儲存) 著色器和著色器常數，但在呼叫<a href="id3dxeffect--end.md"><strong>End</strong></a>時呼叫<a href="id3dxeffect--begin.md"><strong>Begin</strong></a>和還原狀態。</span><span class="sxs-lookup"><span data-stu-id="d208f-113">A stateblock saves state (except shaders and shader constants) when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d208f-114">效果建立旗標</span><span class="sxs-lookup"><span data-stu-id="d208f-114">Effect Creation Flags</span></span></td>
<td><span data-ttu-id="d208f-115">Description</span><span class="sxs-lookup"><span data-stu-id="d208f-115">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d208f-116">D3DXFX_NOT_CLONEABLE</span><span class="sxs-lookup"><span data-stu-id="d208f-116">D3DXFX_NOT_CLONEABLE</span></span></td>
<td><span data-ttu-id="d208f-117">效果將為非 cloneable，且不會包含任何著色器二進位資料。</span><span class="sxs-lookup"><span data-stu-id="d208f-117">The effect will be non-cloneable and will not contain any shader binary data.</span></span> <span data-ttu-id="d208f-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> 不會傳回著色器函式指標。</span><span class="sxs-lookup"><span data-stu-id="d208f-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> will not return shader function pointers.</span></span> <span data-ttu-id="d208f-119">設定此旗標可減少大約50% 的效果記憶體使用量，因為它不需要讓效果系統將著色器的複本保留在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="d208f-119">Setting this flag reduces effect memory usage by about 50% because it eliminates the need for the effect system to keep a copy of the shaders in memory.</span></span> <span data-ttu-id="d208f-120"><a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>、 <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>和<a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>會使用這個旗標。</span><span class="sxs-lookup"><span data-stu-id="d208f-120">This flag is used by <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>, and <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d208f-121">D3DXFX_LARGEADDRESSAWARE</span><span class="sxs-lookup"><span data-stu-id="d208f-121">D3DXFX_LARGEADDRESSAWARE</span></span></td>
<td><span data-ttu-id="d208f-122">可將效果資源配置到電腦的 uppder 位址空間。</span><span class="sxs-lookup"><span data-stu-id="d208f-122">Enables the allocation of an effect resource into the uppder address space of a machine.</span></span> <span data-ttu-id="d208f-123">其中一項重要的限制是，您無法使用字串和控制碼交換。</span><span class="sxs-lookup"><span data-stu-id="d208f-123">One important limitation is that you cannot use strings and handles interchangeably.</span></span> <span data-ttu-id="d208f-124">例如，下列程式將無法再運作。</span><span class="sxs-lookup"><span data-stu-id="d208f-124">For example, the following would no longer work.</span></span> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>g_pEffect->SetMatrix( &quot;g_mWorldViewProjection&quot;, &mWorldViewProjection );</code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d208f-125">相反地，您必須使用 [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) 之類的方法來儲存參數的控制碼，然後用它來將變數傳遞給效果。</span><span class="sxs-lookup"><span data-stu-id="d208f-125">Instead, a method such as [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) must be used to store the handle of the parameter, which is then used to pass variables to the effect.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d208f-126">下表中的常數預設未定義，且必須由開發人員定義。</span><span class="sxs-lookup"><span data-stu-id="d208f-126">The constants in the following table are not defined by default and must be defined by the developer.</span></span>



|                                |                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d208f-127">效果預處理器 \# 定義</span><span class="sxs-lookup"><span data-stu-id="d208f-127">Effect Preprocessor \#define's</span></span> | <span data-ttu-id="d208f-128">Description</span><span class="sxs-lookup"><span data-stu-id="d208f-128">Description</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="d208f-129">D3DXFX \_ LARGEADDRESS \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="d208f-129">D3DXFX\_LARGEADDRESS\_HANDLE</span></span>   | <span data-ttu-id="d208f-130">在包含 d3dx9 之前定義此值，讓您的應用程式在嘗試將字串傳遞至 D3DXHANDLE 參數時無法編譯。</span><span class="sxs-lookup"><span data-stu-id="d208f-130">Define this value before including d3dx9.h so that your application fails to compile when attempting to pass strings into D3DXHANDLE parameters.</span></span> <span data-ttu-id="d208f-131">這有助於確保將有效的資訊傳遞給執行時間。</span><span class="sxs-lookup"><span data-stu-id="d208f-131">This will aid in making sure that valid information is being passed to the runtime.</span></span> |
| <span data-ttu-id="d208f-132">效果連結器旗標</span><span class="sxs-lookup"><span data-stu-id="d208f-132">Effect Linker Flags</span></span>            | <span data-ttu-id="d208f-133">Description</span><span class="sxs-lookup"><span data-stu-id="d208f-133">Description</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="d208f-134">大型 \_ 位址 \_ 感知</span><span class="sxs-lookup"><span data-stu-id="d208f-134">LARGE\_ADDRESS\_AWARE</span></span>          | <span data-ttu-id="d208f-135">設定連結器旗標大型 \_ 位址 \_ 感知 = 1 將可讓應用程式在需要時配置超過2gb 位址限制的資源。</span><span class="sxs-lookup"><span data-stu-id="d208f-135">Setting the linker flag LARGE\_ADDRESS\_AWARE = 1 will will allow the application to allocate resources past the 2GB address limit when needed.</span></span>                                                                                      |



 

<span data-ttu-id="d208f-136">效果系統會使用狀態欄塊來自動儲存和還原狀態。</span><span class="sxs-lookup"><span data-stu-id="d208f-136">The effect system uses state blocks to save and restore state automatically.</span></span> <span data-ttu-id="d208f-137">如需狀態欄塊的詳細資訊，請參閱 [ (Direct3D 9) 的狀態欄塊儲存和還原狀態 ](state-blocks-save-and-restore-state.md)。</span><span class="sxs-lookup"><span data-stu-id="d208f-137">For more information about state blocks, see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d208f-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="d208f-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d208f-139">效果常數</span><span class="sxs-lookup"><span data-stu-id="d208f-139">Effect Constants</span></span>](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




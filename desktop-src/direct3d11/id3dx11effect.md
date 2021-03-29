---
title: 'ID3DX11Effect 介面 (D3dx11effect .h) '
description: ID3DX11Effect 介面會管理一組用於執行轉譯效果的狀態物件、資源和著色器。
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- ID3DX11Effect 介面 Direct3D 11
- ID3DX11Effect 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11Effect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395946ea4276bc57595abdeb18e7d1755ca0ff1d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992327"
---
# <a name="id3dx11effect-interface"></a><span data-ttu-id="e84fc-105">ID3DX11Effect 介面</span><span class="sxs-lookup"><span data-stu-id="e84fc-105">ID3DX11Effect interface</span></span>

<span data-ttu-id="e84fc-106">**ID3DX11Effect** 介面會管理一組用於執行轉譯效果的狀態物件、資源和著色器。</span><span class="sxs-lookup"><span data-stu-id="e84fc-106">An **ID3DX11Effect** interface manages a set of state objects, resources, and shaders for implementing a rendering effect.</span></span>

## <a name="members"></a><span data-ttu-id="e84fc-107">成員</span><span class="sxs-lookup"><span data-stu-id="e84fc-107">Members</span></span>

<span data-ttu-id="e84fc-108">**ID3DX11Effect** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="e84fc-108">The **ID3DX11Effect** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e84fc-109">**ID3DX11Effect** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e84fc-109">**ID3DX11Effect** also has these types of members:</span></span>

-   [<span data-ttu-id="e84fc-110">方法</span><span class="sxs-lookup"><span data-stu-id="e84fc-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e84fc-111">方法</span><span class="sxs-lookup"><span data-stu-id="e84fc-111">Methods</span></span>

<span data-ttu-id="e84fc-112">**ID3DX11Effect** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e84fc-112">The **ID3DX11Effect** interface has these methods.</span></span>



| <span data-ttu-id="e84fc-113">方法</span><span class="sxs-lookup"><span data-stu-id="e84fc-113">Method</span></span>                                                                     | <span data-ttu-id="e84fc-114">描述</span><span class="sxs-lookup"><span data-stu-id="e84fc-114">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e84fc-115">**CloneEffect**</span><span class="sxs-lookup"><span data-stu-id="e84fc-115">**CloneEffect**</span></span>](id3dx11effect-cloneeffect.md)                           | <span data-ttu-id="e84fc-116">建立效果介面的複本。</span><span class="sxs-lookup"><span data-stu-id="e84fc-116">Creates a copy of an effect interface.</span></span><br/>                                         |
| [<span data-ttu-id="e84fc-117">**GetClassLinkage**</span><span class="sxs-lookup"><span data-stu-id="e84fc-117">**GetClassLinkage**</span></span>](id3dx11effect-getclasslinkage.md)                   | <span data-ttu-id="e84fc-118">取得類別連結介面。</span><span class="sxs-lookup"><span data-stu-id="e84fc-118">Gets a class linkage interface.</span></span><br/>                                                |
| [<span data-ttu-id="e84fc-119">**GetConstantBufferByIndex**</span><span class="sxs-lookup"><span data-stu-id="e84fc-119">**GetConstantBufferByIndex**</span></span>](id3dx11effect-getconstantbufferbyindex.md) | <span data-ttu-id="e84fc-120">依索引取得常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e84fc-120">Get a constant buffer by index.</span></span><br/>                                                |
| [<span data-ttu-id="e84fc-121">**GetConstantBufferByName**</span><span class="sxs-lookup"><span data-stu-id="e84fc-121">**GetConstantBufferByName**</span></span>](id3dx11effect-getconstantbufferbyname.md)   | <span data-ttu-id="e84fc-122">依名稱取得常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e84fc-122">Get a constant buffer by name.</span></span><br/>                                                 |
| [<span data-ttu-id="e84fc-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="e84fc-123">**GetDesc**</span></span>](id3dx11effect-getdesc.md)                                   | <span data-ttu-id="e84fc-124">取得效果描述。</span><span class="sxs-lookup"><span data-stu-id="e84fc-124">Get an effect description.</span></span><br/>                                                     |
| [<span data-ttu-id="e84fc-125">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="e84fc-125">**GetDevice**</span></span>](id3dx11effect-getdevice.md)                               | <span data-ttu-id="e84fc-126">取得建立效果的裝置。</span><span class="sxs-lookup"><span data-stu-id="e84fc-126">Get the device that created the effect.</span></span><br/>                                        |
| [<span data-ttu-id="e84fc-127">**GetGroupByIndex**</span><span class="sxs-lookup"><span data-stu-id="e84fc-127">**GetGroupByIndex**</span></span>](id3dx11effect-getgroupbyindex.md)                   | <span data-ttu-id="e84fc-128">依索引取得效果群組。</span><span class="sxs-lookup"><span data-stu-id="e84fc-128">Gets an effect group by index.</span></span><br/>                                                 |
| [<span data-ttu-id="e84fc-129">**GetGroupByName**</span><span class="sxs-lookup"><span data-stu-id="e84fc-129">**GetGroupByName**</span></span>](id3dx11effect-getgroupbyname.md)                     | <span data-ttu-id="e84fc-130">依名稱取得效果群組。</span><span class="sxs-lookup"><span data-stu-id="e84fc-130">Gets an effect group by name.</span></span><br/>                                                  |
| [<span data-ttu-id="e84fc-131">**GetTechniqueByIndex**</span><span class="sxs-lookup"><span data-stu-id="e84fc-131">**GetTechniqueByIndex**</span></span>](id3dx11effect-gettechniquebyindex.md)           | <span data-ttu-id="e84fc-132">依索引取得技術。</span><span class="sxs-lookup"><span data-stu-id="e84fc-132">Get a technique by index.</span></span><br/>                                                      |
| [<span data-ttu-id="e84fc-133">**GetTechniqueByName**</span><span class="sxs-lookup"><span data-stu-id="e84fc-133">**GetTechniqueByName**</span></span>](id3dx11effect-gettechniquebyname.md)             | <span data-ttu-id="e84fc-134">依名稱取得技術。</span><span class="sxs-lookup"><span data-stu-id="e84fc-134">Get a technique by name.</span></span><br/>                                                       |
| [<span data-ttu-id="e84fc-135">**GetVariableByIndex**</span><span class="sxs-lookup"><span data-stu-id="e84fc-135">**GetVariableByIndex**</span></span>](id3dx11effect-getvariablebyindex.md)             | <span data-ttu-id="e84fc-136">依索引取得變數。</span><span class="sxs-lookup"><span data-stu-id="e84fc-136">Get a variable by index.</span></span><br/>                                                       |
| [<span data-ttu-id="e84fc-137">**GetVariableByName**</span><span class="sxs-lookup"><span data-stu-id="e84fc-137">**GetVariableByName**</span></span>](id3dx11effect-getvariablebyname.md)               | <span data-ttu-id="e84fc-138">依名稱取得變數。</span><span class="sxs-lookup"><span data-stu-id="e84fc-138">Get a variable by name.</span></span><br/>                                                        |
| [<span data-ttu-id="e84fc-139">**GetVariableBySemantic**</span><span class="sxs-lookup"><span data-stu-id="e84fc-139">**GetVariableBySemantic**</span></span>](id3dx11effect-getvariablebysemantic.md)       | <span data-ttu-id="e84fc-140">依語義取得變數。</span><span class="sxs-lookup"><span data-stu-id="e84fc-140">Get a variable by semantic.</span></span><br/>                                                    |
| [<span data-ttu-id="e84fc-141">**IsOptimized**</span><span class="sxs-lookup"><span data-stu-id="e84fc-141">**IsOptimized**</span></span>](id3dx11effect-isoptimized.md)                           | <span data-ttu-id="e84fc-142">測試效果，以查看反映中繼資料是否已從記憶體中移除。</span><span class="sxs-lookup"><span data-stu-id="e84fc-142">Test an effect to see if the reflection metadata has been removed from memory.</span></span><br/> |
| [<span data-ttu-id="e84fc-143">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="e84fc-143">**IsValid**</span></span>](id3dx11effect-isvalid.md)                                   | <span data-ttu-id="e84fc-144">測試效果，以查看它是否包含有效的語法。</span><span class="sxs-lookup"><span data-stu-id="e84fc-144">Test an effect to see if it contains valid syntax.</span></span><br/>                             |
| [<span data-ttu-id="e84fc-145">**優化**</span><span class="sxs-lookup"><span data-stu-id="e84fc-145">**Optimize**</span></span>](id3dx11effect-optimize.md)                                 | <span data-ttu-id="e84fc-146">將效果所需的記憶體數量降到最低。</span><span class="sxs-lookup"><span data-stu-id="e84fc-146">Minimize the amount of memory required for an effect.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="e84fc-147">備註</span><span class="sxs-lookup"><span data-stu-id="e84fc-147">Remarks</span></span>

<span data-ttu-id="e84fc-148">藉由呼叫 [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md)來建立效果。</span><span class="sxs-lookup"><span data-stu-id="e84fc-148">An effect is created by calling [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span></span>

<span data-ttu-id="e84fc-149">效果系統會將轉譯所需的資訊群組為包含：用於指派群組中狀態變更的狀態物件、提供輸入資料和儲存輸出資料的資源，以及控制轉譯如何完成的程式，稱為著色器。</span><span class="sxs-lookup"><span data-stu-id="e84fc-149">The effect system groups the information required for rendering into an effect which contains: state objects for assigning state changes in groups, resources for supplying input data and storing output data, and programs that control how the rendering is done called shaders.</span></span>

> [!Note]  
> <span data-ttu-id="e84fc-150">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="e84fc-150">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e84fc-151">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e84fc-151">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e84fc-152">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="e84fc-152">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

> [!Note]
>
> <span data-ttu-id="e84fc-153">如果您呼叫 **ID3DX11Effect** 物件上的 [**Queryinterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))來取出 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面， **queryinterface** 會傳回 E \_ NOINTERFACE。</span><span class="sxs-lookup"><span data-stu-id="e84fc-153">If you call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on an **ID3DX11Effect** object to retrieve the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface, **QueryInterface** returns E\_NOINTERFACE.</span></span> <span data-ttu-id="e84fc-154">若要解決此問題，請使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="e84fc-154">To work around this issue, use the following code:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;
>     pIUnknown->AddRef();</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> ## <a name="requirements"></a><span data-ttu-id="e84fc-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="e84fc-155">Requirements</span></span>
>
> 
>
<span data-ttu-id="e84fc-156">|需求 |值 |</span><span class="sxs-lookup"><span data-stu-id="e84fc-156">| Requirement | Value |</span></span>
> <span data-ttu-id="e84fc-157">|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------| |頭</span><span class="sxs-lookup"><span data-stu-id="e84fc-157">|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------| | Header</span></span><br/>  | <dl> <span data-ttu-id="e84fc-158"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="e84fc-158"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    <span data-ttu-id="e84fc-159">| |圖書館</span><span class="sxs-lookup"><span data-stu-id="e84fc-159">| | Library</span></span><br/> | <dl> <span data-ttu-id="e84fc-160"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="e84fc-160"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |
>
> 
>
> ## <a name="see-also"></a><span data-ttu-id="e84fc-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e84fc-161">See also</span></span>
>
> <dl> <dt>

[<span data-ttu-id="e84fc-162">效果11介面</span><span class="sxs-lookup"><span data-stu-id="e84fc-162">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e84fc-163">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="e84fc-163">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>
>
>  
>
>  
>

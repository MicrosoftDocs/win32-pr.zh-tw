---
title: 複製效果
description: 複製效果會建立第二個與效果幾乎相同的複本。
ms.assetid: e3870363-5ee8-4fdc-a489-cdaeef8c9c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68607d3cc9f00a346fcfa65c255f3caa51dea384
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674003"
---
# <a name="cloning-an-effect"></a><span data-ttu-id="4a126-103">複製效果</span><span class="sxs-lookup"><span data-stu-id="4a126-103">Cloning an Effect</span></span>

<span data-ttu-id="4a126-104">複製效果會建立第二個與效果幾乎相同的複本。</span><span class="sxs-lookup"><span data-stu-id="4a126-104">Cloning an effect creates a second, almost identical copy of the effect.</span></span> <span data-ttu-id="4a126-105">請參閱下列單一辨識符號，以取得為何不精確的說明。</span><span class="sxs-lookup"><span data-stu-id="4a126-105">See the following single qualifier for an explanation of why it is not exact.</span></span> <span data-ttu-id="4a126-106">當您想要在多個執行緒上使用效果架構時，效果的第二個複本會很有用，因為效果執行時間不會以安全線程的速度維持高效能。</span><span class="sxs-lookup"><span data-stu-id="4a126-106">A second copy of an effect is useful when one wants to use the effects framework on multiple threads, since the effect runtime is not thread safe to maintain high performance.</span></span>

<span data-ttu-id="4a126-107">由於裝置內容也是非安全線程，因此不同的執行緒應該將不同的裝置內容傳遞至 ID3DX11EffectPass：： Apply 方法。</span><span class="sxs-lookup"><span data-stu-id="4a126-107">Since device contexts are also non-thread-safe, different threads should pass different device contexts to the ID3DX11EffectPass::Apply method.</span></span>

<span data-ttu-id="4a126-108">您可以使用下列語法來複製效果：</span><span class="sxs-lookup"><span data-stu-id="4a126-108">An effect can be cloned with the following syntax:</span></span>


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



<span data-ttu-id="4a126-109">在上述範例中，複製的複本將會封裝與原始效果相同的狀態，而不論原始效果的狀態為何。</span><span class="sxs-lookup"><span data-stu-id="4a126-109">In the above example, the cloned copy will encapsulate the same state as the original effect, regardless of what state the original effect is in.</span></span> <span data-ttu-id="4a126-110">尤其是：</span><span class="sxs-lookup"><span data-stu-id="4a126-110">In particular:</span></span>

1.  <span data-ttu-id="4a126-111">如果 pEffect 已優化，pCloned 效果就會優化</span><span class="sxs-lookup"><span data-stu-id="4a126-111">If pEffect is optimized, pCloned Effect is optimized</span></span>
2.  <span data-ttu-id="4a126-112">如果 pEffect 有一些使用者管理的變數，pCloned 效果將會有相同的使用者管理變數 (請參閱下面的單一描述) </span><span class="sxs-lookup"><span data-stu-id="4a126-112">If pEffect has some user-managed variables, pCloned Effect will have the same user-managed variables (see the single description below)</span></span>
3.  <span data-ttu-id="4a126-113">任何暫止的變數更新都會 (，直到 pEffect 中的 [套用呼叫更新裝置狀態]) 暫止于 pClonedEffect</span><span class="sxs-lookup"><span data-stu-id="4a126-113">Any pending variable updates (until an Apply call updates device state) in pEffect will be pending in pClonedEffect</span></span>

<span data-ttu-id="4a126-114">下列 Direct3D 11 裝置物件是不可變的，或永遠不會被效果架構更新，因此複製的效果會指向與原始效果相同的物件：</span><span class="sxs-lookup"><span data-stu-id="4a126-114">The following Direct3D 11 device objects are immutable or never updated by the effects framework, so the cloned effect will point to the same objects as the original effect:</span></span>

1.  <span data-ttu-id="4a126-115">狀態欄塊物件 (ID3D11BlendState、ID3D11RasterizerState、ID3D11DepthStencilState、ID3D11SamplerState) </span><span class="sxs-lookup"><span data-stu-id="4a126-115">State block objects (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)</span></span>
2.  <span data-ttu-id="4a126-116">著色器</span><span class="sxs-lookup"><span data-stu-id="4a126-116">Shaders</span></span>
3.  <span data-ttu-id="4a126-117">類別實例</span><span class="sxs-lookup"><span data-stu-id="4a126-117">Class instances</span></span>
4.  <span data-ttu-id="4a126-118">材質 (不包括材質緩衝區) </span><span class="sxs-lookup"><span data-stu-id="4a126-118">Textures (not including texture buffers)</span></span>
5.  <span data-ttu-id="4a126-119">未排序的存取權視圖</span><span class="sxs-lookup"><span data-stu-id="4a126-119">Unordered access views</span></span>

<span data-ttu-id="4a126-120">下列 Direct3D 11 裝置物件都是不可變的，且效果執行時間 (修改，除非在複製的效果中有使用者管理或單一的) ;當非單一時，會建立這些物件的新複本：</span><span class="sxs-lookup"><span data-stu-id="4a126-120">The following Direct3D 11 device objects are both immutable and modified by the effect runtime (unless user-managed or single in a cloned effect); new copies of these objects are created when non-single:</span></span>

1.  <span data-ttu-id="4a126-121">常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="4a126-121">Constant buffers</span></span>
2.  <span data-ttu-id="4a126-122">材質緩衝區</span><span class="sxs-lookup"><span data-stu-id="4a126-122">Texture Buffers</span></span>

## <a name="single-constant-buffers-and-texture-buffers"></a><span data-ttu-id="4a126-123">單一常數緩衝區和材質緩衝區</span><span class="sxs-lookup"><span data-stu-id="4a126-123">Single Constant Buffers and Texture Buffers</span></span>

<span data-ttu-id="4a126-124">請注意，這項討論適用于常數緩衝區和紋理，但會假設常數緩衝區以方便閱讀。</span><span class="sxs-lookup"><span data-stu-id="4a126-124">Note that this discussion applies to both constant buffers and textures, but constant buffers are assumed for ease of reading.</span></span>

<span data-ttu-id="4a126-125">在某些情況下，常數緩衝區只會由一個執行緒更新，但複製的效果所設定的裝置狀態將會使用此資料。</span><span class="sxs-lookup"><span data-stu-id="4a126-125">There may be cases where a constant buffer is only updated by one thread, but device state set by cloned effects will use this data.</span></span> <span data-ttu-id="4a126-126">例如，主要效果可能會更新世界和視野矩陣，這些矩陣是在複製效果中從著色器參考，而不會變更世界和視野矩陣。</span><span class="sxs-lookup"><span data-stu-id="4a126-126">For example, the main effect may update the world and view matrices which are referenced from shaders in cloned effects which do not change the world and view matrices.</span></span> <span data-ttu-id="4a126-127">在這些情況下，複製的效果必須參考目前的常數緩衝區，而不是重新建立它。</span><span class="sxs-lookup"><span data-stu-id="4a126-127">In these cases, the cloned effects need to reference the current constant buffer instead of recreating one.</span></span>

<span data-ttu-id="4a126-128">有兩種方式可以達成此預期的結果：</span><span class="sxs-lookup"><span data-stu-id="4a126-128">There are two ways to achieve this desired result:</span></span>

1.  <span data-ttu-id="4a126-129">在複製的效果上使用 ID3DX11EffectConstantBuffer：： SetConstantBuffer，使其成為使用者管理的</span><span class="sxs-lookup"><span data-stu-id="4a126-129">Use ID3DX11EffectConstantBuffer::SetConstantBuffer on the cloned effect to make it user-managed</span></span>
2.  <span data-ttu-id="4a126-130">在 HLSL 程式碼中將常數緩衝區標示為「單一」，強制在複製之後，將作用中的執行時間視為使用者管理的</span><span class="sxs-lookup"><span data-stu-id="4a126-130">Mark the constant buffer as "single" in the HLSL code, forcing the effect runtime to treat is as user-managed after cloning</span></span>

<span data-ttu-id="4a126-131">上述兩個方法之間有兩種差異。</span><span class="sxs-lookup"><span data-stu-id="4a126-131">There are two differences between the two methods above.</span></span> <span data-ttu-id="4a126-132">首先，在方法1中，會先建立新的 ID3D11Buffer，然後再呼叫 SetConstantBuffer。</span><span class="sxs-lookup"><span data-stu-id="4a126-132">First, in method 1, a new ID3D11Buffer will be created and user before SetConstantBuffer is called.</span></span> <span data-ttu-id="4a126-133">此外，在複製的效果中呼叫 UndoSetConstantBuffer 之後，方法1will 中的變數會指向新建立的緩衝區 (將會在套用) 時更新效果，而方法2中的變數將繼續指向原始緩衝區 (不會在套用) 時更新它。</span><span class="sxs-lookup"><span data-stu-id="4a126-133">Also, after calling UndoSetConstantBuffer in the cloned effect, the variable in method 1will point to the newly-created buffer (which effects will update on Apply) while the variable in method 2 will continue to point to the original buffer (not updating it on Apply).</span></span>

<span data-ttu-id="4a126-134">請參閱 HLSL 中的下列範例：</span><span class="sxs-lookup"><span data-stu-id="4a126-134">See the following example in HLSL:</span></span>


```
cbuffer ObjectData
{
    float4 Position;
};
single cbuffer ViewData
{
    float4x4 ViewMatrix;
};
```



<span data-ttu-id="4a126-135">在複製時，複製的效果會為 ObjectData 建立新的 ID3D11Buffer，並在套用時填入其內容，但參考 ViewData 的原始 ID3D11Buffer。</span><span class="sxs-lookup"><span data-stu-id="4a126-135">While cloning, the cloned effect will create a new ID3D11Buffer for ObjectData, and fill its contents on Apply, but reference the original ID3D11Buffer for ViewData.</span></span> <span data-ttu-id="4a126-136">您可以藉由設定 D3DX11 \_ 效果 \_ 複製 \_ 強制 \_ NONSINGLE 旗標，在複製進程中忽略單一限定詞。</span><span class="sxs-lookup"><span data-stu-id="4a126-136">The single qualifier can be ignored in the cloning process by setting the D3DX11\_EFFECT\_CLONE\_FORCE\_NONSINGLE flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a126-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="4a126-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a126-138"> (Direct3D 11) 的效果 </span><span class="sxs-lookup"><span data-stu-id="4a126-138">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 





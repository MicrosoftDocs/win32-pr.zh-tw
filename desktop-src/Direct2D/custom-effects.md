---
title: 自訂效果
description: 說明如何使用標準 HLSL 撰寫您自己的自訂效果。
ms.assetid: 5D22CA84-6465-4882-863D-81A632ACDD9C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca6b15fe81ff4ccbd6cebbcee8c0d1955967056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093252"
---
# <a name="custom-effects"></a><span data-ttu-id="0918e-103">自訂效果</span><span class="sxs-lookup"><span data-stu-id="0918e-103">Custom effects</span></span>

<span data-ttu-id="0918e-104">[Direct2D](./direct2d-portal.md) 隨附的效果程式庫會執行各種常見的映射作業。</span><span class="sxs-lookup"><span data-stu-id="0918e-104">[Direct2D](./direct2d-portal.md) ships with a library of effects that perform a variety of common image operations.</span></span> <span data-ttu-id="0918e-105">如需效果的完整清單，請參閱 [內建效果](built-in-effects.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="0918e-105">See the [built-in effects](built-in-effects.md) topic for the complete list of effects.</span></span> <span data-ttu-id="0918e-106">針對無法利用內建效果達成的功能，Direct2D 可讓您使用標準 [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)來撰寫自己的自訂效果。</span><span class="sxs-lookup"><span data-stu-id="0918e-106">For functionality that cannot be achieved with the built-in effects, Direct2D allows you to write your own custom effects using standard [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl).</span></span> <span data-ttu-id="0918e-107">您可以將這些自訂效果與 Direct2D 隨附的內建效果一起使用。</span><span class="sxs-lookup"><span data-stu-id="0918e-107">You can use these custom effects alongside the built-in effects that ship with Direct2D.</span></span>

<span data-ttu-id="0918e-108">若要查看完整圖元、頂點和計算著色器效果的範例，請參閱 [D2DCUSTOMEFFECTS SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)。</span><span class="sxs-lookup"><span data-stu-id="0918e-108">To see examples of a complete pixel, vertex, and compute shader effect, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="0918e-109">在本主題中，我們將說明您設計和建立功能完整的自訂效果所需的步驟和概念。</span><span class="sxs-lookup"><span data-stu-id="0918e-109">In this topic, we show you the steps and concepts you need to design and create a fully-featured custom effect.</span></span>

## <a name="introduction-what-is-inside-an-effect"></a><span data-ttu-id="0918e-110">簡介：什麼是作用中？</span><span class="sxs-lookup"><span data-stu-id="0918e-110">Introduction: What is inside an effect?</span></span>

![投影陰影效果圖。](images/custom-effects1.png)

<span data-ttu-id="0918e-112">從概念上來說， [Direct2D](./direct2d-portal.md) 效果會執行映射處理工作，例如變更亮度、對影像進行消除飽和，或如上所示，建立陰影。</span><span class="sxs-lookup"><span data-stu-id="0918e-112">Conceptually, a [Direct2D](./direct2d-portal.md) effect performs an imaging task, like changing brightness, de-saturating an image, or as shown above, creating a drop shadow.</span></span> <span data-ttu-id="0918e-113">應用程式很簡單。</span><span class="sxs-lookup"><span data-stu-id="0918e-113">To the app, they are simple.</span></span> <span data-ttu-id="0918e-114">他們可以接受零個以上的輸入影像、公開多個控制其作業的屬性，以及產生單一輸出影像。</span><span class="sxs-lookup"><span data-stu-id="0918e-114">They can accept zero or more input images, expose multiple properties that control their operation, and generate a single output image.</span></span>

<span data-ttu-id="0918e-115">有四個自訂效果的不同部分是由效果作者負責：</span><span class="sxs-lookup"><span data-stu-id="0918e-115">There are four different parts of a custom effect that an effect author is responsible for:</span></span>

1.  <span data-ttu-id="0918e-116">效果介面：效果介面在概念上定義了應用程式如何與自訂效果互動 (例如效果所接受的輸入數目，以及) 可用的屬性。</span><span class="sxs-lookup"><span data-stu-id="0918e-116">Effect Interface: The effect interface conceptually defines how an app interacts with a custom effect (like how many inputs the effect accepts and what properties are available).</span></span> <span data-ttu-id="0918e-117">效果介面會管理包含實際影像作業的轉換圖形。</span><span class="sxs-lookup"><span data-stu-id="0918e-117">The effect interface manages a transform graph, which contains the actual imaging operations.</span></span>
2.  <span data-ttu-id="0918e-118">轉換圖形：每個效果都會建立由個別轉換所組成的內部轉換圖形。</span><span class="sxs-lookup"><span data-stu-id="0918e-118">Transform graph: Each effect creates an internal transform graph made up of individual transforms.</span></span> <span data-ttu-id="0918e-119">每個轉換都代表單一映射作業。</span><span class="sxs-lookup"><span data-stu-id="0918e-119">Each transform represents a single image operation.</span></span> <span data-ttu-id="0918e-120">效果會負責將這些轉換一起連結到圖形中，以執行預期的圖像效果。</span><span class="sxs-lookup"><span data-stu-id="0918e-120">The effect is responsible for linking these transforms together into a graph to perform the intended imaging effect.</span></span> <span data-ttu-id="0918e-121">效果可以加入、移除、修改及重新排序轉換，以回應效果的外部屬性變更。</span><span class="sxs-lookup"><span data-stu-id="0918e-121">An effect can add, remove, modify, and reorder transforms in response to changes to the effect's external properties.</span></span>
3.  <span data-ttu-id="0918e-122">轉換：轉換代表單一映射作業。</span><span class="sxs-lookup"><span data-stu-id="0918e-122">Transform: A transform represents a single image operation.</span></span> <span data-ttu-id="0918e-123">其主要目的是要存放針對每個輸出圖元執行的著色器。</span><span class="sxs-lookup"><span data-stu-id="0918e-123">Its main purpose is to house the shaders that are executed for each output pixel.</span></span> <span data-ttu-id="0918e-124">為了達到此目的，它會負責根據其著色器中的邏輯來計算其輸出影像的新大小。</span><span class="sxs-lookup"><span data-stu-id="0918e-124">To that end, it is responsible for calculating the new size of its output image based on logic in its shaders.</span></span> <span data-ttu-id="0918e-125">它也必須計算其輸入影像的哪個區域，著色器需要從該區域讀取以轉譯要求的輸出區域。</span><span class="sxs-lookup"><span data-stu-id="0918e-125">It also must calculate which area of its input image the shaders need to read from to render the requested output region.</span></span>
4.  <span data-ttu-id="0918e-126">著色器：當應用程式建立 Direct3D 裝置) 時指定軟體轉譯時，會針對 GPU (或 CPU 上的轉換輸入執行著色器。</span><span class="sxs-lookup"><span data-stu-id="0918e-126">Shader: A shader is executed against the transform's input on the GPU (or CPU if software rendering is specified when the app creates the Direct3D device).</span></span> <span data-ttu-id="0918e-127">效果著色器會以高階網底語言撰寫 ([HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) ，並在效果的編譯期間編譯成位元組程式碼，然後在執行時間由效果載入。</span><span class="sxs-lookup"><span data-stu-id="0918e-127">Effect shaders are written in High Level Shading Language ([HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) and are compiled into byte code during the effect's compilation, which is then loaded by the effect during run-time.</span></span> <span data-ttu-id="0918e-128">本參考檔說明如何撰寫符合 [Direct2D](./direct2d-portal.md)規範的 HLSL。</span><span class="sxs-lookup"><span data-stu-id="0918e-128">This reference document describes how to write [Direct2D](./direct2d-portal.md)-compliant HLSL.</span></span> <span data-ttu-id="0918e-129">Direct3D 檔包含基本的 HLSL 總覽。</span><span class="sxs-lookup"><span data-stu-id="0918e-129">The Direct3D documentation contains a basic HLSL overview.</span></span>

## <a name="creating-an-effect-interface"></a><span data-ttu-id="0918e-130">建立效果介面</span><span class="sxs-lookup"><span data-stu-id="0918e-130">Creating an effect interface</span></span>

<span data-ttu-id="0918e-131">效果介面會定義應用程式與自訂效果的互動方式。</span><span class="sxs-lookup"><span data-stu-id="0918e-131">The effect interface defines how an app interacts with the custom effect.</span></span> <span data-ttu-id="0918e-132">若要建立效果介面，類別必須執行 ID2D1EffectImpl、定義描述效果 (的中繼資料，例如其名稱、輸入計數和屬性) ，以及建立註冊自訂效果以搭配 [Direct2D](./direct2d-portal.md)使用的方法。</span><span class="sxs-lookup"><span data-stu-id="0918e-132">To create an effect interface, a class must implement ID2D1EffectImpl, define metadata that describes the effect (such as its name, input count and properties), and create methods that register the custom effect for use with [Direct2D](./direct2d-portal.md).</span></span>

<span data-ttu-id="0918e-133">一旦執行效果介面的所有元件之後，類別的標頭就會如下所示：</span><span class="sxs-lookup"><span data-stu-id="0918e-133">Once all of the components for an effect interface have been implemented, the class' header will appear like this:</span></span>


```C++
#include <d2d1_1.h>
#include <d2d1effectauthor.h>  
#include <d2d1effecthelpers.h>

// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);

class SampleEffect : public ID2D1EffectImpl
{
public:
    // 2.1 Declare ID2D1EffectImpl implementation methods.
    IFACEMETHODIMP Initialize(
        _In_ ID2D1EffectContext* pContextInternal,
        _In_ ID2D1TransformGraph* pTransformGraph
        );

    IFACEMETHODIMP PrepareForRender(D2D1_CHANGE_TYPE changeType);
    IFACEMETHODIMP SetGraph(_In_ ID2D1TransformGraph* pGraph);

    // 2.2 Declare effect registration methods.
    static HRESULT Register(_In_ ID2D1Factory1* pFactory);
    static HRESULT CreateEffect(_Outptr_ IUnknown** ppEffectImpl);

    // 2.3 Declare IUnknown implementation methods.
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(_In_ REFIID riid, _Outptr_ void** ppOutput);

private:
    // Constructor should be private since it should never be called externally.
    SampleEffect();

    LONG m_refCount; // Internal ref count used by AddRef() and Release() methods.
};
```



### <a name="implement-id2d1effectimpl"></a><span data-ttu-id="0918e-134">執行 ID2D1EffectImpl</span><span class="sxs-lookup"><span data-stu-id="0918e-134">Implement ID2D1EffectImpl</span></span>

<span data-ttu-id="0918e-135">[**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl)介面包含您必須執行的三個方法：</span><span class="sxs-lookup"><span data-stu-id="0918e-135">The [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) interface contains three methods that you must implement:</span></span>

### <a name="initializeid2d1effectcontext-pcontextinternal-id2d1transformgraph-ptransformgraph"></a><span data-ttu-id="0918e-136">Initialize (ID2D1EffectCoNtext \* pCoNtextInternal，ID2D1TransformGraph \* pTransformGraph) </span><span class="sxs-lookup"><span data-stu-id="0918e-136">Initialize(ID2D1EffectContext \*pContextInternal, ID2D1TransformGraph \*pTransformGraph)</span></span>

<span data-ttu-id="0918e-137">[Direct2D](./direct2d-portal.md)會在應用程式呼叫 [**ID2D1DeviceCoNtext：： CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect)方法之後，呼叫 [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize)方法。</span><span class="sxs-lookup"><span data-stu-id="0918e-137">[Direct2D](./direct2d-portal.md) calls the [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method after the [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method has been called by the app.</span></span> <span data-ttu-id="0918e-138">您可以使用這個方法來執行內部初始化或此效果所需的任何其他作業。</span><span class="sxs-lookup"><span data-stu-id="0918e-138">You can use this method to perform internal initialization or any other operations needed for the effect.</span></span> <span data-ttu-id="0918e-139">此外，您可以使用它來建立效果的初始轉換圖形。</span><span class="sxs-lookup"><span data-stu-id="0918e-139">Additionally, you can use it to create the effect's initial transform graph.</span></span>

### <a name="setgraphid2d1transformgraph-ptransformgraph"></a><span data-ttu-id="0918e-140">SetGraph (ID2D1TransformGraph \* pTransformGraph) </span><span class="sxs-lookup"><span data-stu-id="0918e-140">SetGraph(ID2D1TransformGraph \*pTransformGraph)</span></span>

<span data-ttu-id="0918e-141">當效果的輸入數目變更時， [Direct2D](./direct2d-portal.md)會呼叫 [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph)方法。</span><span class="sxs-lookup"><span data-stu-id="0918e-141">[Direct2D](./direct2d-portal.md) calls the [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) method when the number of inputs to the effect is changed.</span></span> <span data-ttu-id="0918e-142">雖然大部分的效果都有固定數目的輸入，但其他像是 [複合效果](composite.md) 的輸入則支援可變的輸入數目。</span><span class="sxs-lookup"><span data-stu-id="0918e-142">While most effects have a constant number of inputs, others like the [Composite effect](composite.md) support a variable number of inputs.</span></span> <span data-ttu-id="0918e-143">此方法可讓這些效果更新其轉換圖形，以回應變更的輸入計數。</span><span class="sxs-lookup"><span data-stu-id="0918e-143">This method allows these effects to update their transform graph in response to a changing input count.</span></span> <span data-ttu-id="0918e-144">如果效果不支援變數輸入計數，則這個方法只會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="0918e-144">If an effect does not support a variable input count, this method can simply return E\_NOTIMPL.</span></span>

### <a name="prepareforrender-d2d1_change_type-changetype"></a><span data-ttu-id="0918e-145">PrepareForRender (D2D1 \_ 變更 \_ 類型 changeType) </span><span class="sxs-lookup"><span data-stu-id="0918e-145">PrepareForRender (D2D1\_CHANGE\_TYPE changeType)</span></span>

<span data-ttu-id="0918e-146">[**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender)方法可讓您有機會執行任何作業，以回應外部變更。</span><span class="sxs-lookup"><span data-stu-id="0918e-146">The [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) method provides an opportunity for effects to perform any operations in response to external changes.</span></span> <span data-ttu-id="0918e-147">如果至少有一個條件成立， [Direct2D](./direct2d-portal.md)就會在呈現效果之前呼叫這個方法：</span><span class="sxs-lookup"><span data-stu-id="0918e-147">[Direct2D](./direct2d-portal.md) calls this method just before it renders an effect if at least one of these is true:</span></span>

-   <span data-ttu-id="0918e-148">效果先前已初始化但尚未繪製。</span><span class="sxs-lookup"><span data-stu-id="0918e-148">The effect has been previously initialized but not yet drawn.</span></span>
-   <span data-ttu-id="0918e-149">效果屬性自上次繪製呼叫之後已經變更。</span><span class="sxs-lookup"><span data-stu-id="0918e-149">An effect property has changed since the last draw call.</span></span>
-   <span data-ttu-id="0918e-150">呼叫 [Direct2D](./direct2d-portal.md) 內容的狀態 (例如 DPI) 自上次繪製呼叫之後已經變更。</span><span class="sxs-lookup"><span data-stu-id="0918e-150">The state of the calling [Direct2D](./direct2d-portal.md) context (like DPI) has changed since the last draw call.</span></span>

### <a name="implement-the-effect-registration-and-callback-methods"></a><span data-ttu-id="0918e-151">實行效果註冊和回呼方法</span><span class="sxs-lookup"><span data-stu-id="0918e-151">Implement the effect registration and callback methods</span></span>

<span data-ttu-id="0918e-152">應用程式必須先向 [Direct2D](./direct2d-portal.md) 註冊效果，才能將其具現化。</span><span class="sxs-lookup"><span data-stu-id="0918e-152">Apps must register effects with [Direct2D](./direct2d-portal.md) before instantiating them.</span></span> <span data-ttu-id="0918e-153">此註冊的範圍是 Direct2D factory 的實例，而且必須在每次執行應用程式時重複。</span><span class="sxs-lookup"><span data-stu-id="0918e-153">This registration is scoped to an instance of a Direct2D factory, and must be repeated each time the app is run.</span></span> <span data-ttu-id="0918e-154">若要啟用此註冊，自訂效果會定義唯一的 GUID、註冊效果的公用方法，以及傳回效果實例的私用回呼方法。</span><span class="sxs-lookup"><span data-stu-id="0918e-154">To enable this registration, a custom effect defines a unique GUID, a public method that registers the effect, and a private callback method that returns an instance of the effect.</span></span>

### <a name="define-a-guid"></a><span data-ttu-id="0918e-155">定義 GUID</span><span class="sxs-lookup"><span data-stu-id="0918e-155">Define a GUID</span></span>

<span data-ttu-id="0918e-156">您必須定義可唯一識別 [Direct2D](./direct2d-portal.md)註冊效果的 GUID。</span><span class="sxs-lookup"><span data-stu-id="0918e-156">You must define a GUID that uniquely identifies the effect for registration with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="0918e-157">應用程式在呼叫 [**ID2D1DeviceCoNtext：： CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect)時，會使用相同的來識別效果。</span><span class="sxs-lookup"><span data-stu-id="0918e-157">The app uses the same to identify the effect when it calls [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).</span></span>

<span data-ttu-id="0918e-158">這段程式碼示範如何定義效果的這類 GUID。</span><span class="sxs-lookup"><span data-stu-id="0918e-158">This code demonstrates defining such a GUID for an effect.</span></span> <span data-ttu-id="0918e-159">您必須使用 GUID 產生工具（例如 guidgen.exe）來建立自己的唯一 GUID。</span><span class="sxs-lookup"><span data-stu-id="0918e-159">You must create its own unique GUID using a GUID generation tool such as guidgen.exe.</span></span>


```C++
// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="define-a-public-registration-method"></a><span data-ttu-id="0918e-160">定義公用註冊方法</span><span class="sxs-lookup"><span data-stu-id="0918e-160">Define a public registration method</span></span>

<span data-ttu-id="0918e-161">接下來，定義應用程式呼叫的公用方法，以使用 [Direct2D](./direct2d-portal.md)註冊效果。</span><span class="sxs-lookup"><span data-stu-id="0918e-161">Next, define a public method for the app to call to register the effect with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="0918e-162">因為效果註冊是 Direct2D factory 實例特有的，所以此方法會接受 [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) 介面作為參數。</span><span class="sxs-lookup"><span data-stu-id="0918e-162">Because effect registration is specific to an instance of a Direct2D factory, the method accepts an [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) interface as a parameter.</span></span> <span data-ttu-id="0918e-163">方法接著會在 **ID2D1Factory1** 參數上呼叫 [**ID2D1Factory1：： RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API，以註冊效果。</span><span class="sxs-lookup"><span data-stu-id="0918e-163">To register the effect, the method then calls the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API on the **ID2D1Factory1** parameter.</span></span>

<span data-ttu-id="0918e-164">此 API 接受 XML 字串來描述效果的中繼資料、輸入和屬性。</span><span class="sxs-lookup"><span data-stu-id="0918e-164">This API accepts an XML string that describes the metadata, inputs, and properties of the effect.</span></span> <span data-ttu-id="0918e-165">效果的中繼資料僅供資訊參考之用，並可透過 [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) 介面查詢應用程式。</span><span class="sxs-lookup"><span data-stu-id="0918e-165">The metadata for an effect is for informational purposes only, and can be queried by the app through the [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) interface.</span></span> <span data-ttu-id="0918e-166">另一方面，輸入和屬性資料是由 [Direct2D](./direct2d-portal.md) 使用，代表效果的功能。</span><span class="sxs-lookup"><span data-stu-id="0918e-166">The input and property data, on the other hand, is used by [Direct2D](./direct2d-portal.md) and represents the effect's functionality.</span></span>

<span data-ttu-id="0918e-167">以下顯示基本範例效果的 XML 字串。</span><span class="sxs-lookup"><span data-stu-id="0918e-167">An XML string for a minimal sample effect is shown here.</span></span> <span data-ttu-id="0918e-168">將自訂屬性新增至效果區段中包含了 XML 的自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="0918e-168">Adding custom properties to the XML is covered in the Adding custom properties to an effect section.</span></span>


```XML
#define XML(X) TEXT(#X) // This macro creates a single string from multiple lines of text.

PCWSTR pszXml =
    XML(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description' type='string' value='This is a demo effect.'/>
            <Inputs>
                <Input name='SourceOne'/>
                <!-- <Input name='SourceTwo'/> -->
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
        </Effect>
        );
```



### <a name="define-an-effect-factory-callback-method"></a><span data-ttu-id="0918e-169">定義效果 factory 回呼方法</span><span class="sxs-lookup"><span data-stu-id="0918e-169">Define an effect factory callback method</span></span>

<span data-ttu-id="0918e-170">效果也必須提供私用回呼方法，以透過單一 IUnknown 參數傳回效果的實例 \* \* 。</span><span class="sxs-lookup"><span data-stu-id="0918e-170">The effect must also provide a private callback method that returns an instance of the effect through a single IUnknown\*\* parameter.</span></span> <span data-ttu-id="0918e-171">當透過 [**ID2D1Factory1：： RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API 透過 [**PD2D1 \_ 效果 \_ FACTORY**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory)參數註冊效果時，會提供此方法的指標給 [Direct2D](./direct2d-portal.md) \\ 。</span><span class="sxs-lookup"><span data-stu-id="0918e-171">A pointer to this method is provided to [Direct2D](./direct2d-portal.md) when the effect is registered via the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API through the [**PD2D1\_EFFECT\_FACTORY**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory)\\ parameter.</span></span>


```C++
HRESULT __stdcall SampleEffect::CreateEffect(_Outptr_ IUnknown** ppEffectImpl)
{
    // This code assumes that the effect class initializes its reference count to 1.
    *ppEffectImpl = static_cast<ID2D1EffectImpl*>(new SampleEffect());

    if (*ppEffectImpl == nullptr)
    {
        return E_OUTOFMEMORY;
    }

    return S_OK;
}
```



### <a name="implement-the-iunknown-interface"></a><span data-ttu-id="0918e-172">執行 IUnknown 介面</span><span class="sxs-lookup"><span data-stu-id="0918e-172">Implement the IUnknown interface</span></span>

<span data-ttu-id="0918e-173">最後，效果必須執行 IUnknown 介面，以與 COM 相容。</span><span class="sxs-lookup"><span data-stu-id="0918e-173">Finally, the effect must implement the IUnknown interface for compatibility with COM.</span></span>

## <a name="creating-the-effects-transform-graph"></a><span data-ttu-id="0918e-174">建立效果的轉換圖形</span><span class="sxs-lookup"><span data-stu-id="0918e-174">Creating the effect's transform graph</span></span>

<span data-ttu-id="0918e-175">效果可以使用數種不同的轉換 (個別的影像作業) 來建立其所需的影像效果。</span><span class="sxs-lookup"><span data-stu-id="0918e-175">An effect can use several different transforms (individual image operations) to create its desired imaging effect.</span></span> <span data-ttu-id="0918e-176">為了控制這些轉換套用至輸入影像的順序，效果會將它們排列成轉換圖形。</span><span class="sxs-lookup"><span data-stu-id="0918e-176">To control the order in which these transforms are applied to the input image, the effect arranges them into a transform graph.</span></span> <span data-ttu-id="0918e-177">轉換圖可利用 [Direct2D](./direct2d-portal.md) 中包含的效果和轉換，以及效果作者所建立的自訂轉換。</span><span class="sxs-lookup"><span data-stu-id="0918e-177">A transform graph can make use of the effects and transforms included in [Direct2D](./direct2d-portal.md) as well as custom transforms created by the effect author.</span></span>

### <a name="using-transforms-included-with-direct2d"></a><span data-ttu-id="0918e-178">使用 Direct2D 隨附的轉換</span><span class="sxs-lookup"><span data-stu-id="0918e-178">Using transforms included with Direct2D</span></span>

<span data-ttu-id="0918e-179">這些是 [Direct2D](./direct2d-portal.md)所提供的最常使用轉換。</span><span class="sxs-lookup"><span data-stu-id="0918e-179">These are the most commonly used transforms provided with [Direct2D](./direct2d-portal.md).</span></span>

-   <span data-ttu-id="0918e-180">[**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform)：這項轉換會根據 blend 描述將任意數目的輸入混合在一起，請參閱 [**D2D1 \_ blend \_ 描述**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) 主題和混合範例的 [Direct2D 複合效果模式範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) 。</span><span class="sxs-lookup"><span data-stu-id="0918e-180">[**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): This transform blends an arbitrary number of inputs together based on a blend description, see the [**D2D1\_BLEND\_DESCRIPTION**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) topic and the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) for blending examples.</span></span> <span data-ttu-id="0918e-181">[**ID2D1EffectCoNtext：： CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform)方法會傳回這項轉換。</span><span class="sxs-lookup"><span data-stu-id="0918e-181">This transform is returned by the [**ID2D1EffectContext::CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) method.</span></span>
-   <span data-ttu-id="0918e-182">[**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform)：此轉換會根據指定的 [**D2D1 \_ 擴充 \_ 模式**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) 來展開影像的輸出大小。</span><span class="sxs-lookup"><span data-stu-id="0918e-182">[**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): This transform expands an image's output size according to the [**D2D1\_EXTEND\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) specified.</span></span> <span data-ttu-id="0918e-183">[**ID2D1EffectCoNtext：： CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform)方法會傳回這項轉換。</span><span class="sxs-lookup"><span data-stu-id="0918e-183">This transform is returned by the [**ID2D1EffectContext::CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) method.</span></span>
-   <span data-ttu-id="0918e-184">[**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform)：此轉換位移 (會將) 其輸入轉譯為任何整數的圖元數。</span><span class="sxs-lookup"><span data-stu-id="0918e-184">[**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): This transform offsets (translates) its input by any whole number of pixels.</span></span> <span data-ttu-id="0918e-185">[**ID2D1EffectCoNtext：： CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform)方法會傳回這項轉換。</span><span class="sxs-lookup"><span data-stu-id="0918e-185">This transform is returned by the [**ID2D1EffectContext::CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) method.</span></span>
-   <span data-ttu-id="0918e-186">您可以使用 [**ID2D1EffectCoNtext：： CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) 方法，將任何現有的效果視為轉換圖形建立用途的轉換。</span><span class="sxs-lookup"><span data-stu-id="0918e-186">Any existing effect can be treated as a transform for the purposes of transform graph creation by using the [**ID2D1EffectContext::CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) method.</span></span>

### <a name="creating-a-single-node-transform-graph"></a><span data-ttu-id="0918e-187">建立單一節點的轉換圖形</span><span class="sxs-lookup"><span data-stu-id="0918e-187">Creating a single-node transform graph</span></span>

<span data-ttu-id="0918e-188">建立轉換之後，效果的輸入必須連接到轉換的輸入，且轉換的輸出必須連接到效果的輸出。</span><span class="sxs-lookup"><span data-stu-id="0918e-188">Once you create a transform, the effect's input needs to be connected to the transform's input, and the transform's output needs to be connected to the effect's output.</span></span> <span data-ttu-id="0918e-189">如果效果只包含單一轉換，您可以使用 [**ID2D1TransformGraph：： SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) 方法輕鬆完成此動作。</span><span class="sxs-lookup"><span data-stu-id="0918e-189">When an effect only contains a single transform, you can use the [**ID2D1TransformGraph::SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) method to easily accomplish this.</span></span>

<span data-ttu-id="0918e-190">您可以使用提供的 ID2D1TransformGraph 參數，在效果的 [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) 或 [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) 方法中建立或修改轉換。</span><span class="sxs-lookup"><span data-stu-id="0918e-190">You can create or modify a transform in the effect's [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) or [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) methods using the provided ID2D1TransformGraph parameter.</span></span> <span data-ttu-id="0918e-191">如果效果需要在無法使用此參數的另一個方法中變更轉換圖形，效果可以將 [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) 參數儲存為類別的成員變數，並在其他位置存取它，例如 [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) 或自訂屬性回呼方法。</span><span class="sxs-lookup"><span data-stu-id="0918e-191">If an effect needs to make changes to the transform graph in another method where this parameter is not available, the effect can save the [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) parameter as a member variable of the class and access it elsewhere, such as [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) or a custom property callback method.</span></span>

<span data-ttu-id="0918e-192">範例 [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) 方法如下所示。</span><span class="sxs-lookup"><span data-stu-id="0918e-192">A sample [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method is shown here.</span></span> <span data-ttu-id="0918e-193">這個方法會建立單一節點的轉換圖形，將每個軸中的影像位移100圖元。</span><span class="sxs-lookup"><span data-stu-id="0918e-193">This method creates a single-node transform graph that offsets the image by one hundred pixels in each axis.</span></span>


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext,
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{
    HRESULT hr = pEffectContext->CreateOffsetTransform(
        D2D1::Point2L(100,100),  // Offsets the input by 100px in each axis.
        &m_pOffsetTransform
        );

    if (SUCCEEDED(hr))
    {
        // Connects the effect's input to the transform's input, and connects
        // the transform's output to the effect's output.
        hr = pTransformGraph->SetSingleTransformNode(m_pOffsetTransform);
    }

    return hr;
}
```



### <a name="creating-a-multi-node-transform-graph"></a><span data-ttu-id="0918e-194">建立多節點轉換圖形</span><span class="sxs-lookup"><span data-stu-id="0918e-194">Creating a multi-node transform graph</span></span>

<span data-ttu-id="0918e-195">將多個轉換新增至效果的轉換圖，可讓您在內部執行多個映射作業，並以單一整合效果的形式呈現給應用程式。</span><span class="sxs-lookup"><span data-stu-id="0918e-195">Adding multiple transforms to an effect's transform graph allows effects to internally perform multiple image operations that are presented to an app as a single unified effect.</span></span>

<span data-ttu-id="0918e-196">如上所述，使用在效果的 [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize)方法中收到的 [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph)參數，可在任何效果方法中編輯效果的轉換圖形。</span><span class="sxs-lookup"><span data-stu-id="0918e-196">As noted above, the effect's transform graph may be edited in any effect method using the [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) parameter received in the effect's [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method.</span></span> <span data-ttu-id="0918e-197">您可以使用該介面上的下列 Api 來建立或修改效果的轉換圖形：</span><span class="sxs-lookup"><span data-stu-id="0918e-197">The following APIs on that interface can be used to create or modify an effect's transform graph:</span></span>

### <a name="addnodeid2d1transformnode-pnode"></a><span data-ttu-id="0918e-198">AddNode (ID2D1TransformNode \* pNode) </span><span class="sxs-lookup"><span data-stu-id="0918e-198">AddNode(ID2D1TransformNode \*pNode)</span></span>

<span data-ttu-id="0918e-199">實際上， [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) 方法會「註冊」具有效果的轉換，而且必須在轉換可以與任何其他轉換圖表方法搭配使用之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="0918e-199">The [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) method, in effect, 'registers' the transform with the effect, and must be called before the transform can be used with any of the other transform graph methods.</span></span>

### <a name="connecttoeffectinputuint32-toeffectinputindex-id2d1transformnode-pnode-uint32-tonodeinputindex"></a><span data-ttu-id="0918e-200">ConnectToEffectInput (UINT32 toEffectInputIndex、ID2D1TransformNode \* pNode、UINT32 toNodeInputIndex) </span><span class="sxs-lookup"><span data-stu-id="0918e-200">ConnectToEffectInput(UINT32 toEffectInputIndex, ID2D1TransformNode \*pNode, UINT32 toNodeInputIndex)</span></span>

<span data-ttu-id="0918e-201">[**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput)方法會將效果的影像輸入連接至轉換的輸入。</span><span class="sxs-lookup"><span data-stu-id="0918e-201">The [**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) method connects the effect's image input to a transform's input.</span></span> <span data-ttu-id="0918e-202">相同的效果輸入可以連接到多個轉換。</span><span class="sxs-lookup"><span data-stu-id="0918e-202">The same effect input can be connected to multiple transforms.</span></span>

### <a name="connectnodeid2d1transformnode-pfromnode-id2d1transformnode-ptonode-uint32-tonodeinputindex"></a><span data-ttu-id="0918e-203">ConnectNode (ID2D1TransformNode \* pFromNode、ID2D1TransformNode \* PTONODE、UINT32 toNodeInputIndex) </span><span class="sxs-lookup"><span data-stu-id="0918e-203">ConnectNode(ID2D1TransformNode \*pFromNode, ID2D1TransformNode \*pToNode, UINT32 toNodeInputIndex)</span></span>

<span data-ttu-id="0918e-204">[**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode)方法會將轉換的輸出連接到另一個轉換的輸入。</span><span class="sxs-lookup"><span data-stu-id="0918e-204">The [**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) method connects a transform's output to another transform's input.</span></span> <span data-ttu-id="0918e-205">轉換輸出可以連接到多個轉換。</span><span class="sxs-lookup"><span data-stu-id="0918e-205">A transform output can be connected to multiple transforms.</span></span>

### <a name="setoutputnodeid2d1transformnode-pnode"></a><span data-ttu-id="0918e-206">SetOutputNode (ID2D1TransformNode \* pNode) </span><span class="sxs-lookup"><span data-stu-id="0918e-206">SetOutputNode(ID2D1TransformNode \*pNode)</span></span>

<span data-ttu-id="0918e-207">[**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode)方法會將轉換的輸出連接到效果的輸出。</span><span class="sxs-lookup"><span data-stu-id="0918e-207">The [**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) method connects a transform's output to the effect's output.</span></span> <span data-ttu-id="0918e-208">因為效果只會有一個輸出，所以只能將單一轉換指定為「輸出節點」。</span><span class="sxs-lookup"><span data-stu-id="0918e-208">Because an effect only has one output, only a single transform can be designated as the 'output node'.</span></span>

<span data-ttu-id="0918e-209">此程式碼會使用兩個不同的轉換來建立統一效果。</span><span class="sxs-lookup"><span data-stu-id="0918e-209">This code uses two separate transforms to create a unified effect.</span></span> <span data-ttu-id="0918e-210">在此情況下，效果是轉譯的陰影。</span><span class="sxs-lookup"><span data-stu-id="0918e-210">In this case, the effect is a translated drop shadow.</span></span>


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext, 
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{   
    // Create the shadow effect.
    HRESULT hr = pEffectContext->CreateEffect(CLSID_D2D1Shadow, &m_pShadowEffect);

    // Create the shadow transform from the shadow effect.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateTransformNodeFromEffect(m_pShadowEffect, &m_pShadowTransform);
    }

    // Create the offset transform.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateOffsetTransform(
            D2D1::Point2L(0,0),
            &m_pOffsetTransform
            );
    }

    // Register both transforms with the effect graph.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pShadowTransform);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pOffsetTransform);
    }

    // Connect the custom effect's input to the shadow transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectToEffectInput(
            0,                  // Input index of the effect.
            m_pShadowTransform, // The receiving transform.
            0                   // Input index of the receiving transform.
            );
    }

    // Connect the shadow transform's output to the offset transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectNode(
            m_pShadowTransform, // 'From' node.
            m_pOffsetTransform, // 'To' node.
            0                   // Input index of the 'to' node. There is only one output for the 'From' node.
            );
    }

    // Connect the offset transform's output to the custom effect's output.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->SetOutputNode(
            m_pOffsetTransform
            );
    }

    return hr;
}
```



## <a name="adding-custom-properties-to-an-effect"></a><span data-ttu-id="0918e-211">將自訂屬性新增至效果</span><span class="sxs-lookup"><span data-stu-id="0918e-211">Adding custom properties to an effect</span></span>

<span data-ttu-id="0918e-212">效果可以定義自訂屬性，以允許應用程式在執行時間變更效果的行為。</span><span class="sxs-lookup"><span data-stu-id="0918e-212">Effects can define custom properties that allow an app to change the effect's behavior during runtime.</span></span> <span data-ttu-id="0918e-213">定義自訂效果的屬性有三個步驟：</span><span class="sxs-lookup"><span data-stu-id="0918e-213">There are three steps to define a property for a custom effect:</span></span>

### <a name="add-the-property-metadata-to-the-effects-registration-data"></a><span data-ttu-id="0918e-214">將屬性中繼資料新增至效果的註冊資料</span><span class="sxs-lookup"><span data-stu-id="0918e-214">Add the property metadata to the effect's registration data</span></span>

### <a name="add-property-to-registration-xml"></a><span data-ttu-id="0918e-215">將屬性新增至註冊 XML</span><span class="sxs-lookup"><span data-stu-id="0918e-215">Add property to registration XML</span></span>

<span data-ttu-id="0918e-216">您必須在效果的初始註冊時，定義自訂效果的屬性（ [Direct2D](./direct2d-portal.md)）。</span><span class="sxs-lookup"><span data-stu-id="0918e-216">You must define a custom effect's properties during the effect's initial registration with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="0918e-217">首先，您必須使用新的屬性，更新其公開註冊方法中的效果註冊 XML：</span><span class="sxs-lookup"><span data-stu-id="0918e-217">First, you must update the effect's registration XML in its public registration method with the new property:</span></span>


```C++
PCWSTR pszXml =
    TEXT(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description'
                type='string'
                value='Translates an image by a user-specifiable amount.'/>
            <Inputs>
                <Input name='Source'/>
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
            <Property name='Offset' type='vector2'>
                <Property name='DisplayName' type='string' value='Image Offset'/>
                <!— Optional sub-properties -->
                <Property name='Min' type='vector2' value='(-1000.0, -1000.0)' />
                <Property name='Max' type='vector2' value='(1000.0, 1000.0)' />
                <Property name='Default' type='vector2' value='(0.0, 0.0)' />
            </Property>
        </Effect>
        );
```



<span data-ttu-id="0918e-218">當您在 XML 中定義效果屬性時，它需要名稱、類型和顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="0918e-218">When you define an effect property in XML, it needs a name, a type, and a display name.</span></span> <span data-ttu-id="0918e-219">屬性的顯示名稱，以及整體效果的類別、作者和描述值都可以當地語系化。</span><span class="sxs-lookup"><span data-stu-id="0918e-219">A property's display name, as well as the overall effect's category, author, and description values can and should be localized.</span></span>

<span data-ttu-id="0918e-220">針對每個屬性，效果可以選擇性地指定預設值、最小值和最大值。</span><span class="sxs-lookup"><span data-stu-id="0918e-220">For each property, an effect can optionally specify default, min, and max values.</span></span> <span data-ttu-id="0918e-221">這些值僅供參考之用。</span><span class="sxs-lookup"><span data-stu-id="0918e-221">These values are for informational use only.</span></span> <span data-ttu-id="0918e-222">[Direct2D](./direct2d-portal.md)不會強制執行。</span><span class="sxs-lookup"><span data-stu-id="0918e-222">They are not enforced by [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="0918e-223">您必須自行在效果類別中執行任何指定的預設/最小/最大邏輯。</span><span class="sxs-lookup"><span data-stu-id="0918e-223">It is up to you to implement any specified default/min/max logic in the effect class yourself.</span></span>

<span data-ttu-id="0918e-224">在 XML 中針對屬性所列的類型值，必須符合屬性的 getter 和 setter 方法所使用的對應資料類型。</span><span class="sxs-lookup"><span data-stu-id="0918e-224">The type value listed in the XML for the property must match the corresponding data type used by the property's getter and setter methods.</span></span> <span data-ttu-id="0918e-225">下表顯示每個資料類型的對應 XML 值：</span><span class="sxs-lookup"><span data-stu-id="0918e-225">Corresponding XML values for each data type are shown in this table:</span></span>



| <span data-ttu-id="0918e-226">資料類型</span><span class="sxs-lookup"><span data-stu-id="0918e-226">Data type</span></span>                                                                                                                              | <span data-ttu-id="0918e-227">對應的 XML 值</span><span class="sxs-lookup"><span data-stu-id="0918e-227">Corresponding XML value</span></span> |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span data-ttu-id="0918e-228">PWSTR</span><span class="sxs-lookup"><span data-stu-id="0918e-228">PWSTR</span></span>                                                                                                                                  | <span data-ttu-id="0918e-229">字串</span><span class="sxs-lookup"><span data-stu-id="0918e-229">string</span></span>                  |
| <span data-ttu-id="0918e-230">BOOL</span><span class="sxs-lookup"><span data-stu-id="0918e-230">BOOL</span></span>                                                                                                                                   | <span data-ttu-id="0918e-231">bool</span><span class="sxs-lookup"><span data-stu-id="0918e-231">bool</span></span>                    |
| <span data-ttu-id="0918e-232">UINT</span><span class="sxs-lookup"><span data-stu-id="0918e-232">UINT</span></span>                                                                                                                                   | <span data-ttu-id="0918e-233">uint32</span><span class="sxs-lookup"><span data-stu-id="0918e-233">uint32</span></span>                  |
| <span data-ttu-id="0918e-234">INT</span><span class="sxs-lookup"><span data-stu-id="0918e-234">INT</span></span>                                                                                                                                    | <span data-ttu-id="0918e-235">int32</span><span class="sxs-lookup"><span data-stu-id="0918e-235">int32</span></span>                   |
| <span data-ttu-id="0918e-236">FLOAT</span><span class="sxs-lookup"><span data-stu-id="0918e-236">FLOAT</span></span>                                                                                                                                  | <span data-ttu-id="0918e-237">FLOAT</span><span class="sxs-lookup"><span data-stu-id="0918e-237">float</span></span>                   |
| [<span data-ttu-id="0918e-238">**D2D \_ 向量 \_ 2f**</span><span class="sxs-lookup"><span data-stu-id="0918e-238">**D2D\_VECTOR\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f)                                                                                               | <span data-ttu-id="0918e-239">vector2</span><span class="sxs-lookup"><span data-stu-id="0918e-239">vector2</span></span>                 |
| [<span data-ttu-id="0918e-240">**D2D \_ 向量 \_ 3F**</span><span class="sxs-lookup"><span data-stu-id="0918e-240">**D2D\_VECTOR\_3F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f)                                                                                               | <span data-ttu-id="0918e-241">vector3</span><span class="sxs-lookup"><span data-stu-id="0918e-241">vector3</span></span>                 |
| [<span data-ttu-id="0918e-242">**D2D \_ 向量 \_ 4F**</span><span class="sxs-lookup"><span data-stu-id="0918e-242">**D2D\_VECTOR\_4F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f)                                                                                               | <span data-ttu-id="0918e-243">vector4</span><span class="sxs-lookup"><span data-stu-id="0918e-243">vector4</span></span>                 |
| <span data-ttu-id="0918e-244">[**D2D \_ 矩陣 \_ 3X2 \_ F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool))</span><span class="sxs-lookup"><span data-stu-id="0918e-244">[**D2D\_MATRIX\_3X2\_F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool))</span></span> | <span data-ttu-id="0918e-245">matrix3x2</span><span class="sxs-lookup"><span data-stu-id="0918e-245">matrix3x2</span></span>               |
| [<span data-ttu-id="0918e-246">**D2D \_ 矩陣 \_ 4X3 \_ F**</span><span class="sxs-lookup"><span data-stu-id="0918e-246">**D2D\_MATRIX\_4X3\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)                                                                                        | <span data-ttu-id="0918e-247">matrix4x3</span><span class="sxs-lookup"><span data-stu-id="0918e-247">matrix4x3</span></span>               |
| [<span data-ttu-id="0918e-248">**D2D \_ 矩陣 \_ 4x4 \_ F**</span><span class="sxs-lookup"><span data-stu-id="0918e-248">**D2D\_MATRIX\_4X4\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f)                                                                                        | <span data-ttu-id="0918e-249">matrix4x4</span><span class="sxs-lookup"><span data-stu-id="0918e-249">matrix4x4</span></span>               |
| [<span data-ttu-id="0918e-250">**D2D \_ 矩陣 \_ 5X4 \_ F**</span><span class="sxs-lookup"><span data-stu-id="0918e-250">**D2D\_MATRIX\_5X4\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f)                                                                                        | <span data-ttu-id="0918e-251">matrix5x4</span><span class="sxs-lookup"><span data-stu-id="0918e-251">matrix5x4</span></span>               |
| <span data-ttu-id="0918e-252">位元組\[\]</span><span class="sxs-lookup"><span data-stu-id="0918e-252">BYTE\[\]</span></span>                                                                                                                               | <span data-ttu-id="0918e-253">blob</span><span class="sxs-lookup"><span data-stu-id="0918e-253">blob</span></span>                    |
| <span data-ttu-id="0918e-254">IUnknown\*</span><span class="sxs-lookup"><span data-stu-id="0918e-254">IUnknown\*</span></span>                                                                                                                             | <span data-ttu-id="0918e-255">iunknown</span><span class="sxs-lookup"><span data-stu-id="0918e-255">iunknown</span></span>                |
| <span data-ttu-id="0918e-256">[**ID2D1ColorCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*</span><span class="sxs-lookup"><span data-stu-id="0918e-256">[**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*</span></span>                                                                                       | <span data-ttu-id="0918e-257">colorcoNtext</span><span class="sxs-lookup"><span data-stu-id="0918e-257">colorcontext</span></span>            |
| <span data-ttu-id="0918e-258">CLSID</span><span class="sxs-lookup"><span data-stu-id="0918e-258">CLSID</span></span>                                                                                                                                  | <span data-ttu-id="0918e-259">clsid</span><span class="sxs-lookup"><span data-stu-id="0918e-259">clsid</span></span>                   |
| <span data-ttu-id="0918e-260">列舉 ([**D2D1 \_ 插補 \_ 模式**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode)等 ) </span><span class="sxs-lookup"><span data-stu-id="0918e-260">Enumeration ([**D2D1\_INTERPOLATION\_MODE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode), etc.)</span></span>                                                | <span data-ttu-id="0918e-261">列舉</span><span class="sxs-lookup"><span data-stu-id="0918e-261">enum</span></span>                    |



 

### <a name="map-the-new-property-to-getter-and-setter-methods"></a><span data-ttu-id="0918e-262">將新的屬性對應至 getter 和 setter 方法</span><span class="sxs-lookup"><span data-stu-id="0918e-262">Map the new property to getter and setter methods</span></span>

<span data-ttu-id="0918e-263">接下來，效果必須將這個新的屬性對應至 getter 和 setter 方法。</span><span class="sxs-lookup"><span data-stu-id="0918e-263">Next, the effect must map this new property to getter and setter methods.</span></span> <span data-ttu-id="0918e-264">這是透過傳遞至 [**ID2D1Factory1：： RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring)方法的 [**D2D1 \_ 屬性 \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding)系結陣列來完成。</span><span class="sxs-lookup"><span data-stu-id="0918e-264">This is done through the [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array that is passed into the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) method.</span></span>

<span data-ttu-id="0918e-265">[**D2D1 \_ 屬性 \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding)系結陣列看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="0918e-265">The [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array looks like this:</span></span>


```C++
const D2D1_PROPERTY_BINDING bindings[] =
{
    D2D1_VALUE_TYPE_BINDING(
        L"Offset",      // The name of property. Must match name attribute in XML.
        &SetOffset,     // The setter method that is called on "SetValue".
        &GetOffset      // The getter method that is called on "GetValue".
        )
};
```



<span data-ttu-id="0918e-266">建立 XML 和系結陣列之後，請將其傳遞至 [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) 方法：</span><span class="sxs-lookup"><span data-stu-id="0918e-266">Once you create the XML and bindings array, pass them into the [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) method:</span></span>


```C++
pFactory->RegisterEffectFromString(
    CLSID_SampleEffect,  // GUID defined in class header file.
    pszXml,              // Previously-defined XML that describes effect.
    bindings,            // The previously-defined property bindings array.
    ARRAYSIZE(bindings), // Number of entries in the property bindings array.    
    CreateEffect         // Static method that returns an instance of the effect's class.
    );
```



<span data-ttu-id="0918e-267">D2D1 VALUE 型別系結 \_ \_ \_ 宏需要效果類別在其他任何介面之前繼承自 [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) 。</span><span class="sxs-lookup"><span data-stu-id="0918e-267">The D2D1\_VALUE\_TYPE\_BINDING macro requires the effect class to inherit from [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) before any other interface.</span></span>

<span data-ttu-id="0918e-268">效果的自訂屬性會依照在 XML 中宣告的順序來編制索引，而一旦建立之後，應用程式就可以使用 [**ID2D1Properties：： SetValue**](id2d1properties-setvalue-overload.md) 和 [**ID2D1Properties：： GetValue**](id2d1properties-getvalue-overload.md) 方法來存取這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0918e-268">Custom properties for an effect are indexed in the order they are declared in the XML, and once created can be accessed by the app using the [**ID2D1Properties::SetValue**](id2d1properties-setvalue-overload.md) and [**ID2D1Properties::GetValue**](id2d1properties-getvalue-overload.md) methods.</span></span> <span data-ttu-id="0918e-269">為了方便起見，您可以建立公用列舉，以列出效果標頭檔中的每個屬性：</span><span class="sxs-lookup"><span data-stu-id="0918e-269">For convenience, you can create a public enumeration that lists each property in the effect's header file:</span></span>


```C++
typedef enum SAMPLEEFFECT_PROP
{
    SAMPLEFFECT_PROP_OFFSET = 0
};
```



### <a name="create-the-getter-and-setter-methods-for-the-property"></a><span data-ttu-id="0918e-270">建立屬性的 getter 和 setter 方法</span><span class="sxs-lookup"><span data-stu-id="0918e-270">Create the getter and setter methods for the property</span></span>

<span data-ttu-id="0918e-271">下一步是建立新屬性的 getter 和 setter 方法。</span><span class="sxs-lookup"><span data-stu-id="0918e-271">The next step is to create the getter and setter methods for the new property.</span></span> <span data-ttu-id="0918e-272">方法的名稱必須符合 [**D2D1 \_ 屬性 \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) 系結陣列中所指定的名稱。</span><span class="sxs-lookup"><span data-stu-id="0918e-272">The names of the methods must match the ones specified in the [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array.</span></span> <span data-ttu-id="0918e-273">此外，在效果的 XML 中指定的屬性類型，必須符合 setter 方法參數的類型和 getter 方法的傳回值。</span><span class="sxs-lookup"><span data-stu-id="0918e-273">In addition, the property type specified in the effect's XML must match the type of the setter method's parameter and the getter method's return value.</span></span>


```C++
HRESULT SampleEffect::SetOffset(D2D_VECTOR_2F offset)
{
    // Method must manually clamp to values defined in XML.
    offset.x = min(offset.x, 1000.0f); 
    offset.x = max(offset.x, -1000.0f); 

    offset.y = min(offset.y, 1000.0f); 
    offset.y = max(offset.y, -1000.0f); 

    m_offset = offset;

    return S_OK;
}

D2D_VECTOR_2F SampleEffect::GetOffset() const
{
    return m_offset;
}
```



### <a name="update-effects-transforms-in-response-to-property-change"></a><span data-ttu-id="0918e-274">更新效果的轉換，以回應屬性變更</span><span class="sxs-lookup"><span data-stu-id="0918e-274">Update effect's transforms in response to property change</span></span>

<span data-ttu-id="0918e-275">若要實際更新效果的影像輸出以回應屬性變更，效果需要變更其基礎轉換。</span><span class="sxs-lookup"><span data-stu-id="0918e-275">To actually update an effect's image output in response to a property change, the effect needs to change its underlying transforms.</span></span> <span data-ttu-id="0918e-276">這通常會在效果的 [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) 方法中完成，而 [Direct2D](./direct2d-portal.md) 會在其中一個效果的屬性變更時自動呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="0918e-276">This is typically done in the effect's [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) method which [Direct2D](./direct2d-portal.md) automatically calls when one of an effect's properties has been changed.</span></span> <span data-ttu-id="0918e-277">不過，您可以在任何效果的方法中更新轉換：例如 Initialize 或效果的屬性 setter 方法。</span><span class="sxs-lookup"><span data-stu-id="0918e-277">However, transforms can be updated in any of the effect's methods: such as Initialize or the effect's property setter methods.</span></span>

<span data-ttu-id="0918e-278">例如，如果效果包含 [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) ，而且想要修改其位移值以回應變更的效果位移屬性，它會在 [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender)中新增下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="0918e-278">For example, if an effect contained an [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) and wanted to modify its offset value in response to the effect's Offset property being changed, it would add the following code in [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender):</span></span>


```C++
IFACEMETHODIMP SampleEffect::PrepareForRender(D2D1_CHANGE_TYPE changeType)
{
    // All effect properties are DPI independent (specified in DIPs). In this offset
    // example, the offset value provided must be scaled from DIPs to pixels to ensure
    // a consistent appearance at different DPIs (excluding minor scaling artifacts).
    // A context's DPI can be retrieved using the ID2D1EffectContext::GetDPI API.
    
    D2D1_POINT_2L pixelOffset;
    pixelOffset.x = static_cast<LONG>(m_offset.x * (m_dpiX / 96.0f));
    pixelOffset.y = static_cast<LONG>(m_offset.y * (m_dpiY / 96.0f));
    
    // Update the effect's offset transform with the new offset value.
    m_pOffsetTransform->SetOffset(pixelOffset);

    return S_OK;
}
```



## <a name="creating-a-custom-transform"></a><span data-ttu-id="0918e-279">建立自訂轉換</span><span class="sxs-lookup"><span data-stu-id="0918e-279">Creating a custom transform</span></span>

<span data-ttu-id="0918e-280">若要在 [Direct2D](./direct2d-portal.md)中所提供的映射作業以外的範圍執行，您必須執行自訂轉換。</span><span class="sxs-lookup"><span data-stu-id="0918e-280">To implement image operations beyond what is provided in [Direct2D](./direct2d-portal.md), you must implement custom transforms.</span></span> <span data-ttu-id="0918e-281">自訂轉換可以使用自訂 HLSL 著色器，任意變更輸入影像。</span><span class="sxs-lookup"><span data-stu-id="0918e-281">Custom transforms can arbitrarily change an input image through the use of custom HLSL shaders.</span></span>

<span data-ttu-id="0918e-282">轉換會根據所使用的著色器類型來執行兩個不同介面的其中一個。</span><span class="sxs-lookup"><span data-stu-id="0918e-282">Transforms implement one of two different interfaces depending on the types of shaders they use.</span></span> <span data-ttu-id="0918e-283">使用圖元和/或頂點著色器的轉換必須執行 [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform)，而使用計算著色器的轉換必須執行 [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform)。</span><span class="sxs-lookup"><span data-stu-id="0918e-283">Transforms using pixel and/or vertex shaders must implement [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), while transforms using compute shaders must implement [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform).</span></span> <span data-ttu-id="0918e-284">這些介面都繼承自 [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)。</span><span class="sxs-lookup"><span data-stu-id="0918e-284">These interfaces both inherit from [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span></span> <span data-ttu-id="0918e-285">本節著重于如何執行兩者通用的功能。</span><span class="sxs-lookup"><span data-stu-id="0918e-285">This section focuses on implementing the functionality that is common to both.</span></span>

<span data-ttu-id="0918e-286">[**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)介面有四個要執行的方法：</span><span class="sxs-lookup"><span data-stu-id="0918e-286">The [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) interface has four methods to implement:</span></span>

### <a name="getinputcount"></a><span data-ttu-id="0918e-287">GetInputCount</span><span class="sxs-lookup"><span data-stu-id="0918e-287">GetInputCount</span></span>

<span data-ttu-id="0918e-288">這個方法會傳回整數，表示轉換的輸入計數。</span><span class="sxs-lookup"><span data-stu-id="0918e-288">This method returns an integer representing the input count for the transform.</span></span>


```C++
IFACEMETHODIMP_(UINT32) GetInputCount() const
{
    return 1;
}
```



### <a name="mapinputrectstooutputrect"></a><span data-ttu-id="0918e-289">MapInputRectsToOutputRect</span><span class="sxs-lookup"><span data-stu-id="0918e-289">MapInputRectsToOutputRect</span></span>

<span data-ttu-id="0918e-290">[Direct2D](./direct2d-portal.md) 會在每次轉譯轉換時呼叫 [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) 方法。</span><span class="sxs-lookup"><span data-stu-id="0918e-290">[Direct2D](./direct2d-portal.md) calls the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) method each time the transform is rendered.</span></span> <span data-ttu-id="0918e-291">Direct2D 會將代表每個輸入之界限的矩形傳遞至轉換。</span><span class="sxs-lookup"><span data-stu-id="0918e-291">Direct2D passes a rectangle representing the bounds of each of the inputs to the transform.</span></span> <span data-ttu-id="0918e-292">接著，轉換會負責計算輸出影像的界限。</span><span class="sxs-lookup"><span data-stu-id="0918e-292">The transform is then responsible for calculating the bounds of the output image.</span></span> <span data-ttu-id="0918e-293">這個介面上所有方法的矩形大小 ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) 是以圖元為單位來定義，而不是 dip。</span><span class="sxs-lookup"><span data-stu-id="0918e-293">The size of the rectangles for all the methods on this interface ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) are defined in pixels, not DIPs.</span></span>

<span data-ttu-id="0918e-294">這個方法也會根據其著色器的邏輯和每個輸入的不透明區域，負責計算不透明的輸出區域。</span><span class="sxs-lookup"><span data-stu-id="0918e-294">This method is also responsible for calculating the region of the output that is opaque based on the logic of its shader and the opaque regions of each input.</span></span> <span data-ttu-id="0918e-295">影像的不透明區域的定義，就是將整個矩形的 Alpha 色板視為 ' 1 '。</span><span class="sxs-lookup"><span data-stu-id="0918e-295">An opaque region of an image is defined as that where the alpha channel is '1' for the entirety of the rectangle.</span></span> <span data-ttu-id="0918e-296">如果不清楚轉換的輸出是否為不透明，則輸出不透明的矩形應該設定為 (0、0、0、0) 為安全值。</span><span class="sxs-lookup"><span data-stu-id="0918e-296">If it is unclear whether a transform's output is opaque, the output opaque rectangle should be set to (0, 0, 0, 0) as a safe value.</span></span> <span data-ttu-id="0918e-297">[Direct2D](./direct2d-portal.md) 會使用此資訊來執行具有「保證不透明」內容的轉譯優化。</span><span class="sxs-lookup"><span data-stu-id="0918e-297">[Direct2D](./direct2d-portal.md) uses this info to perform rendering optimizations with 'guaranteed opaque' content.</span></span> <span data-ttu-id="0918e-298">如果這個值不正確，可能會導致轉譯不正確。</span><span class="sxs-lookup"><span data-stu-id="0918e-298">If this value is inaccurate, it can result in incorrect rendering.</span></span>

<span data-ttu-id="0918e-299">您可以修改轉換的轉譯行為 (如在此方法期間的第6到第8節) 所定義。</span><span class="sxs-lookup"><span data-stu-id="0918e-299">The you can modify the transform's rendering behavior (as defined in sections 6 through 8) during this method.</span></span> <span data-ttu-id="0918e-300">不過，您無法修改轉換圖形中的其他轉換，也無法在此修改圖形版面配置本身。</span><span class="sxs-lookup"><span data-stu-id="0918e-300">However, the you can't modify other transforms in the transform graph, or the graph layout itself here.</span></span>


```C++
IFACEMETHODIMP SampleTransform::MapInputRectsToOutputRect(
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
    UINT32 inputRectCount,
    _Out_ D2D1_RECT_L* pOutputRect,
    _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
    )
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The output of the transform will be the same size as the input.
    *pOutputRect = pInputRects[0];
    // Indicate that the image's opacity has not changed.
    *pOutputOpaqueSubRect = pInputOpaqueSubRects[0];
    // The size of the input image can be saved here for subsequent operations.
    m_inputRect = pInputRects[0];

    return S_OK;
}
```



<span data-ttu-id="0918e-301">如需更複雜的範例，請考慮如何表示簡單的模糊運算：</span><span class="sxs-lookup"><span data-stu-id="0918e-301">For a more complex example, consider how a simple blur operation would be represented:</span></span>

<span data-ttu-id="0918e-302">如果模糊運算使用5圖元半徑，則輸出矩形的大小必須展開5圖元，如下所示。</span><span class="sxs-lookup"><span data-stu-id="0918e-302">If a blur operation uses a 5 pixel radius, the size of the output rectangle must expand by 5 pixels, as shown below.</span></span> <span data-ttu-id="0918e-303">修改矩形座標時，轉換必須確保其邏輯不會造成矩形座標中的任何 over/下溢。</span><span class="sxs-lookup"><span data-stu-id="0918e-303">When modifying rectangle coordinates, a transform must ensure that its logic does not cause any over/underflows in the rectangle coordinates.</span></span>


```C++
// Expand output image by 5 pixels.

// Do not expand empty input rectangles.
if (pInputRects[0].right  > pInputRects[0].left &&
    pInputRects[0].bottom > pInputRects[0].top
    )
{
    pOutputRect->left   = ((pInputRects[0].left   - 5) < pInputRects[0].left  ) ? (pInputRects[0].left   - 5) : LONG_MIN;
    pOutputRect->top    = ((pInputRects[0].top    - 5) < pInputRects[0].top   ) ? (pInputRects[0].top    - 5) : LONG_MIN;
    pOutputRect->right  = ((pInputRects[0].right  + 5) > pInputRects[0].right ) ? (pInputRects[0].right  + 5) : LONG_MAX;
    pOutputRect->bottom = ((pInputRects[0].bottom + 5) > pInputRects[0].bottom) ? (pInputRects[0].bottom + 5) : LONG_MAX;
}
```



<span data-ttu-id="0918e-304">因為影像模糊，所以不透明的影像區域現在可能是部分透明的。</span><span class="sxs-lookup"><span data-stu-id="0918e-304">Because the image is blurred, a region of the image which was opaque may now be partially transparent.</span></span> <span data-ttu-id="0918e-305">這是因為影像外面的區域預設為透明黑色，而此透明度將會混合到邊緣周圍的影像。</span><span class="sxs-lookup"><span data-stu-id="0918e-305">This is because the area outside the image defaults to transparent black and this transparency will be blended into the image around the edges.</span></span> <span data-ttu-id="0918e-306">轉換必須反映其輸出不透明的矩形計算：</span><span class="sxs-lookup"><span data-stu-id="0918e-306">The transform must reflect this in its output opaque rectangle calculations:</span></span>


```C++
// Shrink opaque region by 5 pixels.
pOutputOpaqueSubRect->left   = pInputOpaqueSubRects[0].left   + 5;
pOutputOpaqueSubRect->top    = pInputOpaqueSubRects[0].top    + 5;
pOutputOpaqueSubRect->right  = pInputOpaqueSubRects[0].right  - 5;
pOutputOpaqueSubRect->bottom = pInputOpaqueSubRects[0].bottom - 5;
```



<span data-ttu-id="0918e-307">這些計算會在此視覺化：</span><span class="sxs-lookup"><span data-stu-id="0918e-307">These calculations are visualized here:</span></span>

![矩形計算圖例。](images/custom-effects2.png)

<span data-ttu-id="0918e-309">如需此方法的詳細資訊，請參閱 [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) 參考頁面。</span><span class="sxs-lookup"><span data-stu-id="0918e-309">For more info about this method, see the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) reference page.</span></span>

### <a name="mapoutputrecttoinputrects"></a><span data-ttu-id="0918e-310">MapOutputRectToInputRects</span><span class="sxs-lookup"><span data-stu-id="0918e-310">MapOutputRectToInputRects</span></span>

<span data-ttu-id="0918e-311">[Direct2D](./direct2d-portal.md)會在 [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect)之後呼叫 [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects)方法。</span><span class="sxs-lookup"><span data-stu-id="0918e-311">[Direct2D](./direct2d-portal.md) calls the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) method after [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span> <span data-ttu-id="0918e-312">轉換必須計算需要讀取的影像部分，才能正確轉譯要求的輸出區域。</span><span class="sxs-lookup"><span data-stu-id="0918e-312">The transform must calculate what portion of the image it needs to read from in order to correctly render the requested output region.</span></span>

<span data-ttu-id="0918e-313">如同之前，如果效果嚴格地對應圖元1-1，則可以將輸出矩形傳遞至輸入矩形：</span><span class="sxs-lookup"><span data-stu-id="0918e-313">As before, if an effect strictly maps pixels 1-1, it can pass the output rectangle through to the input rectangle:</span></span>


```C++
IFACEMETHODIMP SampleTransform::MapOutputRectToInputRects(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
    UINT32 inputRectCount
    ) const
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The input needed for the transform is the same as the visible output.
    pInputRects[0] = *pOutputRect;
    return S_OK;
}
```



<span data-ttu-id="0918e-314">同樣地，如果轉換縮小或展開影像 (例如此處的模糊範例) ，圖元通常會使用周圍圖元來計算其值。</span><span class="sxs-lookup"><span data-stu-id="0918e-314">Likewise, if a transform shrinks or expands an image (like the blur example here), pixels often use surrounding pixels to calculate their value.</span></span> <span data-ttu-id="0918e-315">使用模糊時，圖元會以周圍的圖元為平均值，即使超出輸入影像的界限也是如此。</span><span class="sxs-lookup"><span data-stu-id="0918e-315">With a blur, a pixel is averaged with its surrounding pixels, even if they are outside of the bounds of the input image.</span></span> <span data-ttu-id="0918e-316">此行為會反映在計算中。</span><span class="sxs-lookup"><span data-stu-id="0918e-316">This behavior is reflected in the calculation.</span></span> <span data-ttu-id="0918e-317">與之前相同，轉換會在展開矩形座標時檢查溢位。</span><span class="sxs-lookup"><span data-stu-id="0918e-317">As before, the transform checks for overflows when expanding a rectangle's coordinates.</span></span>


```C++
// Expand the input rectangle to reflect that more pixels need to 
// be read from than are necessarily rendered in the effect's output.
pInputRects[0].left   = ((pOutputRect->left   - 5) < pOutputRect->left  ) ? (pOutputRect->left   - 5) : LONG_MIN;
pInputRects[0].top    = ((pOutputRect->top    - 5) < pOutputRect->top   ) ? (pOutputRect->top    - 5) : LONG_MIN;
pInputRects[0].right  = ((pOutputRect->right  + 5) > pOutputRect->right ) ? (pOutputRect->right  + 5) : LONG_MAX;
pInputRects[0].bottom = ((pOutputRect->bottom + 5) > pOutputRect->bottom) ? (pOutputRect->bottom + 5) : LONG_MAX;
```



<span data-ttu-id="0918e-318">此圖以視覺化方式呈現計算。</span><span class="sxs-lookup"><span data-stu-id="0918e-318">This figure visualizes the calculation.</span></span> <span data-ttu-id="0918e-319">[Direct2D](./direct2d-portal.md) 會自動取樣不存在輸入影像的透明黑色圖元，讓模糊與螢幕上現有的內容逐漸混合。</span><span class="sxs-lookup"><span data-stu-id="0918e-319">[Direct2D](./direct2d-portal.md) automatically samples transparent black pixels where the input image doesn't exist, allowing the blur to be blended gradually with the existing content on the screen.</span></span>

![矩形外的效果取樣透明黑色圖元的圖例。](images/custom-effects3.png)

<span data-ttu-id="0918e-321">如果對應不是一般的，則這個方法應該將輸入矩形設定為最大區域，以保證結果正確。</span><span class="sxs-lookup"><span data-stu-id="0918e-321">If the mapping is non-trivial, then this method should set the input rectangle to the maximum area to guarantee correct results.</span></span> <span data-ttu-id="0918e-322">若要這樣做，請將左邊和上邊緣設定為 INT \_ MIN，並將右和下邊緣設定為 int \_ MAX。</span><span class="sxs-lookup"><span data-stu-id="0918e-322">To do this, set the left and top edges to INT\_MIN, and the right and bottom edges to INT\_MAX.</span></span>

<span data-ttu-id="0918e-323">如需此方法的詳細資訊，請參閱 [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) 主題。</span><span class="sxs-lookup"><span data-stu-id="0918e-323">For more info about this method, see the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) topic.</span></span>

### <a name="mapinvalidrect"></a><span data-ttu-id="0918e-324">MapInvalidRect</span><span class="sxs-lookup"><span data-stu-id="0918e-324">MapInvalidRect</span></span>

<span data-ttu-id="0918e-325">[Direct2D](./direct2d-portal.md) 也會呼叫 [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) 方法。</span><span class="sxs-lookup"><span data-stu-id="0918e-325">[Direct2D](./direct2d-portal.md) also calls the [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) method.</span></span> <span data-ttu-id="0918e-326">不過，不同于 [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) 和 [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) 方法 Direct2D 不保證會在任何特定時間呼叫它。</span><span class="sxs-lookup"><span data-stu-id="0918e-326">However, unlike the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) and [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) methods Direct2D is not guaranteed to call it at any particular time.</span></span> <span data-ttu-id="0918e-327">這個方法在概念上會決定必須重新轉譯轉換輸出的哪個部分，以回應部分或其所有輸入變更。</span><span class="sxs-lookup"><span data-stu-id="0918e-327">This method conceptually decides what part of a transform's output needs to be re-rendered in response to part or all of its input changing.</span></span> <span data-ttu-id="0918e-328">有三種不同的案例可計算轉換的無效 rect。</span><span class="sxs-lookup"><span data-stu-id="0918e-328">There are three different scenarios for which to calculate a transform's invalid rect.</span></span>

### <a name="transforms-with-one-to-one-pixel-mapping"></a><span data-ttu-id="0918e-329">使用一對一圖元對應的轉換</span><span class="sxs-lookup"><span data-stu-id="0918e-329">Transforms with one-to-one pixel mapping</span></span>

<span data-ttu-id="0918e-330">針對對應圖元1-1 的轉換，只要將不正確輸入矩形傳遞到不正確輸出矩形即可：</span><span class="sxs-lookup"><span data-stu-id="0918e-330">For transforms that map pixels 1-1, simply pass the invalid input rectangle through to the invalid output rectangle:</span></span>


```C++
IFACEMETHODIMP SampleTransform::MapInvalidRect(
    UINT32 inputIndex,
    D2D1_RECT_L invalidInputRect,
    _Out_ D2D1_RECT_L* pInvalidOutputRect
    ) const
{
    // This transform is designed to only accept one input.
    if (inputIndex != 0)
    {
        return E_INVALIDARG;
    }

    // If part of the transform's input is invalid, mark the corresponding
    // output region as invalid. 
    *pInvalidOutputRect = invalidInputRect;

    return S_OK;
}
```



### <a name="transforms-with-many-to-many-pixel-mapping"></a><span data-ttu-id="0918e-331">具有多對多圖元對應的轉換</span><span class="sxs-lookup"><span data-stu-id="0918e-331">Transforms with many-to-many pixel mapping</span></span>

<span data-ttu-id="0918e-332">當轉換的輸出圖元相依于其周圍區域時，不正確輸入矩形必須相對應展開。</span><span class="sxs-lookup"><span data-stu-id="0918e-332">When a transform's output pixels are dependent on their surrounding area, the invalid input rectangle must correspondingly be expanded.</span></span> <span data-ttu-id="0918e-333">這是為了反映出無效輸入矩形周圍的圖元也會受到影響，而且會變成無效。</span><span class="sxs-lookup"><span data-stu-id="0918e-333">This is to reflect that pixels surrounding the invalid input rectangle will also be affected and become invalid.</span></span> <span data-ttu-id="0918e-334">例如，五個圖元模糊會使用下列計算：</span><span class="sxs-lookup"><span data-stu-id="0918e-334">For example, a five pixel blur uses the following calculation:</span></span>


```C++
// Expand the input invalid rectangle by five pixels in each direction. This
// reflects that a change in part of the given input image will cause a change
// in an expanded part of the output image (five pixels in each direction).
pInvalidOutputRect->left   = ((invalidInputRect.left   - 5) < invalidInputRect.left  ) ? (invalidInputRect.left   - 5) : LONG_MIN;
pInvalidOutputRect->top    = ((invalidInputRect.top    - 5) < invalidInputRect.top   ) ? (invalidInputRect.top    - 5) : LONG_MIN;
pInvalidOutputRect->right  = ((invalidInputRect.right  + 5) > invalidInputRect.right ) ? (invalidInputRect.right  + 5) : LONG_MAX;
pInvalidOutputRect->bottom = ((invalidInputRect.bottom + 5) > invalidInputRect.bottom) ? (invalidInputRect.bottom + 5) : LONG_MAX;
```



### <a name="transforms-with-complex-pixel-mapping"></a><span data-ttu-id="0918e-335">具有複雜圖元對應的轉換</span><span class="sxs-lookup"><span data-stu-id="0918e-335">Transforms with complex pixel mapping</span></span>

<span data-ttu-id="0918e-336">針對輸入和輸出圖元沒有簡單對應的轉換，整個輸出可以標示為無效。</span><span class="sxs-lookup"><span data-stu-id="0918e-336">For transforms where input and output pixels do not have a simple mapping, the entire output can be marked as invalid.</span></span> <span data-ttu-id="0918e-337">例如，如果轉換只是輸出輸入的平均色彩，則即使輸入的小部分變更，轉換的整個輸出也會變更。</span><span class="sxs-lookup"><span data-stu-id="0918e-337">For example, if a transform simply outputs the average color of the input, the entire output of the transform changes if even a small part of the input is changed.</span></span> <span data-ttu-id="0918e-338">在此情況下，不正確輸出矩形應該設定為邏輯上的無限矩形， (如下所示) 。</span><span class="sxs-lookup"><span data-stu-id="0918e-338">In this case, the invalid output rectangle should be set to a logically infinite rectangle (shown below).</span></span> <span data-ttu-id="0918e-339">[Direct2D](./direct2d-portal.md) 會自動將此個到輸出的範圍。</span><span class="sxs-lookup"><span data-stu-id="0918e-339">[Direct2D](./direct2d-portal.md) automatically clamps this to the bounds of the output.</span></span>


```C++
// If any change in the input image affects the entire output, the
// transform should set pInvalidOutputRect to a logically infinite rect.
*pInvalidOutputRect = D2D1::RectL(LONG_MIN, LONG_MIN, LONG_MAX, LONG_MAX);
```



<span data-ttu-id="0918e-340">如需此方法的詳細資訊，請參閱 [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) 主題。</span><span class="sxs-lookup"><span data-stu-id="0918e-340">For more info about this method, see the [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) topic.</span></span>

<span data-ttu-id="0918e-341">完成這些方法之後，轉換的標頭就會包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="0918e-341">Once these methods have been implemented, your transform's header will contain the following:</span></span>


```C++
class SampleTransform : public ID2D1Transform 
{
public:
    SampleTransform();

    // ID2D1TransformNode Methods:
    IFACEMETHODIMP_(UINT32) GetInputCount() const;
    
    // ID2D1Transform Methods:
    IFACEMETHODIMP MapInputRectsToOutputRect(
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
        UINT32 inputRectCount,
        _Out_ D2D1_RECT_L* pOutputRect,
        _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
        );    

    IFACEMETHODIMP MapOutputRectToInputRects(
        _In_ const D2D1_RECT_L* pOutputRect,
        _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
        UINT32 inputRectCount
        ) const;

    IFACEMETHODIMP MapInvalidRect(
        UINT32 inputIndex,
        D2D1_RECT_L invalidInputRect,
        _Out_ D2D1_RECT_L* pInvalidOutputRect 
        ) const;

    // IUnknown Methods:
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(REFIID riid, _Outptr_ void** ppOutput);

private:
    LONG m_cRef; // Internal ref count used by AddRef() and Release() methods.
    D2D1_RECT_L m_inputRect; // Stores the size of the input image.
};
```



## <a name="adding-a-pixel-shader-to-a-custom-transform"></a><span data-ttu-id="0918e-342">將圖元著色器新增至自訂轉換</span><span class="sxs-lookup"><span data-stu-id="0918e-342">Adding a pixel shader to a custom transform</span></span>

<span data-ttu-id="0918e-343">一旦建立轉換，就必須提供會操作影像圖元的著色器。</span><span class="sxs-lookup"><span data-stu-id="0918e-343">Once a transform has been created, it needs to provide a shader that will manipulate the image pixels.</span></span> <span data-ttu-id="0918e-344">本節涵蓋搭配自訂轉換使用圖元著色器的步驟。</span><span class="sxs-lookup"><span data-stu-id="0918e-344">This section covers the steps to using a pixel shader with a custom transform.</span></span>

### <a name="implementing-id2d1drawtransform"></a><span data-ttu-id="0918e-345">執行 ID2D1DrawTransform</span><span class="sxs-lookup"><span data-stu-id="0918e-345">Implementing ID2D1DrawTransform</span></span>

<span data-ttu-id="0918e-346">若要使用圖元著色器，轉換必須執行 [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) 介面，此介面繼承自第5節中所述的 [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) 介面。</span><span class="sxs-lookup"><span data-stu-id="0918e-346">To use a pixel shader, the transform must implement the [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) interface, which inherits from the [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) interface described in section 5.</span></span> <span data-ttu-id="0918e-347">此介面包含一個要執行的新方法：</span><span class="sxs-lookup"><span data-stu-id="0918e-347">This interface contains one new method to implement:</span></span>

### <a name="setdrawinfoid2d1drawinfo-pdrawinfo"></a><span data-ttu-id="0918e-348">SetDrawInfo (ID2D1DrawInfo \* pDrawInfo) </span><span class="sxs-lookup"><span data-stu-id="0918e-348">SetDrawInfo(ID2D1DrawInfo \*pDrawInfo)</span></span>

<span data-ttu-id="0918e-349">當第一次將轉換新增至效果的轉換圖形時， [Direct2D](./direct2d-portal.md)會呼叫 [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo)方法。</span><span class="sxs-lookup"><span data-stu-id="0918e-349">[Direct2D](./direct2d-portal.md) calls the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method when the transform is first added to an effect's transform graph.</span></span> <span data-ttu-id="0918e-350">這個方法會提供 [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) 參數，以控制轉換的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="0918e-350">This method provides an [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter that controls how the transform is rendered.</span></span> <span data-ttu-id="0918e-351">請參閱此處提供之方法的 **ID2D1DrawInfo** 主題。</span><span class="sxs-lookup"><span data-stu-id="0918e-351">See the **ID2D1DrawInfo** topic for the methods available here.</span></span>

<span data-ttu-id="0918e-352">如果轉換選擇將此參數儲存為類別成員變數，則可以從其他方法（例如屬性 setter 或 [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect)）存取和變更 *drawInfo* 物件。</span><span class="sxs-lookup"><span data-stu-id="0918e-352">If the transform chooses to store this parameter as a class member variable, the *drawInfo* object can be accessed and changed from other methods such as property setters or [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span> <span data-ttu-id="0918e-353">值得注意的是，它無法從 [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)的 [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects)或 [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect)方法中呼叫。</span><span class="sxs-lookup"><span data-stu-id="0918e-353">Notably, it cannot be called from the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) or [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) methods on [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span></span>

### <a name="creating-a-guid-for-the-pixel-shader"></a><span data-ttu-id="0918e-354">建立圖元著色器的 GUID</span><span class="sxs-lookup"><span data-stu-id="0918e-354">Creating a GUID for the pixel shader</span></span>

<span data-ttu-id="0918e-355">接下來，轉換必須定義圖元著色器本身的唯一 GUID。</span><span class="sxs-lookup"><span data-stu-id="0918e-355">Next, the transform must define a unique GUID for the pixel shader itself.</span></span> <span data-ttu-id="0918e-356">當 [Direct2D](./direct2d-portal.md) 將著色器載入記憶體時，以及當轉換選擇要用於執行的圖元著色器時，就會使用這種方式。</span><span class="sxs-lookup"><span data-stu-id="0918e-356">This is used when [Direct2D](./direct2d-portal.md) loads the shader into memory, as well as when the transform chooses which pixel shader to use for execution.</span></span> <span data-ttu-id="0918e-357">包含在 Visual Studio 中的工具（例如 guidgen.exe）可以用來產生隨機的 GUID。</span><span class="sxs-lookup"><span data-stu-id="0918e-357">Tools such as guidgen.exe, which is included with Visual Studio, can be used to generate a random GUID.</span></span>


```C++
// Example GUID used to uniquely identify HLSL shader. Passed to Direct2D during
// shader load, and used by the transform to identify the shader for the
// ID2D1DrawInfo::SetPixelShader method. The effect author should create a
// unique name for the shader as well as a unique GUID using
// a GUID generation tool.
DEFINE_GUID(GUID_SamplePixelShader, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="loading-the-pixel-shader-with-direct2d"></a><span data-ttu-id="0918e-358">使用 Direct2D 載入圖元著色器</span><span class="sxs-lookup"><span data-stu-id="0918e-358">Loading the pixel shader with Direct2D</span></span>

<span data-ttu-id="0918e-359">圖元著色器必須先載入至記憶體，才能供轉換使用。</span><span class="sxs-lookup"><span data-stu-id="0918e-359">A pixel shader must be loaded into memory before it can be used by the transform.</span></span>

<span data-ttu-id="0918e-360">若要將圖元著色器載入至記憶體，轉換應該從讀取已編譯的著色器位元組程式碼。Visual Studio (所產生的 CSO 檔案，請參閱 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 檔，以取得) 至位元組陣列的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0918e-360">To load the pixel shader into memory, the transform should read the compiled shader byte code from the .CSO file generated by Visual Studio (see [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) documentation for details) into a byte array.</span></span> <span data-ttu-id="0918e-361">這項技術在 [D2DCUSTOMEFFECTS SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)中有詳細的示範。</span><span class="sxs-lookup"><span data-stu-id="0918e-361">This technique is demonstrated in detail in the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="0918e-362">將著色器資料載入位元組陣列之後，請在效果的 [**ID2D1EffectCoNtext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)物件上呼叫 [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)方法。</span><span class="sxs-lookup"><span data-stu-id="0918e-362">Once the shader data has been loaded into a byte array, call the [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) method on the effect's [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) object.</span></span> <span data-ttu-id="0918e-363">已載入具有相同 GUID 的著色器時， [Direct2D](./direct2d-portal.md)會忽略對 **LoadPixelShader** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="0918e-363">[Direct2D](./direct2d-portal.md) ignores calls to **LoadPixelShader** when a shader with the same GUID has already been loaded.</span></span>

<span data-ttu-id="0918e-364">在圖元著色器載入至記憶體後，轉換必須將其 GUID 傳遞給 [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo)方法期間所提供之 [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo)參數上的 [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer)方法，以選取要執行的轉換。</span><span class="sxs-lookup"><span data-stu-id="0918e-364">After a pixel shader has been loaded into memory, the transform needs to select it for execution by passing its GUID to the [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) method on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter provided during the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method.</span></span> <span data-ttu-id="0918e-365">在選取要執行之前，必須先將圖元著色器載入至記憶體。</span><span class="sxs-lookup"><span data-stu-id="0918e-365">The pixel shader must be already loaded into memory before being selected for execution.</span></span>

### <a name="changing-shader-operation-with-constant-buffers"></a><span data-ttu-id="0918e-366">使用常數緩衝區變更著色器作業</span><span class="sxs-lookup"><span data-stu-id="0918e-366">Changing shader operation with constant buffers</span></span>

<span data-ttu-id="0918e-367">若要變更著色器的執行方式，轉換可以將常數緩衝區傳遞給圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="0918e-367">To change how a shader executes, a transform may pass a constant buffer to the pixel shader.</span></span> <span data-ttu-id="0918e-368">若要這樣做，轉換會在類別標頭中定義包含所需變數的結構：</span><span class="sxs-lookup"><span data-stu-id="0918e-368">To do so, a transform defines a struct that contains the desired variables in the class header:</span></span>


```C++
// This struct defines the constant buffer of the pixel shader.
struct
{
    float valueOne;
    float valueTwo;
} m_constantBuffer;
```



<span data-ttu-id="0918e-369">接著，轉換會在 [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo)方法中提供的 [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo)參數上呼叫 [**ID2D1DrawInfo：： SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer)方法，以將此緩衝區傳遞給著色器。</span><span class="sxs-lookup"><span data-stu-id="0918e-369">The transform then calls the [**ID2D1DrawInfo::SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) method on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter provided in the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method to pass this buffer to the shader.</span></span>

<span data-ttu-id="0918e-370">[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)也需要定義表示常數緩衝區的對應結構。</span><span class="sxs-lookup"><span data-stu-id="0918e-370">The [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) also needs to define a corresponding struct that represents the constant buffer.</span></span> <span data-ttu-id="0918e-371">著色器結構中所包含的變數必須符合轉換結構中的變數。</span><span class="sxs-lookup"><span data-stu-id="0918e-371">The variables contained in the shader's struct must match those in the transform's struct.</span></span>


```C++
cbuffer constants : register(b0)
{
    float valueOne : packoffset(c0.x);
    float valueTwo : packoffset(c0.y);
};
```



<span data-ttu-id="0918e-372">一旦定義緩衝區後，就可以從圖元著色器內的任何位置讀取包含在內的值。</span><span class="sxs-lookup"><span data-stu-id="0918e-372">Once the buffer has been defined, the values contained within can be read from anywhere within the pixel shader.</span></span>

### <a name="writing-a-pixel-shader-for-direct2d"></a><span data-ttu-id="0918e-373">為 Direct2D 撰寫圖元著色器</span><span class="sxs-lookup"><span data-stu-id="0918e-373">Writing a pixel shader for Direct2D</span></span>

<span data-ttu-id="0918e-374">[Direct2D](./direct2d-portal.md) 轉換使用以標準 [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)撰寫的著色器。</span><span class="sxs-lookup"><span data-stu-id="0918e-374">[Direct2D](./direct2d-portal.md) transforms use shaders authored using standard [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span> <span data-ttu-id="0918e-375">不過，撰寫從轉換內容執行的圖元著色器有幾個重要概念。</span><span class="sxs-lookup"><span data-stu-id="0918e-375">However, there are a few key concepts to writing a pixel shader that executes from the context of a transform.</span></span> <span data-ttu-id="0918e-376">如需完整功能的圖元著色器的完整範例，請參閱 [D2DCUSTOMEFFECTS SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)。</span><span class="sxs-lookup"><span data-stu-id="0918e-376">For a completed example of a fully functionally pixel shader, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="0918e-377">[Direct2D](./direct2d-portal.md) 會自動將轉換的輸入對應至 HLSL 中的 [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) 和 [**SamplerState**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) 物件。</span><span class="sxs-lookup"><span data-stu-id="0918e-377">[Direct2D](./direct2d-portal.md) automatically maps a transform's inputs to [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**SamplerState**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) objects in the HLSL.</span></span> <span data-ttu-id="0918e-378">第一個 **Texture2D** 位於登錄 t0，第一個 **SamplerState** 位於 register s0。</span><span class="sxs-lookup"><span data-stu-id="0918e-378">The first **Texture2D** is located at register t0, and the first **SamplerState** is located at register s0.</span></span> <span data-ttu-id="0918e-379">每個額外的輸入都位於下一個對應的暫存器 (t1 和 s1，例如) 。</span><span class="sxs-lookup"><span data-stu-id="0918e-379">Each additional input is located at the next corresponding registers (t1 and s1 for example).</span></span> <span data-ttu-id="0918e-380">您可以藉由呼叫 **Texture2D** 物件的範例，並傳入對應的 **SamplerState** 物件和材質座標，來取樣特定輸入的圖元資料。</span><span class="sxs-lookup"><span data-stu-id="0918e-380">Pixel data for a particular input can be sampled by calling Sample on the **Texture2D** object and passing in the corresponding **SamplerState** object and the texel coordinates.</span></span>

<span data-ttu-id="0918e-381">每個呈現的圖元都會執行一次自訂圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="0918e-381">A custom pixel shader is run once for each pixel that is rendered.</span></span> <span data-ttu-id="0918e-382">每次執行著色器時， [Direct2D](./direct2d-portal.md) 會自動提供三個參數來識別其目前的執行位置：</span><span class="sxs-lookup"><span data-stu-id="0918e-382">Each time the shader is run, [Direct2D](./direct2d-portal.md) automatically provides three parameters that identify its current execution position:</span></span>

-   <span data-ttu-id="0918e-383">場景-space 輸出：此參數代表整體目標介面的目前執行位置。</span><span class="sxs-lookup"><span data-stu-id="0918e-383">Scene-space output: This parameter represents the current execution position in terms of the overall target surface.</span></span> <span data-ttu-id="0918e-384">它是以圖元來定義，而其最小值/最大值會對應至 [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect)所傳回之矩形的界限。</span><span class="sxs-lookup"><span data-stu-id="0918e-384">It is defined in pixels and its min/max values correspond to the bounds of the rectangle returned by [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span>
-   <span data-ttu-id="0918e-385">剪輯空間輸出：此參數是由 Direct3D 使用，且不能用於轉換的圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="0918e-385">Clip-space output: This parameter is used by Direct3D, and is must not be used in a transform's pixel shader.</span></span>
-   <span data-ttu-id="0918e-386">材質-space 輸入：這個參數代表特定輸入材質中的目前執行位置。</span><span class="sxs-lookup"><span data-stu-id="0918e-386">Texel-space input: This parameter represents the current execution position in a particular input texture.</span></span> <span data-ttu-id="0918e-387">著色器不應該依賴此值的計算方式。</span><span class="sxs-lookup"><span data-stu-id="0918e-387">A shader should not take any dependencies on how this value is calculated.</span></span> <span data-ttu-id="0918e-388">它應該只使用它來取樣圖元著色器的輸入，如下列程式碼所示：</span><span class="sxs-lookup"><span data-stu-id="0918e-388">It should only use it to sample the pixel shader's input, as shown in the code below:</span></span>


```C++
Texture2D InputTexture : register(t0);
SamplerState InputSampler : register(s0);

float4 main(
    float4 clipSpaceOutput  : SV_POSITION,
    float4 sceneSpaceOutput : SCENE_POSITION,
    float4 texelSpaceInput0 : TEXCOORD0
    ) : SV_Target
{
    // Samples pixel from ten pixels above current position.

    float2 sampleLocation =
        texelSpaceInput0.xy    // Sample position for the current output pixel.
        + float2(0,-10)        // An offset from which to sample the input, specified in pixels.
        * texelSpaceInput0.zw; // Multiplier that converts pixel offset to sample position offset.

    float4 color = InputTexture.Sample(
        InputSampler,          // Sampler and Texture must match for a given input.
        sampleLocation
        );

    return color;
}
```



## <a name="adding-a-vertex-shader-to-a-custom-transform"></a><span data-ttu-id="0918e-389">將頂點著色器加入至自訂轉換</span><span class="sxs-lookup"><span data-stu-id="0918e-389">Adding a vertex shader to a custom transform</span></span>

<span data-ttu-id="0918e-390">您可以使用頂點著色器來完成不同于圖元著色器的影像案例。</span><span class="sxs-lookup"><span data-stu-id="0918e-390">You can use vertex shaders to accomplish different imaging scenarios than pixel shaders.</span></span> <span data-ttu-id="0918e-391">尤其是，頂點著色器可以藉由轉換構成影像的頂點來執行以幾何為基礎的影像效果。</span><span class="sxs-lookup"><span data-stu-id="0918e-391">In particular, vertex shaders can perform geometry-based image effects by transforming vertices that comprise an image.</span></span> <span data-ttu-id="0918e-392">頂點著色器可以與轉換指定的圖元著色器分開使用或搭配使用。</span><span class="sxs-lookup"><span data-stu-id="0918e-392">Vertex shaders can be used independently of or in conjunction with transform-specified pixel shaders.</span></span> <span data-ttu-id="0918e-393">如果未指定頂點著色器， [Direct2D](./direct2d-portal.md) 會在預設的頂點著色器中替代，以搭配自訂圖元著色器使用。</span><span class="sxs-lookup"><span data-stu-id="0918e-393">If a vertex shader is not specified, [Direct2D](./direct2d-portal.md) substitutes in a default vertex shader for use with the custom pixel shader.</span></span>

<span data-ttu-id="0918e-394">將頂點著色器加入至自訂轉換的程式，與圖元著色器的程式類似–轉換會實 [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) 介面、建立 GUID，並 (選擇性地) 將常數緩衝區傳遞給著色器。</span><span class="sxs-lookup"><span data-stu-id="0918e-394">The process for adding a vertex shader to a custom transform is similar to that of a pixel shader – the transform implements the [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) interface, creates a GUID, and (optionally) passes constant buffers to the shader.</span></span> <span data-ttu-id="0918e-395">不過，有幾個重要的額外步驟，對頂點著色器而言是唯一的：</span><span class="sxs-lookup"><span data-stu-id="0918e-395">However, there are a few key additional steps that are unique to vertex shaders:</span></span>

### <a name="creating-a-vertex-buffer"></a><span data-ttu-id="0918e-396">建立頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="0918e-396">Creating a vertex buffer</span></span>

<span data-ttu-id="0918e-397">依定義的頂點著色器會在傳遞給它的頂點上執行，而不是個別圖元。</span><span class="sxs-lookup"><span data-stu-id="0918e-397">A vertex shader by definition executes on vertices passed to it, not individual pixels.</span></span> <span data-ttu-id="0918e-398">若要指定要在其上執行之著色器的頂點，轉換會建立要傳遞給著色器的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0918e-398">To specify the vertices for the shader to execute on, a transform creates a vertex buffer to pass to the shader.</span></span> <span data-ttu-id="0918e-399">頂點緩衝區的版面配置已超出本檔的範圍。</span><span class="sxs-lookup"><span data-stu-id="0918e-399">The layout of vertex buffers is beyond the scope of this document.</span></span> <span data-ttu-id="0918e-400">如需詳細資訊，請參閱 [Direct3D 參考](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ，或 [D2DCustomEffects SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) 以取得範例執行。</span><span class="sxs-lookup"><span data-stu-id="0918e-400">Please see the [Direct3D reference](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) for details, or the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a sample implementation.</span></span>

<span data-ttu-id="0918e-401">在記憶體中建立頂點緩衝區之後，轉換會在包含效果的 [**ID2D1EffectCoNtext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)物件上使用 [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer)方法，將該資料傳遞給 GPU。</span><span class="sxs-lookup"><span data-stu-id="0918e-401">After creating a vertex buffer in memory, the transform uses the [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) method on the containing effect's [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) object to pass that data to the GPU.</span></span> <span data-ttu-id="0918e-402">同樣地，請參閱 [D2DCUSTOMEFFECTS SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) 以取得範例執行。</span><span class="sxs-lookup"><span data-stu-id="0918e-402">Again, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a sample implementation.</span></span>

<span data-ttu-id="0918e-403">如果轉換未指定任何頂點緩衝區， [Direct2D](./direct2d-portal.md) 會傳遞代表矩形影像位置的預設頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0918e-403">If no vertex buffer is specified by the transform, [Direct2D](./direct2d-portal.md) passes a default vertex buffer representing the rectangular image location.</span></span>

### <a name="changing-setdrawinfo-to-utilize-a-vertex-shader"></a><span data-ttu-id="0918e-404">變更 SetDrawInfo 以利用頂點著色器</span><span class="sxs-lookup"><span data-stu-id="0918e-404">Changing SetDrawInfo to utilize a vertex shader</span></span>

<span data-ttu-id="0918e-405">如同使用圖元著色器，轉換必須載入並選取要執行的頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="0918e-405">Like with pixel shaders, the transform must load and select a vertex shader for execution.</span></span> <span data-ttu-id="0918e-406">為了載入頂點著色器，它會在效果的 Initialize 方法中收到的 [**ID2D1EffectCoNtext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)方法上呼叫 [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader)方法。</span><span class="sxs-lookup"><span data-stu-id="0918e-406">To load the vertex shader, it calls the [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) method on the [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) method received in the effect's Initialize method.</span></span> <span data-ttu-id="0918e-407">若要選取要執行的頂點著色器，它會在轉換的 [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo)方法中收到的 [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo)參數上呼叫 [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) 。</span><span class="sxs-lookup"><span data-stu-id="0918e-407">To select the vertex shader for execution, it calls [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter received in the transform's [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method.</span></span> <span data-ttu-id="0918e-408">這個方法會接受先前載入之頂點著色器的 GUID，以及 (選擇性地) 先前建立的頂點緩衝區，以供著色器執行。</span><span class="sxs-lookup"><span data-stu-id="0918e-408">This method accepts a GUID for a previously-loaded vertex shader as well as (optionally) a previously-created vertex buffer for the shader to execute on.</span></span>

### <a name="implementing-a-direct2d-vertex-shader"></a><span data-ttu-id="0918e-409">執行 Direct2D 頂點著色器</span><span class="sxs-lookup"><span data-stu-id="0918e-409">Implementing a Direct2D vertex shader</span></span>

<span data-ttu-id="0918e-410">繪圖轉換可以同時包含圖元著色器和頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="0918e-410">A draw transform can contain both a pixel shader and a vertex shader.</span></span> <span data-ttu-id="0918e-411">如果轉換同時定義圖元著色器和端點著色器，則會直接將頂點著色器的輸出提供給圖元著色器：應用程式可以自訂頂點著色器的傳回簽章，或圖元著色器的參數，只要它們是一致的。</span><span class="sxs-lookup"><span data-stu-id="0918e-411">If a transform defines both a pixel shader and a vertex shader, then the output from the vertex shader is given directly to the pixel shader: the app can customize the return signature of the vertex shader / the parameters of the pixel shader as long as they are consistent.</span></span>

<span data-ttu-id="0918e-412">另一方面，如果轉換只包含頂點著色器，並且依賴 [Direct2D](./direct2d-portal.md)的預設傳遞圖元著色器，它必須傳回下列預設輸出：</span><span class="sxs-lookup"><span data-stu-id="0918e-412">On the other hand, if a transform only contains a vertex shader, and relies on [Direct2D](./direct2d-portal.md)'s default pass-through pixel shader, it must return the following default output:</span></span>


```C++
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



<span data-ttu-id="0918e-413">頂點著色器會在著色器的場景空間輸出變數中儲存其頂點轉換的結果。</span><span class="sxs-lookup"><span data-stu-id="0918e-413">A vertex shader stores the result of its vertex transformations in the shader's Scene-space output variable.</span></span> <span data-ttu-id="0918e-414">為了計算剪輯空間輸出和材質空間輸入變數， [Direct2D](./direct2d-portal.md) 會自動在常數緩衝區中提供轉換矩陣：</span><span class="sxs-lookup"><span data-stu-id="0918e-414">To compute the Clip-space output and the Texel-space input variables, [Direct2D](./direct2d-portal.md) automatically provides conversion matrices in a constant buffer:</span></span>


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};
```



<span data-ttu-id="0918e-415">您可以在下面找到範例頂點著色器程式碼，其使用轉換矩陣來計算 [Direct2D](./direct2d-portal.md)預期的正確剪輯和材質空間：</span><span class="sxs-lookup"><span data-stu-id="0918e-415">Sample vertex shader code can be found below that uses the conversion matrices to calculate the correct clip and texel spaces expected by [Direct2D](./direct2d-portal.md):</span></span>


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};

// Default output structure. This can be customized if transform also contains pixel shader.
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};

// The parameter(s) passed to the vertex shader are defined by the vertex buffer's layout
// as specified by the transform. If no vertex buffer is specified, Direct2D passes two
// triangles representing the rectangular image with the following layout:
//
//    float4 outputScenePosition : OUTPUT_SCENE_POSITION;
//
//    The x and y coordinates of the outputScenePosition variable represent the image's
//    position on the screen. The z and w coordinates are used for perspective and
//    depth-buffering.

VSOut GeometryVS(float4 outputScenePosition : OUTPUT_SCENE_POSITION) 
{
    VSOut output;

    // Compute Scene-space output (vertex simply passed-through here). 
    output.sceneSpaceOutput.x = outputScenePosition.x;
    output.sceneSpaceOutput.y = outputScenePosition.y;
    output.sceneSpaceOutput.z = outputScenePosition.z;
    output.sceneSpaceOutput.w = outputScenePosition.w;

    // Generate standard Clip-space output coordinates.
    output.clipSpaceOutput.x = (output.sceneSpaceOutput.x * sceneToOutputX[0]) +
        output.sceneSpaceOutput.w * sceneToOutputX[1];

    output.clipSpaceOutput.y = (output.sceneSpaceOutput.y * sceneToOutputY[0]) + 
        output.sceneSpaceOutput.w * sceneToOutputY[1];

    output.clipSpaceOutput.z = output.sceneSpaceOutput.z;
    output.clipSpaceOutput.w = output.sceneSpaceOutput.w;

    // Generate standard Texel-space input coordinates.
    output.texelSpaceInput0.x = (outputScenePosition.x * sceneToInput0X[0]) + sceneToInput0X[1];
    output.texelSpaceInput0.y = (outputScenePosition.y * sceneToInput0Y[0]) + sceneToInput0Y[1];
    output.texelSpaceInput0.z = sceneToInput0X[0];
    output.texelSpaceInput0.w = sceneToInput0Y[0];

    return output;  
}
```



<span data-ttu-id="0918e-416">上述程式碼可以當做頂點著色器的起點使用。</span><span class="sxs-lookup"><span data-stu-id="0918e-416">The above code can be used as a starting point for a vertex shader.</span></span> <span data-ttu-id="0918e-417">它只會通過輸入影像，而不會執行任何轉換。</span><span class="sxs-lookup"><span data-stu-id="0918e-417">It merely passes through the input image without performing any transforms.</span></span> <span data-ttu-id="0918e-418">同樣地，請參閱 [D2DCUSTOMEFFECTS SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) ，以取得完全實作為頂點著色器的轉換。</span><span class="sxs-lookup"><span data-stu-id="0918e-418">Again, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a fully-implemented vertex shader-based transform.</span></span>

<span data-ttu-id="0918e-419">如果轉換未指定任何頂點緩衝區， [Direct2D](./direct2d-portal.md) 會在代表矩形影像位置的預設頂點緩衝區中替代。</span><span class="sxs-lookup"><span data-stu-id="0918e-419">If no vertex buffer is specified by the transform, [Direct2D](./direct2d-portal.md) substitutes in a default vertex buffer representing the rectangular image location.</span></span> <span data-ttu-id="0918e-420">頂點著色器的參數會變更為預設著色器輸出的參數：</span><span class="sxs-lookup"><span data-stu-id="0918e-420">The parameters to the vertex shader are changed to those of the default shader output:</span></span>


```C++
struct VSIn
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



<span data-ttu-id="0918e-421">頂點著色器可能不會修改其 *sceneSpaceOutput* 和 *clipSpaceOutput* 參數。</span><span class="sxs-lookup"><span data-stu-id="0918e-421">The vertex shader may not modify its *sceneSpaceOutput* and *clipSpaceOutput* parameters.</span></span> <span data-ttu-id="0918e-422">它必須原封不動地傳回。</span><span class="sxs-lookup"><span data-stu-id="0918e-422">It must return them unchanged.</span></span> <span data-ttu-id="0918e-423">不過，它可能會針對每個輸入影像修改 (s) 的 *texelSpaceInput* 參數。</span><span class="sxs-lookup"><span data-stu-id="0918e-423">It may however modify the *texelSpaceInput* parameter(s) for each input image.</span></span> <span data-ttu-id="0918e-424">如果轉換也包含自訂圖元著色器，則端點著色器仍能將額外的自訂參數直接傳遞給圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="0918e-424">If the transform also contains a custom pixel shader, the vertex shader is still able to pass additional custom parameters directly to the pixel shader.</span></span> <span data-ttu-id="0918e-425">此外， *sceneSpace* 轉換會將自訂緩衝區 (B0) 不再提供。</span><span class="sxs-lookup"><span data-stu-id="0918e-425">Additionally, the *sceneSpace* conversion matrices custom buffer (b0) is no longer provided.</span></span>

## <a name="adding-a-compute-shader-to-a-custom-transform"></a><span data-ttu-id="0918e-426">將計算著色器新增至自訂轉換</span><span class="sxs-lookup"><span data-stu-id="0918e-426">Adding a compute shader to a custom transform</span></span>

<span data-ttu-id="0918e-427">最後，自訂轉換可能會利用特定案例的計算著色器。</span><span class="sxs-lookup"><span data-stu-id="0918e-427">Finally, custom transforms may utilize compute shaders for certain targeted scenarios.</span></span> <span data-ttu-id="0918e-428">計算著色器可以用來執行需要對輸入和輸出影像緩衝區有任意存取權的複雜影像效果。</span><span class="sxs-lookup"><span data-stu-id="0918e-428">Compute shaders can be used to implement complex image effects that require arbitrary access to input and output image buffers.</span></span> <span data-ttu-id="0918e-429">例如，基本的長條圖演算法因為記憶體存取限制，而無法使用圖元著色器來執行。</span><span class="sxs-lookup"><span data-stu-id="0918e-429">For example, a basic histogram algorithm cannot be implemented with a pixel shader due to limitations on memory access.</span></span>

<span data-ttu-id="0918e-430">由於計算著色器的硬體功能層級需求高於圖元著色器，因此應該盡可能使用圖元著色器來執行指定的效果。</span><span class="sxs-lookup"><span data-stu-id="0918e-430">Because compute shaders have higher hardware feature level requirements than pixel shaders, pixel shaders should be used when possible to implement a given effect.</span></span> <span data-ttu-id="0918e-431">具體而言，計算著色器只會在大部分的 DirectX 10 層級卡片和更高版本上執行。</span><span class="sxs-lookup"><span data-stu-id="0918e-431">Specifically, compute shaders only run on most DirectX 10 level cards and higher.</span></span> <span data-ttu-id="0918e-432">如果轉換選擇使用計算著色器，則在具現化期間，除了執行 [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) 介面之外，還必須檢查是否有適當的硬體支援。</span><span class="sxs-lookup"><span data-stu-id="0918e-432">If a transform chooses to use a compute shader, it must check for the appropriate hardware support during instantiation in addition to implementing the [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) interface.</span></span>

### <a name="checking-for-compute-shader-support"></a><span data-ttu-id="0918e-433">檢查計算著色器支援</span><span class="sxs-lookup"><span data-stu-id="0918e-433">Checking for Compute Shader support</span></span>

<span data-ttu-id="0918e-434">如果效果使用計算著色器，則必須在建立時使用 [**ID2D1EffectCoNtext：： CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) 方法檢查計算著色器支援。</span><span class="sxs-lookup"><span data-stu-id="0918e-434">If an effect uses a compute shader, it must check for compute shader support during its creation using the [**ID2D1EffectContext::CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) method.</span></span> <span data-ttu-id="0918e-435">如果 GPU 不支援計算著色器，則效果必須傳回 [**D2DERR 的 \_ \_ 裝置 \_ 功能不足**](direct2d-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="0918e-435">If the GPU does not support compute shaders, the effect must return [**D2DERR\_INSUFFICIENT\_DEVICE\_CAPABILITIES**](direct2d-error-codes.md).</span></span>

<span data-ttu-id="0918e-436">轉換可以使用的計算著色器有兩種不同的類型：著色器模型 4 (DirectX 10) 和著色器模型 5 (DirectX 11) 。</span><span class="sxs-lookup"><span data-stu-id="0918e-436">There are two different types of compute shaders that a transform can use: Shader Model 4 (DirectX 10) and Shader Model 5 (DirectX 11).</span></span> <span data-ttu-id="0918e-437">著色器模型4著色器有某些限制。</span><span class="sxs-lookup"><span data-stu-id="0918e-437">There are certain limitations to Shader Model 4 shaders.</span></span> <span data-ttu-id="0918e-438">請參閱 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 檔以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0918e-438">See the [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) documentation for details.</span></span> <span data-ttu-id="0918e-439">轉換可以包含這兩種著色器，並可在需要時切換回著色器模型4：請參閱 [D2DCUSTOMEFFECTS SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) 以取得此的執行。</span><span class="sxs-lookup"><span data-stu-id="0918e-439">Transforms can contain both types of shaders, and can fall back to Shader Model 4 when required: see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for an implementation of this.</span></span>

### <a name="implement-id2d1computetransform"></a><span data-ttu-id="0918e-440">執行 ID2D1ComputeTransform</span><span class="sxs-lookup"><span data-stu-id="0918e-440">Implement ID2D1ComputeTransform</span></span>

<span data-ttu-id="0918e-441">此介面包含兩個新的方法，可在 [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))中執行：</span><span class="sxs-lookup"><span data-stu-id="0918e-441">This interface contains two new methods to implement in addition to the ones in [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):</span></span>

### <a name="setcomputeinfoid2d1computeinfo-pcomputeinfo"></a><span data-ttu-id="0918e-442">SetComputeInfo (ID2D1ComputeInfo \* pComputeInfo) </span><span class="sxs-lookup"><span data-stu-id="0918e-442">SetComputeInfo(ID2D1ComputeInfo \*pComputeInfo)</span></span>

<span data-ttu-id="0918e-443">如同使用圖元和頂點著色器， [Direct2D](./direct2d-portal.md) 會在第一次將轉換新增至效果的轉換圖表時呼叫 [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) 方法。</span><span class="sxs-lookup"><span data-stu-id="0918e-443">Like with pixel and vertex shaders, [Direct2D](./direct2d-portal.md) calls the [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) method when the transform is first added to an effect's transform graph.</span></span> <span data-ttu-id="0918e-444">這個方法會提供 [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) 參數，以控制轉換的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="0918e-444">This method provides an [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) parameter that controls how the transform is rendered.</span></span> <span data-ttu-id="0918e-445">這包括透過 [**ID2D1ComputeInfo：： SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) 方法選擇要執行的計算著色器。</span><span class="sxs-lookup"><span data-stu-id="0918e-445">This includes choosing the compute shader to execute through the [**ID2D1ComputeInfo::SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) method.</span></span> <span data-ttu-id="0918e-446">如果轉換選擇將此參數儲存為類別成員變數，則可以從任何轉換或效果方法存取和變更，但 [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) 和 [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) 方法除外。</span><span class="sxs-lookup"><span data-stu-id="0918e-446">If the transform chooses to store this parameter as a class member variable, it can be accessed and changed from any transform or effect method with the exception of the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) and [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) methods.</span></span> <span data-ttu-id="0918e-447">如需其他可用的方法，請參閱 **ID2D1ComputeInfo** 主題。</span><span class="sxs-lookup"><span data-stu-id="0918e-447">See the **ID2D1ComputeInfo** topic for other methods available here.</span></span>

### <a name="calculatethreadgroupsid2d1computeinfo-poutputrect-uint32-pdimensionx-uint32-pdimensiony-uint32-pdimensionz"></a><span data-ttu-id="0918e-448">CalculateThreadgroups (ID2D1ComputeInfo \* pOutputRect、uint32 \* PDIMENSIONX、uint32 \* pDimensionY、uint32 \* pDimensionZ) </span><span class="sxs-lookup"><span data-stu-id="0918e-448">CalculateThreadgroups(ID2D1ComputeInfo \*pOutputRect, UINT32 \*pDimensionX, UINT32 \*pDimensionY, UINT32 \*pDimensionZ)</span></span>

<span data-ttu-id="0918e-449">雖然圖元著色器是以每個圖元為基礎執行，而且頂點著色器會以每個頂點為基礎執行，但是計算著色器會以每個 'threadgroup 的為基礎執行。</span><span class="sxs-lookup"><span data-stu-id="0918e-449">Whereas pixel shaders are executed on a per-pixel basis and vertex shaders are executed on a per-vertex basis, compute shaders are executed on a per-'threadgroup' basis.</span></span> <span data-ttu-id="0918e-450">Threadgroup 代表在 GPU 上同時執行的執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="0918e-450">A threadgroup represents a number of threads that execute concurrently on the GPU.</span></span> <span data-ttu-id="0918e-451">計算著色器 HLSL 程式碼會決定每個 threadgroup 應執行多少執行緒。</span><span class="sxs-lookup"><span data-stu-id="0918e-451">The compute shader HLSL code decides how many threads should be executed per threadgroup.</span></span> <span data-ttu-id="0918e-452">效果會根據著色器的邏輯，調整 threadgroups 數目，讓著色器執行所需的次數。</span><span class="sxs-lookup"><span data-stu-id="0918e-452">The effect scales the number of threadgroups so that the shader executes the desired number of times, depending on the shader's logic.</span></span>

<span data-ttu-id="0918e-453">[**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups)方法可讓轉換根據影像大小和轉換專屬的著色器知識，告知 [Direct2D](./direct2d-portal.md)需要多少執行緒群組。</span><span class="sxs-lookup"><span data-stu-id="0918e-453">The [**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) method allows the transform to inform [Direct2D](./direct2d-portal.md) how many thread groups are required, based on the size of the image and the transform's own knowledge of the shader.</span></span>

<span data-ttu-id="0918e-454">計算著色器執行的次數是此處指定的 threadgroup 計數產品，以及計算著色器 [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)中的 ' numthreads ' 注釋。</span><span class="sxs-lookup"><span data-stu-id="0918e-454">The number of times the compute shader is executed is a product of the threadgroup counts specified here and the 'numthreads' annotation in the compute shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span> <span data-ttu-id="0918e-455">例如，如果轉換將 threadgroup 維度設定為 (2，2，1) 著色器會為每個 threadgroup 指定 (3，3，1) 執行緒，然後執行 4 threadgroups，其中每個都有9個執行緒，總共36個執行緒實例。</span><span class="sxs-lookup"><span data-stu-id="0918e-455">For example, if the transform sets the threadgroup dimensions to be (2,2,1) the shader specifies (3,3,1) threads per threadgroup, then 4 threadgroups will be executed, each with 9 threads in them, for a total of 36 thread instances.</span></span>

<span data-ttu-id="0918e-456">常見的案例是針對計算著色器的每個實例處理一個輸出圖元。</span><span class="sxs-lookup"><span data-stu-id="0918e-456">A common scenario is to process one output pixel for each instance of the compute shader.</span></span> <span data-ttu-id="0918e-457">若要計算此案例的執行緒群組數目，轉換會將影像的寬度和高度除以 [計算著色器] [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)中的 [numthreads] 注釋的個別 x 和 y 維度。</span><span class="sxs-lookup"><span data-stu-id="0918e-457">To calculate the number of thread groups for this scenario, the transform divides the width and height of the image by the respective x and y dimensions of the 'numthreads' annotation in the compute shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span>

<span data-ttu-id="0918e-458">重要的是，如果執行此除法，則要求的執行緒群組數目必須一律無條件進位到最接近的整數，否則就不會執行「餘數」圖元。</span><span class="sxs-lookup"><span data-stu-id="0918e-458">Importantly, if this division is performed, then the number of thread groups requested must always be rounded up to the nearest integer, otherwise the 'remainder' pixels will not be executed upon.</span></span> <span data-ttu-id="0918e-459">如果著色器 (例如) 計算每個執行緒的單一圖元，則方法的程式碼會如下所示。</span><span class="sxs-lookup"><span data-stu-id="0918e-459">If a shader (for example) computes a single pixel with each thread, the method's code would appear as follows.</span></span>


```C++
IFACEMETHODIMP SampleTransform::CalculateThreadgroups(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_ UINT32* pDimensionX,
    _Out_ UINT32* pDimensionY,
    _Out_ UINT32* pDimensionZ
    )
{    
    // The input image's dimensions are divided by the corresponding number of threads in each
    // threadgroup. This is specified in the HLSL, and in this example is 24 for both the x and y
    // dimensions. Dividing the image dimensions by these values calculates the number of
    // thread groups that need to be executed.

    *pDimensionX = static_cast<UINT32>(
         ceil((m_inputRect.right - m_inputRect.left) / 24.0f);

    *pDimensionY = static_cast<UINT32>(
         ceil((m_inputRect.bottom - m_inputRect.top) / 24.0f);

    // The z dimension is set to '1' in this example because the shader will
    // only be executed once for each pixel in the two-dimensional input image.
    // This value can be increased to perform additional executions for a given
    // input position.
    *pDimensionZ = 1;

    return S_OK;
}
```



<span data-ttu-id="0918e-460">[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)會使用下列程式碼來指定每個執行緒群組中的執行緒數目：</span><span class="sxs-lookup"><span data-stu-id="0918e-460">The [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) uses the following code to specify the number of threads in each thread group:</span></span>


```hlsl
// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup. 
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(24, 24, 1)]
void main(
...
```



<span data-ttu-id="0918e-461">在執行期間，會將目前的 threadgroup 和目前的執行緒索引作為參數傳遞給著色器方法：</span><span class="sxs-lookup"><span data-stu-id="0918e-461">During execution, the current threadgroup and current thread index are passed as parameters to the shader method:</span></span>


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in ID2D1ComputeTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
...
```



### <a name="reading-image-data"></a><span data-ttu-id="0918e-462">讀取影像資料</span><span class="sxs-lookup"><span data-stu-id="0918e-462">Reading image data</span></span>

<span data-ttu-id="0918e-463">計算著色器會以單一二維材質存取轉換的輸入影像：</span><span class="sxs-lookup"><span data-stu-id="0918e-463">Compute shaders access the transform's input image as a single two-dimensional texture:</span></span>


```hlsl
Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);
```



<span data-ttu-id="0918e-464">不過，就像圖元著色器一樣，不保證影像的資料會在材質 (0、0) 開始。</span><span class="sxs-lookup"><span data-stu-id="0918e-464">However, like pixel shaders, the image's data is not guaranteed to begin at (0, 0) on the texture.</span></span> <span data-ttu-id="0918e-465">相反地， [Direct2D](./direct2d-portal.md) 會提供可讓著色器彌補任何位移的系統常數：</span><span class="sxs-lookup"><span data-stu-id="0918e-465">Instead, [Direct2D](./direct2d-portal.md) provides system constants that allow shaders to compensate for any offset:</span></span>


```hlsl
// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the input rectangle to the shader in terms of pixels.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}
```



<span data-ttu-id="0918e-466">一旦定義上述常數緩衝區和 helper 方法之後，著色器就可以使用下列程式來取樣影像資料：</span><span class="sxs-lookup"><span data-stu-id="0918e-466">Once the above constant buffer and helper method have been defined, the shader can sample image data using the following:</span></span>


```hlsl
float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by input image offset.
            ),
        0
        );
```



### <a name="writing-image-data"></a><span data-ttu-id="0918e-467">寫入影像資料</span><span class="sxs-lookup"><span data-stu-id="0918e-467">Writing image data</span></span>

<span data-ttu-id="0918e-468">[Direct2D](./direct2d-portal.md) 預期著色器會定義要放置結果影像的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0918e-468">[Direct2D](./direct2d-portal.md) expects a shader to define an output buffer for the resulting image to be placed.</span></span> <span data-ttu-id="0918e-469">在著色器模型 4 (DirectX 10) 中，由於功能條件約束，這必須是一維緩衝區：</span><span class="sxs-lookup"><span data-stu-id="0918e-469">In Shader Model 4 (DirectX 10), this must be a single-dimensional buffer due to feature constraints:</span></span>


```hlsl
// Shader Model 4 does not support RWTexture2D, must use 1D buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);
```



<span data-ttu-id="0918e-470">輸出材質會先編制資料列索引，以允許儲存整個影像。</span><span class="sxs-lookup"><span data-stu-id="0918e-470">The output texture is indexed row-first to allow the entire image to be stored.</span></span>


```hlsl
uint imageWidth = resultRect[2] - resultRect[0];
uint imageHeight = resultRect[3] - resultRect[1];
OutputTexture[yIndex * imageWidth + xIndex] = color;
```



<span data-ttu-id="0918e-471">另一方面，著色器模型 5 (DirectX 11) 著色器可以使用二維輸出紋理：</span><span class="sxs-lookup"><span data-stu-id="0918e-471">On the other hand, Shader Model 5 (DirectX 11) shaders can use two-dimensional output textures:</span></span>


```hlsl
RWTexture2D<float4> OutputTexture : register(t1);
```



<span data-ttu-id="0918e-472">在著色器模型5著色器中， [Direct2D](./direct2d-portal.md) 會在常數緩衝區中提供額外的 ' outputOffset ' 參數。</span><span class="sxs-lookup"><span data-stu-id="0918e-472">With Shader Model 5 shaders, [Direct2D](./direct2d-portal.md) provides an additional 'outputOffset' parameter in the constant buffer.</span></span> <span data-ttu-id="0918e-473">著色器的輸出應以此數量 offsetted：</span><span class="sxs-lookup"><span data-stu-id="0918e-473">The shader's output should be offsetted by this amount:</span></span>


```hlsl
OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



<span data-ttu-id="0918e-474">完成的傳遞著色器模型5計算著色器如下所示。</span><span class="sxs-lookup"><span data-stu-id="0918e-474">A completed pass-through Shader Model 5 compute shader is shown below.</span></span> <span data-ttu-id="0918e-475">在其中，每個計算著色器執行緒都會讀取並寫入輸入影像的單一圖元。</span><span class="sxs-lookup"><span data-stu-id="0918e-475">In it, each of the compute shader threads reads and writes a single pixel of the input image.</span></span>


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

RWTexture2D<float4> OutputTexture : register(t1);

// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    int2 outputOffset;
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 5, z <= 64 and x*y*z <= 1024
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    uint imageWidth = resultRect.z - resultRect.x;
    uint imageHeight = resultRect.w - resultRect.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is
    // executed in chunks sized by the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups.
    // For this reason each shader should ensure the current dispatchThreadId is within the bounds of the input
    // image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



<span data-ttu-id="0918e-476">下列程式碼顯示對應的著色器模型4版本著色器。</span><span class="sxs-lookup"><span data-stu-id="0918e-476">The code below shows the equivalent Shader Model 4 version of the shader.</span></span> <span data-ttu-id="0918e-477">請注意，著色器現在會轉譯成一維輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0918e-477">Notice that the shader now renders into a single-dimensional output buffer.</span></span>


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

// Shader Model 4 does not support RWTexture2D, must use one-dimensional buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);

// These are default constants passed by D2D. See PixelShader and VertexShader
// projects for how to pass custom values into a shader.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y, groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint imageWidth = resultRect[2] - resultRect[0];
    uint imageHeight = resultRect[3] - resultRect[1];

    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is executed in chunks sized by
    // the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups. For this reason each shader should ensure the current
    // dispatchThreadId is within the bounds of the input image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[yIndex * imageWidth + xIndex] = color;
}
```



## <a name="related-topics"></a><span data-ttu-id="0918e-478">相關主題</span><span class="sxs-lookup"><span data-stu-id="0918e-478">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0918e-479">D2DCustomEffects SDK 範例</span><span class="sxs-lookup"><span data-stu-id="0918e-479">D2DCustomEffects SDK sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)
</dt> </dl>

 

 
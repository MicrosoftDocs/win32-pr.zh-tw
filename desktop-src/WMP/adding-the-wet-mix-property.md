---
title: 新增濕混合屬性
description: 新增濕混合屬性
ms.assetid: 4605d893-8ac0-42fd-a1ac-51430561f174
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性
- 外掛程式，Echo 範例屬性
- 數位信號處理外掛程式，Echo 範例屬性
- DSP 外掛程式，Echo 範例屬性
- Echo DSP 外掛程式範例，屬性
- Echo DSP 外掛程式範例，濕混合屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6af8e7b4857ccbf6b725044575d1b8524aaf50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300927"
---
# <a name="adding-the-wet-mix-property"></a><span data-ttu-id="9da1c-109">新增濕混合屬性</span><span class="sxs-lookup"><span data-stu-id="9da1c-109">Adding the Wet Mix Property</span></span>

<span data-ttu-id="9da1c-110">您必須加入程式碼，才能為效果層級提供其他屬性。</span><span class="sxs-lookup"><span data-stu-id="9da1c-110">You must add the code to provide the additional property for the effect level.</span></span>

<span data-ttu-id="9da1c-111">將 [屬性新增至範例音訊 DSP 外掛程式](adding-properties-to-the-sample-audio-dsp-plug-in.md) 的區段提供如何使用 Visual C++ 新增屬性的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9da1c-111">The section [Adding Properties to the Sample Audio DSP Plug-in](adding-properties-to-the-sample-audio-dsp-plug-in.md) provides details about how to add a new property using Visual C++.</span></span> <span data-ttu-id="9da1c-112">本節說明如何手動新增程式碼。</span><span class="sxs-lookup"><span data-stu-id="9da1c-112">This section shows you how to add the code manually.</span></span> <span data-ttu-id="9da1c-113">這需要在您修改延遲時間屬性程式碼的相同三個位置中加入程式碼。</span><span class="sxs-lookup"><span data-stu-id="9da1c-113">This entails adding code in the same three places where you modified the code for the delay time property.</span></span>

<span data-ttu-id="9da1c-114">加入 get wetmix 的原型 \_ ，並 \_ 立即在 Echo 中的其他屬性方法原型後面放置 wetmix 方法。</span><span class="sxs-lookup"><span data-stu-id="9da1c-114">Add the prototypes for the get\_wetmix and put\_wetmix methods immediately following the other property method prototypes in Echo.h.</span></span> <span data-ttu-id="9da1c-115">使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="9da1c-115">Use the following syntax:</span></span>


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



<span data-ttu-id="9da1c-116">現在，在 Echo 中的其他屬性執行之後，新增每個方法的實作為。</span><span class="sxs-lookup"><span data-stu-id="9da1c-116">Now, add the implementation for each method immediately following the other property implementations in Echo.cpp.</span></span> <span data-ttu-id="9da1c-117">下列範例會顯示這兩種方法的程式碼：</span><span class="sxs-lookup"><span data-stu-id="9da1c-117">The following example shows the code for both methods:</span></span>


```C++
// Property get to retrieve the wet mix value by using the public interface.
STDMETHODIMP CEcho::get_wetmix(double *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_fWetMix;

    return S_OK;
}

// Property put to store the wet mix value by using the public interface.
STDMETHODIMP CEcho::put_wetmix(double newVal)
{
    m_fWetMix = newVal;

    // Calculate m_fDryMix
    m_fDryMix = 1.0 - m_fWetMix;
    
    return S_OK;
}

```



<span data-ttu-id="9da1c-118">請注意，put wetmix 的實 \_ 值包含用來計算 m fDryMix 正確值的程式碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9da1c-118">Notice that the implementation of put\_wetmix includes the code to calculate the correct value for m\_fDryMix.</span></span> <span data-ttu-id="9da1c-119">每次針對 m fWetMix 指定新值時 \_ ，就需要進行這項計算。</span><span class="sxs-lookup"><span data-stu-id="9da1c-119">Each time a new value is specified for m\_fWetMix, this calculation is required.</span></span>

<span data-ttu-id="9da1c-120">在介面定義中加入下列程式碼，緊接在 Echo 中 delay 方法的程式碼之後：</span><span class="sxs-lookup"><span data-stu-id="9da1c-120">Add the following code in the interface definition just after the code for the delay methods in Echo.idl:</span></span>


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a><span data-ttu-id="9da1c-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="9da1c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9da1c-122">**Echo 範例屬性**</span><span class="sxs-lookup"><span data-stu-id="9da1c-122">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 





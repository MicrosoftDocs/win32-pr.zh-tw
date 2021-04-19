---
title: D1114 非選擇性指標 Null
ms.assetid: 62f0f247-8359-4f75-b3ce-195202d491d5
description: Interface：：方法的參數不是選擇性的。 傳遞了 Null 指標。 這會導致 Direct2D 損毀。
keywords:
- D1114 非選擇性指標 Null Direct2D
topic_type:
- apiref
api_name:
- D1114 Non Optional Pointer NULL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: abf8f070e339f2dcda5f818f5ffd5386c33d0e29
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/27/2021
ms.locfileid: "107001636"
---
# <a name="d1114-non-optional-pointer-null"></a><span data-ttu-id="3e99f-106">D1114：非選擇性指標 Null</span><span class="sxs-lookup"><span data-stu-id="3e99f-106">D1114: Non Optional Pointer NULL</span></span>

<span data-ttu-id="3e99f-107">\[  \] *Interface*：：*方法* 的參數參數不是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="3e99f-107">The parameter \[*parameter*\] for *interface*::*method* is not optional.</span></span> <span data-ttu-id="3e99f-108">傳遞了 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="3e99f-108">A **NULL** pointer was passed.</span></span> <span data-ttu-id="3e99f-109">這會導致 Direct2D 損毀。</span><span class="sxs-lookup"><span data-stu-id="3e99f-109">This will cause Direct2D to crash.</span></span>

### <a name="placeholders"></a><span data-ttu-id="3e99f-110">預留位置</span><span class="sxs-lookup"><span data-stu-id="3e99f-110">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="3e99f-111"><span id="parameter"></span><span id="PARAMETER"></span>*參數*</span><span class="sxs-lookup"><span data-stu-id="3e99f-111"><span id="parameter"></span><span id="PARAMETER"></span>*parameter*</span></span>
</dt> <dd>

<span data-ttu-id="3e99f-112">包含 **Null** 指標的參數名稱。</span><span class="sxs-lookup"><span data-stu-id="3e99f-112">The name of the parameter that contains the **NULL** pointer.</span></span>

</dd> <dt>

<span data-ttu-id="3e99f-113"><span id="interface"></span><span id="INTERFACE"></span>*介面*</span><span class="sxs-lookup"><span data-stu-id="3e99f-113"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="3e99f-114">*方法* 所屬的介面名稱。</span><span class="sxs-lookup"><span data-stu-id="3e99f-114">The name of the interface to which the *method* belongs.</span></span>

</dd> <dt>

<span data-ttu-id="3e99f-115"><span id="method"></span><span id="METHOD"></span>*方法*</span><span class="sxs-lookup"><span data-stu-id="3e99f-115"><span id="method"></span><span id="METHOD"></span>*method*</span></span>
</dt> <dd>

<span data-ttu-id="3e99f-116">收到無效參數之方法的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e99f-116">The name of the method that received the invalid parameter.</span></span>

</dd> </dl> 




 

### <a name="examples"></a><span data-ttu-id="3e99f-117">範例</span><span class="sxs-lookup"><span data-stu-id="3e99f-117">Examples</span></span>

<span data-ttu-id="3e99f-118">下列範例顯示 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法收到非選擇性 *GEOMETRY* 參數的 Null 指標。</span><span class="sxs-lookup"><span data-stu-id="3e99f-118">The following example shows that the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method receives a NULL pointer for the non-optional *geometry* parameter.</span></span>


```C++
        m_pRenderTarget->FillGeometry(NULL, m_pYellowGreenBrush);
```



<span data-ttu-id="3e99f-119">此範例會產生下列 debug 訊息：</span><span class="sxs-lookup"><span data-stu-id="3e99f-119">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG ERROR - The parameter [geometry] for ID2D1RenderTarget::FillGeometry is not optional. 
A NULL pointer was passed. This will cause Direct2D to crash.
```

## <a name="possible-causes"></a><span data-ttu-id="3e99f-120">可能的原因</span><span class="sxs-lookup"><span data-stu-id="3e99f-120">Possible Causes</span></span>

<span data-ttu-id="3e99f-121">傳遞非選擇性參數的 Null 指標。</span><span class="sxs-lookup"><span data-stu-id="3e99f-121">A NULL pointer was passed for a non-optional parameter.</span></span>

## <a name="fixes"></a><span data-ttu-id="3e99f-122">修正</span><span class="sxs-lookup"><span data-stu-id="3e99f-122">Fixes</span></span>

<span data-ttu-id="3e99f-123">確定非選擇性參數沒有 Null 指標。</span><span class="sxs-lookup"><span data-stu-id="3e99f-123">Ensure that a non-optional parameter does not have a NULL pointer.</span></span>

 

 

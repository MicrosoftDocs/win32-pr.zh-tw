---
title: D1115 列舉值無效
description: D1115 列舉值無效
ms.assetid: cfffd2b8-a7d3-4a60-8586-81d8435936a6
keywords:
- D1115 列舉值無效 Direct2D
topic_type:
- apiref
api_name:
- D1115 Enumeration Value Not Valid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edcfe70c67e61a3b8bfc435adfdaa017a1c62b22
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/27/2021
ms.locfileid: "106999761"
---
# <a name="d1115-enumeration-value-not-valid"></a><span data-ttu-id="852cb-104">D1115：列舉值無效</span><span class="sxs-lookup"><span data-stu-id="852cb-104">D1115: Enumeration Value Not Valid</span></span>

<span data-ttu-id="852cb-105">\[  \] \[  \] *Interface*：：*method* 值為 value 的參數參數不是有效的列舉值。</span><span class="sxs-lookup"><span data-stu-id="852cb-105">The parameter \[*parameter*\] with value \[*value*\] for *interface*::*method* is not a valid enumeration value.</span></span>

## <a name="placeholders"></a><span data-ttu-id="852cb-106">預留位置</span><span class="sxs-lookup"><span data-stu-id="852cb-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="852cb-107"><span id="parameter"></span><span id="PARAMETER"></span>*參數*</span><span class="sxs-lookup"><span data-stu-id="852cb-107"><span id="parameter"></span><span id="PARAMETER"></span>*parameter*</span></span>
</dt> <dd>

<span data-ttu-id="852cb-108">收到未預期之類型的參數名稱。</span><span class="sxs-lookup"><span data-stu-id="852cb-108">The name of the parameter that received the unexpected type.</span></span>

</dd> <dt>

<span data-ttu-id="852cb-109"><span id="value"></span><span id="VALUE"></span>*價值*</span><span class="sxs-lookup"><span data-stu-id="852cb-109"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="852cb-110">不正確列舉值。</span><span class="sxs-lookup"><span data-stu-id="852cb-110">The invalid enumeration value.</span></span>

</dd> <dt>

<span data-ttu-id="852cb-111"><span id="interface"></span><span id="INTERFACE"></span>*介面*</span><span class="sxs-lookup"><span data-stu-id="852cb-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="852cb-112">*方法* 所屬的介面名稱。</span><span class="sxs-lookup"><span data-stu-id="852cb-112">The name of the interface to which the *method* belongs.</span></span>

</dd> <dt>

<span data-ttu-id="852cb-113"><span id="method"></span><span id="METHOD"></span>*方法*</span><span class="sxs-lookup"><span data-stu-id="852cb-113"><span id="method"></span><span id="METHOD"></span>*method*</span></span>
</dt> <dd>

<span data-ttu-id="852cb-114">收到無效列舉值之方法的名稱。</span><span class="sxs-lookup"><span data-stu-id="852cb-114">The name of the method that received the invalid enumeration value.</span></span>

</dd> </dl> 




 

## <a name="examples"></a><span data-ttu-id="852cb-115">範例</span><span class="sxs-lookup"><span data-stu-id="852cb-115">Examples</span></span>

<span data-ttu-id="852cb-116">下列範例會指定 [**D2D1 轉譯 \_ \_ 目標 \_ 型**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) 別列舉值30（超出預期的範圍）。</span><span class="sxs-lookup"><span data-stu-id="852cb-116">The following example specifies a [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) enumeration value of 30, which is outside the expected range.</span></span>


```C++
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties((D2D1_RENDER_TARGET_TYPE)(30)),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



<span data-ttu-id="852cb-117">此範例會產生下列 debug 訊息：</span><span class="sxs-lookup"><span data-stu-id="852cb-117">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG ERROR - The parameter [renderTargetProperties->type] with value [30] 
for ID2D1Factory::CreateHwndRenderTarget is not a valid enumeration value.
```

## <a name="possible-causes"></a><span data-ttu-id="852cb-118">可能的原因</span><span class="sxs-lookup"><span data-stu-id="852cb-118">Possible Causes</span></span>

<span data-ttu-id="852cb-119">參數使用了不正確列舉值。</span><span class="sxs-lookup"><span data-stu-id="852cb-119">A parameter used an invalid enumeration value.</span></span>

## <a name="fixes"></a><span data-ttu-id="852cb-120">修正</span><span class="sxs-lookup"><span data-stu-id="852cb-120">Fixes</span></span>

<span data-ttu-id="852cb-121">請使用有效的列舉值。</span><span class="sxs-lookup"><span data-stu-id="852cb-121">Use a valid enumeration value.</span></span>

> [!Note]  
> <span data-ttu-id="852cb-122">Debug 層目前只會檢查個別的列舉值;它不會檢查位組合是否有效。</span><span class="sxs-lookup"><span data-stu-id="852cb-122">The debug layer currently checks only the individual enumeration values; it does not check whether a bitwise combination is valid.</span></span>

 

 

 

---
title: " (Direct3D 11) 的批註語法"
description: 批註是使用者定義的資訊片段，以本節所述的語法來宣告。
ms.assetid: a81198d2-c4d7-47b5-b3b8-2de11a9ee9a3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9583dafd3e1fb314ae6ac9e53d609bebc74a030
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933267"
---
# <a name="annotation-syntax-direct3d-11"></a><span data-ttu-id="fb73d-103"> (Direct3D 11) 的批註語法</span><span class="sxs-lookup"><span data-stu-id="fb73d-103">Annotation Syntax (Direct3D 11)</span></span>

<span data-ttu-id="fb73d-104">批註是使用者定義的資訊片段，以本節所述的語法來宣告。</span><span class="sxs-lookup"><span data-stu-id="fb73d-104">An annotation is a user-defined piece of information, declared with the syntax described in this section.</span></span>



| <span data-ttu-id="fb73d-105"><*DataType* *名稱*  =  *值*;*...*; ></span><span class="sxs-lookup"><span data-stu-id="fb73d-105"><*DataType* *Name* = *Value*; *...* ;></span></span> |
|----------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="fb73d-106">參數</span><span class="sxs-lookup"><span data-stu-id="fb73d-106">Parameters</span></span>



| <span data-ttu-id="fb73d-107">項目</span><span class="sxs-lookup"><span data-stu-id="fb73d-107">Item</span></span>                                                                                                   | <span data-ttu-id="fb73d-108">描述</span><span class="sxs-lookup"><span data-stu-id="fb73d-108">Description</span></span>                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb73d-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*資料類型*</span><span class="sxs-lookup"><span data-stu-id="fb73d-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*DataType*</span></span><br/> | <span data-ttu-id="fb73d-110">\[在 \] 資料類型中，包含任何純量 [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) 類型以及 [字串類型](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar)。</span><span class="sxs-lookup"><span data-stu-id="fb73d-110">\[in\] The data type, which includes any [scalar HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) type as well as the [string type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).</span></span><br/> |
| <span data-ttu-id="fb73d-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*名字*</span><span class="sxs-lookup"><span data-stu-id="fb73d-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span><br/>                 | <span data-ttu-id="fb73d-112">\[\]表示批註名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="fb73d-112">\[in\] An ASCII string, that represents the annotation name.</span></span><br/>                                                                                                          |
| <span data-ttu-id="fb73d-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*價值*</span><span class="sxs-lookup"><span data-stu-id="fb73d-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Value*</span></span><br/>             | <span data-ttu-id="fb73d-114">\[在 \] 批註的初始值中。</span><span class="sxs-lookup"><span data-stu-id="fb73d-114">\[in\] The initial value of the annotation.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="fb73d-115"><span id="..."></span>*...*</span><span class="sxs-lookup"><span data-stu-id="fb73d-115"><span id="..."></span>*...*</span></span><br/>                                                                 | <span data-ttu-id="fb73d-116">\[在 \] 其他批註中 (名稱/值組) 。</span><span class="sxs-lookup"><span data-stu-id="fb73d-116">\[in\] Additional annotations (name-value pairs).</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="fb73d-117">備註</span><span class="sxs-lookup"><span data-stu-id="fb73d-117">Remarks</span></span>

<span data-ttu-id="fb73d-118">您可以在角括弧內加入多個注釋，每一個都以分號分隔。</span><span class="sxs-lookup"><span data-stu-id="fb73d-118">You may add more than one annotation within the angle brackets, each one separated by a semicolon.</span></span> <span data-ttu-id="fb73d-119">效果架構 Api 會辨識全域變數上的注釋;所有其他注釋都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="fb73d-119">The effect framework APIs recognize annotations on global variables; all other annotations are ignored.</span></span>

## <a name="example"></a><span data-ttu-id="fb73d-120">範例</span><span class="sxs-lookup"><span data-stu-id="fb73d-120">Example</span></span>

<span data-ttu-id="fb73d-121">以下是一些範例。</span><span class="sxs-lookup"><span data-stu-id="fb73d-121">Here are some examples.</span></span>


```
       
int i <int blabla=27; string blacksheep="Hello There";>;

int j <int bambam=30; string blacksheep="Goodbye There";> = 5 ;

float y <float y=2.3;> = 2.3, z <float y=1.3;> = 1.3 ;

half w <half GlobalW = 3.62;>;

float4 main(float4 pos : SV_POSITION ) : SV_POSITION
{
    pos.y = pos.x > 0 ? pos.w * 1.3 : pos.z * .032;
    for (int x = i; x < j ; x++) 
    {
        pos.w = pos.w * pos.y + x + j - y * w;
    } 

return pos;
}
```



## <a name="related-topics"></a><span data-ttu-id="fb73d-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="fb73d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb73d-123">效果格式</span><span class="sxs-lookup"><span data-stu-id="fb73d-123">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="fb73d-124">效果變數語法</span><span class="sxs-lookup"><span data-stu-id="fb73d-124">Effect Variable Syntax</span></span>](d3d11-effect-variable-syntax.md)
</dt> </dl>

 


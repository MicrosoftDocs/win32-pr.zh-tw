---
description: 批註是以下列語法宣告的使用者定義資訊片段。
ms.assetid: 9178e61e-05a4-441c-a9f1-e05e23ab48a5
title: " (Direct3D 10) 的批註語法"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303065e9c49c380a5accba6faadbc641ec0f528a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847615"
---
# <a name="annotation-syntax-direct3d-10"></a><span data-ttu-id="7a2d6-103"> (Direct3D 10) 的批註語法</span><span class="sxs-lookup"><span data-stu-id="7a2d6-103">Annotation Syntax (Direct3D 10)</span></span>

<span data-ttu-id="7a2d6-104">批註是以下列語法宣告的使用者定義資訊片段。</span><span class="sxs-lookup"><span data-stu-id="7a2d6-104">An annotation is a user-defined piece of information, declared with the following syntax.</span></span>



| <span data-ttu-id="7a2d6-105"><*DataType* *名稱*  =  *值*; ...;></span><span class="sxs-lookup"><span data-stu-id="7a2d6-105"><*DataType* *Name* = *Value*; ... ;></span></span> |
|--------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="7a2d6-106">參數</span><span class="sxs-lookup"><span data-stu-id="7a2d6-106">Parameters</span></span>



| <span data-ttu-id="7a2d6-107">項目</span><span class="sxs-lookup"><span data-stu-id="7a2d6-107">Item</span></span>                                                                                                   | <span data-ttu-id="7a2d6-108">描述</span><span class="sxs-lookup"><span data-stu-id="7a2d6-108">Description</span></span>                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a2d6-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*資料類型*</span><span class="sxs-lookup"><span data-stu-id="7a2d6-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*DataType*</span></span><br/> | <span data-ttu-id="7a2d6-110">\[在 \] 資料類型中，包含任何純量 [HLSL](../direct3dhlsl/dx-graphics-hlsl-scalar.md) 類型以及 [字串類型](../direct3dhlsl/dx-graphics-hlsl-scalar.md)。</span><span class="sxs-lookup"><span data-stu-id="7a2d6-110">\[in\] The data type, which includes any [scalar HLSL](../direct3dhlsl/dx-graphics-hlsl-scalar.md) type as well as the [string type](../direct3dhlsl/dx-graphics-hlsl-scalar.md).</span></span><br/> |
| <span data-ttu-id="7a2d6-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*名字*</span><span class="sxs-lookup"><span data-stu-id="7a2d6-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span><br/>                 | <span data-ttu-id="7a2d6-112">\[\]表示批註名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="7a2d6-112">\[in\] An ASCII string, that represents the annotation name.</span></span><br/>                                                                                                          |
| <span data-ttu-id="7a2d6-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*價值*</span><span class="sxs-lookup"><span data-stu-id="7a2d6-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Value*</span></span><br/>             | <span data-ttu-id="7a2d6-114">\[在 \] 批註的初始值中。</span><span class="sxs-lookup"><span data-stu-id="7a2d6-114">\[in\] The initial value of the annotation.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="7a2d6-115"><span id="..."></span>*...*</span><span class="sxs-lookup"><span data-stu-id="7a2d6-115"><span id="..."></span>*...*</span></span><br/>                                                                 | <span data-ttu-id="7a2d6-116">\[在 \] 其他批註中 (名稱/值組) 。</span><span class="sxs-lookup"><span data-stu-id="7a2d6-116">\[in\] Additional annotations (name-value pairs).</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="7a2d6-117">備註</span><span class="sxs-lookup"><span data-stu-id="7a2d6-117">Remarks</span></span>

<span data-ttu-id="7a2d6-118">您可以在角括弧內加入多個注釋，每一個都以分號分隔。</span><span class="sxs-lookup"><span data-stu-id="7a2d6-118">You may add more than one annotation within the angle brackets, each one separated by a semicolon.</span></span> <span data-ttu-id="7a2d6-119">效果架構 Api 會辨識全域變數上的注釋;所有其他注釋都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="7a2d6-119">The effect framework APIs recognize annotations on global variables; all other annotations are ignored.</span></span>

## <a name="example"></a><span data-ttu-id="7a2d6-120">範例</span><span class="sxs-lookup"><span data-stu-id="7a2d6-120">Example</span></span>

<span data-ttu-id="7a2d6-121">以下是一些範例。</span><span class="sxs-lookup"><span data-stu-id="7a2d6-121">Here are some examples.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7a2d6-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="7a2d6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a2d6-123">效果變數語法</span><span class="sxs-lookup"><span data-stu-id="7a2d6-123">Effect Variable Syntax</span></span>](d3d10-effect-variable-syntax.md)
</dt> </dl>

 

 

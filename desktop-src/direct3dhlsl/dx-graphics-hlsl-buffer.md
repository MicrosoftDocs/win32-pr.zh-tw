---
title: 緩衝區類型
description: 使用下列語法來宣告緩衝區變數。
ms.assetid: f21f0de5-58e3-466b-97bb-e4e7efa9cc1c
keywords:
- 緩衝區類型 HLSL
topic_type:
- apiref
api_name:
- Buffer Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e36030f3dd31f1bdada238e89c1048e4971cd45c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023676"
---
# <a name="buffer-type"></a><span data-ttu-id="91cfd-104">緩衝區類型</span><span class="sxs-lookup"><span data-stu-id="91cfd-104">Buffer Type</span></span>

<span data-ttu-id="91cfd-105">使用下列語法來宣告緩衝區變數。</span><span class="sxs-lookup"><span data-stu-id="91cfd-105">Use the following syntax to declare a buffer variable.</span></span>



| <span data-ttu-id="91cfd-106">緩衝區<*類型* >  *名稱*;</span><span class="sxs-lookup"><span data-stu-id="91cfd-106">Buffer<*Type*> *Name*;</span></span> |
|------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="91cfd-107">參數</span><span class="sxs-lookup"><span data-stu-id="91cfd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91cfd-108"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**緩衝區**</span><span class="sxs-lookup"><span data-stu-id="91cfd-108"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="91cfd-109">必要關鍵字。</span><span class="sxs-lookup"><span data-stu-id="91cfd-109">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="91cfd-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*類型*</span><span class="sxs-lookup"><span data-stu-id="91cfd-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="91cfd-111">其中一個純 [量](dx-graphics-hlsl-scalar.md)、 [向量](dx-graphics-hlsl-vector.md)和某些 [矩陣](dx-graphics-hlsl-matrix.md) HLSL 類型。</span><span class="sxs-lookup"><span data-stu-id="91cfd-111">One of the [scalar](dx-graphics-hlsl-scalar.md), [vector](dx-graphics-hlsl-vector.md), and some [matrix](dx-graphics-hlsl-matrix.md) HLSL types.</span></span> <span data-ttu-id="91cfd-112">您可以宣告具有矩陣的緩衝區變數，只要它符合 4 32 位數量即可。</span><span class="sxs-lookup"><span data-stu-id="91cfd-112">You can declare a buffer variable with a matrix as long as it fits in 4 32-bit quantities.</span></span> <span data-ttu-id="91cfd-113">因此，您可以撰寫 `Buffer<float2x2>` 。</span><span class="sxs-lookup"><span data-stu-id="91cfd-113">So, you can write `Buffer<float2x2>`.</span></span> <span data-ttu-id="91cfd-114">但 `Buffer<float4x4>` 太大，編譯器將會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="91cfd-114">But `Buffer<float4x4>` is too large, and the compiler will generate an error.</span></span>

</dd> <dt>

<span data-ttu-id="91cfd-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*名字*</span><span class="sxs-lookup"><span data-stu-id="91cfd-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="91cfd-116">可唯一識別變數名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="91cfd-116">An ASCII string that uniquely identifies the variable name.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="91cfd-117">範例</span><span class="sxs-lookup"><span data-stu-id="91cfd-117">Example</span></span>

<span data-ttu-id="91cfd-118">以下是 [PipesGS 範例](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx)中 PipesGS 檔案的緩衝區宣告範例。</span><span class="sxs-lookup"><span data-stu-id="91cfd-118">Here is an example of a buffer declaration from the PipesGS.fx file in [PipesGS Sample](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).</span></span>


```
Buffer<float4> g_Buffer;
```



<span data-ttu-id="91cfd-119">使用 Load HLSL 內建函式的多 [**載**](dx-graphics-hlsl-to-load.md) 版本，從緩衝區讀取資料，此函式會採用一個輸入參數 (整數索引) 。</span><span class="sxs-lookup"><span data-stu-id="91cfd-119">Data is read from a buffer using an overloaded version of the [**Load**](dx-graphics-hlsl-to-load.md) HLSL intrinsic function that takes one input parameter (an integer index).</span></span> <span data-ttu-id="91cfd-120">緩衝區的存取方式就像是元素陣列;因此，此範例會讀取第二個元素。</span><span class="sxs-lookup"><span data-stu-id="91cfd-120">A buffer is accessed like an array of elements; therefore, this example reads the second element.</span></span>


```
float4 bufferData = g_Buffer.Load( 1 );
```



<span data-ttu-id="91cfd-121">使用 [資料流程輸出階段](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) 將資料輸出到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="91cfd-121">Use the [stream-output stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) to output data to a buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="91cfd-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91cfd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91cfd-123"> (DirectX HLSL) 的資料類型 </span><span class="sxs-lookup"><span data-stu-id="91cfd-123">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 
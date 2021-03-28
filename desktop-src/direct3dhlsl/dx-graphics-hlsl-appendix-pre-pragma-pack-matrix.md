---
title: pack_matrix pragma 指示詞
description: 指定矩陣之封裝對齊的 Pragma 指示詞。
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix pragma 指示詞 HLSL
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4bb5474702a1caba3f772002c34677601715caff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022473"
---
# <a name="pack_matrix-pragma-directive"></a><span data-ttu-id="74651-104">pack \_ 矩陣 pragma 指示詞</span><span class="sxs-lookup"><span data-stu-id="74651-104">pack\_matrix pragma Directive</span></span>

<span data-ttu-id="74651-105">指定矩陣之封裝對齊的 Pragma 指示詞。</span><span class="sxs-lookup"><span data-stu-id="74651-105">Pragma directive that specifies packing alignment for matrices.</span></span>



| <span data-ttu-id="74651-106">\#pragma pack \_ 矩陣 ( *對齊* ) </span><span class="sxs-lookup"><span data-stu-id="74651-106">\#pragma pack\_matrix( *alignment* )</span></span> |
|--------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="74651-107">參數</span><span class="sxs-lookup"><span data-stu-id="74651-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74651-108">項目</span><span class="sxs-lookup"><span data-stu-id="74651-108">Item</span></span></th>
<th><span data-ttu-id="74651-109">描述</span><span class="sxs-lookup"><span data-stu-id="74651-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="74651-110"><span id="alignment"></span><span id="ALIGNMENT"></span><em>對準</em></span><span class="sxs-lookup"><span data-stu-id="74651-110"><span id="alignment"></span><span id="ALIGNMENT"></span><em>alignment</em></span></span><br/></td>
<td><span data-ttu-id="74651-111">矩陣的對齊設定。</span><span class="sxs-lookup"><span data-stu-id="74651-111">Alignment to set for matrices.</span></span> <span data-ttu-id="74651-112">此參數可以採用下表所列的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="74651-112">This parameter can take one of the values listed in the following table.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="74651-113">值</span><span class="sxs-lookup"><span data-stu-id="74651-113">Value</span></span></th>
<th><span data-ttu-id="74651-114">描述</span><span class="sxs-lookup"><span data-stu-id="74651-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="74651-115">column_major</span><span class="sxs-lookup"><span data-stu-id="74651-115">column_major</span></span></td>
<td><span data-ttu-id="74651-116">預設值。</span><span class="sxs-lookup"><span data-stu-id="74651-116">Default.</span></span> <span data-ttu-id="74651-117">將矩陣封裝對齊設定為數據行主要。</span><span class="sxs-lookup"><span data-stu-id="74651-117">Sets the matrix packing alignment to column major.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74651-118">row_major</span><span class="sxs-lookup"><span data-stu-id="74651-118">row_major</span></span></td>
<td><span data-ttu-id="74651-119">將矩陣封裝對齊設定為 [資料列主要]。</span><span class="sxs-lookup"><span data-stu-id="74651-119">Sets the matrix packing alignment to row major.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="74651-120">範例</span><span class="sxs-lookup"><span data-stu-id="74651-120">Examples</span></span>

<span data-ttu-id="74651-121">下列範例會將矩陣封裝對齊設定為 [資料列主要]。</span><span class="sxs-lookup"><span data-stu-id="74651-121">The following example sets the matrix packing alignment to row major.</span></span>


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a><span data-ttu-id="74651-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74651-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74651-123"> (DirectX HLSL) 的預處理器指示詞 </span><span class="sxs-lookup"><span data-stu-id="74651-123">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="74651-124">\# (DirectX HLSL) 的 pragma 指示詞 </span><span class="sxs-lookup"><span data-stu-id="74651-124">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 






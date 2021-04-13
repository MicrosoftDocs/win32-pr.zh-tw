---
description: 將參數對應至頂點或圖元著色器暫存器的語法。 它們也可以是附加至非註冊參數的選擇性描述性字串。
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: 'D3DXSEMANTIC 結構 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSEMANTIC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 08a30ac4d669beb5b93f2823219cb167d9e8d67f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386447"
---
# <a name="d3dxsemantic-structure"></a><span data-ttu-id="b9b46-104">D3DXSEMANTIC 結構</span><span class="sxs-lookup"><span data-stu-id="b9b46-104">D3DXSEMANTIC structure</span></span>

<span data-ttu-id="b9b46-105">將參數對應至頂點或圖元著色器暫存器的語法。</span><span class="sxs-lookup"><span data-stu-id="b9b46-105">Semantics map a parameter to vertex or pixel shader registers.</span></span> <span data-ttu-id="b9b46-106">它們也可以是附加至非註冊參數的選擇性描述性字串。</span><span class="sxs-lookup"><span data-stu-id="b9b46-106">They can also be optional descriptive strings attached to non-register parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9b46-107">語法</span><span class="sxs-lookup"><span data-stu-id="b9b46-107">Syntax</span></span>


```C++
typedef struct D3DXSEMANTIC {
  UINT Usage;
  UINT UsageIndex;
} D3DXSEMANTIC, *LPD3DXSEMANTIC;
```



## <a name="members"></a><span data-ttu-id="b9b46-108">成員</span><span class="sxs-lookup"><span data-stu-id="b9b46-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b9b46-109">**使用量**</span><span class="sxs-lookup"><span data-stu-id="b9b46-109">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="b9b46-110">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9b46-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b9b46-111">識別如何使用資源的選項。</span><span class="sxs-lookup"><span data-stu-id="b9b46-111">Options that identify how resources are used.</span></span> <span data-ttu-id="b9b46-112">請參閱 [**D3DDECLUSAGE**](./d3ddeclusage.md)。</span><span class="sxs-lookup"><span data-stu-id="b9b46-112">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9b46-113">**UsageIndex**</span><span class="sxs-lookup"><span data-stu-id="b9b46-113">**UsageIndex**</span></span>
</dt> <dd>

<span data-ttu-id="b9b46-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9b46-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b9b46-115">修改如何解讀使用方式的選項。</span><span class="sxs-lookup"><span data-stu-id="b9b46-115">Options that modify how the usage is interpreted.</span></span> <span data-ttu-id="b9b46-116">使用方式和使用方式索引組成頂點宣告。</span><span class="sxs-lookup"><span data-stu-id="b9b46-116">The usage and usage index make up a vertex declaration.</span></span> <span data-ttu-id="b9b46-117">請參閱 [ (Direct3D 9) 的頂點 ](vertex-declaration.md)宣告。</span><span class="sxs-lookup"><span data-stu-id="b9b46-117">See [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9b46-118">備註</span><span class="sxs-lookup"><span data-stu-id="b9b46-118">Remarks</span></span>

<span data-ttu-id="b9b46-119">頂點和圖元著色器、輸入和輸出暫存器需要有語義。</span><span class="sxs-lookup"><span data-stu-id="b9b46-119">Semantics are required for vertex and pixel shader, input and output registers.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9b46-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9b46-120">Requirements</span></span>



| <span data-ttu-id="b9b46-121">需求</span><span class="sxs-lookup"><span data-stu-id="b9b46-121">Requirement</span></span> | <span data-ttu-id="b9b46-122">值</span><span class="sxs-lookup"><span data-stu-id="b9b46-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9b46-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b9b46-123">Header</span></span><br/> | <dl> <span data-ttu-id="b9b46-124"><dt>D3dx9shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="b9b46-124"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9b46-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9b46-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9b46-126">效果結構</span><span class="sxs-lookup"><span data-stu-id="b9b46-126">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 

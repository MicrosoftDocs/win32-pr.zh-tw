---
description: ID3DXEffectCompiler 介面會從函式或頂點著色器編譯效果。
ms.assetid: 2d1dbc63-1eb9-4736-a0b5-7f899c0638be
title: 'ID3DXEffectCompiler 介面 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d69cbcd6c14bb3a874a382f46fe5aee6619b8168
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322715"
---
# <a name="id3dxeffectcompiler-interface"></a><span data-ttu-id="a7d46-103">ID3DXEffectCompiler 介面</span><span class="sxs-lookup"><span data-stu-id="a7d46-103">ID3DXEffectCompiler interface</span></span>

<span data-ttu-id="a7d46-104">**ID3DXEffectCompiler** 介面會從函式或頂點著色器編譯效果。</span><span class="sxs-lookup"><span data-stu-id="a7d46-104">The **ID3DXEffectCompiler** interface compiles an effect from a function or from a vertex shader.</span></span>

## <a name="members"></a><span data-ttu-id="a7d46-105">成員</span><span class="sxs-lookup"><span data-stu-id="a7d46-105">Members</span></span>

<span data-ttu-id="a7d46-106">**ID3DXEffectCompiler** 介面繼承自 [**ID3DXBaseEffect**](id3dxbaseeffect.md)。</span><span class="sxs-lookup"><span data-stu-id="a7d46-106">The **ID3DXEffectCompiler** interface inherits from [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span> <span data-ttu-id="a7d46-107">**ID3DXEffectCompiler** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a7d46-107">**ID3DXEffectCompiler** also has these types of members:</span></span>

-   [<span data-ttu-id="a7d46-108">方法</span><span class="sxs-lookup"><span data-stu-id="a7d46-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a7d46-109">方法</span><span class="sxs-lookup"><span data-stu-id="a7d46-109">Methods</span></span>

<span data-ttu-id="a7d46-110">**ID3DXEffectCompiler** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a7d46-110">The **ID3DXEffectCompiler** interface has these methods.</span></span>



| <span data-ttu-id="a7d46-111">方法</span><span class="sxs-lookup"><span data-stu-id="a7d46-111">Method</span></span>                                                      | <span data-ttu-id="a7d46-112">描述</span><span class="sxs-lookup"><span data-stu-id="a7d46-112">Description</span></span>                                                                                                                                 |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7d46-113">**CompileEffect**</span><span class="sxs-lookup"><span data-stu-id="a7d46-113">**CompileEffect**</span></span>](id3dxeffectcompiler--compileeffect.md) | <span data-ttu-id="a7d46-114">編譯效果。</span><span class="sxs-lookup"><span data-stu-id="a7d46-114">Compile an effect.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="a7d46-115">**CompileShader**</span><span class="sxs-lookup"><span data-stu-id="a7d46-115">**CompileShader**</span></span>](id3dxeffectcompiler--compileshader.md) | <span data-ttu-id="a7d46-116">從包含一或多個函式的效果編譯著色器。</span><span class="sxs-lookup"><span data-stu-id="a7d46-116">Compiles a shader from an effect that contains one or more functions.</span></span><br/>                                                            |
| [<span data-ttu-id="a7d46-117">**GetLiteral**</span><span class="sxs-lookup"><span data-stu-id="a7d46-117">**GetLiteral**</span></span>](id3dxeffectcompiler--getliteral.md)       | <span data-ttu-id="a7d46-118">取得參數的常值狀態。</span><span class="sxs-lookup"><span data-stu-id="a7d46-118">Gets a literal status of a parameter.</span></span> <span data-ttu-id="a7d46-119">常值參數的值不會在效果的存留期間變更。</span><span class="sxs-lookup"><span data-stu-id="a7d46-119">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span><br/>      |
| [<span data-ttu-id="a7d46-120">**SetLiteral**</span><span class="sxs-lookup"><span data-stu-id="a7d46-120">**SetLiteral**</span></span>](id3dxeffectcompiler--setliteral.md)       | <span data-ttu-id="a7d46-121">切換參數的常值狀態。</span><span class="sxs-lookup"><span data-stu-id="a7d46-121">Toggles the literal status of a parameter.</span></span> <span data-ttu-id="a7d46-122">常值參數的值不會在效果的存留期間變更。</span><span class="sxs-lookup"><span data-stu-id="a7d46-122">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a7d46-123">備註</span><span class="sxs-lookup"><span data-stu-id="a7d46-123">Remarks</span></span>

<span data-ttu-id="a7d46-124">ID3DXEffectCompiler 介面的取得方式是呼叫 [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)、 [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)或 [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)。</span><span class="sxs-lookup"><span data-stu-id="a7d46-124">The ID3DXEffectCompiler interface is obtained by calling [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md), or [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md).</span></span>

<span data-ttu-id="a7d46-125">LPD3DXEFFECTCOMPILER 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="a7d46-125">The LPD3DXEFFECTCOMPILER type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectCompiler ID3DXEffectCompiler;
typedef interface ID3DXEffectCompiler *LPD3DXEFFECTCOMPILER;
```



## <a name="requirements"></a><span data-ttu-id="a7d46-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7d46-126">Requirements</span></span>



| <span data-ttu-id="a7d46-127">需求</span><span class="sxs-lookup"><span data-stu-id="a7d46-127">Requirement</span></span> | <span data-ttu-id="a7d46-128">值</span><span class="sxs-lookup"><span data-stu-id="a7d46-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d46-129">標頭</span><span class="sxs-lookup"><span data-stu-id="a7d46-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a7d46-130"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="a7d46-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="a7d46-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="a7d46-131">Library</span></span><br/> | <dl> <span data-ttu-id="a7d46-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7d46-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a7d46-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7d46-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7d46-134">**ID3DXBaseEffect**</span><span class="sxs-lookup"><span data-stu-id="a7d46-134">**ID3DXBaseEffect**</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="a7d46-135">效果介面</span><span class="sxs-lookup"><span data-stu-id="a7d46-135">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a7d46-136">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="a7d46-136">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="a7d46-137">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="a7d46-137">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="a7d46-138">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="a7d46-138">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 





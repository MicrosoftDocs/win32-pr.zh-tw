---
description: 描述效果物件的傳遞。
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: 'D3DXPASS_DESC 結構 (D3dx9effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPASS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: a147f737057a5b2cff6ea436d9d2e47920a67a4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322636"
---
# <a name="d3dxpass_desc-structure"></a><span data-ttu-id="2ecdb-103">D3DXPASS \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="2ecdb-103">D3DXPASS\_DESC structure</span></span>

<span data-ttu-id="2ecdb-104">描述效果物件的傳遞。</span><span class="sxs-lookup"><span data-stu-id="2ecdb-104">Describes a pass for an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ecdb-105">語法</span><span class="sxs-lookup"><span data-stu-id="2ecdb-105">Syntax</span></span>


```C++
typedef struct D3DXPASS_DESC {
  LPCSTR      Name;
  UINT        Annotations;
  const DWORD *pVertexShaderFunction;
  const DWORD *pPixelShaderFunction;
} D3DXPASS_DESC, *LPD3DXPASS_DESC;
```



## <a name="members"></a><span data-ttu-id="2ecdb-106">成員</span><span class="sxs-lookup"><span data-stu-id="2ecdb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2ecdb-107">**名稱**</span><span class="sxs-lookup"><span data-stu-id="2ecdb-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="2ecdb-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ecdb-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2ecdb-109">用於傳遞的字串值。</span><span class="sxs-lookup"><span data-stu-id="2ecdb-109">String value used for the pass.</span></span>

</dd> <dt>

<span data-ttu-id="2ecdb-110">**註解**</span><span class="sxs-lookup"><span data-stu-id="2ecdb-110">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="2ecdb-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ecdb-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2ecdb-112">批註是使用者特定的資料，可附加至任何技術、傳遞或參數。</span><span class="sxs-lookup"><span data-stu-id="2ecdb-112">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="2ecdb-113">請參閱 [使用 \_ 批註將資訊新增至效果參數](using-an-effect.md)。</span><span class="sxs-lookup"><span data-stu-id="2ecdb-113">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ecdb-114">**pVertexShaderFunction**</span><span class="sxs-lookup"><span data-stu-id="2ecdb-114">**pVertexShaderFunction**</span></span>
</dt> <dd>

<span data-ttu-id="2ecdb-115">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ecdb-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="2ecdb-116">頂點著色器函式的指標。</span><span class="sxs-lookup"><span data-stu-id="2ecdb-116">Pointer to the vertex shader function.</span></span> <span data-ttu-id="2ecdb-117">如果使用 [D3DXFX \_ NOT \_ CLONEABLE](d3dxfx.md)建立效果，此結構會在由 [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)呼叫時傳回 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="2ecdb-117">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this structure will return a **NULL** pointer when called by [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ecdb-118">**pPixelShaderFunction**</span><span class="sxs-lookup"><span data-stu-id="2ecdb-118">**pPixelShaderFunction**</span></span>
</dt> <dd>

<span data-ttu-id="2ecdb-119">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ecdb-119">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="2ecdb-120">圖元著色器函式的指標。</span><span class="sxs-lookup"><span data-stu-id="2ecdb-120">Pointer to the pixel shader function.</span></span> <span data-ttu-id="2ecdb-121">如果使用 [D3DXFX \_ NOT \_ CLONEABLE](d3dxfx.md)建立效果，此結構會在由 [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)呼叫時傳回 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="2ecdb-121">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this structure will return a **NULL** pointer when called by [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ecdb-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ecdb-122">Requirements</span></span>



| <span data-ttu-id="2ecdb-123">需求</span><span class="sxs-lookup"><span data-stu-id="2ecdb-123">Requirement</span></span> | <span data-ttu-id="2ecdb-124">值</span><span class="sxs-lookup"><span data-stu-id="2ecdb-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ecdb-125">標頭</span><span class="sxs-lookup"><span data-stu-id="2ecdb-125">Header</span></span><br/> | <dl> <span data-ttu-id="2ecdb-126"><dt>D3dx9effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ecdb-126"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ecdb-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ecdb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ecdb-128">效果結構</span><span class="sxs-lookup"><span data-stu-id="2ecdb-128">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[<span data-ttu-id="2ecdb-129">**GetPassDesc**</span><span class="sxs-lookup"><span data-stu-id="2ecdb-129">**GetPassDesc**</span></span>](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 

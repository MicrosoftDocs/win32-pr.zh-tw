---
description: 描述效果所使用的技術。
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: 'D3DXTECHNIQUE_DESC 結構 (D3dx9effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTECHNIQUE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 35dd483a983f17371d6a77e6c020b3a45d9e9360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035342"
---
# <a name="d3dxtechnique_desc-structure"></a><span data-ttu-id="e6fdc-103">D3DXTECHNIQUE \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="e6fdc-103">D3DXTECHNIQUE\_DESC structure</span></span>

<span data-ttu-id="e6fdc-104">描述效果所使用的技術。</span><span class="sxs-lookup"><span data-stu-id="e6fdc-104">Describes a technique used by an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6fdc-105">語法</span><span class="sxs-lookup"><span data-stu-id="e6fdc-105">Syntax</span></span>


```C++
typedef struct D3DXTECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DXTECHNIQUE_DESC, *LPD3DXTECHNIQUE_DESC;
```



## <a name="members"></a><span data-ttu-id="e6fdc-106">成員</span><span class="sxs-lookup"><span data-stu-id="e6fdc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e6fdc-107">**名稱**</span><span class="sxs-lookup"><span data-stu-id="e6fdc-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="e6fdc-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6fdc-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6fdc-109">包含技術名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="e6fdc-109">String that contains the technique name.</span></span>

</dd> <dt>

<span data-ttu-id="e6fdc-110">**通過**</span><span class="sxs-lookup"><span data-stu-id="e6fdc-110">**Passes**</span></span>
</dt> <dd>

<span data-ttu-id="e6fdc-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6fdc-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6fdc-112">此技術所需的轉譯行程數目。</span><span class="sxs-lookup"><span data-stu-id="e6fdc-112">Number of rendering passes the technique requires.</span></span> <span data-ttu-id="e6fdc-113">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="e6fdc-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e6fdc-114">**註解**</span><span class="sxs-lookup"><span data-stu-id="e6fdc-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="e6fdc-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6fdc-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6fdc-116">注釋的數目。</span><span class="sxs-lookup"><span data-stu-id="e6fdc-116">The number of annotations.</span></span> <span data-ttu-id="e6fdc-117">請參閱 [使用 \_ 批註將資訊新增至效果參數](using-an-effect.md)。</span><span class="sxs-lookup"><span data-stu-id="e6fdc-117">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6fdc-118">備註</span><span class="sxs-lookup"><span data-stu-id="e6fdc-118">Remarks</span></span>

<span data-ttu-id="e6fdc-119">有些視訊卡可以在單一階段中轉譯兩個材質。</span><span class="sxs-lookup"><span data-stu-id="e6fdc-119">Some video cards can render two textures in a single pass.</span></span> <span data-ttu-id="e6fdc-120">但是，如果卡片沒有這項功能，通常可以在兩個階段中轉譯相同的效果，每次行程都使用一個材質。</span><span class="sxs-lookup"><span data-stu-id="e6fdc-120">However, if a card does not have this capability, it is often possible to render the same effect in two passes, using one texture for each pass.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6fdc-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6fdc-121">Requirements</span></span>



| <span data-ttu-id="e6fdc-122">需求</span><span class="sxs-lookup"><span data-stu-id="e6fdc-122">Requirement</span></span> | <span data-ttu-id="e6fdc-123">值</span><span class="sxs-lookup"><span data-stu-id="e6fdc-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6fdc-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e6fdc-124">Header</span></span><br/> | <dl> <span data-ttu-id="e6fdc-125"><dt>D3dx9effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6fdc-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6fdc-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6fdc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6fdc-127">效果結構</span><span class="sxs-lookup"><span data-stu-id="e6fdc-127">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 

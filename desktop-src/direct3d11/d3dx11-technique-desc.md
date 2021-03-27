---
title: 'D3DX11_TECHNIQUE_DESC 結構 (D3dx11effect .h) '
description: 描述效果技巧。
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- D3DX11_TECHNIQUE_DESC 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TECHNIQUE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31158b93b8121ac3393e0935cee31c6361b894d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696731"
---
# <a name="d3dx11_technique_desc-structure"></a><span data-ttu-id="9e70e-104">D3DX11 \_ 技術 \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="9e70e-104">D3DX11\_TECHNIQUE\_DESC structure</span></span>

<span data-ttu-id="9e70e-105">描述效果技巧。</span><span class="sxs-lookup"><span data-stu-id="9e70e-105">Describes an effect technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e70e-106">語法</span><span class="sxs-lookup"><span data-stu-id="9e70e-106">Syntax</span></span>


```C++
typedef struct _D3DX11_TECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DX11_TECHNIQUE_DESC;
```



## <a name="members"></a><span data-ttu-id="9e70e-107">成員</span><span class="sxs-lookup"><span data-stu-id="9e70e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9e70e-108">**名稱**</span><span class="sxs-lookup"><span data-stu-id="9e70e-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="9e70e-109">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9e70e-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="9e70e-110">這項技術的名稱 (Null （如果不是匿名) ）。</span><span class="sxs-lookup"><span data-stu-id="9e70e-110">Name of this technique (NULL if not anonymous).</span></span>

</dd> <dt>

<span data-ttu-id="9e70e-111">**通過**</span><span class="sxs-lookup"><span data-stu-id="9e70e-111">**Passes**</span></span>
</dt> <dd>

<span data-ttu-id="9e70e-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9e70e-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="9e70e-113">技術中包含的傳遞數目。</span><span class="sxs-lookup"><span data-stu-id="9e70e-113">Number of passes contained in the technique.</span></span>

</dd> <dt>

<span data-ttu-id="9e70e-114">**註解**</span><span class="sxs-lookup"><span data-stu-id="9e70e-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="9e70e-115">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9e70e-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="9e70e-116">這項技術的附注數目。</span><span class="sxs-lookup"><span data-stu-id="9e70e-116">Number of annotations on this technique.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e70e-117">備註</span><span class="sxs-lookup"><span data-stu-id="9e70e-117">Remarks</span></span>

<span data-ttu-id="9e70e-118">D3DX11 \_ 技術 \_ DESC 適用于 [**ID3DX11EffectTechnique：： GetDesc**](id3dx11effecttechnique-getdesc.md)。</span><span class="sxs-lookup"><span data-stu-id="9e70e-118">D3DX11\_TECHNIQUE\_DESC is used with [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e70e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e70e-119">Requirements</span></span>



| <span data-ttu-id="9e70e-120">需求</span><span class="sxs-lookup"><span data-stu-id="9e70e-120">Requirement</span></span> | <span data-ttu-id="9e70e-121">值</span><span class="sxs-lookup"><span data-stu-id="9e70e-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e70e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9e70e-122">Header</span></span><br/> | <dl> <span data-ttu-id="9e70e-123"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="9e70e-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e70e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e70e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e70e-125">效果11結構</span><span class="sxs-lookup"><span data-stu-id="9e70e-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 


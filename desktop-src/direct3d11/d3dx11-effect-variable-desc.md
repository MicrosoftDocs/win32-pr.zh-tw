---
title: 'D3DX11_EFFECT_VARIABLE_DESC 結構 (D3dx11effect .h) '
description: 描述效果變數。
ms.assetid: 9c975ad4-b90e-4e69-b78f-4f5cc61083ff
keywords:
- D3DX11_EFFECT_VARIABLE_DESC 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_VARIABLE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a83121c930c5a634434161c998c72215e227f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992366"
---
# <a name="d3dx11_effect_variable_desc-structure"></a><span data-ttu-id="70eef-104">D3DX11 \_ 效果 \_ 變數 \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="70eef-104">D3DX11\_EFFECT\_VARIABLE\_DESC structure</span></span>

<span data-ttu-id="70eef-105">描述效果變數。</span><span class="sxs-lookup"><span data-stu-id="70eef-105">Describes an effect variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="70eef-106">語法</span><span class="sxs-lookup"><span data-stu-id="70eef-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_VARIABLE_DESC {
  LPCSTR Name;
  LPCSTR Semantic;
  UINT   Flags;
  UINT   Annotations;
  UINT   BufferOffset;
  UINT   ExplicitBindPoint;
} D3DX11_EFFECT_VARIABLE_DESC;
```



## <a name="members"></a><span data-ttu-id="70eef-107">成員</span><span class="sxs-lookup"><span data-stu-id="70eef-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="70eef-108">**名稱**</span><span class="sxs-lookup"><span data-stu-id="70eef-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="70eef-109">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="70eef-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="70eef-110">此變數、注釋或結構成員的名稱。</span><span class="sxs-lookup"><span data-stu-id="70eef-110">Name of this variable, annotation, or structure member.</span></span>

</dd> <dt>

<span data-ttu-id="70eef-111">**語義**</span><span class="sxs-lookup"><span data-stu-id="70eef-111">**Semantic**</span></span>
</dt> <dd>

<span data-ttu-id="70eef-112">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="70eef-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="70eef-113">此變數或結構成員的語義字串 (注釋的 Null 或不存在) 。</span><span class="sxs-lookup"><span data-stu-id="70eef-113">Semantic string of this variable or structure member (NULL for annotations or if not present).</span></span>

</dd> <dt>

<span data-ttu-id="70eef-114">**旗標**</span><span class="sxs-lookup"><span data-stu-id="70eef-114">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="70eef-115">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="70eef-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="70eef-116">適用于效果變數的選擇性旗標。</span><span class="sxs-lookup"><span data-stu-id="70eef-116">Optional flags for effect variables.</span></span>

</dd> <dt>

<span data-ttu-id="70eef-117">**註解**</span><span class="sxs-lookup"><span data-stu-id="70eef-117">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="70eef-118">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="70eef-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="70eef-119">此變數的注釋數目 (永遠為0，表示注釋) 。</span><span class="sxs-lookup"><span data-stu-id="70eef-119">Number of annotations on this variable (always 0 for annotations).</span></span>

</dd> <dt>

<span data-ttu-id="70eef-120">**BufferOffset**</span><span class="sxs-lookup"><span data-stu-id="70eef-120">**BufferOffset**</span></span>
</dt> <dd>

<span data-ttu-id="70eef-121">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="70eef-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="70eef-122">包含 cbuffer 或 tbuffer 的位移 (永遠為0，適用于不在常數緩衝區) 的注釋或變數。</span><span class="sxs-lookup"><span data-stu-id="70eef-122">Offset into containing cbuffer or tbuffer (always 0 for annotations or variables not in constant buffers).</span></span>

</dd> <dt>

<span data-ttu-id="70eef-123">**ExplicitBindPoint**</span><span class="sxs-lookup"><span data-stu-id="70eef-123">**ExplicitBindPoint**</span></span>
</dt> <dd>

<span data-ttu-id="70eef-124">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="70eef-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="70eef-125">如果已使用 register 關鍵字明確系結變數，則使用。</span><span class="sxs-lookup"><span data-stu-id="70eef-125">Used if the variable has been explicitly bound using the register keyword.</span></span> <span data-ttu-id="70eef-126">檢查 D3DX11 \_ 效果 \_ 變數 \_ 明確 \_ 綁定 \_ 點的旗標。</span><span class="sxs-lookup"><span data-stu-id="70eef-126">Check Flags for D3DX11\_EFFECT\_VARIABLE\_EXPLICIT\_BIND\_POINT.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70eef-127">備註</span><span class="sxs-lookup"><span data-stu-id="70eef-127">Remarks</span></span>

<span data-ttu-id="70eef-128">D3DX11 \_ 效果 \_ 變數 \_ DESC 可與 [**ID3DX11EffectVariable：： GetDesc**](id3dx11effectvariable-getdesc.md)搭配使用。</span><span class="sxs-lookup"><span data-stu-id="70eef-128">D3DX11\_EFFECT\_VARIABLE\_DESC is used with [**ID3DX11EffectVariable::GetDesc**](id3dx11effectvariable-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70eef-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="70eef-129">Requirements</span></span>



| <span data-ttu-id="70eef-130">需求</span><span class="sxs-lookup"><span data-stu-id="70eef-130">Requirement</span></span> | <span data-ttu-id="70eef-131">值</span><span class="sxs-lookup"><span data-stu-id="70eef-131">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="70eef-132">標頭</span><span class="sxs-lookup"><span data-stu-id="70eef-132">Header</span></span><br/> | <dl> <span data-ttu-id="70eef-133"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="70eef-133"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70eef-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70eef-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70eef-135">效果11結構</span><span class="sxs-lookup"><span data-stu-id="70eef-135">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 


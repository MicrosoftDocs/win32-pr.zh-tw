---
title: 'D3DX11_EFFECT_DESC 結構 (D3dx11effect .h) '
description: 描述效果。
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- D3DX11_EFFECT_DESC 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d43b37d13a8b3f076cc3c5967dac9a95ed18a5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974717"
---
# <a name="d3dx11_effect_desc-structure"></a><span data-ttu-id="f1627-104">D3DX11 \_ 效果 \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="f1627-104">D3DX11\_EFFECT\_DESC structure</span></span>

<span data-ttu-id="f1627-105">描述效果。</span><span class="sxs-lookup"><span data-stu-id="f1627-105">Describes an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1627-106">語法</span><span class="sxs-lookup"><span data-stu-id="f1627-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_DESC {
  UINT ConstantBuffers;
  UINT GlobalVariables;
  UINT InterfaceVariables;
  UINT Techniques;
  UINT Groups;
} D3DX11_EFFECT_DESC;
```



## <a name="members"></a><span data-ttu-id="f1627-107">成員</span><span class="sxs-lookup"><span data-stu-id="f1627-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f1627-108">**ConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="f1627-108">**ConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="f1627-109">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f1627-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f1627-110">此效果中的常數緩衝區數目。</span><span class="sxs-lookup"><span data-stu-id="f1627-110">Number of constant buffers in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="f1627-111">**GlobalVariables**</span><span class="sxs-lookup"><span data-stu-id="f1627-111">**GlobalVariables**</span></span>
</dt> <dd>

<span data-ttu-id="f1627-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f1627-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f1627-113">此效果中的全域變數數目。</span><span class="sxs-lookup"><span data-stu-id="f1627-113">Number of global variables in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="f1627-114">**InterfaceVariables**</span><span class="sxs-lookup"><span data-stu-id="f1627-114">**InterfaceVariables**</span></span>
</dt> <dd>

<span data-ttu-id="f1627-115">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f1627-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f1627-116">此效果中的全域介面數目。</span><span class="sxs-lookup"><span data-stu-id="f1627-116">Number of global interfaces in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="f1627-117">**技術**</span><span class="sxs-lookup"><span data-stu-id="f1627-117">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="f1627-118">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f1627-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f1627-119">此效果中的技巧數目。</span><span class="sxs-lookup"><span data-stu-id="f1627-119">Number of techniques in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="f1627-120">**群組**</span><span class="sxs-lookup"><span data-stu-id="f1627-120">**Groups**</span></span>
</dt> <dd>

<span data-ttu-id="f1627-121">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f1627-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="f1627-122">此效果中的群組數目。</span><span class="sxs-lookup"><span data-stu-id="f1627-122">Number of groups in this effect.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1627-123">備註</span><span class="sxs-lookup"><span data-stu-id="f1627-123">Remarks</span></span>

<span data-ttu-id="f1627-124">D3DX11 \_ 效果 \_ DESC 適用于 [**ID3DX11Effect：： GetDesc**](id3dx11effect-getdesc.md)。</span><span class="sxs-lookup"><span data-stu-id="f1627-124">D3DX11\_EFFECT\_DESC is used with [**ID3DX11Effect::GetDesc**](id3dx11effect-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1627-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1627-125">Requirements</span></span>



| <span data-ttu-id="f1627-126">需求</span><span class="sxs-lookup"><span data-stu-id="f1627-126">Requirement</span></span> | <span data-ttu-id="f1627-127">值</span><span class="sxs-lookup"><span data-stu-id="f1627-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1627-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f1627-128">Header</span></span><br/> | <dl> <span data-ttu-id="f1627-129"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1627-129"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1627-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1627-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1627-131">效果11結構</span><span class="sxs-lookup"><span data-stu-id="f1627-131">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 


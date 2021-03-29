---
title: 'D3DX11_PASS_DESC 結構 (D3dx11effect .h) '
description: 描述包含管線狀態的效果階段。
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- D3DX11_PASS_DESC 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4d7f10268db0515b2f7e3772332b34427ba67a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974708"
---
# <a name="d3dx11_pass_desc-structure"></a><span data-ttu-id="150fe-104">D3DX11 \_ PASS \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="150fe-104">D3DX11\_PASS\_DESC structure</span></span>

<span data-ttu-id="150fe-105">描述包含管線狀態的效果階段。</span><span class="sxs-lookup"><span data-stu-id="150fe-105">Describes an effect pass, which contains pipeline state.</span></span>

## <a name="syntax"></a><span data-ttu-id="150fe-106">語法</span><span class="sxs-lookup"><span data-stu-id="150fe-106">Syntax</span></span>


```C++
typedef struct _D3DX11_PASS_DESC {
  LPCSTR Name;
  UINT   Annotations;
  BYTE   *pIAInputSignature;
  SIZE_T IAInputSignatureSize;
  UINT   StencilRef;
  UINT   SampleMask;
  FLOAT  BlendFactor[4];
} D3DX11_PASS_DESC;
```



## <a name="members"></a><span data-ttu-id="150fe-107">成員</span><span class="sxs-lookup"><span data-stu-id="150fe-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="150fe-108">**名稱**</span><span class="sxs-lookup"><span data-stu-id="150fe-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="150fe-109">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="150fe-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="150fe-110">如果不是匿名) ，此傳遞的名稱 (**為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="150fe-110">Name of this pass (**NULL** if not anonymous).</span></span>

</dd> <dt>

<span data-ttu-id="150fe-111">**註解**</span><span class="sxs-lookup"><span data-stu-id="150fe-111">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="150fe-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="150fe-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="150fe-113">此傳遞的注釋數目。</span><span class="sxs-lookup"><span data-stu-id="150fe-113">Number of annotations on this pass.</span></span>

</dd> <dt>

<span data-ttu-id="150fe-114">**pIAInputSignature**</span><span class="sxs-lookup"><span data-stu-id="150fe-114">**pIAInputSignature**</span></span>
</dt> <dd>

<span data-ttu-id="150fe-115">類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="150fe-115">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="150fe-116">從頂點著色器或幾何著色器 (的簽章（如果沒有頂點著色) 器，則為 Null），如果不存在則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="150fe-116">Signature from the vertex shader or geometry shader (if there is no vertex shader) or **NULL** if neither exists.</span></span>

</dd> <dt>

<span data-ttu-id="150fe-117">**IAInputSignatureSize**</span><span class="sxs-lookup"><span data-stu-id="150fe-117">**IAInputSignatureSize**</span></span>
</dt> <dd>

<span data-ttu-id="150fe-118">類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="150fe-118">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="150fe-119">Singature 大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="150fe-119">Singature size in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="150fe-120">**StencilRef**</span><span class="sxs-lookup"><span data-stu-id="150fe-120">**StencilRef**</span></span>
</dt> <dd>

<span data-ttu-id="150fe-121">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="150fe-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="150fe-122">深度樣板狀態中所使用的樣板參考值。</span><span class="sxs-lookup"><span data-stu-id="150fe-122">The stencil-reference value used in the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="150fe-123">**SampleMask**</span><span class="sxs-lookup"><span data-stu-id="150fe-123">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="150fe-124">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="150fe-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="150fe-125">Blend 狀態的範例遮罩。</span><span class="sxs-lookup"><span data-stu-id="150fe-125">The sample mask for the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="150fe-126">**BlendFactor**</span><span class="sxs-lookup"><span data-stu-id="150fe-126">**BlendFactor**</span></span>
</dt> <dd>

<span data-ttu-id="150fe-127">類型： **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="150fe-127">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="150fe-128">Blend 狀態 (RGBA) 的每個元件 blend 因數。</span><span class="sxs-lookup"><span data-stu-id="150fe-128">The per-component blend factors (RGBA) for the blend state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="150fe-129">備註</span><span class="sxs-lookup"><span data-stu-id="150fe-129">Remarks</span></span>

<span data-ttu-id="150fe-130">D3DX11 \_ PASS \_ DESC 適用于 [**ID3DX11EffectPass：： GetDesc**](id3dx11effectpass-getdesc.md)。</span><span class="sxs-lookup"><span data-stu-id="150fe-130">D3DX11\_PASS\_DESC is used with [**ID3DX11EffectPass::GetDesc**](id3dx11effectpass-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="150fe-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="150fe-131">Requirements</span></span>



| <span data-ttu-id="150fe-132">需求</span><span class="sxs-lookup"><span data-stu-id="150fe-132">Requirement</span></span> | <span data-ttu-id="150fe-133">值</span><span class="sxs-lookup"><span data-stu-id="150fe-133">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="150fe-134">標頭</span><span class="sxs-lookup"><span data-stu-id="150fe-134">Header</span></span><br/> | <dl> <span data-ttu-id="150fe-135"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="150fe-135"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="150fe-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="150fe-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="150fe-137">效果11結構</span><span class="sxs-lookup"><span data-stu-id="150fe-137">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 


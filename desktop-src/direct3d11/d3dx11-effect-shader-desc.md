---
title: 'D3DX11_EFFECT_SHADER_DESC 結構 (D3dx11effect .h) '
description: 描述效果著色器。
ms.assetid: 4377eec6-f331-4cad-bf16-189d6296f886
keywords:
- D3DX11_EFFECT_SHADER_DESC 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c518d4f7930d0651e519d23218121b8ed4bed288
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854067"
---
# <a name="d3dx11_effect_shader_desc-structure"></a><span data-ttu-id="b106c-104">D3DX11 \_ 效果 \_ 著色器 \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="b106c-104">D3DX11\_EFFECT\_SHADER\_DESC structure</span></span>

<span data-ttu-id="b106c-105">描述效果著色器。</span><span class="sxs-lookup"><span data-stu-id="b106c-105">Describes an effect shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="b106c-106">語法</span><span class="sxs-lookup"><span data-stu-id="b106c-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_SHADER_DESC {
  const BYTE *pInputSignature;
  BOOL       IsInline;
  const BYTE *pBytecode;
  UINT       BytecodeLength;
  LPCSTR     SODecls[D3D11_SO_STREAM_COUNT];
  UINT       RasterizedStream;
  UINT       NumInputSignatureEntries;
  UINT       NumOutputSignatureEntries;
  UINT       NumPatchConstantSignatureEntries;
} D3DX11_EFFECT_SHADER_DESC;
```



## <a name="members"></a><span data-ttu-id="b106c-107">成員</span><span class="sxs-lookup"><span data-stu-id="b106c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b106c-108">**pInputSignature**</span><span class="sxs-lookup"><span data-stu-id="b106c-108">**pInputSignature**</span></span>
</dt> <dd>

<span data-ttu-id="b106c-109">類型： **Const [**BYTE**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="b106c-109">Type: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="b106c-110">傳遞至 CreateInputLayout。</span><span class="sxs-lookup"><span data-stu-id="b106c-110">Passed into CreateInputLayout.</span></span> <span data-ttu-id="b106c-111">只適用于頂點著色器或幾何著色器。</span><span class="sxs-lookup"><span data-stu-id="b106c-111">Only valid on a vertex shader or geometry shader.</span></span> <span data-ttu-id="b106c-112">請參閱 [**ID3D11Device：： CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)。</span><span class="sxs-lookup"><span data-stu-id="b106c-112">See [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).</span></span>

</dd> <dt>

<span data-ttu-id="b106c-113">**IsInline**</span><span class="sxs-lookup"><span data-stu-id="b106c-113">**IsInline**</span></span>
</dt> <dd>

<span data-ttu-id="b106c-114">類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b106c-114">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b106c-115">**TRUE** 表示著色器是以內嵌方式定義的。否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="b106c-115">**TRUE** is the shader is defined inline; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b106c-116">**pBytecode**</span><span class="sxs-lookup"><span data-stu-id="b106c-116">**pBytecode**</span></span>
</dt> <dd>

<span data-ttu-id="b106c-117">類型： **Const [**BYTE**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="b106c-117">Type: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="b106c-118">著色器位元組的位元組。</span><span class="sxs-lookup"><span data-stu-id="b106c-118">Shader bytecode.</span></span>

</dd> <dt>

<span data-ttu-id="b106c-119">**BytecodeLength**</span><span class="sxs-lookup"><span data-stu-id="b106c-119">**BytecodeLength**</span></span>
</dt> <dd>

<span data-ttu-id="b106c-120">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b106c-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b106c-121">PBytecode 的長度。</span><span class="sxs-lookup"><span data-stu-id="b106c-121">The length of pBytecode.</span></span>

</dd> <dt>

<span data-ttu-id="b106c-122">**SODecls**</span><span class="sxs-lookup"><span data-stu-id="b106c-122">**SODecls**</span></span>
</dt> <dd>

<span data-ttu-id="b106c-123">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b106c-123">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b106c-124">使用) 將幾何著色器的宣告字串 (資料流程。</span><span class="sxs-lookup"><span data-stu-id="b106c-124">Stream out declaration string (for geometry shader with SO).</span></span>

</dd> <dt>

<span data-ttu-id="b106c-125">**RasterizedStream**</span><span class="sxs-lookup"><span data-stu-id="b106c-125">**RasterizedStream**</span></span>
</dt> <dd>

<span data-ttu-id="b106c-126">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b106c-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b106c-127">指出哪些資料流程是柵格化的。</span><span class="sxs-lookup"><span data-stu-id="b106c-127">Indicates which stream is rasterized.</span></span> <span data-ttu-id="b106c-128">D3D11 幾何著色器最多可以輸出四個數據流，其中一個可以進行柵格化。</span><span class="sxs-lookup"><span data-stu-id="b106c-128">D3D11 geometry shaders can output up to four streams of data, one of which can be rasterized.</span></span>

</dd> <dt>

<span data-ttu-id="b106c-129">**NumInputSignatureEntries**</span><span class="sxs-lookup"><span data-stu-id="b106c-129">**NumInputSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="b106c-130">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b106c-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b106c-131">輸入簽章中的專案數。</span><span class="sxs-lookup"><span data-stu-id="b106c-131">Number of entries in the input signature.</span></span>

</dd> <dt>

<span data-ttu-id="b106c-132">**NumOutputSignatureEntries**</span><span class="sxs-lookup"><span data-stu-id="b106c-132">**NumOutputSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="b106c-133">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b106c-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b106c-134">輸出特徵標記中的專案數。</span><span class="sxs-lookup"><span data-stu-id="b106c-134">Number of entries in the output signature.</span></span>

</dd> <dt>

<span data-ttu-id="b106c-135">**NumPatchConstantSignatureEntries**</span><span class="sxs-lookup"><span data-stu-id="b106c-135">**NumPatchConstantSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="b106c-136">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b106c-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b106c-137">Patch 常數簽章中的專案數。</span><span class="sxs-lookup"><span data-stu-id="b106c-137">Number of entries in the patch constant signature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b106c-138">備註</span><span class="sxs-lookup"><span data-stu-id="b106c-138">Remarks</span></span>

<span data-ttu-id="b106c-139">D3DX11 \_ 效果 \_ 著色器 \_ DESC 適用于 [**ID3DX11EffectShaderVariable：： GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md)。</span><span class="sxs-lookup"><span data-stu-id="b106c-139">D3DX11\_EFFECT\_SHADER\_DESC is used with [**ID3DX11EffectShaderVariable::GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b106c-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="b106c-140">Requirements</span></span>



| <span data-ttu-id="b106c-141">需求</span><span class="sxs-lookup"><span data-stu-id="b106c-141">Requirement</span></span> | <span data-ttu-id="b106c-142">值</span><span class="sxs-lookup"><span data-stu-id="b106c-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b106c-143">標頭</span><span class="sxs-lookup"><span data-stu-id="b106c-143">Header</span></span><br/> | <dl> <span data-ttu-id="b106c-144"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="b106c-144"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b106c-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b106c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b106c-146">效果11結構</span><span class="sxs-lookup"><span data-stu-id="b106c-146">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 


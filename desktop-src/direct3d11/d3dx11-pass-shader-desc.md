---
title: 'D3DX11_PASS_SHADER_DESC 結構 (D3dx11effect .h) '
description: 描述效果傳遞。
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- D3DX11_PASS_SHADER_DESC 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cac6e842dabeaabc60451737fae56eb2cb61915
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974707"
---
# <a name="d3dx11_pass_shader_desc-structure"></a><span data-ttu-id="aea47-104">D3DX11 \_ PASS \_ 著色器 \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="aea47-104">D3DX11\_PASS\_SHADER\_DESC structure</span></span>

<span data-ttu-id="aea47-105">描述效果傳遞。</span><span class="sxs-lookup"><span data-stu-id="aea47-105">Describes an effect pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="aea47-106">語法</span><span class="sxs-lookup"><span data-stu-id="aea47-106">Syntax</span></span>


```C++
typedef struct _D3DX11_PASS_SHADER_DESC {
  ID3DX11EffectShaderVariable *pShaderVariable;
  UINT                        ShaderIndex;
} D3DX11_PASS_SHADER_DESC;
```



## <a name="members"></a><span data-ttu-id="aea47-107">成員</span><span class="sxs-lookup"><span data-stu-id="aea47-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="aea47-108">**pShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="aea47-108">**pShaderVariable**</span></span>
</dt> <dd>

<span data-ttu-id="aea47-109">類型： **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="aea47-109">Type: **[**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="aea47-110">此著色器來源的變數。</span><span class="sxs-lookup"><span data-stu-id="aea47-110">The variable that this shader came from.</span></span>

</dd> <dt>

<span data-ttu-id="aea47-111">**ShaderIndex**</span><span class="sxs-lookup"><span data-stu-id="aea47-111">**ShaderIndex**</span></span>
</dt> <dd>

<span data-ttu-id="aea47-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="aea47-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="aea47-113">如果陣列) ，則為 pShaderVariable 的元素 (如果不適用則為0。</span><span class="sxs-lookup"><span data-stu-id="aea47-113">The element of pShaderVariable (if an array) or 0 if not applicable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aea47-114">備註</span><span class="sxs-lookup"><span data-stu-id="aea47-114">Remarks</span></span>

<span data-ttu-id="aea47-115">D3DX11 \_ PASS \_ 著色器 \_ DESC 適用于 [**ID3DX11EffectPass**](id3dx11effectpass.md) Get \* ShaderDesc 方法。</span><span class="sxs-lookup"><span data-stu-id="aea47-115">D3DX11\_PASS\_SHADER\_DESC is used with [**ID3DX11EffectPass**](id3dx11effectpass.md) Get\*ShaderDesc methods.</span></span>

<span data-ttu-id="aea47-116">如果這是內嵌著色器指派，則傳回的介面將會是匿名著色器變數，但無法以任何其他方式抓取。</span><span class="sxs-lookup"><span data-stu-id="aea47-116">If this is an inline shader assignment, the returned interface will be an anonymous shader variable, which is not retrievable any other way.</span></span> <span data-ttu-id="aea47-117">變數描述中的名稱將會是 "$Anonymous"。</span><span class="sxs-lookup"><span data-stu-id="aea47-117">It's name in the variable description will be "$Anonymous".</span></span> <span data-ttu-id="aea47-118">如果在 pass 區塊中沒有這個型別的指派，pShaderVariable！ = **Null**，但是 pShaderVariable->IsValid () = = **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="aea47-118">If there is no assignment of this type in the pass block, pShaderVariable != **NULL**, but pShaderVariable->IsValid() == **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="aea47-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="aea47-119">Requirements</span></span>



| <span data-ttu-id="aea47-120">需求</span><span class="sxs-lookup"><span data-stu-id="aea47-120">Requirement</span></span> | <span data-ttu-id="aea47-121">值</span><span class="sxs-lookup"><span data-stu-id="aea47-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="aea47-122">標頭</span><span class="sxs-lookup"><span data-stu-id="aea47-122">Header</span></span><br/> | <dl> <span data-ttu-id="aea47-123"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="aea47-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aea47-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aea47-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aea47-125">效果11結構</span><span class="sxs-lookup"><span data-stu-id="aea47-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 


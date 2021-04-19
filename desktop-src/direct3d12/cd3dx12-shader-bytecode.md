---
title: 'CD3DX12_SHADER_BYTECODE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 著色器位元組程式碼 \_ 結構。
ms.assetid: 09CEFCCE-C499-493D-ACDE-806E09995315
keywords:
- CD3DX12_SHADER_BYTECODE 結構
topic_type:
- apiref
api_name:
- CD3DX12_SHADER_BYTECODE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227c18913492d6533b08f49f5761fab1b93e97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106979870"
---
# <a name="cd3dx12_shader_bytecode-structure"></a><span data-ttu-id="4978f-104">CD3DX12 \_ 著色器 \_ 位元組位元組結構</span><span class="sxs-lookup"><span data-stu-id="4978f-104">CD3DX12\_SHADER\_BYTECODE structure</span></span>

<span data-ttu-id="4978f-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 著色器 \_ 位元組**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) 程式碼結構。</span><span class="sxs-lookup"><span data-stu-id="4978f-105">A helper structure to enable easy initialization of a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4978f-106">語法</span><span class="sxs-lookup"><span data-stu-id="4978f-106">Syntax</span></span>


```C++
struct CD3DX12_SHADER_BYTECODE  : public D3D12_SHADER_BYTECODE{
   CD3DX12_SHADER_BYTECODE();
   explicit CD3DX12_SHADER_BYTECODE(const D3D12_SHADER_BYTECODE &o);
   CD3DX12_SHADER_BYTECODE(ID3DBlob* pShaderBlob);
   CD3DX12_SHADER_BYTECODE(const void* _pShaderBytecode, SIZE_T bytecodeLength);
   operator const D3D12_SHADER_BYTECODE&() const;
};
```



## <a name="members"></a><span data-ttu-id="4978f-107">成員</span><span class="sxs-lookup"><span data-stu-id="4978f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4978f-108">**CD3DX12 \_ 著色器 \_ 位元組 ()**</span><span class="sxs-lookup"><span data-stu-id="4978f-108">**CD3DX12\_SHADER\_BYTECODE()**</span></span>
</dt> <dd>

<span data-ttu-id="4978f-109">建立 CD3DX12 著色器位元組程式碼的新、未初始化的實例 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="4978f-109">Creates a new, uninitialized, instance of a CD3DX12\_SHADER\_BYTECODE.</span></span>

</dd> <dt>

<span data-ttu-id="4978f-110">**明確的 CD3DX12 \_ 著色器 \_ 位元組 (const D3D12 \_ 著色器 \_ 位元組 &o)**</span><span class="sxs-lookup"><span data-stu-id="4978f-110">**explicit CD3DX12\_SHADER\_BYTECODE(const D3D12\_SHADER\_BYTECODE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="4978f-111">建立 CD3DX12 著色器位元組程式碼的新實例 \_ \_ ，並以另一個 [**D3D12 \_ 著色器 \_ 位元組**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) 程式碼結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="4978f-111">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initialized with the contents of another [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4978f-112">**CD3DX12 \_ 著色器 \_ 位元組 (ID3DBlob \* pShaderBlob)**</span><span class="sxs-lookup"><span data-stu-id="4978f-112">**CD3DX12\_SHADER\_BYTECODE(ID3DBlob\* pShaderBlob)**</span></span>
</dt> <dd>

<span data-ttu-id="4978f-113">建立 CD3DX12 \_ 著色器位元組程式碼的新實例 \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="4978f-113">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initializing the following parameters:</span></span>

<span data-ttu-id="4978f-114">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \*pShaderBlob</span><span class="sxs-lookup"><span data-stu-id="4978f-114">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))\* pShaderBlob</span></span>

</dd> <dt>

<span data-ttu-id="4978f-115">**CD3DX12 \_ 著色器 \_ 位元組空間 (const void \* \_ PShaderBytecode，SIZE \_ T bytecodeLength)**</span><span class="sxs-lookup"><span data-stu-id="4978f-115">**CD3DX12\_SHADER\_BYTECODE(const void\* \_pShaderBytecode, SIZE\_T bytecodeLength)**</span></span>
</dt> <dd>

<span data-ttu-id="4978f-116">建立 CD3DX12 \_ 著色器位元組程式碼的新實例 \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="4978f-116">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initializing the following parameters:</span></span>

<span data-ttu-id="4978f-117">void \* \_ pShaderBytecode</span><span class="sxs-lookup"><span data-stu-id="4978f-117">void\* \_pShaderBytecode</span></span>

<span data-ttu-id="4978f-118">大小 \_ T bytecodeLength</span><span class="sxs-lookup"><span data-stu-id="4978f-118">SIZE\_T bytecodeLength</span></span>

</dd> <dt>

<span data-ttu-id="4978f-119">**運算子 const D3D12 \_ 著色器 \_ 位元組& () const**</span><span class="sxs-lookup"><span data-stu-id="4978f-119">**operator const D3D12\_SHADER\_BYTECODE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="4978f-120">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="4978f-120">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4978f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="4978f-121">Requirements</span></span>



| <span data-ttu-id="4978f-122">需求</span><span class="sxs-lookup"><span data-stu-id="4978f-122">Requirement</span></span> | <span data-ttu-id="4978f-123">值</span><span class="sxs-lookup"><span data-stu-id="4978f-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4978f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="4978f-124">Header</span></span><br/> | <dl> <span data-ttu-id="4978f-125"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="4978f-125"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4978f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4978f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4978f-127">**D3D12 \_ 著色器 \_ 位元組碼**</span><span class="sxs-lookup"><span data-stu-id="4978f-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[<span data-ttu-id="4978f-128">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="4978f-128">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 


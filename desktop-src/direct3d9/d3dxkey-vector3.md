---
description: 描述在主要畫面格動畫中使用的向量索引鍵。 它會在指定的時間指定一個向量。 這可用於調整和轉譯金鑰。
ms.assetid: 7a7ba2ce-c9f3-4a04-b865-39de9070868b
title: 'D3DXKEY_VECTOR3 結構 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_VECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 41aec16da30a6e8742290b747b844b7fb22f6650
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000589"
---
# <a name="d3dxkey_vector3-structure"></a><span data-ttu-id="d2035-105">D3DXKEY \_ VECTOR3 結構</span><span class="sxs-lookup"><span data-stu-id="d2035-105">D3DXKEY\_VECTOR3 structure</span></span>

<span data-ttu-id="d2035-106">描述在主要畫面格動畫中使用的向量索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d2035-106">Describes a vector key for use in key frame animation.</span></span> <span data-ttu-id="d2035-107">它會在指定的時間指定一個向量。</span><span class="sxs-lookup"><span data-stu-id="d2035-107">It specifies a vector at a given time.</span></span> <span data-ttu-id="d2035-108">這可用於調整和轉譯金鑰。</span><span class="sxs-lookup"><span data-stu-id="d2035-108">This is used for scale and translation keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2035-109">語法</span><span class="sxs-lookup"><span data-stu-id="d2035-109">Syntax</span></span>


```C++
typedef struct D3DXKEY_VECTOR3 {
  FLOAT       Time;
  D3DXVECTOR3 Value;
} D3DXKEY_VECTOR3, *LPD3DXKEY_VECTOR3;
```



## <a name="members"></a><span data-ttu-id="d2035-110">成員</span><span class="sxs-lookup"><span data-stu-id="d2035-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="d2035-111">**Time**</span><span class="sxs-lookup"><span data-stu-id="d2035-111">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="d2035-112">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2035-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d2035-113">主要畫面格時間戳記。</span><span class="sxs-lookup"><span data-stu-id="d2035-113">Key frame time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="d2035-114">**值**</span><span class="sxs-lookup"><span data-stu-id="d2035-114">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="d2035-115">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)**</span><span class="sxs-lookup"><span data-stu-id="d2035-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d2035-116">提供尺規和/或轉譯值的 [**D3DXVECTOR3**](d3dxvector3.md) 3d 向量。</span><span class="sxs-lookup"><span data-stu-id="d2035-116">[**D3DXVECTOR3**](d3dxvector3.md) 3D vector that supplies scale and/or translation values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2035-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2035-117">Requirements</span></span>



| <span data-ttu-id="d2035-118">需求</span><span class="sxs-lookup"><span data-stu-id="d2035-118">Requirement</span></span> | <span data-ttu-id="d2035-119">值</span><span class="sxs-lookup"><span data-stu-id="d2035-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2035-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d2035-120">Header</span></span><br/> | <dl> <span data-ttu-id="d2035-121"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2035-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2035-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2035-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2035-123">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="d2035-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

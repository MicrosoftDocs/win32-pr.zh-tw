---
description: 描述在主要畫面格動畫中使用的四元數索引鍵。 四元數索引鍵是指定時間的四元值。
ms.assetid: 8f5b74a3-f712-40ac-942c-a2189c2327c8
title: 'D3DXKEY_QUATERNION 結構 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_QUATERNION
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12e4deead606c1a2c5b103ed9fd0e31e23515982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322900"
---
# <a name="d3dxkey_quaternion-structure"></a><span data-ttu-id="d92de-104">D3DXKEY \_ 四元數結構</span><span class="sxs-lookup"><span data-stu-id="d92de-104">D3DXKEY\_QUATERNION structure</span></span>

<span data-ttu-id="d92de-105">描述在主要畫面格動畫中使用的四元數索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d92de-105">Describes a quaternion key for use in key frame animation.</span></span> <span data-ttu-id="d92de-106">四元數索引鍵是指定時間的四元值。</span><span class="sxs-lookup"><span data-stu-id="d92de-106">A quaternion key is a quaternion value at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="d92de-107">語法</span><span class="sxs-lookup"><span data-stu-id="d92de-107">Syntax</span></span>


```C++
typedef struct D3DXKEY_QUATERNION {
  FLOAT          Time;
  D3DXQUATERNION Value;
} D3DXKEY_QUATERNION, *LPD3DXKEY_QUATERNION;
```



## <a name="members"></a><span data-ttu-id="d92de-108">成員</span><span class="sxs-lookup"><span data-stu-id="d92de-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d92de-109">**Time**</span><span class="sxs-lookup"><span data-stu-id="d92de-109">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="d92de-110">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d92de-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d92de-111">時間值。</span><span class="sxs-lookup"><span data-stu-id="d92de-111">Time value.</span></span>

</dd> <dt>

<span data-ttu-id="d92de-112">**值**</span><span class="sxs-lookup"><span data-stu-id="d92de-112">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="d92de-113">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="d92de-113">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d92de-114">提供旋轉值的 [**D3DXQUATERNION**](d3dxquaternion.md)四元數。</span><span class="sxs-lookup"><span data-stu-id="d92de-114">[**D3DXQUATERNION**](d3dxquaternion.md) quaternion that supplies rotation values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d92de-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d92de-115">Requirements</span></span>



| <span data-ttu-id="d92de-116">需求</span><span class="sxs-lookup"><span data-stu-id="d92de-116">Requirement</span></span> | <span data-ttu-id="d92de-117">值</span><span class="sxs-lookup"><span data-stu-id="d92de-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d92de-118">標頭</span><span class="sxs-lookup"><span data-stu-id="d92de-118">Header</span></span><br/> | <dl> <span data-ttu-id="d92de-119"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="d92de-119"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d92de-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d92de-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d92de-121">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="d92de-121">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

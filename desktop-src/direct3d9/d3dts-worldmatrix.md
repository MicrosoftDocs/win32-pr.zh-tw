---
description: 將範圍0到255之間的索引對應到相對應的轉換狀態。
ms.assetid: b0a1548c-de5d-4eff-baf9-4aecb5e13443
title: 'D3DTS_WORLDMATRIX 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDMATRIX
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f80996a37e2fb48bf8ca7ea73f714b04e711b263
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514576"
---
# <a name="d3dts_worldmatrix-macro"></a><span data-ttu-id="0d8ce-103">D3DTS \_ WORLDMATRIX 宏</span><span class="sxs-lookup"><span data-stu-id="0d8ce-103">D3DTS\_WORLDMATRIX macro</span></span>

<span data-ttu-id="0d8ce-104">將範圍0到255之間的索引對應到相對應的轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="0d8ce-104">Maps indices in the range 0 through 255 to the corresponding transform states.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d8ce-105">語法</span><span class="sxs-lookup"><span data-stu-id="0d8ce-105">Syntax</span></span>


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLDMATRIX(
   int index
);
```



## <a name="parameters"></a><span data-ttu-id="0d8ce-106">參數</span><span class="sxs-lookup"><span data-stu-id="0d8ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d8ce-107">*index*</span><span class="sxs-lookup"><span data-stu-id="0d8ce-107">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="0d8ce-108">範圍0到255的索引值。</span><span class="sxs-lookup"><span data-stu-id="0d8ce-108">An index value in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d8ce-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d8ce-109">Return value</span></span>

<span data-ttu-id="0d8ce-110">對應至指定 *索引* 的 [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) 。</span><span class="sxs-lookup"><span data-stu-id="0d8ce-110">The [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) that maps to the given *index*.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d8ce-111">備註</span><span class="sxs-lookup"><span data-stu-id="0d8ce-111">Remarks</span></span>

<span data-ttu-id="0d8ce-112">系統會保留範圍256到511的轉換狀態，以儲存最多可使用8位索引編制索引的256矩陣。</span><span class="sxs-lookup"><span data-stu-id="0d8ce-112">Transform states in the range 256 through 511 are reserved to store up to 256 matrices that can be indexed using 8-bit indices.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d8ce-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d8ce-113">Requirements</span></span>



| <span data-ttu-id="0d8ce-114">需求</span><span class="sxs-lookup"><span data-stu-id="0d8ce-114">Requirement</span></span> | <span data-ttu-id="0d8ce-115">值</span><span class="sxs-lookup"><span data-stu-id="0d8ce-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d8ce-116">標頭</span><span class="sxs-lookup"><span data-stu-id="0d8ce-116">Header</span></span><br/> | <dl> <span data-ttu-id="0d8ce-117"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d8ce-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d8ce-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d8ce-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d8ce-119">巨集</span><span class="sxs-lookup"><span data-stu-id="0d8ce-119">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="0d8ce-120">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="0d8ce-120">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 

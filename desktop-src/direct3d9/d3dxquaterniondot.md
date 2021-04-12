---
description: 傳回兩個四元數的點乘積。
ms.assetid: 2ed9aca9-0526-4b92-bd66-b09dcf4f474a
title: 'D3DXQuaternionDot 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e893ed9260c0d843e8454d96ab5b634741ee60d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323184"
---
# <a name="d3dxquaterniondot-function"></a><span data-ttu-id="42057-103">D3DXQuaternionDot 函式</span><span class="sxs-lookup"><span data-stu-id="42057-103">D3DXQuaternionDot function</span></span>

<span data-ttu-id="42057-104">傳回兩個四元數的點乘積。</span><span class="sxs-lookup"><span data-stu-id="42057-104">Returns the dot product of two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="42057-105">語法</span><span class="sxs-lookup"><span data-stu-id="42057-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionDot(
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="42057-106">參數</span><span class="sxs-lookup"><span data-stu-id="42057-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42057-107">*pQ1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42057-107">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42057-108">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="42057-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="42057-109">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="42057-109">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="42057-110">*pQ2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42057-110">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42057-111">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="42057-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="42057-112">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="42057-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42057-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="42057-113">Return value</span></span>

<span data-ttu-id="42057-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42057-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42057-115">兩個四元數的點乘積。</span><span class="sxs-lookup"><span data-stu-id="42057-115">The dot product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="42057-116">備註</span><span class="sxs-lookup"><span data-stu-id="42057-116">Remarks</span></span>

<span data-ttu-id="42057-117">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="42057-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="42057-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="42057-118">Requirements</span></span>



| <span data-ttu-id="42057-119">需求</span><span class="sxs-lookup"><span data-stu-id="42057-119">Requirement</span></span> | <span data-ttu-id="42057-120">值</span><span class="sxs-lookup"><span data-stu-id="42057-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42057-121">標頭</span><span class="sxs-lookup"><span data-stu-id="42057-121">Header</span></span><br/>  | <dl> <span data-ttu-id="42057-122"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="42057-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="42057-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="42057-123">Library</span></span><br/> | <dl> <span data-ttu-id="42057-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="42057-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="42057-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42057-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42057-126">數學函數</span><span class="sxs-lookup"><span data-stu-id="42057-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 

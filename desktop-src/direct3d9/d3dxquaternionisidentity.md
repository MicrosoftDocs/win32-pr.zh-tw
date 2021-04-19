---
description: 判斷四元數是否為識別四元數。
ms.assetid: 1cd39e1b-9b68-434d-b7b0-3ec6cddb8757
title: 'D3DXQuaternionIsIdentity 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b2b02bdddb4b7a2d31a685f576434e34952c0a22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982223"
---
# <a name="d3dxquaternionisidentity-function"></a><span data-ttu-id="6c6f5-103">D3DXQuaternionIsIdentity 函式</span><span class="sxs-lookup"><span data-stu-id="6c6f5-103">D3DXQuaternionIsIdentity function</span></span>

<span data-ttu-id="6c6f5-104">判斷四元數是否為識別四元數。</span><span class="sxs-lookup"><span data-stu-id="6c6f5-104">Determines if a quaternion is an identity quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c6f5-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c6f5-105">Syntax</span></span>


```C++
BOOL D3DXQuaternionIsIdentity(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="6c6f5-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c6f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c6f5-107">*pQ* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c6f5-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6f5-108">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="6c6f5-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6c6f5-109">將針對身分識別進行測試的 [**D3DXQUATERNION**](d3dxquaternion.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="6c6f5-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that will be tested for identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c6f5-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c6f5-110">Return value</span></span>

<span data-ttu-id="6c6f5-111">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c6f5-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c6f5-112">如果四元數是識別四元數，此函數會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6c6f5-112">If the quaternion is an identity quaternion, this function returns **TRUE**.</span></span> <span data-ttu-id="6c6f5-113">否則，此函式會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6c6f5-113">Otherwise, this function returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c6f5-114">備註</span><span class="sxs-lookup"><span data-stu-id="6c6f5-114">Remarks</span></span>

<span data-ttu-id="6c6f5-115">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="6c6f5-115">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c6f5-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c6f5-116">Requirements</span></span>



| <span data-ttu-id="6c6f5-117">需求</span><span class="sxs-lookup"><span data-stu-id="6c6f5-117">Requirement</span></span> | <span data-ttu-id="6c6f5-118">值</span><span class="sxs-lookup"><span data-stu-id="6c6f5-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c6f5-119">標頭</span><span class="sxs-lookup"><span data-stu-id="6c6f5-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6c6f5-120"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c6f5-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6c6f5-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="6c6f5-121">Library</span></span><br/> | <dl> <span data-ttu-id="6c6f5-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c6f5-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6c6f5-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c6f5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c6f5-124">數學函數</span><span class="sxs-lookup"><span data-stu-id="6c6f5-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6c6f5-125">**D3DXQuaternionIdentity**</span><span class="sxs-lookup"><span data-stu-id="6c6f5-125">**D3DXQuaternionIdentity**</span></span>](d3dxquaternionidentity.md)
</dt> </dl>

 

 

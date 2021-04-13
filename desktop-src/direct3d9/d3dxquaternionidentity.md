---
description: 傳回識別四元數。
ms.assetid: 8088897b-5755-4ea0-afef-bd49d1921f5c
title: 'D3DXQuaternionIdentity 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2db9dd0638f5ba67b2dc2e8b8c248889225aaca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322835"
---
# <a name="d3dxquaternionidentity-function"></a><span data-ttu-id="90479-103">D3DXQuaternionIdentity 函式</span><span class="sxs-lookup"><span data-stu-id="90479-103">D3DXQuaternionIdentity function</span></span>

<span data-ttu-id="90479-104">傳回識別四元數。</span><span class="sxs-lookup"><span data-stu-id="90479-104">Returns the identity quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="90479-105">語法</span><span class="sxs-lookup"><span data-stu-id="90479-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionIdentity(
  _Inout_ D3DXQUATERNION *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="90479-106">參數</span><span class="sxs-lookup"><span data-stu-id="90479-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90479-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="90479-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="90479-108">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="90479-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="90479-109">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="90479-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90479-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="90479-110">Return value</span></span>

<span data-ttu-id="90479-111">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="90479-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="90479-112">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是身分識別四元數。</span><span class="sxs-lookup"><span data-stu-id="90479-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the identity quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="90479-113">備註</span><span class="sxs-lookup"><span data-stu-id="90479-113">Remarks</span></span>

<span data-ttu-id="90479-114">假設有一個四元數 (x、y、z、w) ， **D3DXQuaternionIdentity** 函數會傳回四元數 (0、0、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="90479-114">Given a quaternion (x, y, z, w), the **D3DXQuaternionIdentity** function will return the quaternion (0, 0, 0, 1).</span></span>

<span data-ttu-id="90479-115">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="90479-115">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="90479-116">如此一來， **D3DXQuaternionIdentity** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="90479-116">In this way, the **D3DXQuaternionIdentity** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="90479-117">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="90479-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="90479-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="90479-118">Requirements</span></span>



| <span data-ttu-id="90479-119">需求</span><span class="sxs-lookup"><span data-stu-id="90479-119">Requirement</span></span> | <span data-ttu-id="90479-120">值</span><span class="sxs-lookup"><span data-stu-id="90479-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90479-121">標頭</span><span class="sxs-lookup"><span data-stu-id="90479-121">Header</span></span><br/>  | <dl> <span data-ttu-id="90479-122"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="90479-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="90479-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="90479-123">Library</span></span><br/> | <dl> <span data-ttu-id="90479-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="90479-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="90479-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90479-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90479-126">數學函數</span><span class="sxs-lookup"><span data-stu-id="90479-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="90479-127">**D3DXQuaternionIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="90479-127">**D3DXQuaternionIsIdentity**</span></span>](d3dxquaternionisidentity.md)
</dt> </dl>

 

 





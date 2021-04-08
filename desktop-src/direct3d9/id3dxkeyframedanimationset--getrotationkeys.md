---
description: 使用主要畫面格動畫所用的旋轉金鑰資料來填滿陣列。
ms.assetid: 9ae8bc28-d231-4d50-98f0-762b2d2c04e8
title: 'ID3DXKeyframedAnimationSet：： GetRotationKeys 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af9242ccf75bc1e5443f040399ffbd8a939ed92e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696816"
---
# <a name="id3dxkeyframedanimationsetgetrotationkeys-method"></a><span data-ttu-id="7f93d-103">ID3DXKeyframedAnimationSet：： GetRotationKeys 方法</span><span class="sxs-lookup"><span data-stu-id="7f93d-103">ID3DXKeyframedAnimationSet::GetRotationKeys method</span></span>

<span data-ttu-id="7f93d-104">使用主要畫面格動畫所用的旋轉金鑰資料來填滿陣列。</span><span class="sxs-lookup"><span data-stu-id="7f93d-104">Fills an array with rotational key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f93d-105">語法</span><span class="sxs-lookup"><span data-stu-id="7f93d-105">Syntax</span></span>


```C++
HRESULT GetRotationKeys(
  [in] UINT                 Animation,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="7f93d-106">參數</span><span class="sxs-lookup"><span data-stu-id="7f93d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f93d-107">*動畫* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7f93d-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f93d-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f93d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f93d-109">動畫索引。</span><span class="sxs-lookup"><span data-stu-id="7f93d-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="7f93d-110">*pRotationKeys* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7f93d-110">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f93d-111">類型： **[ **LPD3DXKEY \_ 四元數**](d3dxkey-quaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="7f93d-111">Type: **[**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)**</span></span>

<span data-ttu-id="7f93d-112">[**D3DXKEY \_ 四元**](d3dxkey-quaternion.md)數四元數之使用者配置陣列的指標，此方法是用來填滿動畫旋轉資料。</span><span class="sxs-lookup"><span data-stu-id="7f93d-112">Pointer to a user-allocated array of [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md) quaternions that the method is to fill with animation rotation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f93d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f93d-113">Return value</span></span>

<span data-ttu-id="7f93d-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7f93d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7f93d-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="7f93d-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7f93d-116">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="7f93d-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f93d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f93d-117">Requirements</span></span>



| <span data-ttu-id="7f93d-118">需求</span><span class="sxs-lookup"><span data-stu-id="7f93d-118">Requirement</span></span> | <span data-ttu-id="7f93d-119">值</span><span class="sxs-lookup"><span data-stu-id="7f93d-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f93d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="7f93d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7f93d-121"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f93d-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7f93d-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f93d-122">Library</span></span><br/> | <dl> <span data-ttu-id="7f93d-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f93d-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7f93d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f93d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f93d-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="7f93d-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="7f93d-126">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="7f93d-126">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> </dl>

 

 

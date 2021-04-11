---
description: 設定骨骼位移矩陣。
ms.assetid: f8ac1117-510d-42af-a6bf-422cbaaf6b74
title: 'ID3DXSkinInfo：： SetBoneOffsetMatrix 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 283d36bb68e33cfa0e2349bab304b0cdde7ef77e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696556"
---
# <a name="id3dxskininfosetboneoffsetmatrix-method"></a><span data-ttu-id="a50eb-103">ID3DXSkinInfo：： SetBoneOffsetMatrix 方法</span><span class="sxs-lookup"><span data-stu-id="a50eb-103">ID3DXSkinInfo::SetBoneOffsetMatrix method</span></span>

<span data-ttu-id="a50eb-104">設定骨骼位移矩陣。</span><span class="sxs-lookup"><span data-stu-id="a50eb-104">Sets the bone offset matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a50eb-105">語法</span><span class="sxs-lookup"><span data-stu-id="a50eb-105">Syntax</span></span>


```C++
HRESULT SetBoneOffsetMatrix(
  [in]       DWORD      Bone,
  [in] const D3DXMATRIX *pBoneTransform
);
```



## <a name="parameters"></a><span data-ttu-id="a50eb-106">參數</span><span class="sxs-lookup"><span data-stu-id="a50eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a50eb-107">*骨骼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a50eb-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a50eb-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a50eb-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a50eb-109">骨骼編號。</span><span class="sxs-lookup"><span data-stu-id="a50eb-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="a50eb-110">*pBoneTransform* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a50eb-110">*pBoneTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a50eb-111">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a50eb-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a50eb-112">骨骼位移矩陣的指標。</span><span class="sxs-lookup"><span data-stu-id="a50eb-112">Pointer to the bone offset matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a50eb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a50eb-113">Return value</span></span>

<span data-ttu-id="a50eb-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a50eb-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a50eb-115">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="a50eb-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a50eb-116">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="a50eb-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a50eb-117">備註</span><span class="sxs-lookup"><span data-stu-id="a50eb-117">Remarks</span></span>

<span data-ttu-id="a50eb-118">[**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md)會傳回骨骼名稱。</span><span class="sxs-lookup"><span data-stu-id="a50eb-118">Bone names are returned by [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a50eb-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a50eb-119">Requirements</span></span>



| <span data-ttu-id="a50eb-120">需求</span><span class="sxs-lookup"><span data-stu-id="a50eb-120">Requirement</span></span> | <span data-ttu-id="a50eb-121">值</span><span class="sxs-lookup"><span data-stu-id="a50eb-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a50eb-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a50eb-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a50eb-123"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="a50eb-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a50eb-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="a50eb-124">Library</span></span><br/> | <dl> <span data-ttu-id="a50eb-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a50eb-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a50eb-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a50eb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a50eb-127">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="a50eb-127">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="a50eb-128">**ID3DXSkinInfo::GetBoneOffsetMatrix**</span><span class="sxs-lookup"><span data-stu-id="a50eb-128">**ID3DXSkinInfo::GetBoneOffsetMatrix**</span></span>](id3dxskininfo--getboneoffsetmatrix.md)
</dt> </dl>

 

 

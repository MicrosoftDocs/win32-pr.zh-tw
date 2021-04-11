---
description: 設定骨骼名稱。
ms.assetid: 2eecddb8-4efa-41a3-be83-7404047a9857
title: 'ID3DXSkinInfo：： SetBoneName 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c9190c12eac21963d116f60d5a7aa09f97db796
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196171"
---
# <a name="id3dxskininfosetbonename-method"></a><span data-ttu-id="6ba30-103">ID3DXSkinInfo：： SetBoneName 方法</span><span class="sxs-lookup"><span data-stu-id="6ba30-103">ID3DXSkinInfo::SetBoneName method</span></span>

<span data-ttu-id="6ba30-104">設定骨骼名稱。</span><span class="sxs-lookup"><span data-stu-id="6ba30-104">Sets the bone name.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ba30-105">語法</span><span class="sxs-lookup"><span data-stu-id="6ba30-105">Syntax</span></span>


```C++
HRESULT SetBoneName(
  [in] DWORD  Bone,
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="6ba30-106">參數</span><span class="sxs-lookup"><span data-stu-id="6ba30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ba30-107">*骨骼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ba30-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba30-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ba30-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ba30-109">骨骼編號</span><span class="sxs-lookup"><span data-stu-id="6ba30-109">Bone number</span></span>

</dd> <dt>

<span data-ttu-id="6ba30-110">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ba30-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba30-111">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ba30-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ba30-112">骨骼名稱</span><span class="sxs-lookup"><span data-stu-id="6ba30-112">Bone name</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ba30-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ba30-113">Return value</span></span>

<span data-ttu-id="6ba30-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6ba30-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6ba30-115">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="6ba30-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6ba30-116">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="6ba30-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ba30-117">備註</span><span class="sxs-lookup"><span data-stu-id="6ba30-117">Remarks</span></span>

<span data-ttu-id="6ba30-118">[**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md)會傳回骨骼名稱。</span><span class="sxs-lookup"><span data-stu-id="6ba30-118">Bone names are returned by [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ba30-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ba30-119">Requirements</span></span>



| <span data-ttu-id="6ba30-120">需求</span><span class="sxs-lookup"><span data-stu-id="6ba30-120">Requirement</span></span> | <span data-ttu-id="6ba30-121">值</span><span class="sxs-lookup"><span data-stu-id="6ba30-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba30-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6ba30-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6ba30-123"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="6ba30-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6ba30-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="6ba30-124">Library</span></span><br/> | <dl> <span data-ttu-id="6ba30-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ba30-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6ba30-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ba30-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ba30-127">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="6ba30-127">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="6ba30-128">**ID3DXSkinInfo::GetBoneName**</span><span class="sxs-lookup"><span data-stu-id="6ba30-128">**ID3DXSkinInfo::GetBoneName**</span></span>](id3dxskininfo--getbonename.md)
</dt> </dl>

 

 

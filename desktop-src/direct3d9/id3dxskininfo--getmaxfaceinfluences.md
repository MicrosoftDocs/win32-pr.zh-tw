---
description: 取得具有指定之索引緩衝區的三角形網格中最大臉部影響。
ms.assetid: 72dc2440-87df-461e-80d0-9ad9b1e4d8ee
title: 'ID3DXSkinInfo：： GetMaxFaceInfluences 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxFaceInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 11724c50d5224f0bcb2c9ced25523b869f3e347f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386418"
---
# <a name="id3dxskininfogetmaxfaceinfluences-method"></a><span data-ttu-id="35214-103">ID3DXSkinInfo：： GetMaxFaceInfluences 方法</span><span class="sxs-lookup"><span data-stu-id="35214-103">ID3DXSkinInfo::GetMaxFaceInfluences method</span></span>

<span data-ttu-id="35214-104">取得具有指定之索引緩衝區的三角形網格中最大臉部影響。</span><span class="sxs-lookup"><span data-stu-id="35214-104">Gets the maximum face influences in a triangle mesh with the specified index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="35214-105">語法</span><span class="sxs-lookup"><span data-stu-id="35214-105">Syntax</span></span>


```C++
HRESULT GetMaxFaceInfluences(
  [in] LPDIRECT3DINDEXBUFFER9 pIB,
  [in] DWORD                  NumFaces,
  [in] DWORD                  *maxFaceInfluences
);
```



## <a name="parameters"></a><span data-ttu-id="35214-106">參數</span><span class="sxs-lookup"><span data-stu-id="35214-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35214-107">*pIB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35214-107">*pIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35214-108">類型： **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="35214-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**</span></span>

<span data-ttu-id="35214-109">包含網格索引資料之索引緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="35214-109">Pointer to the index buffer that contains the mesh index data.</span></span>

</dd> <dt>

<span data-ttu-id="35214-110">*NumFaces* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35214-110">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35214-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35214-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35214-112">網格中的臉部數目。</span><span class="sxs-lookup"><span data-stu-id="35214-112">Number of faces in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="35214-113">*maxFaceInfluences* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35214-113">*maxFaceInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35214-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="35214-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="35214-115">最大臉部影響的指標。</span><span class="sxs-lookup"><span data-stu-id="35214-115">Pointer to the maximum face influences.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35214-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="35214-116">Return value</span></span>

<span data-ttu-id="35214-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="35214-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="35214-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="35214-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="35214-119">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="35214-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="35214-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="35214-120">Requirements</span></span>



| <span data-ttu-id="35214-121">需求</span><span class="sxs-lookup"><span data-stu-id="35214-121">Requirement</span></span> | <span data-ttu-id="35214-122">值</span><span class="sxs-lookup"><span data-stu-id="35214-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35214-123">標頭</span><span class="sxs-lookup"><span data-stu-id="35214-123">Header</span></span><br/>  | <dl> <span data-ttu-id="35214-124"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="35214-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="35214-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="35214-125">Library</span></span><br/> | <dl> <span data-ttu-id="35214-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="35214-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="35214-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35214-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35214-128">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="35214-128">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 

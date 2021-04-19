---
description: 取得修補程式的屬性。
ms.assetid: 601a3275-25ea-4e16-8297-a9fc1f5fdd49
title: 'ID3DXPatchMesh：： GetPatchInfo 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetPatchInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 70308857aa66551ed371dbe511acb6bd2d211bfb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999023"
---
# <a name="id3dxpatchmeshgetpatchinfo-method"></a><span data-ttu-id="b7d1c-103">ID3DXPatchMesh：： GetPatchInfo 方法</span><span class="sxs-lookup"><span data-stu-id="b7d1c-103">ID3DXPatchMesh::GetPatchInfo method</span></span>

<span data-ttu-id="b7d1c-104">取得修補程式的屬性。</span><span class="sxs-lookup"><span data-stu-id="b7d1c-104">Gets the attributes of the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d1c-105">語法</span><span class="sxs-lookup"><span data-stu-id="b7d1c-105">Syntax</span></span>


```C++
HRESULT GetPatchInfo(
  [out, retval] LPD3DXPATCHINFO PatchInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b7d1c-106">參數</span><span class="sxs-lookup"><span data-stu-id="b7d1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7d1c-107">*PatchInfo* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="b7d1c-107">*PatchInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d1c-108">類型： **[ **LPD3DXPATCHINFO**](d3dxpatchinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="b7d1c-108">Type: **[**LPD3DXPATCHINFO**](d3dxpatchinfo.md)**</span></span>

<span data-ttu-id="b7d1c-109">包含 patch 屬性之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b7d1c-109">Pointer to the structures containing the patch attributes.</span></span> <span data-ttu-id="b7d1c-110">如需修補程式屬性的詳細資訊，請參閱 [**D3DXPATCHINFO**](d3dxpatchinfo.md)。</span><span class="sxs-lookup"><span data-stu-id="b7d1c-110">For more information about patch attributes, see [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7d1c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7d1c-111">Return value</span></span>

<span data-ttu-id="b7d1c-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7d1c-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7d1c-113">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="b7d1c-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b7d1c-114">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="b7d1c-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d1c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7d1c-115">Requirements</span></span>



| <span data-ttu-id="b7d1c-116">需求</span><span class="sxs-lookup"><span data-stu-id="b7d1c-116">Requirement</span></span> | <span data-ttu-id="b7d1c-117">值</span><span class="sxs-lookup"><span data-stu-id="b7d1c-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d1c-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b7d1c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b7d1c-119"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7d1c-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b7d1c-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="b7d1c-120">Library</span></span><br/> | <dl> <span data-ttu-id="b7d1c-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7d1c-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b7d1c-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7d1c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d1c-123">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="b7d1c-123">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 





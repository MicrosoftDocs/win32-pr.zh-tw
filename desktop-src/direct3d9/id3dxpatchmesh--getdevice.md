---
description: 取得建立網格的裝置。
ms.assetid: b03dadda-ca54-4a55-a0a5-cf5ccdb55a72
title: 'ID3DXPatchMesh：： GetDevice 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a026398b719bf3ba9a9c02082105cbc7dd299013
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946234"
---
# <a name="id3dxpatchmeshgetdevice-method"></a><span data-ttu-id="ae0e5-103">ID3DXPatchMesh：： GetDevice 方法</span><span class="sxs-lookup"><span data-stu-id="ae0e5-103">ID3DXPatchMesh::GetDevice method</span></span>

<span data-ttu-id="ae0e5-104">取得建立網格的裝置。</span><span class="sxs-lookup"><span data-stu-id="ae0e5-104">Gets the device that created the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae0e5-105">語法</span><span class="sxs-lookup"><span data-stu-id="ae0e5-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="ae0e5-106">參數</span><span class="sxs-lookup"><span data-stu-id="ae0e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae0e5-107">*ppDevice* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ae0e5-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae0e5-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="ae0e5-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="ae0e5-109">裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="ae0e5-109">Pointer to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae0e5-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae0e5-110">Return value</span></span>

<span data-ttu-id="ae0e5-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae0e5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae0e5-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="ae0e5-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ae0e5-113">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="ae0e5-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae0e5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae0e5-114">Requirements</span></span>



| <span data-ttu-id="ae0e5-115">需求</span><span class="sxs-lookup"><span data-stu-id="ae0e5-115">Requirement</span></span> | <span data-ttu-id="ae0e5-116">值</span><span class="sxs-lookup"><span data-stu-id="ae0e5-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae0e5-117">標頭</span><span class="sxs-lookup"><span data-stu-id="ae0e5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ae0e5-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="ae0e5-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ae0e5-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="ae0e5-119">Library</span></span><br/> | <dl> <span data-ttu-id="ae0e5-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae0e5-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ae0e5-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae0e5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae0e5-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="ae0e5-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 

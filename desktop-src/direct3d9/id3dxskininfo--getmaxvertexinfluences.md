---
description: 取得網格中任何頂點的最大影響數目。
ms.assetid: 012168e8-30e5-4571-b793-647ab23df068
title: 'ID3DXSkinInfo：： GetMaxVertexInfluences 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxVertexInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2acae5cc119df25989e6bf22692ec1609ffa9408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946040"
---
# <a name="id3dxskininfogetmaxvertexinfluences-method"></a><span data-ttu-id="1d3cc-103">ID3DXSkinInfo：： GetMaxVertexInfluences 方法</span><span class="sxs-lookup"><span data-stu-id="1d3cc-103">ID3DXSkinInfo::GetMaxVertexInfluences method</span></span>

<span data-ttu-id="1d3cc-104">取得網格中任何頂點的最大影響數目。</span><span class="sxs-lookup"><span data-stu-id="1d3cc-104">Gets the maximum number of influences for any vertex in the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d3cc-105">語法</span><span class="sxs-lookup"><span data-stu-id="1d3cc-105">Syntax</span></span>


```C++
HRESULT GetMaxVertexInfluences(
  [in] DWORD *maxVertexInfluences
);
```



## <a name="parameters"></a><span data-ttu-id="1d3cc-106">參數</span><span class="sxs-lookup"><span data-stu-id="1d3cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d3cc-107">*maxVertexInfluences* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1d3cc-107">*maxVertexInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d3cc-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1d3cc-108">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1d3cc-109">頂點影響最大值的指標。</span><span class="sxs-lookup"><span data-stu-id="1d3cc-109">Pointer to the maximum vertex influence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d3cc-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d3cc-110">Return value</span></span>

<span data-ttu-id="1d3cc-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1d3cc-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1d3cc-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="1d3cc-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1d3cc-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="1d3cc-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d3cc-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d3cc-114">Requirements</span></span>



| <span data-ttu-id="1d3cc-115">需求</span><span class="sxs-lookup"><span data-stu-id="1d3cc-115">Requirement</span></span> | <span data-ttu-id="1d3cc-116">值</span><span class="sxs-lookup"><span data-stu-id="1d3cc-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d3cc-117">標頭</span><span class="sxs-lookup"><span data-stu-id="1d3cc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1d3cc-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="1d3cc-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1d3cc-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="1d3cc-119">Library</span></span><br/> | <dl> <span data-ttu-id="1d3cc-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d3cc-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1d3cc-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d3cc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d3cc-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="1d3cc-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 

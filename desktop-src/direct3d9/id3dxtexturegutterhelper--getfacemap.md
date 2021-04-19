---
description: 抓取每個材質所屬之網格臉部的索引。
ms.assetid: 3eb3461c-4e16-4c89-9ca9-fc9c6b5638c7
title: 'ID3DXTextureGutterHelper：： GetFaceMap 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8164ec35c3b3596914577287ecc6b9285142fca8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986749"
---
# <a name="id3dxtexturegutterhelpergetfacemap-method"></a><span data-ttu-id="1bec3-103">ID3DXTextureGutterHelper：： GetFaceMap 方法</span><span class="sxs-lookup"><span data-stu-id="1bec3-103">ID3DXTextureGutterHelper::GetFaceMap method</span></span>

<span data-ttu-id="1bec3-104">抓取每個材質所屬之網格臉部的索引。</span><span class="sxs-lookup"><span data-stu-id="1bec3-104">Retrieves the index of the mesh face to which each texel belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bec3-105">語法</span><span class="sxs-lookup"><span data-stu-id="1bec3-105">Syntax</span></span>


```C++
HRESULT GetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a><span data-ttu-id="1bec3-106">參數</span><span class="sxs-lookup"><span data-stu-id="1bec3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bec3-107">*pFaceData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1bec3-107">*pFaceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bec3-108">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1bec3-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1bec3-109">每個材質所屬之網格臉部的索引指標。</span><span class="sxs-lookup"><span data-stu-id="1bec3-109">Pointer to the index of the mesh face to which each texel belongs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bec3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="1bec3-110">Return value</span></span>

<span data-ttu-id="1bec3-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1bec3-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1bec3-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="1bec3-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1bec3-113">如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="1bec3-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="1bec3-114">備註</span><span class="sxs-lookup"><span data-stu-id="1bec3-114">Remarks</span></span>

<span data-ttu-id="1bec3-115">這個方法所傳回的網狀臉部資料僅適用于有效的 (非類別 0) 材質。</span><span class="sxs-lookup"><span data-stu-id="1bec3-115">The mesh face data returned by this method is valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="1bec3-116">[**ID3DXTextureGutterHelper：： GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) 會傳回非零值給有效 (非類別 0) 材質。</span><span class="sxs-lookup"><span data-stu-id="1bec3-116">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return nonzero values for valid (non-class 0) texels.</span></span>

<span data-ttu-id="1bec3-117">針對 [**類別2材質**](id3dxtexturegutterhelper.md)，這個方法會抓取最接近的臉部。</span><span class="sxs-lookup"><span data-stu-id="1bec3-117">For [**class 2 texels**](id3dxtexturegutterhelper.md), this method retrieves the closest face.</span></span>

<span data-ttu-id="1bec3-118">應用程式必須配置並管理 pFaceData。</span><span class="sxs-lookup"><span data-stu-id="1bec3-118">The application must allocate and manage pFaceData.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bec3-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bec3-119">Requirements</span></span>



| <span data-ttu-id="1bec3-120">需求</span><span class="sxs-lookup"><span data-stu-id="1bec3-120">Requirement</span></span> | <span data-ttu-id="1bec3-121">值</span><span class="sxs-lookup"><span data-stu-id="1bec3-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bec3-122">標頭</span><span class="sxs-lookup"><span data-stu-id="1bec3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1bec3-123"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="1bec3-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1bec3-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="1bec3-124">Library</span></span><br/> | <dl> <span data-ttu-id="1bec3-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bec3-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1bec3-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1bec3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bec3-127">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="1bec3-127">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 

---
description: 設定每個材質所屬之網格臉部的索引。
ms.assetid: 45d931bc-fb8b-48da-b30d-99d5dc183494
title: 'ID3DXTextureGutterHelper：： SetFaceMap 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ba0472052d5e2e06d759c83a404a197ecda148f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196401"
---
# <a name="id3dxtexturegutterhelpersetfacemap-method"></a><span data-ttu-id="03619-103">ID3DXTextureGutterHelper：： SetFaceMap 方法</span><span class="sxs-lookup"><span data-stu-id="03619-103">ID3DXTextureGutterHelper::SetFaceMap method</span></span>

<span data-ttu-id="03619-104">設定每個材質所屬之網格臉部的索引。</span><span class="sxs-lookup"><span data-stu-id="03619-104">Sets the index of the mesh face to which each texel belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="03619-105">語法</span><span class="sxs-lookup"><span data-stu-id="03619-105">Syntax</span></span>


```C++
HRESULT SetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a><span data-ttu-id="03619-106">參數</span><span class="sxs-lookup"><span data-stu-id="03619-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03619-107">*pFaceData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="03619-107">*pFaceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03619-108">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="03619-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="03619-109">每個材質所屬之網格臉部的索引指標。</span><span class="sxs-lookup"><span data-stu-id="03619-109">Pointer to the index of the mesh face to which each texel belongs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03619-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="03619-110">Return value</span></span>

<span data-ttu-id="03619-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="03619-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="03619-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="03619-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="03619-113">如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="03619-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="03619-114">備註</span><span class="sxs-lookup"><span data-stu-id="03619-114">Remarks</span></span>

<span data-ttu-id="03619-115">只有有效 (非類別 0) 材質時，這個方法的網狀臉部資料輸入才有效。</span><span class="sxs-lookup"><span data-stu-id="03619-115">The mesh face data input to this method is valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="03619-116">[**ID3DXTextureGutterHelper：： GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) 會針對有效的材質傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="03619-116">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return non-zero values for valid texels.</span></span>

## <a name="requirements"></a><span data-ttu-id="03619-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="03619-117">Requirements</span></span>



| <span data-ttu-id="03619-118">需求</span><span class="sxs-lookup"><span data-stu-id="03619-118">Requirement</span></span> | <span data-ttu-id="03619-119">值</span><span class="sxs-lookup"><span data-stu-id="03619-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03619-120">標頭</span><span class="sxs-lookup"><span data-stu-id="03619-120">Header</span></span><br/>  | <dl> <span data-ttu-id="03619-121"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="03619-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="03619-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="03619-122">Library</span></span><br/> | <dl> <span data-ttu-id="03619-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="03619-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="03619-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03619-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03619-125">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="03619-125">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 

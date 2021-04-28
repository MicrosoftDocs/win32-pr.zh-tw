---
description: D3DX10CreateSkinInfo 函式-使用宣告子建立空白的外觀網格物件。
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: 'D3DX10CreateSkinInfo 函式 (D3DX10Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSkinInfo
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 17d6ec99d3f43c41d56deebef81a021c81ec1d69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103596"
---
# <a name="d3dx10createskininfo-function"></a><span data-ttu-id="7e408-103">D3DX10CreateSkinInfo 函式</span><span class="sxs-lookup"><span data-stu-id="7e408-103">D3DX10CreateSkinInfo function</span></span>

<span data-ttu-id="7e408-104">使用宣告子建立空白的外觀網格物件。</span><span class="sxs-lookup"><span data-stu-id="7e408-104">Creates an empty skin mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e408-105">語法</span><span class="sxs-lookup"><span data-stu-id="7e408-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="7e408-106">參數</span><span class="sxs-lookup"><span data-stu-id="7e408-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e408-107">*ppSkinInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7e408-107">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e408-108">類型： **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e408-108">Type: **[**LPD3DX10SKININFO**](id3dx10skininfo.md)\***</span></span>

<span data-ttu-id="7e408-109">[**ID3DX10SkinInfo 介面**](id3dx10skininfo.md)指標的位址，表示所建立的面板網格物件。</span><span class="sxs-lookup"><span data-stu-id="7e408-109">Address of a pointer to an [**ID3DX10SkinInfo Interface**](id3dx10skininfo.md), representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e408-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="7e408-110">Return value</span></span>

<span data-ttu-id="7e408-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7e408-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7e408-112">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="7e408-112">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7e408-113">如果函式失敗，則傳回值可以是： E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="7e408-113">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e408-114">備註</span><span class="sxs-lookup"><span data-stu-id="7e408-114">Remarks</span></span>

<span data-ttu-id="7e408-115">使用 [**ID3DX10SkinInfo：： SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) 來填入這個方法所傳回的空白麵板網格物件。</span><span class="sxs-lookup"><span data-stu-id="7e408-115">Use the [**ID3DX10SkinInfo::SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e408-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e408-116">Requirements</span></span>



| <span data-ttu-id="7e408-117">需求</span><span class="sxs-lookup"><span data-stu-id="7e408-117">Requirement</span></span> | <span data-ttu-id="7e408-118">值</span><span class="sxs-lookup"><span data-stu-id="7e408-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e408-119">標頭</span><span class="sxs-lookup"><span data-stu-id="7e408-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7e408-120"><dt>D3DX10Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="7e408-120"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7e408-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="7e408-121">Library</span></span><br/> | <dl> <span data-ttu-id="7e408-122"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e408-122"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7e408-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e408-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e408-124">網格函數</span><span class="sxs-lookup"><span data-stu-id="7e408-124">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="7e408-125">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="7e408-125">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 





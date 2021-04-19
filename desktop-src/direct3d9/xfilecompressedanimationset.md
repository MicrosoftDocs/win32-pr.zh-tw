---
description: 識別壓縮的主要畫面格動畫資料。
ms.assetid: 2aab46db-e0ad-4bbb-b1c5-a254ec6cb984
title: 'XFILECOMPRESSEDANIMATIONSET 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XFILECOMPRESSEDANIMATIONSET
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 240cac57c9c0d123203ee4599c14092df1327f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000573"
---
# <a name="xfilecompressedanimationset-structure"></a><span data-ttu-id="11ca6-103">XFILECOMPRESSEDANIMATIONSET 結構</span><span class="sxs-lookup"><span data-stu-id="11ca6-103">XFILECOMPRESSEDANIMATIONSET structure</span></span>

<span data-ttu-id="11ca6-104">識別壓縮的主要畫面格動畫資料。</span><span class="sxs-lookup"><span data-stu-id="11ca6-104">Identifies compressed key frame animation data.</span></span>

## <a name="syntax"></a><span data-ttu-id="11ca6-105">語法</span><span class="sxs-lookup"><span data-stu-id="11ca6-105">Syntax</span></span>


```C++
typedef struct XFILECOMPRESSEDANIMATIONSET {
  DWORD CompressedBlockSize;
  FLOAT TicksPerSec;
  DWORD PlaybackType;
  DWORD BufferLength;
} XFILECOMPRESSEDANIMATIONSET, *LPXFILECOMPRESSEDANIMATIONSET;
```



## <a name="members"></a><span data-ttu-id="11ca6-106">成員</span><span class="sxs-lookup"><span data-stu-id="11ca6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="11ca6-107">**CompressedBlockSize**</span><span class="sxs-lookup"><span data-stu-id="11ca6-107">**CompressedBlockSize**</span></span>
</dt> <dd>

<span data-ttu-id="11ca6-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11ca6-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="11ca6-109">壓縮的主要畫面格動畫資料緩衝區中壓縮資料的總大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="11ca6-109">Total size, in bytes, of the compressed data in the compressed key frame animation data buffer.</span></span>

</dd> <dt>

<span data-ttu-id="11ca6-110">**TicksPerSec**</span><span class="sxs-lookup"><span data-stu-id="11ca6-110">**TicksPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="11ca6-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11ca6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="11ca6-112">每秒發生的動畫主要畫面格刻度數目。</span><span class="sxs-lookup"><span data-stu-id="11ca6-112">Number of animation key frame ticks that occur per second.</span></span>

</dd> <dt>

<span data-ttu-id="11ca6-113">**PlaybackType**</span><span class="sxs-lookup"><span data-stu-id="11ca6-113">**PlaybackType**</span></span>
</dt> <dd>

<span data-ttu-id="11ca6-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11ca6-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="11ca6-115">動畫集合播放迴圈的型別。</span><span class="sxs-lookup"><span data-stu-id="11ca6-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="11ca6-116">請參閱 [**D3DXPLAYBACK \_ 類型**](./d3dxplayback-type.md)。</span><span class="sxs-lookup"><span data-stu-id="11ca6-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="11ca6-117">**BufferLength**</span><span class="sxs-lookup"><span data-stu-id="11ca6-117">**BufferLength**</span></span>
</dt> <dd>

<span data-ttu-id="11ca6-118">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11ca6-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="11ca6-119">保存壓縮的主要畫面格動畫資料所需的緩衝區大小下限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="11ca6-119">Minimum buffer size, in bytes, required to hold compressed key frame animation data.</span></span> <span data-ttu-id="11ca6-120">值等於 ( ( CompressedBlockSize + 3 ) /4 ) 。</span><span class="sxs-lookup"><span data-stu-id="11ca6-120">Value is equal to ( ( CompressedBlockSize + 3 ) / 4 ).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11ca6-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="11ca6-121">Requirements</span></span>



| <span data-ttu-id="11ca6-122">需求</span><span class="sxs-lookup"><span data-stu-id="11ca6-122">Requirement</span></span> | <span data-ttu-id="11ca6-123">值</span><span class="sxs-lookup"><span data-stu-id="11ca6-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11ca6-124">標頭</span><span class="sxs-lookup"><span data-stu-id="11ca6-124">Header</span></span><br/> | <dl> <span data-ttu-id="11ca6-125"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="11ca6-125"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11ca6-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11ca6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11ca6-127">D3DX X 檔案結構</span><span class="sxs-lookup"><span data-stu-id="11ca6-127">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="11ca6-128">**ID3DXCompressedAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="11ca6-128">**ID3DXCompressedAnimationSet**</span></span>](id3dxcompressedanimationset.md)
</dt> </dl>

 

 

---
description: 要在其上進行軟體外觀的頂點 decl 成員。 這可搭配 ID3DX10SkinInfo：:D oSoftwareSkinning API 使用。
ms.assetid: 67c817cd-ce78-4e8b-bdc3-7c4d6670dee1
title: 'D3DX10_SKINNING_CHANNEL 結構 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SKINNING_CHANNEL
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 79f5807dc2539d770d3caa41bddf7aa4960ce682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196318"
---
# <a name="d3dx10_skinning_channel-structure"></a><span data-ttu-id="c7da6-104">D3DX10 \_ 外觀 \_ 通道結構</span><span class="sxs-lookup"><span data-stu-id="c7da6-104">D3DX10\_SKINNING\_CHANNEL structure</span></span>

<span data-ttu-id="c7da6-105">要在其上進行軟體外觀的頂點 decl 成員。</span><span class="sxs-lookup"><span data-stu-id="c7da6-105">The member of the vertex decl to do the software skinning on.</span></span> <span data-ttu-id="c7da6-106">這可搭配 [**ID3DX10SkinInfo：:D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) API 使用。</span><span class="sxs-lookup"><span data-stu-id="c7da6-106">This is used with the [**ID3DX10SkinInfo::DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md) API.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7da6-107">語法</span><span class="sxs-lookup"><span data-stu-id="c7da6-107">Syntax</span></span>


```C++
typedef struct D3DX10_SKINNING_CHANNEL {
  UINT SrcOffset;
  UINT DestOffset;
  BOOL IsNormal;
} D3DX10_SKINNING_CHANNEL, *LPD3DX10_SKINNING_CHANNEL;
```



## <a name="members"></a><span data-ttu-id="c7da6-108">成員</span><span class="sxs-lookup"><span data-stu-id="c7da6-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c7da6-109">**SrcOffset**</span><span class="sxs-lookup"><span data-stu-id="c7da6-109">**SrcOffset**</span></span>
</dt> <dd>

<span data-ttu-id="c7da6-110">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7da6-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7da6-111">從每個來源頂點的開頭算起的位移。</span><span class="sxs-lookup"><span data-stu-id="c7da6-111">Offset from the beginning of each source vertex.</span></span>

</dd> <dt>

<span data-ttu-id="c7da6-112">**DestOffset**</span><span class="sxs-lookup"><span data-stu-id="c7da6-112">**DestOffset**</span></span>
</dt> <dd>

<span data-ttu-id="c7da6-113">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7da6-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7da6-114">從每個目的地頂點的開頭算起的位移。</span><span class="sxs-lookup"><span data-stu-id="c7da6-114">Offset from the beginning of each destination vertex.</span></span>

</dd> <dt>

<span data-ttu-id="c7da6-115">**IsNormal**</span><span class="sxs-lookup"><span data-stu-id="c7da6-115">**IsNormal**</span></span>
</dt> <dd>

<span data-ttu-id="c7da6-116">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7da6-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7da6-117">判斷要在 [**ID3DX10SkinInfo：:D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) API 中使用的矩陣陣列。</span><span class="sxs-lookup"><span data-stu-id="c7da6-117">Determines which array of matrices to use in the [**ID3DX10SkinInfo::DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md) API.</span></span> <span data-ttu-id="c7da6-118">若為 true，則會使用 *pInverseTransposeBoneMatrices* ，否則會使用 *pBoneMatrices* 。</span><span class="sxs-lookup"><span data-stu-id="c7da6-118">If this is true, the *pInverseTransposeBoneMatrices* will be used, otherwise *pBoneMatrices* will be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7da6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7da6-119">Requirements</span></span>



| <span data-ttu-id="c7da6-120">需求</span><span class="sxs-lookup"><span data-stu-id="c7da6-120">Requirement</span></span> | <span data-ttu-id="c7da6-121">值</span><span class="sxs-lookup"><span data-stu-id="c7da6-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c7da6-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c7da6-122">Header</span></span><br/> | <dl> <span data-ttu-id="c7da6-123"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7da6-123"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7da6-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7da6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7da6-125">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="c7da6-125">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 

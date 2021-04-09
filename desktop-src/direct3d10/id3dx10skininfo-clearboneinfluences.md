---
description: 清除其所影響之骨骼的頂點清單。
ms.assetid: 1ba6f43a-1f85-4057-b0ed-247cc38d4932
title: 'ID3DX10SkinInfo：： ClearBoneInfluences 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.ClearBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6f161ba400b684b12d6b0a091abb1fa452d476b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946108"
---
# <a name="id3dx10skininfoclearboneinfluences-method"></a><span data-ttu-id="c2836-103">ID3DX10SkinInfo：： ClearBoneInfluences 方法</span><span class="sxs-lookup"><span data-stu-id="c2836-103">ID3DX10SkinInfo::ClearBoneInfluences method</span></span>

<span data-ttu-id="c2836-104">清除其所影響之骨骼的頂點清單。</span><span class="sxs-lookup"><span data-stu-id="c2836-104">Clear a bone's list of vertices that it influences.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2836-105">語法</span><span class="sxs-lookup"><span data-stu-id="c2836-105">Syntax</span></span>


```C++
HRESULT ClearBoneInfluences(
  [in] UINT BoneIndex
);
```



## <a name="parameters"></a><span data-ttu-id="c2836-106">參數</span><span class="sxs-lookup"><span data-stu-id="c2836-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2836-107">*BoneIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2836-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2836-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2836-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2836-109">指定現有骨骼的索引。</span><span class="sxs-lookup"><span data-stu-id="c2836-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="c2836-110">必須介於0和 [**ID3DX10SkinInfo：： GetNumBones**](id3dx10skininfo-getnumbones.md)所傳回的值之間。</span><span class="sxs-lookup"><span data-stu-id="c2836-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2836-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2836-111">Return value</span></span>

<span data-ttu-id="c2836-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c2836-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c2836-113">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c2836-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c2836-114">如果方法失敗，則傳回值可以是： E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="c2836-114">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2836-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2836-115">Requirements</span></span>



| <span data-ttu-id="c2836-116">需求</span><span class="sxs-lookup"><span data-stu-id="c2836-116">Requirement</span></span> | <span data-ttu-id="c2836-117">值</span><span class="sxs-lookup"><span data-stu-id="c2836-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2836-118">標頭</span><span class="sxs-lookup"><span data-stu-id="c2836-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c2836-119"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="c2836-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2836-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="c2836-120">Library</span></span><br/> | <dl> <span data-ttu-id="c2836-121"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2836-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2836-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2836-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2836-123">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="c2836-123">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="c2836-124">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="c2836-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

---
description: 移除骨骼。
ms.assetid: efb88108-5c76-47c8-b8ce-1ba29cb18ba4
title: 'ID3DX10SkinInfo：： RemoveBone 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemoveBone
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 49fd24c5661bbedb7fb839171fa4a835f07e446a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997619"
---
# <a name="id3dx10skininforemovebone-method"></a><span data-ttu-id="ebdad-103">ID3DX10SkinInfo：： RemoveBone 方法</span><span class="sxs-lookup"><span data-stu-id="ebdad-103">ID3DX10SkinInfo::RemoveBone method</span></span>

<span data-ttu-id="ebdad-104">移除骨骼。</span><span class="sxs-lookup"><span data-stu-id="ebdad-104">Remove a bone.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebdad-105">語法</span><span class="sxs-lookup"><span data-stu-id="ebdad-105">Syntax</span></span>


```C++
HRESULT RemoveBone(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="ebdad-106">參數</span><span class="sxs-lookup"><span data-stu-id="ebdad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebdad-107">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ebdad-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebdad-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ebdad-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ebdad-109">指定要移除之骨骼的索引。</span><span class="sxs-lookup"><span data-stu-id="ebdad-109">An index that specifies which bone to remove.</span></span> <span data-ttu-id="ebdad-110">必須介於0和 [**ID3DX10SkinInfo：： GetNumBones**](id3dx10skininfo-getnumbones.md)所傳回的值之間。</span><span class="sxs-lookup"><span data-stu-id="ebdad-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebdad-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ebdad-111">Return value</span></span>

<span data-ttu-id="ebdad-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ebdad-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ebdad-113">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ebdad-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ebdad-114">如果方法失敗，則傳回值可以是： E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="ebdad-114">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebdad-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebdad-115">Requirements</span></span>



| <span data-ttu-id="ebdad-116">需求</span><span class="sxs-lookup"><span data-stu-id="ebdad-116">Requirement</span></span> | <span data-ttu-id="ebdad-117">值</span><span class="sxs-lookup"><span data-stu-id="ebdad-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ebdad-118">標頭</span><span class="sxs-lookup"><span data-stu-id="ebdad-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ebdad-119"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="ebdad-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ebdad-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="ebdad-120">Library</span></span><br/> | <dl> <span data-ttu-id="ebdad-121"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebdad-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebdad-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebdad-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebdad-123">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="ebdad-123">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="ebdad-124">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="ebdad-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

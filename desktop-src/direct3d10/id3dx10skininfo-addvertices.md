---
description: 配置其他頂點的空間。
ms.assetid: dd6445ea-4754-4ba3-a264-59295325ee08
title: 'ID3DX10SkinInfo：： AddVertices 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8f126b31c375e4e3463133960c5a1bcfbd995b62
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976751"
---
# <a name="id3dx10skininfoaddvertices-method"></a><span data-ttu-id="74ab9-103">ID3DX10SkinInfo：： AddVertices 方法</span><span class="sxs-lookup"><span data-stu-id="74ab9-103">ID3DX10SkinInfo::AddVertices method</span></span>

<span data-ttu-id="74ab9-104">配置其他頂點的空間。</span><span class="sxs-lookup"><span data-stu-id="74ab9-104">Allocate space for additional vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="74ab9-105">語法</span><span class="sxs-lookup"><span data-stu-id="74ab9-105">Syntax</span></span>


```C++
HRESULT AddVertices(
  [in] UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="74ab9-106">參數</span><span class="sxs-lookup"><span data-stu-id="74ab9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74ab9-107">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74ab9-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74ab9-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74ab9-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74ab9-109">要加入的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="74ab9-109">The number of vertices to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74ab9-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="74ab9-110">Return value</span></span>

<span data-ttu-id="74ab9-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74ab9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74ab9-112">如果這個方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="74ab9-112">If this method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="74ab9-113">如果方法失敗，則傳回值可以是： E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="74ab9-113">If the method fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="74ab9-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="74ab9-114">Requirements</span></span>



| <span data-ttu-id="74ab9-115">需求</span><span class="sxs-lookup"><span data-stu-id="74ab9-115">Requirement</span></span> | <span data-ttu-id="74ab9-116">值</span><span class="sxs-lookup"><span data-stu-id="74ab9-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74ab9-117">標頭</span><span class="sxs-lookup"><span data-stu-id="74ab9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="74ab9-118"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="74ab9-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="74ab9-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="74ab9-119">Library</span></span><br/> | <dl> <span data-ttu-id="74ab9-120"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="74ab9-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74ab9-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74ab9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74ab9-122">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="74ab9-122">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="74ab9-123">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="74ab9-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

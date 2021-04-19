---
description: 設定網格的索引資料。
ms.assetid: f3e7e166-94b5-45f6-9d43-8d7e32b7b523
title: 'ID3DX10Mesh：： SetIndexData 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetIndexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f561a4109fbab2163b2ec51e95b45a618da5b6d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998587"
---
# <a name="id3dx10meshsetindexdata-method"></a><span data-ttu-id="1a69d-103">ID3DX10Mesh：： SetIndexData 方法</span><span class="sxs-lookup"><span data-stu-id="1a69d-103">ID3DX10Mesh::SetIndexData method</span></span>

<span data-ttu-id="1a69d-104">設定網格的索引資料。</span><span class="sxs-lookup"><span data-stu-id="1a69d-104">Set the mesh's index data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a69d-105">語法</span><span class="sxs-lookup"><span data-stu-id="1a69d-105">Syntax</span></span>


```C++
HRESULT SetIndexData(
  [in] const void *pData,
  [in]       UINT cIndices
);
```



## <a name="parameters"></a><span data-ttu-id="1a69d-106">參數</span><span class="sxs-lookup"><span data-stu-id="1a69d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a69d-107">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1a69d-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a69d-108">類型： **const void \***</span><span class="sxs-lookup"><span data-stu-id="1a69d-108">Type: **const void\***</span></span>

<span data-ttu-id="1a69d-109">索引資料。</span><span class="sxs-lookup"><span data-stu-id="1a69d-109">The index data.</span></span>

</dd> <dt>

<span data-ttu-id="1a69d-110">*cIndices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1a69d-110">*cIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a69d-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a69d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a69d-112">.Pdata 中的索引數目。</span><span class="sxs-lookup"><span data-stu-id="1a69d-112">The number of indices in pData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a69d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a69d-113">Return value</span></span>

<span data-ttu-id="1a69d-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1a69d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1a69d-115">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1a69d-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a69d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a69d-116">Requirements</span></span>



| <span data-ttu-id="1a69d-117">需求</span><span class="sxs-lookup"><span data-stu-id="1a69d-117">Requirement</span></span> | <span data-ttu-id="1a69d-118">值</span><span class="sxs-lookup"><span data-stu-id="1a69d-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a69d-119">標頭</span><span class="sxs-lookup"><span data-stu-id="1a69d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1a69d-120"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="1a69d-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a69d-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="1a69d-121">Library</span></span><br/> | <dl> <span data-ttu-id="1a69d-122"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a69d-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a69d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a69d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a69d-124">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="1a69d-124">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="1a69d-125">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="1a69d-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

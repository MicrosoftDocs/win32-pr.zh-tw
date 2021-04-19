---
description: 設定網狀網格的相鄰資料。
ms.assetid: 67d51ce0-7fe2-484d-9874-f1fa59632d59
title: 'ID3DX10Mesh：： SetAdjacencyData 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAdjacencyData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6fabced002caf424fa1fcbcefcb3b326b0c71f7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999975"
---
# <a name="id3dx10meshsetadjacencydata-method"></a><span data-ttu-id="19135-103">ID3DX10Mesh：： SetAdjacencyData 方法</span><span class="sxs-lookup"><span data-stu-id="19135-103">ID3DX10Mesh::SetAdjacencyData method</span></span>

<span data-ttu-id="19135-104">設定網狀網格的相鄰資料。</span><span class="sxs-lookup"><span data-stu-id="19135-104">Set the mesh's adjacency data.</span></span>

## <a name="syntax"></a><span data-ttu-id="19135-105">語法</span><span class="sxs-lookup"><span data-stu-id="19135-105">Syntax</span></span>


```C++
HRESULT SetAdjacencyData(
  [in] const UINT *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="19135-106">參數</span><span class="sxs-lookup"><span data-stu-id="19135-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19135-107">*pAdjacency* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19135-107">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19135-108">類型： **Const [**UINT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="19135-108">Type: **const [**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="19135-109">要設定的相鄰資料。</span><span class="sxs-lookup"><span data-stu-id="19135-109">The adjacency data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19135-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="19135-110">Return value</span></span>

<span data-ttu-id="19135-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19135-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19135-112">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="19135-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19135-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="19135-113">Requirements</span></span>



| <span data-ttu-id="19135-114">需求</span><span class="sxs-lookup"><span data-stu-id="19135-114">Requirement</span></span> | <span data-ttu-id="19135-115">值</span><span class="sxs-lookup"><span data-stu-id="19135-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19135-116">標頭</span><span class="sxs-lookup"><span data-stu-id="19135-116">Header</span></span><br/>  | <dl> <span data-ttu-id="19135-117"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="19135-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="19135-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="19135-118">Library</span></span><br/> | <dl> <span data-ttu-id="19135-119"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="19135-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19135-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19135-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19135-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="19135-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="19135-122">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="19135-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

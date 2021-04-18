---
description: 取得網狀的點 rep 緩衝區。
ms.assetid: 4be7bee5-15ea-496f-83c2-a3a9bafd97c6
title: 'ID3DX10Mesh：： GetPointRepBuffer 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetPointRepBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 131094792f35b21fd230b66bda6a43fb104b65ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116233"
---
# <a name="id3dx10meshgetpointrepbuffer-method"></a><span data-ttu-id="16be3-103">ID3DX10Mesh：： GetPointRepBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="16be3-103">ID3DX10Mesh::GetPointRepBuffer method</span></span>

<span data-ttu-id="16be3-104">取得網狀的點 rep 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="16be3-104">Get the mesh's point rep buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="16be3-105">語法</span><span class="sxs-lookup"><span data-stu-id="16be3-105">Syntax</span></span>


```C++
HRESULT GetPointRepBuffer(
  [out] ID3DX10MeshBuffer **ppPointReps
);
```



## <a name="parameters"></a><span data-ttu-id="16be3-106">參數</span><span class="sxs-lookup"><span data-stu-id="16be3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16be3-107">*ppPointReps* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="16be3-107">*ppPointReps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16be3-108">類型： **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="16be3-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="16be3-109">包含網格點代表資料的網狀緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="16be3-109">Pointer to a mesh buffer containing the mesh's point rep data.</span></span> <span data-ttu-id="16be3-110">請參閱 [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="16be3-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16be3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="16be3-111">Return value</span></span>

<span data-ttu-id="16be3-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="16be3-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="16be3-113">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="16be3-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16be3-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="16be3-114">Requirements</span></span>



| <span data-ttu-id="16be3-115">需求</span><span class="sxs-lookup"><span data-stu-id="16be3-115">Requirement</span></span> | <span data-ttu-id="16be3-116">值</span><span class="sxs-lookup"><span data-stu-id="16be3-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16be3-117">標頭</span><span class="sxs-lookup"><span data-stu-id="16be3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="16be3-118"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="16be3-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="16be3-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="16be3-119">Library</span></span><br/> | <dl> <span data-ttu-id="16be3-120"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="16be3-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16be3-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16be3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16be3-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="16be3-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="16be3-123">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="16be3-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 





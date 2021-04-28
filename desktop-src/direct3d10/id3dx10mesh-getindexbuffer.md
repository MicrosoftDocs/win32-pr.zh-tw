---
description: ID3DX10Mesh：： GetIndexBuffer 方法-捕獲索引緩衝區中的資料。
ms.assetid: 7e25ad67-7f9d-4c23-a029-a2262034ef38
title: 'ID3DX10Mesh：： GetIndexBuffer 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 751d6dd0376dc73f0213ddb83a19954dc154d633
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084026"
---
# <a name="id3dx10meshgetindexbuffer-method"></a><span data-ttu-id="c160c-103">ID3DX10Mesh：： GetIndexBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="c160c-103">ID3DX10Mesh::GetIndexBuffer method</span></span>

<span data-ttu-id="c160c-104">抓取索引緩衝區中的資料。</span><span class="sxs-lookup"><span data-stu-id="c160c-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c160c-105">語法</span><span class="sxs-lookup"><span data-stu-id="c160c-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out] ID3DX10MeshBuffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="c160c-106">參數</span><span class="sxs-lookup"><span data-stu-id="c160c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c160c-107">*ppIndexBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c160c-107">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c160c-108">類型： **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c160c-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="c160c-109">ID3DX10MeshBuffer 介面指標的位址，表示與網格相關聯的索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c160c-109">Address of a pointer to a ID3DX10MeshBuffer interface, representing the index buffer associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c160c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c160c-110">Return value</span></span>

<span data-ttu-id="c160c-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c160c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c160c-112">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c160c-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c160c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c160c-113">Requirements</span></span>



| <span data-ttu-id="c160c-114">需求</span><span class="sxs-lookup"><span data-stu-id="c160c-114">Requirement</span></span> | <span data-ttu-id="c160c-115">值</span><span class="sxs-lookup"><span data-stu-id="c160c-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c160c-116">標頭</span><span class="sxs-lookup"><span data-stu-id="c160c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c160c-117"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="c160c-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c160c-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="c160c-118">Library</span></span><br/> | <dl> <span data-ttu-id="c160c-119"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c160c-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c160c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c160c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c160c-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="c160c-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="c160c-122">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="c160c-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 





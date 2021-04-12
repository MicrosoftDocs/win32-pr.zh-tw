---
description: 取得網狀緩衝區記憶體的指標，以修改其內容。
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: 'ID3DX10MeshBuffer：： Map 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Map
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b8cb03e128a6673963ce2d3cde993babb03da5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322955"
---
# <a name="id3dx10meshbuffermap-method"></a><span data-ttu-id="59901-103">ID3DX10MeshBuffer：： Map 方法</span><span class="sxs-lookup"><span data-stu-id="59901-103">ID3DX10MeshBuffer::Map method</span></span>

<span data-ttu-id="59901-104">取得網狀緩衝區記憶體的指標，以修改其內容。</span><span class="sxs-lookup"><span data-stu-id="59901-104">Get a pointer to the mesh buffer memory to modify its contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="59901-105">語法</span><span class="sxs-lookup"><span data-stu-id="59901-105">Syntax</span></span>


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="59901-106">參數</span><span class="sxs-lookup"><span data-stu-id="59901-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59901-107">*ppData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="59901-107">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59901-108">類型： **void \* \***</span><span class="sxs-lookup"><span data-stu-id="59901-108">Type: **void\*\***</span></span>

<span data-ttu-id="59901-109">緩衝區資料的指標。</span><span class="sxs-lookup"><span data-stu-id="59901-109">Pointer to the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="59901-110">*pSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="59901-110">*pSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59901-111">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="59901-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="59901-112">以位元組為單位的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="59901-112">Size of the buffer in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59901-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="59901-113">Return value</span></span>

<span data-ttu-id="59901-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59901-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59901-115">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="59901-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="59901-116">備註</span><span class="sxs-lookup"><span data-stu-id="59901-116">Remarks</span></span>



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59901-117">Direct3D 9 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="59901-117">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="59901-118">Direct3D 10 中的 map () 類似于 Direct3D 9 中的資源對應 () 。</span><span class="sxs-lookup"><span data-stu-id="59901-118">Map() in Direct3D 10 is analogous to resource Map() in Direct3D 9.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="59901-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="59901-119">Requirements</span></span>



| <span data-ttu-id="59901-120">需求</span><span class="sxs-lookup"><span data-stu-id="59901-120">Requirement</span></span> | <span data-ttu-id="59901-121">值</span><span class="sxs-lookup"><span data-stu-id="59901-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59901-122">標頭</span><span class="sxs-lookup"><span data-stu-id="59901-122">Header</span></span><br/>  | <dl> <span data-ttu-id="59901-123"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="59901-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="59901-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="59901-124">Library</span></span><br/> | <dl> <span data-ttu-id="59901-125"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="59901-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59901-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59901-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59901-127">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="59901-127">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="59901-128">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="59901-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

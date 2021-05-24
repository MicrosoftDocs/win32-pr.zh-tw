---
description: 取消對應緩衝區。
ms.assetid: 47f125cd-5c0a-4814-93c5-f2f11ce33ea6
title: 'ID3DX10MeshBuffer：：取消對應方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Unmap
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 11b15f8bc1e4103503b183672ebd31e92b4daea7
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335372"
---
# <a name="id3dx10meshbufferunmap-method"></a><span data-ttu-id="f83ac-103">ID3DX10MeshBuffer：：取消對應方法</span><span class="sxs-lookup"><span data-stu-id="f83ac-103">ID3DX10MeshBuffer::Unmap method</span></span>

<span data-ttu-id="f83ac-104">取消對應緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f83ac-104">Unmap a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f83ac-105">語法</span><span class="sxs-lookup"><span data-stu-id="f83ac-105">Syntax</span></span>


```C++
HRESULT Unmap();
```



## <a name="parameters"></a><span data-ttu-id="f83ac-106">參數</span><span class="sxs-lookup"><span data-stu-id="f83ac-106">Parameters</span></span>

<span data-ttu-id="f83ac-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f83ac-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f83ac-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f83ac-108">Return value</span></span>

<span data-ttu-id="f83ac-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f83ac-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f83ac-110">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f83ac-110">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f83ac-111">備註</span><span class="sxs-lookup"><span data-stu-id="f83ac-111">Remarks</span></span>



<span data-ttu-id="f83ac-112">Direct3D 9 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="f83ac-112">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="f83ac-113">Direct3D 10 中的取消對應 () 類似于 Direct3D 9 中的資源解除鎖定 () 。</span><span class="sxs-lookup"><span data-stu-id="f83ac-113">Unmap() in Direct3D 10 is analogous to resource Unlock() in Direct3D 9.</span></span>



 

## <a name="requirements"></a><span data-ttu-id="f83ac-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f83ac-114">Requirements</span></span>



| <span data-ttu-id="f83ac-115">需求</span><span class="sxs-lookup"><span data-stu-id="f83ac-115">Requirement</span></span> | <span data-ttu-id="f83ac-116">值</span><span class="sxs-lookup"><span data-stu-id="f83ac-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f83ac-117">標頭</span><span class="sxs-lookup"><span data-stu-id="f83ac-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f83ac-118"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="f83ac-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f83ac-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="f83ac-119">Library</span></span><br/> | <dl> <span data-ttu-id="f83ac-120"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f83ac-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f83ac-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f83ac-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f83ac-122">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="f83ac-122">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="f83ac-123">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="f83ac-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 





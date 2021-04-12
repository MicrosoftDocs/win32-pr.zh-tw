---
description: Unassociates 具有 ID3DXPRTBuffer 物件的附加 ID3DXTextureGutterHelper 物件。
ms.assetid: 0bd8322a-8af1-4173-bbe3-9134c831cf3a
title: 'ID3DXPRTBuffer：： ReleaseGH 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ReleaseGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9fb7a68f11d21065d6b4911b9ee7f58920aeb25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386524"
---
# <a name="id3dxprtbufferreleasegh-method"></a><span data-ttu-id="e6cb1-103">ID3DXPRTBuffer：： ReleaseGH 方法</span><span class="sxs-lookup"><span data-stu-id="e6cb1-103">ID3DXPRTBuffer::ReleaseGH method</span></span>

<span data-ttu-id="e6cb1-104">Unassociates 具有 [**ID3DXPRTBuffer**](id3dxprtbuffer.md)物件的附加 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md)物件。</span><span class="sxs-lookup"><span data-stu-id="e6cb1-104">Unassociates an attached [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6cb1-105">語法</span><span class="sxs-lookup"><span data-stu-id="e6cb1-105">Syntax</span></span>


```C++
HRESULT ReleaseGH();
```



## <a name="parameters"></a><span data-ttu-id="e6cb1-106">參數</span><span class="sxs-lookup"><span data-stu-id="e6cb1-106">Parameters</span></span>

<span data-ttu-id="e6cb1-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e6cb1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6cb1-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6cb1-108">Return value</span></span>

<span data-ttu-id="e6cb1-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e6cb1-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e6cb1-110">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="e6cb1-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6cb1-111">備註</span><span class="sxs-lookup"><span data-stu-id="e6cb1-111">Remarks</span></span>

<span data-ttu-id="e6cb1-112">這個方法會釋放 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e6cb1-112">This method releases the pointer to the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) interface.</span></span>

<span data-ttu-id="e6cb1-113">您必須確保 [**ID3DXPRTBuffer：： AttachGH**](id3dxprtbuffer--attachgh.md) 呼叫的數目符合 **ID3DXPRTBuffer：： ReleaseGH** 呼叫的數目。</span><span class="sxs-lookup"><span data-stu-id="e6cb1-113">You must ensure that the number of [**ID3DXPRTBuffer::AttachGH**](id3dxprtbuffer--attachgh.md) calls matches the number of **ID3DXPRTBuffer::ReleaseGH** calls.</span></span> <span data-ttu-id="e6cb1-114">在呼叫 **ID3DXPRTBuffer：： ReleaseGH** 之後，不應該再使用 **ID3DXPRTBuffer：： AttachGH** 所傳回的 pGH 指標。</span><span class="sxs-lookup"><span data-stu-id="e6cb1-114">After calling **ID3DXPRTBuffer::ReleaseGH**, the pGH pointer returned by **ID3DXPRTBuffer::AttachGH** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6cb1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6cb1-115">Requirements</span></span>



| <span data-ttu-id="e6cb1-116">需求</span><span class="sxs-lookup"><span data-stu-id="e6cb1-116">Requirement</span></span> | <span data-ttu-id="e6cb1-117">值</span><span class="sxs-lookup"><span data-stu-id="e6cb1-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6cb1-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e6cb1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e6cb1-119"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6cb1-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e6cb1-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="e6cb1-120">Library</span></span><br/> | <dl> <span data-ttu-id="e6cb1-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6cb1-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e6cb1-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6cb1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6cb1-123">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="e6cb1-123">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="e6cb1-124">**ID3DXPRTBuffer::AttachGH**</span><span class="sxs-lookup"><span data-stu-id="e6cb1-124">**ID3DXPRTBuffer::AttachGH**</span></span>](id3dxprtbuffer--attachgh.md)
</dt> </dl>

 

 





---
description: 將 ID3DXTextureGutterHelper 物件與 ID3DXPRTBuffer 物件建立關聯。
ms.assetid: 095fea82-ac7a-42fa-990a-084715c73823
title: 'ID3DXPRTBuffer：： AttachGH 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AttachGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba5afa238107d60620291b50b8f184eb4e5d361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988606"
---
# <a name="id3dxprtbufferattachgh-method"></a><span data-ttu-id="fe313-103">ID3DXPRTBuffer：： AttachGH 方法</span><span class="sxs-lookup"><span data-stu-id="fe313-103">ID3DXPRTBuffer::AttachGH method</span></span>

<span data-ttu-id="fe313-104">將 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) 物件與 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件建立關聯。</span><span class="sxs-lookup"><span data-stu-id="fe313-104">Associates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe313-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe313-105">Syntax</span></span>


```C++
HRESULT AttachGH(
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a><span data-ttu-id="fe313-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe313-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe313-107">*pGH* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe313-107">*pGH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe313-108">類型： **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span><span class="sxs-lookup"><span data-stu-id="fe313-108">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span></span>

<span data-ttu-id="fe313-109">包含材質裝訂邊資料之物件的 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="fe313-109">Pointer to the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) interface of an object that contains texture gutter data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe313-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe313-110">Return value</span></span>

<span data-ttu-id="fe313-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe313-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe313-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="fe313-112">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe313-113">備註</span><span class="sxs-lookup"><span data-stu-id="fe313-113">Remarks</span></span>

<span data-ttu-id="fe313-114">[**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md)物件的參考計數會自動遞增1。</span><span class="sxs-lookup"><span data-stu-id="fe313-114">The reference count of the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object will automatically be incremented by one.</span></span> <span data-ttu-id="fe313-115">將會釋放任何現有的 **ID3DXTextureGutterHelper** 指標。</span><span class="sxs-lookup"><span data-stu-id="fe313-115">Any existing **ID3DXTextureGutterHelper** pointers will be released.</span></span>

<span data-ttu-id="fe313-116">您必須確保 **ID3DXPRTBuffer：： AttachGH** 呼叫的數目符合 [**ID3DXPRTBuffer：： ReleaseGH**](id3dxprtbuffer--releasegh.md) 呼叫的數目。</span><span class="sxs-lookup"><span data-stu-id="fe313-116">You must ensure that the number of **ID3DXPRTBuffer::AttachGH** calls matches the number of [**ID3DXPRTBuffer::ReleaseGH**](id3dxprtbuffer--releasegh.md) calls.</span></span> <span data-ttu-id="fe313-117">在呼叫 **ID3DXPRTBuffer：： ReleaseGH** 之後，不應該再使用 **ID3DXPRTBuffer：： AttachGH** 所傳回的 pGH 指標。</span><span class="sxs-lookup"><span data-stu-id="fe313-117">After calling **ID3DXPRTBuffer::ReleaseGH**, the pGH pointer returned by **ID3DXPRTBuffer::AttachGH** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe313-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe313-118">Requirements</span></span>



| <span data-ttu-id="fe313-119">需求</span><span class="sxs-lookup"><span data-stu-id="fe313-119">Requirement</span></span> | <span data-ttu-id="fe313-120">值</span><span class="sxs-lookup"><span data-stu-id="fe313-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe313-121">標頭</span><span class="sxs-lookup"><span data-stu-id="fe313-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fe313-122"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe313-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fe313-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="fe313-123">Library</span></span><br/> | <dl> <span data-ttu-id="fe313-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe313-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fe313-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe313-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe313-126">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="fe313-126">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="fe313-127">**ID3DXPRTBuffer::ReleaseGH**</span><span class="sxs-lookup"><span data-stu-id="fe313-127">**ID3DXPRTBuffer::ReleaseGH**</span></span>](id3dxprtbuffer--releasegh.md)
</dt> </dl>

 

 





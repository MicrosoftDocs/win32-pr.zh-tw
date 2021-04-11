---
description: 結束 ID3DXPRTBuffer：： LockBuffer 所傳回之 ppData 指標的存留期。
ms.assetid: 25464566-8a93-48a4-93fa-17828861f98c
title: 'ID3DXPRTBuffer：： UnlockBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.UnlockBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9a17d8f186fc1baf62dda3652372c4e73a5de141
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196336"
---
# <a name="id3dxprtbufferunlockbuffer-method"></a><span data-ttu-id="d52d9-103">ID3DXPRTBuffer：： UnlockBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="d52d9-103">ID3DXPRTBuffer::UnlockBuffer method</span></span>

<span data-ttu-id="d52d9-104">結束 [**ID3DXPRTBuffer：： LockBuffer**](id3dxprtbuffer--lockbuffer.md)所傳回之 ppData 指標的存留期。</span><span class="sxs-lookup"><span data-stu-id="d52d9-104">Ends the lifespan of the ppData pointer returned by [**ID3DXPRTBuffer::LockBuffer**](id3dxprtbuffer--lockbuffer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d52d9-105">語法</span><span class="sxs-lookup"><span data-stu-id="d52d9-105">Syntax</span></span>


```C++
HRESULT UnlockBuffer();
```



## <a name="parameters"></a><span data-ttu-id="d52d9-106">參數</span><span class="sxs-lookup"><span data-stu-id="d52d9-106">Parameters</span></span>

<span data-ttu-id="d52d9-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d52d9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d52d9-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d52d9-108">Return value</span></span>

<span data-ttu-id="d52d9-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d52d9-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d52d9-110">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="d52d9-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="d52d9-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="d52d9-111">Requirements</span></span>



| <span data-ttu-id="d52d9-112">需求</span><span class="sxs-lookup"><span data-stu-id="d52d9-112">Requirement</span></span> | <span data-ttu-id="d52d9-113">值</span><span class="sxs-lookup"><span data-stu-id="d52d9-113">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d52d9-114">標頭</span><span class="sxs-lookup"><span data-stu-id="d52d9-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d52d9-115"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="d52d9-115"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d52d9-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="d52d9-116">Library</span></span><br/> | <dl> <span data-ttu-id="d52d9-117"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d52d9-117"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d52d9-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d52d9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d52d9-119">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="d52d9-119">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 





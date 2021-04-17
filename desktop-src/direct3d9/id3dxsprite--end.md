---
description: 呼叫 ID3DXSprite：： Flush，然後將裝置狀態還原為 ID3DXSprite：： Begin 之前的狀態。
ms.assetid: 603c69f7-13a8-4646-b367-6f2d21b1a2a0
title: 'ID3DXSprite：： End 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2991cb8a4ae62b5d9ec71450d8e55fbdcdce050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386487"
---
# <a name="id3dxspriteend-method"></a><span data-ttu-id="adf53-103">ID3DXSprite：： End 方法</span><span class="sxs-lookup"><span data-stu-id="adf53-103">ID3DXSprite::End method</span></span>

<span data-ttu-id="adf53-104">呼叫 [**ID3DXSprite：： Flush**](id3dxsprite--flush.md) ，然後將裝置狀態還原為 [**ID3DXSprite：： Begin**](id3dxsprite--begin.md) 之前的狀態。</span><span class="sxs-lookup"><span data-stu-id="adf53-104">Calls [**ID3DXSprite::Flush**](id3dxsprite--flush.md) and restores the device state to how it was before [**ID3DXSprite::Begin**](id3dxsprite--begin.md) was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="adf53-105">語法</span><span class="sxs-lookup"><span data-stu-id="adf53-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="adf53-106">參數</span><span class="sxs-lookup"><span data-stu-id="adf53-106">Parameters</span></span>

<span data-ttu-id="adf53-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="adf53-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="adf53-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="adf53-108">Return value</span></span>

<span data-ttu-id="adf53-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="adf53-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="adf53-110">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="adf53-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="adf53-111">如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="adf53-111">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="adf53-112">備註</span><span class="sxs-lookup"><span data-stu-id="adf53-112">Remarks</span></span>

<span data-ttu-id="adf53-113">**ID3DXSprite：： End** 不能用來取代 [**IDirect3DDevice9：： EndScene**](/windows/desktop/api) 或 [**ID3DXRenderToSurface：： EndScene**](id3dxrendertosurface--endscene.md)。</span><span class="sxs-lookup"><span data-stu-id="adf53-113">**ID3DXSprite::End** cannot be used as a substitute for either [**IDirect3DDevice9::EndScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="adf53-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="adf53-114">Requirements</span></span>



| <span data-ttu-id="adf53-115">需求</span><span class="sxs-lookup"><span data-stu-id="adf53-115">Requirement</span></span> | <span data-ttu-id="adf53-116">值</span><span class="sxs-lookup"><span data-stu-id="adf53-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="adf53-117">標頭</span><span class="sxs-lookup"><span data-stu-id="adf53-117">Header</span></span><br/>  | <dl> <span data-ttu-id="adf53-118"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="adf53-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="adf53-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="adf53-119">Library</span></span><br/> | <dl> <span data-ttu-id="adf53-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="adf53-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="adf53-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adf53-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf53-122">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="adf53-122">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="adf53-123">**ID3DXSprite：： Begin**</span><span class="sxs-lookup"><span data-stu-id="adf53-123">**ID3DXSprite::Begin**</span></span>](id3dxsprite--begin.md)
</dt> </dl>

 

 





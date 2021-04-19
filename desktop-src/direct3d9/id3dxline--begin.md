---
description: 準備裝置來繪製線條。
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: 'ID3DXLine：： Begin 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ee241b39f2d0c1939cf2cb0cc09e079abd3430a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989221"
---
# <a name="id3dxlinebegin-method"></a><span data-ttu-id="d9915-103">ID3DXLine：： Begin 方法</span><span class="sxs-lookup"><span data-stu-id="d9915-103">ID3DXLine::Begin method</span></span>

<span data-ttu-id="d9915-104">準備裝置來繪製線條。</span><span class="sxs-lookup"><span data-stu-id="d9915-104">Prepares a device for drawing lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9915-105">語法</span><span class="sxs-lookup"><span data-stu-id="d9915-105">Syntax</span></span>


```C++
HRESULT Begin();
```



## <a name="parameters"></a><span data-ttu-id="d9915-106">參數</span><span class="sxs-lookup"><span data-stu-id="d9915-106">Parameters</span></span>

<span data-ttu-id="d9915-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d9915-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9915-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9915-108">Return value</span></span>

<span data-ttu-id="d9915-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d9915-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d9915-110">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="d9915-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d9915-111">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="d9915-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9915-112">備註</span><span class="sxs-lookup"><span data-stu-id="d9915-112">Remarks</span></span>

<span data-ttu-id="d9915-113">呼叫 **ID3DXLine：： Begin** 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="d9915-113">Calling **ID3DXLine::Begin** is optional.</span></span> <span data-ttu-id="d9915-114">如果在 ID3DXLine：： Begin/ID3DXLine：： End sequence 之外呼叫，draw 函數將會在內部呼叫 ID3DXLine：： Begin 和 ID3DXLine：： End。</span><span class="sxs-lookup"><span data-stu-id="d9915-114">If called outside of a ID3DXLine::Begin/ID3DXLine::End sequence, the draw functions will internally call ID3DXLine::Begin and ID3DXLine::End.</span></span> <span data-ttu-id="d9915-115">為了避免額外負荷，如果連續呼叫多個繪製函數，則應該使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="d9915-115">To avoid extra overhead, this method should be used if more than one draw function will be called successively.</span></span>

<span data-ttu-id="d9915-116">您必須從 [**IDirect3DDevice9：： BeginScene**](/windows/desktop/api) 和 [**IDirect3DDevice9：： EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) 序列內呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="d9915-116">This method must be called from inside an [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) and [**IDirect3DDevice9::EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) sequence.</span></span>

<span data-ttu-id="d9915-117">ID3DXLine：： Begin 不能用來取代 [**IDirect3DDevice9：： BeginScene**](/windows/desktop/api) 或 [**ID3DXRenderToSurface：： BeginScene**](id3dxrendertosurface--beginscene.md)。</span><span class="sxs-lookup"><span data-stu-id="d9915-117">ID3DXLine::Begin cannot be used as a substitute for either [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9915-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9915-118">Requirements</span></span>



| <span data-ttu-id="d9915-119">需求</span><span class="sxs-lookup"><span data-stu-id="d9915-119">Requirement</span></span> | <span data-ttu-id="d9915-120">值</span><span class="sxs-lookup"><span data-stu-id="d9915-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9915-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d9915-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d9915-122"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="d9915-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d9915-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="d9915-123">Library</span></span><br/> | <dl> <span data-ttu-id="d9915-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9915-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d9915-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9915-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9915-126">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="d9915-126">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 

---
description: 將裝置狀態還原為呼叫 ID3DXLine：： Begin 時的狀態。
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: 'ID3DXLine：： End 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69d8324ab54f37af3f45a5475f08894e278c32e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982235"
---
# <a name="id3dxlineend-method"></a><span data-ttu-id="6e979-103">ID3DXLine：： End 方法</span><span class="sxs-lookup"><span data-stu-id="6e979-103">ID3DXLine::End method</span></span>

<span data-ttu-id="6e979-104">將裝置狀態還原為呼叫 [**ID3DXLine：： Begin**](id3dxline--begin.md) 時的狀態。</span><span class="sxs-lookup"><span data-stu-id="6e979-104">Restores the device state to how it was when [**ID3DXLine::Begin**](id3dxline--begin.md) was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e979-105">語法</span><span class="sxs-lookup"><span data-stu-id="6e979-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="6e979-106">參數</span><span class="sxs-lookup"><span data-stu-id="6e979-106">Parameters</span></span>

<span data-ttu-id="6e979-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6e979-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e979-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e979-108">Return value</span></span>

<span data-ttu-id="6e979-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6e979-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6e979-110">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="6e979-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6e979-111">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="6e979-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e979-112">備註</span><span class="sxs-lookup"><span data-stu-id="6e979-112">Remarks</span></span>

<span data-ttu-id="6e979-113">**ID3DXLine：： End** 不能用來取代 [**IDirect3DDevice9：： EndScene**](/windows/desktop/api) 或 [**ID3DXRenderToSurface：： EndScene**](id3dxrendertosurface--endscene.md)。</span><span class="sxs-lookup"><span data-stu-id="6e979-113">**ID3DXLine::End** cannot be used as a substitute for either [**IDirect3DDevice9::EndScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e979-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e979-114">Requirements</span></span>



| <span data-ttu-id="6e979-115">需求</span><span class="sxs-lookup"><span data-stu-id="6e979-115">Requirement</span></span> | <span data-ttu-id="6e979-116">值</span><span class="sxs-lookup"><span data-stu-id="6e979-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e979-117">標頭</span><span class="sxs-lookup"><span data-stu-id="6e979-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6e979-118"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e979-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="6e979-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="6e979-119">Library</span></span><br/> | <dl> <span data-ttu-id="6e979-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e979-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6e979-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e979-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e979-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="6e979-122">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="6e979-123">**ID3DXLine：： Begin**</span><span class="sxs-lookup"><span data-stu-id="6e979-123">**ID3DXLine::Begin**</span></span>](id3dxline--begin.md)
</dt> </dl>

 

 





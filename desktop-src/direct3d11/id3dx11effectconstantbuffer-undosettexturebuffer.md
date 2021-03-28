---
title: 'ID3DX11EffectConstantBuffer UndoSetTextureBuffer 方法 (D3dx11effect .h) '
description: 還原先前設定的材質緩衝區。
ms.assetid: 982e7899-9569-4611-9fe0-b78624acba2c
keywords:
- UndoSetTextureBuffer 方法 Direct3D 11
- UndoSetTextureBuffer 方法 Direct3D 11，ID3DX11EffectConstantBuffer 介面
- ID3DX11EffectConstantBuffer 介面 Direct3D 11，UndoSetTextureBuffer 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.UndoSetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5e1e1b2be167466da5a4d92999646bb7c8f225
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323080"
---
# <a name="id3dx11effectconstantbufferundosettexturebuffer-method"></a><span data-ttu-id="0b6ac-106">ID3DX11EffectConstantBuffer：： UndoSetTextureBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="0b6ac-106">ID3DX11EffectConstantBuffer::UndoSetTextureBuffer method</span></span>

<span data-ttu-id="0b6ac-107">還原先前設定的材質緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0b6ac-107">Reverts a previously set texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b6ac-108">語法</span><span class="sxs-lookup"><span data-stu-id="0b6ac-108">Syntax</span></span>


```C++
HRESULT UndoSetTextureBuffer();
```



## <a name="parameters"></a><span data-ttu-id="0b6ac-109">參數</span><span class="sxs-lookup"><span data-stu-id="0b6ac-109">Parameters</span></span>

<span data-ttu-id="0b6ac-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0b6ac-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b6ac-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0b6ac-111">Return value</span></span>

<span data-ttu-id="0b6ac-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b6ac-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b6ac-113">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="0b6ac-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0b6ac-114">備註</span><span class="sxs-lookup"><span data-stu-id="0b6ac-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0b6ac-115">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="0b6ac-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0b6ac-116">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0b6ac-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0b6ac-117">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="0b6ac-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0b6ac-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b6ac-118">Requirements</span></span>



| <span data-ttu-id="0b6ac-119">需求</span><span class="sxs-lookup"><span data-stu-id="0b6ac-119">Requirement</span></span> | <span data-ttu-id="0b6ac-120">值</span><span class="sxs-lookup"><span data-stu-id="0b6ac-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6ac-121">標頭</span><span class="sxs-lookup"><span data-stu-id="0b6ac-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0b6ac-122"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="0b6ac-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0b6ac-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="0b6ac-123">Library</span></span><br/> | <dl> <span data-ttu-id="0b6ac-124"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="0b6ac-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b6ac-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b6ac-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b6ac-126">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="0b6ac-126">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 






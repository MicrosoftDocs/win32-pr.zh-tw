---
title: 'ID3DX11EffectConstantBuffer GetConstantBuffer 方法 (D3dx11effect .h) '
description: 取得常數緩衝區。
ms.assetid: 857b3dc2-41ae-4a52-904a-9ca8f0afeb9e
keywords:
- GetConstantBuffer 方法 Direct3D 11
- GetConstantBuffer 方法 Direct3D 11，ID3DX11EffectConstantBuffer 介面
- ID3DX11EffectConstantBuffer 介面 Direct3D 11，GetConstantBuffer 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.GetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041ca2fea028cb86d0959313bae73c320e6e5a36
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035437"
---
# <a name="id3dx11effectconstantbuffergetconstantbuffer-method"></a><span data-ttu-id="287a0-106">ID3DX11EffectConstantBuffer：： GetConstantBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="287a0-106">ID3DX11EffectConstantBuffer::GetConstantBuffer method</span></span>

<span data-ttu-id="287a0-107">取得常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="287a0-107">Get a constant-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="287a0-108">語法</span><span class="sxs-lookup"><span data-stu-id="287a0-108">Syntax</span></span>


```C++
HRESULT GetConstantBuffer(
   ID3D11Buffer **ppConstantBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="287a0-109">參數</span><span class="sxs-lookup"><span data-stu-id="287a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="287a0-110">*ppConstantBuffer*</span><span class="sxs-lookup"><span data-stu-id="287a0-110">*ppConstantBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="287a0-111">類型： **[ **ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="287a0-111">Type: **[**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\*\***</span></span>

<span data-ttu-id="287a0-112">常數緩衝區介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="287a0-112">The address of a pointer to a constant-buffer interface.</span></span> <span data-ttu-id="287a0-113">請參閱 [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)。</span><span class="sxs-lookup"><span data-stu-id="287a0-113">See [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="287a0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="287a0-114">Return value</span></span>

<span data-ttu-id="287a0-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="287a0-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="287a0-116">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="287a0-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="287a0-117">備註</span><span class="sxs-lookup"><span data-stu-id="287a0-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="287a0-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="287a0-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="287a0-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="287a0-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="287a0-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="287a0-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="287a0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="287a0-121">Requirements</span></span>



| <span data-ttu-id="287a0-122">需求</span><span class="sxs-lookup"><span data-stu-id="287a0-122">Requirement</span></span> | <span data-ttu-id="287a0-123">值</span><span class="sxs-lookup"><span data-stu-id="287a0-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="287a0-124">標頭</span><span class="sxs-lookup"><span data-stu-id="287a0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="287a0-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="287a0-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="287a0-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="287a0-126">Library</span></span><br/> | <dl> <span data-ttu-id="287a0-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="287a0-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="287a0-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="287a0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="287a0-129">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="287a0-129">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 






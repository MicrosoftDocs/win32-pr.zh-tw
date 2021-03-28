---
title: 'ID3DX11Effect GetConstantBufferByIndex 方法 (D3dx11effect .h) '
description: 依索引取得常數緩衝區。
ms.assetid: 146b146b-89ff-4d56-9ac7-e67a92a30e26
keywords:
- GetConstantBufferByIndex 方法 Direct3D 11
- GetConstantBufferByIndex 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetConstantBufferByIndex 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfbc44b2d9ceea1bcfbf854a8d3c6998d03e3eec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974660"
---
# <a name="id3dx11effectgetconstantbufferbyindex-method"></a><span data-ttu-id="db32b-106">ID3DX11Effect：： GetConstantBufferByIndex 方法</span><span class="sxs-lookup"><span data-stu-id="db32b-106">ID3DX11Effect::GetConstantBufferByIndex method</span></span>

<span data-ttu-id="db32b-107">依索引取得常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="db32b-107">Get a constant buffer by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="db32b-108">語法</span><span class="sxs-lookup"><span data-stu-id="db32b-108">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="db32b-109">參數</span><span class="sxs-lookup"><span data-stu-id="db32b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db32b-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="db32b-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="db32b-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="db32b-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="db32b-112">以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="db32b-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db32b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="db32b-113">Return value</span></span>

<span data-ttu-id="db32b-114">類型： **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="db32b-114">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="db32b-115">指向 [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="db32b-115">A pointer to a [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="db32b-116">備註</span><span class="sxs-lookup"><span data-stu-id="db32b-116">Remarks</span></span>

<span data-ttu-id="db32b-117">包含將由應用程式讀取/寫入之變數的效果，必須至少有一個常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="db32b-117">An effect that contains a variable that will be read/written by an application requires at least one constant buffer.</span></span> <span data-ttu-id="db32b-118">為了達到最佳效能，效果應該根據更新的頻率，將變數組織成一或多個常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="db32b-118">For best performance, an effect should organize variables into one or more constant buffers based on their frequency of update.</span></span>

> [!Note]  
> <span data-ttu-id="db32b-119">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="db32b-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="db32b-120">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="db32b-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="db32b-121">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="db32b-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="db32b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="db32b-122">Requirements</span></span>



| <span data-ttu-id="db32b-123">需求</span><span class="sxs-lookup"><span data-stu-id="db32b-123">Requirement</span></span> | <span data-ttu-id="db32b-124">值</span><span class="sxs-lookup"><span data-stu-id="db32b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db32b-125">標頭</span><span class="sxs-lookup"><span data-stu-id="db32b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="db32b-126"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="db32b-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="db32b-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="db32b-127">Library</span></span><br/> | <dl> <span data-ttu-id="db32b-128"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="db32b-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db32b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db32b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db32b-130">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="db32b-130">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 


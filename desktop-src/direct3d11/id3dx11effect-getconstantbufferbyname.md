---
title: 'ID3DX11Effect GetConstantBufferByName 方法 (D3dx11effect .h) '
description: 依名稱取得常數緩衝區。
ms.assetid: 11757615-4068-430d-9ab0-f83f02af8e55
keywords:
- GetConstantBufferByName 方法 Direct3D 11
- GetConstantBufferByName 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetConstantBufferByName 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa01d20bfeebfa3f689a58aae5c5face8b879e3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854056"
---
# <a name="id3dx11effectgetconstantbufferbyname-method"></a><span data-ttu-id="ebcd2-106">ID3DX11Effect：： GetConstantBufferByName 方法</span><span class="sxs-lookup"><span data-stu-id="ebcd2-106">ID3DX11Effect::GetConstantBufferByName method</span></span>

<span data-ttu-id="ebcd2-107">依名稱取得常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ebcd2-107">Get a constant buffer by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebcd2-108">語法</span><span class="sxs-lookup"><span data-stu-id="ebcd2-108">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="ebcd2-109">參數</span><span class="sxs-lookup"><span data-stu-id="ebcd2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebcd2-110">*名稱*</span><span class="sxs-lookup"><span data-stu-id="ebcd2-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="ebcd2-111">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ebcd2-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ebcd2-112">常數緩衝區名稱。</span><span class="sxs-lookup"><span data-stu-id="ebcd2-112">The constant-buffer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebcd2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ebcd2-113">Return value</span></span>

<span data-ttu-id="ebcd2-114">類型： **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ebcd2-114">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="ebcd2-115">名稱所表示之常數緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="ebcd2-115">A pointer to the constant buffer indicated by the Name.</span></span> <span data-ttu-id="ebcd2-116">請參閱 [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="ebcd2-116">See [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ebcd2-117">備註</span><span class="sxs-lookup"><span data-stu-id="ebcd2-117">Remarks</span></span>

<span data-ttu-id="ebcd2-118">包含將由應用程式讀取/寫入之變數的效果，必須至少有一個常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ebcd2-118">An effect that contains a variable that will be read/written by an application requires at least one constant buffer.</span></span> <span data-ttu-id="ebcd2-119">為了達到最佳效能，效果應該根據更新的頻率，將變數組織成一或多個常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ebcd2-119">For best performance, an effect should organize variables into one or more constant buffers based on their frequency of update.</span></span>

> [!Note]  
> <span data-ttu-id="ebcd2-120">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="ebcd2-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ebcd2-121">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ebcd2-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ebcd2-122">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="ebcd2-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ebcd2-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebcd2-123">Requirements</span></span>



| <span data-ttu-id="ebcd2-124">需求</span><span class="sxs-lookup"><span data-stu-id="ebcd2-124">Requirement</span></span> | <span data-ttu-id="ebcd2-125">值</span><span class="sxs-lookup"><span data-stu-id="ebcd2-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebcd2-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ebcd2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ebcd2-127"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="ebcd2-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ebcd2-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="ebcd2-128">Library</span></span><br/> | <dl> <span data-ttu-id="ebcd2-129"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="ebcd2-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebcd2-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebcd2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebcd2-131">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="ebcd2-131">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 


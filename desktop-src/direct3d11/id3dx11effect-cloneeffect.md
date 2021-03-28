---
title: 'ID3DX11Effect CloneEffect 方法 (D3dx11effect .h) '
description: 建立效果介面的複本。
ms.assetid: 98cc8e25-38c5-4b87-99eb-39d2edd9053c
keywords:
- CloneEffect 方法 Direct3D 11
- CloneEffect 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，CloneEffect 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.CloneEffect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dc7e47d1c50d0e41c29c90102afaaebdce8dda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974721"
---
# <a name="id3dx11effectcloneeffect-method"></a><span data-ttu-id="a119c-106">ID3DX11Effect：： CloneEffect 方法</span><span class="sxs-lookup"><span data-stu-id="a119c-106">ID3DX11Effect::CloneEffect method</span></span>

<span data-ttu-id="a119c-107">建立效果介面的複本。</span><span class="sxs-lookup"><span data-stu-id="a119c-107">Creates a copy of an effect interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a119c-108">語法</span><span class="sxs-lookup"><span data-stu-id="a119c-108">Syntax</span></span>


```C++
HRESULT CloneEffect(
   UINT          Flags,
   ID3DX11Effect **ppClonedEffect
);
```



## <a name="parameters"></a><span data-ttu-id="a119c-109">參數</span><span class="sxs-lookup"><span data-stu-id="a119c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a119c-110">*旗標*</span><span class="sxs-lookup"><span data-stu-id="a119c-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="a119c-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a119c-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a119c-112">影響建立複製效果的旗標。</span><span class="sxs-lookup"><span data-stu-id="a119c-112">Flags affecting the creation of the cloned effect.</span></span> <span data-ttu-id="a119c-113">可以是0或下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a119c-113">Can be 0 or one of the following values.</span></span>



| <span data-ttu-id="a119c-114">旗標</span><span class="sxs-lookup"><span data-stu-id="a119c-114">Flag</span></span>                                    | <span data-ttu-id="a119c-115">描述</span><span class="sxs-lookup"><span data-stu-id="a119c-115">Description</span></span>                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a119c-116">D3DX11 \_ 效果 \_ 複製 \_ 強制 \_ NONSINGLE</span><span class="sxs-lookup"><span data-stu-id="a119c-116">D3DX11\_EFFECT\_CLONE\_FORCE\_NONSINGLE</span></span> | <span data-ttu-id="a119c-117">忽略 cbuffers 上的所有 "single" 限定詞。</span><span class="sxs-lookup"><span data-stu-id="a119c-117">Ignore all "single" qualifiers on cbuffers.</span></span> <span data-ttu-id="a119c-118">所有 cbuffers 都將會在複製的效果中建立自己的 [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)。</span><span class="sxs-lookup"><span data-stu-id="a119c-118">All cbuffers will have their own [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)s created in the cloned effect.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a119c-119">*ppClonedEffect*</span><span class="sxs-lookup"><span data-stu-id="a119c-119">*ppClonedEffect*</span></span> 
</dt> <dd>

<span data-ttu-id="a119c-120">類型： **[ **ID3DX11Effect**](id3dx11effect.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a119c-120">Type: **[**ID3DX11Effect**](id3dx11effect.md)\*\***</span></span>

<span data-ttu-id="a119c-121">將設定為效果複本之 [**ID3DX11Effect**](id3dx11effect.md) 指標的指標。</span><span class="sxs-lookup"><span data-stu-id="a119c-121">Pointer to an [**ID3DX11Effect**](id3dx11effect.md) pointer that will be set to the copy of the effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a119c-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="a119c-122">Return value</span></span>

<span data-ttu-id="a119c-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a119c-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a119c-124">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="a119c-124">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a119c-125">備註</span><span class="sxs-lookup"><span data-stu-id="a119c-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a119c-126">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="a119c-126">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a119c-127">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a119c-127">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a119c-128">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="a119c-128">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a119c-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="a119c-129">Requirements</span></span>



| <span data-ttu-id="a119c-130">需求</span><span class="sxs-lookup"><span data-stu-id="a119c-130">Requirement</span></span> | <span data-ttu-id="a119c-131">值</span><span class="sxs-lookup"><span data-stu-id="a119c-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a119c-132">標頭</span><span class="sxs-lookup"><span data-stu-id="a119c-132">Header</span></span><br/>  | <dl> <span data-ttu-id="a119c-133"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="a119c-133"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a119c-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="a119c-134">Library</span></span><br/> | <dl> <span data-ttu-id="a119c-135"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="a119c-135"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a119c-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a119c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a119c-137">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="a119c-137">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 


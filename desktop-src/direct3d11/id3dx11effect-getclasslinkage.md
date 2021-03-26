---
title: 'ID3DX11Effect GetClassLinkage 方法 (D3dx11effect .h) '
description: 取得類別連結介面。
ms.assetid: 006c900d-3464-4666-9fe9-d62ba8cb2b7f
keywords:
- GetClassLinkage 方法 Direct3D 11
- GetClassLinkage 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetClassLinkage 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetClassLinkage
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b19f14794186f85d0a51f21bc6b2759e512998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946067"
---
# <a name="id3dx11effectgetclasslinkage-method"></a><span data-ttu-id="1e5b4-106">ID3DX11Effect：： GetClassLinkage 方法</span><span class="sxs-lookup"><span data-stu-id="1e5b4-106">ID3DX11Effect::GetClassLinkage method</span></span>

<span data-ttu-id="1e5b4-107">取得類別連結介面。</span><span class="sxs-lookup"><span data-stu-id="1e5b4-107">Gets a class linkage interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e5b4-108">語法</span><span class="sxs-lookup"><span data-stu-id="1e5b4-108">Syntax</span></span>


```C++
ID3D11ClassLinkage* GetClassLinkage();
```



## <a name="parameters"></a><span data-ttu-id="1e5b4-109">參數</span><span class="sxs-lookup"><span data-stu-id="1e5b4-109">Parameters</span></span>

<span data-ttu-id="1e5b4-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1e5b4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e5b4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e5b4-111">Return value</span></span>

<span data-ttu-id="1e5b4-112">類型： **[ **ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)\***</span><span class="sxs-lookup"><span data-stu-id="1e5b4-112">Type: **[**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)\***</span></span>

<span data-ttu-id="1e5b4-113">傳回 [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1e5b4-113">Returns a pointer to an [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e5b4-114">備註</span><span class="sxs-lookup"><span data-stu-id="1e5b4-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1e5b4-115">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="1e5b4-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1e5b4-116">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1e5b4-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1e5b4-117">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="1e5b4-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1e5b4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e5b4-118">Requirements</span></span>



| <span data-ttu-id="1e5b4-119">需求</span><span class="sxs-lookup"><span data-stu-id="1e5b4-119">Requirement</span></span> | <span data-ttu-id="1e5b4-120">值</span><span class="sxs-lookup"><span data-stu-id="1e5b4-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e5b4-121">標頭</span><span class="sxs-lookup"><span data-stu-id="1e5b4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1e5b4-122"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="1e5b4-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1e5b4-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="1e5b4-123">Library</span></span><br/> | <dl> <span data-ttu-id="1e5b4-124"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="1e5b4-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e5b4-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e5b4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e5b4-126">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="1e5b4-126">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 






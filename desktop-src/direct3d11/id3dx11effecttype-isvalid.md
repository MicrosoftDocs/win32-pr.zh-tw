---
title: 'ID3DX11EffectType IsValid 方法 (D3dx11effect .h) '
description: 測試效果類型是否有效。
ms.assetid: 3c1d93a0-92a1-4969-a561-5156e2cd2f3b
keywords:
- IsValid 方法 Direct3D 11
- IsValid 方法 Direct3D 11、ID3DX11EffectType 介面
- ID3DX11EffectType 介面 Direct3D 11，IsValid 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectType.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9254513622ff7c0705c01b0ee15262126c096ede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696600"
---
# <a name="id3dx11effecttypeisvalid-method"></a><span data-ttu-id="74cd4-106">ID3DX11EffectType：： IsValid 方法</span><span class="sxs-lookup"><span data-stu-id="74cd4-106">ID3DX11EffectType::IsValid method</span></span>

<span data-ttu-id="74cd4-107">測試效果類型是否有效。</span><span class="sxs-lookup"><span data-stu-id="74cd4-107">Tests that the effect type is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="74cd4-108">語法</span><span class="sxs-lookup"><span data-stu-id="74cd4-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="74cd4-109">參數</span><span class="sxs-lookup"><span data-stu-id="74cd4-109">Parameters</span></span>

<span data-ttu-id="74cd4-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="74cd4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="74cd4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="74cd4-111">Return value</span></span>

<span data-ttu-id="74cd4-112">類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="74cd4-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="74cd4-113">如果有效，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="74cd4-113">**TRUE** if it is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="74cd4-114">備註</span><span class="sxs-lookup"><span data-stu-id="74cd4-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="74cd4-115">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="74cd4-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="74cd4-116">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="74cd4-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="74cd4-117">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="74cd4-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="74cd4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="74cd4-118">Requirements</span></span>



| <span data-ttu-id="74cd4-119">需求</span><span class="sxs-lookup"><span data-stu-id="74cd4-119">Requirement</span></span> | <span data-ttu-id="74cd4-120">值</span><span class="sxs-lookup"><span data-stu-id="74cd4-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74cd4-121">標頭</span><span class="sxs-lookup"><span data-stu-id="74cd4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="74cd4-122"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="74cd4-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="74cd4-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="74cd4-123">Library</span></span><br/> | <dl> <span data-ttu-id="74cd4-124"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="74cd4-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74cd4-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74cd4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74cd4-126">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="74cd4-126">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 


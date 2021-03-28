---
title: 'ID3DX11EffectType GetMemberTypeByName 方法 (D3dx11effect .h) '
description: 依名稱取得成員類型。
ms.assetid: 0c5a732b-7c3a-41da-b7de-dc464eed814a
keywords:
- GetMemberTypeByName 方法 Direct3D 11
- GetMemberTypeByName 方法 Direct3D 11，ID3DX11EffectType 介面
- ID3DX11EffectType 介面 Direct3D 11，GetMemberTypeByName 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e573bcdc2dc4470e87539a307cdc38b71a6320ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992174"
---
# <a name="id3dx11effecttypegetmembertypebyname-method"></a><span data-ttu-id="54c9d-106">ID3DX11EffectType：： GetMemberTypeByName 方法</span><span class="sxs-lookup"><span data-stu-id="54c9d-106">ID3DX11EffectType::GetMemberTypeByName method</span></span>

<span data-ttu-id="54c9d-107">依名稱取得成員類型。</span><span class="sxs-lookup"><span data-stu-id="54c9d-107">Get an member type by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="54c9d-108">語法</span><span class="sxs-lookup"><span data-stu-id="54c9d-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="54c9d-109">參數</span><span class="sxs-lookup"><span data-stu-id="54c9d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54c9d-110">*名稱*</span><span class="sxs-lookup"><span data-stu-id="54c9d-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="54c9d-111">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="54c9d-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="54c9d-112">成員的名稱。</span><span class="sxs-lookup"><span data-stu-id="54c9d-112">A member's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54c9d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="54c9d-113">Return value</span></span>

<span data-ttu-id="54c9d-114">類型： **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="54c9d-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="54c9d-115">[**ID3DX11EffectType**](id3dx11effecttype.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="54c9d-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="54c9d-116">備註</span><span class="sxs-lookup"><span data-stu-id="54c9d-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="54c9d-117">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="54c9d-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="54c9d-118">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="54c9d-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="54c9d-119">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="54c9d-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="54c9d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="54c9d-120">Requirements</span></span>



| <span data-ttu-id="54c9d-121">需求</span><span class="sxs-lookup"><span data-stu-id="54c9d-121">Requirement</span></span> | <span data-ttu-id="54c9d-122">值</span><span class="sxs-lookup"><span data-stu-id="54c9d-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54c9d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="54c9d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="54c9d-124"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="54c9d-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="54c9d-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="54c9d-125">Library</span></span><br/> | <dl> <span data-ttu-id="54c9d-126"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="54c9d-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54c9d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54c9d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54c9d-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="54c9d-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 


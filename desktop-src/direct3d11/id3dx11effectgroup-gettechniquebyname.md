---
title: 'ID3DX11EffectGroup GetTechniqueByName 方法 (D3dx11effect .h) '
description: '依名稱取得技術。 |ID3DX11EffectGroup GetTechniqueByName 方法 (D3dx11effect .h) '
ms.assetid: 160c6d57-bec4-4718-8fad-fc9c0746736c
keywords:
- GetTechniqueByName 方法 Direct3D 11
- GetTechniqueByName 方法 Direct3D 11，ID3DX11EffectGroup 介面
- ID3DX11EffectGroup 介面 Direct3D 11，GetTechniqueByName 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5121f67345ba863d773d8e7a73a5d6fa8b69895
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974572"
---
# <a name="id3dx11effectgroupgettechniquebyname-method"></a><span data-ttu-id="8864b-107">ID3DX11EffectGroup：： GetTechniqueByName 方法</span><span class="sxs-lookup"><span data-stu-id="8864b-107">ID3DX11EffectGroup::GetTechniqueByName method</span></span>

<span data-ttu-id="8864b-108">依名稱取得技術。</span><span class="sxs-lookup"><span data-stu-id="8864b-108">Get a technique by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="8864b-109">語法</span><span class="sxs-lookup"><span data-stu-id="8864b-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="8864b-110">參數</span><span class="sxs-lookup"><span data-stu-id="8864b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8864b-111">*名稱*</span><span class="sxs-lookup"><span data-stu-id="8864b-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="8864b-112">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8864b-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8864b-113">技術的名稱。</span><span class="sxs-lookup"><span data-stu-id="8864b-113">The name of the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8864b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="8864b-114">Return value</span></span>

<span data-ttu-id="8864b-115">類型： **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="8864b-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="8864b-116">指向 [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)的指標，如果找不到該技術，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="8864b-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md), or **NULL** if the technique is not found.</span></span>

## <a name="remarks"></a><span data-ttu-id="8864b-117">備註</span><span class="sxs-lookup"><span data-stu-id="8864b-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8864b-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="8864b-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8864b-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8864b-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8864b-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="8864b-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8864b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8864b-121">Requirements</span></span>



| <span data-ttu-id="8864b-122">需求</span><span class="sxs-lookup"><span data-stu-id="8864b-122">Requirement</span></span> | <span data-ttu-id="8864b-123">值</span><span class="sxs-lookup"><span data-stu-id="8864b-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8864b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8864b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8864b-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="8864b-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8864b-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="8864b-126">Library</span></span><br/> | <dl> <span data-ttu-id="8864b-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="8864b-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8864b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8864b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8864b-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="8864b-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 


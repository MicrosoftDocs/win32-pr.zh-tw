---
title: 'ID3DX11EffectVariable GetMemberByName 方法 (D3dx11effect .h) '
description: 依名稱取得結構成員。
ms.assetid: 09f7f2f8-f55f-411c-8130-6ae44015d58a
keywords:
- GetMemberByName 方法 Direct3D 11
- GetMemberByName 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，GetMemberByName 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9851a2f74502a79b5cc85c494e468c4a346798f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992385"
---
# <a name="id3dx11effectvariablegetmemberbyname-method"></a><span data-ttu-id="2fc06-106">ID3DX11EffectVariable：： GetMemberByName 方法</span><span class="sxs-lookup"><span data-stu-id="2fc06-106">ID3DX11EffectVariable::GetMemberByName method</span></span>

<span data-ttu-id="2fc06-107">依名稱取得結構成員。</span><span class="sxs-lookup"><span data-stu-id="2fc06-107">Get a structure member by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fc06-108">語法</span><span class="sxs-lookup"><span data-stu-id="2fc06-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetMemberByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="2fc06-109">參數</span><span class="sxs-lookup"><span data-stu-id="2fc06-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fc06-110">*名稱*</span><span class="sxs-lookup"><span data-stu-id="2fc06-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="2fc06-111">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2fc06-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2fc06-112">成員名稱。</span><span class="sxs-lookup"><span data-stu-id="2fc06-112">Member name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fc06-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2fc06-113">Return value</span></span>

<span data-ttu-id="2fc06-114">類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="2fc06-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="2fc06-115">[**ID3DX11EffectVariable**](id3dx11effectvariable.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="2fc06-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2fc06-116">備註</span><span class="sxs-lookup"><span data-stu-id="2fc06-116">Remarks</span></span>

<span data-ttu-id="2fc06-117">如果效果變數是結構，請使用這個方法來依名稱查詢成員。</span><span class="sxs-lookup"><span data-stu-id="2fc06-117">If the effect variable is an structure, use this method to look up a member by name.</span></span>

> [!Note]  
> <span data-ttu-id="2fc06-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="2fc06-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2fc06-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="2fc06-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2fc06-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="2fc06-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2fc06-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fc06-121">Requirements</span></span>



| <span data-ttu-id="2fc06-122">需求</span><span class="sxs-lookup"><span data-stu-id="2fc06-122">Requirement</span></span> | <span data-ttu-id="2fc06-123">值</span><span class="sxs-lookup"><span data-stu-id="2fc06-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fc06-124">標頭</span><span class="sxs-lookup"><span data-stu-id="2fc06-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2fc06-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="2fc06-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2fc06-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="2fc06-126">Library</span></span><br/> | <dl> <span data-ttu-id="2fc06-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="2fc06-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fc06-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fc06-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fc06-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="2fc06-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 


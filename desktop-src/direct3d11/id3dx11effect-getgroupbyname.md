---
title: 'ID3DX11Effect GetGroupByName 方法 (D3dx11effect .h) '
description: 依名稱取得效果群組。
ms.assetid: 14b4b484-848a-409c-9a99-207ab25b7566
keywords:
- GetGroupByName 方法 Direct3D 11
- GetGroupByName 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetGroupByName 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1c2132dedb34fe71db30bf82b1c6d336f110a8f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992344"
---
# <a name="id3dx11effectgetgroupbyname-method"></a><span data-ttu-id="bf7bb-106">ID3DX11Effect：： GetGroupByName 方法</span><span class="sxs-lookup"><span data-stu-id="bf7bb-106">ID3DX11Effect::GetGroupByName method</span></span>

<span data-ttu-id="bf7bb-107">依名稱取得效果群組。</span><span class="sxs-lookup"><span data-stu-id="bf7bb-107">Gets an effect group by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf7bb-108">語法</span><span class="sxs-lookup"><span data-stu-id="bf7bb-108">Syntax</span></span>


```C++
ID3DX11EffectGroup* GetGroupByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="bf7bb-109">參數</span><span class="sxs-lookup"><span data-stu-id="bf7bb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf7bb-110">*名稱*</span><span class="sxs-lookup"><span data-stu-id="bf7bb-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="bf7bb-111">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bf7bb-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bf7bb-112">效果群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf7bb-112">Name of the effect group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf7bb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf7bb-113">Return value</span></span>

<span data-ttu-id="bf7bb-114">類型： **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf7bb-114">Type: **[**ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span></span>

<span data-ttu-id="bf7bb-115">[**ID3DX11EffectGroup**](id3dx11effectgroup.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="bf7bb-115">A pointer to an [**ID3DX11EffectGroup**](id3dx11effectgroup.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf7bb-116">備註</span><span class="sxs-lookup"><span data-stu-id="bf7bb-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bf7bb-117">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="bf7bb-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bf7bb-118">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="bf7bb-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bf7bb-119">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="bf7bb-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bf7bb-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf7bb-120">Requirements</span></span>



| <span data-ttu-id="bf7bb-121">需求</span><span class="sxs-lookup"><span data-stu-id="bf7bb-121">Requirement</span></span> | <span data-ttu-id="bf7bb-122">值</span><span class="sxs-lookup"><span data-stu-id="bf7bb-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf7bb-123">標頭</span><span class="sxs-lookup"><span data-stu-id="bf7bb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="bf7bb-124"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="bf7bb-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bf7bb-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="bf7bb-125">Library</span></span><br/> | <dl> <span data-ttu-id="bf7bb-126"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="bf7bb-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf7bb-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf7bb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf7bb-128">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="bf7bb-128">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 


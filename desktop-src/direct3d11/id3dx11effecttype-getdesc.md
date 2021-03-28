---
title: 'ID3DX11EffectType GetDesc 方法 (D3dx11effect .h) '
description: 取得效果類型描述。
ms.assetid: 08a8a1b6-fe2d-431b-a0e4-d628f0ceb1a0
keywords:
- GetDesc 方法 Direct3D 11
- GetDesc 方法 Direct3D 11，ID3DX11EffectType 介面
- ID3DX11EffectType 介面 Direct3D 11，GetDesc 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1ee52e4c6628c00b0155e5bd3081b6c4fd8c46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992375"
---
# <a name="id3dx11effecttypegetdesc-method"></a><span data-ttu-id="d36df-106">ID3DX11EffectType：： GetDesc 方法</span><span class="sxs-lookup"><span data-stu-id="d36df-106">ID3DX11EffectType::GetDesc method</span></span>

<span data-ttu-id="d36df-107">取得效果類型描述。</span><span class="sxs-lookup"><span data-stu-id="d36df-107">Get an effect-type description.</span></span>

## <a name="syntax"></a><span data-ttu-id="d36df-108">語法</span><span class="sxs-lookup"><span data-stu-id="d36df-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_TYPE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="d36df-109">參數</span><span class="sxs-lookup"><span data-stu-id="d36df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d36df-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="d36df-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="d36df-111">類型： **[ **D3DX11 \_ 效果 \_ 類型 \_ DESC**](d3dx11-effect-type-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="d36df-111">Type: **[**D3DX11\_EFFECT\_TYPE\_DESC**](d3dx11-effect-type-desc.md)\***</span></span>

<span data-ttu-id="d36df-112">效果類型描述的指標。</span><span class="sxs-lookup"><span data-stu-id="d36df-112">A pointer to an effect-type description.</span></span> <span data-ttu-id="d36df-113">請參閱 [**D3DX11 \_ 效果 \_ 類型 \_ DESC**](d3dx11-effect-type-desc.md)。</span><span class="sxs-lookup"><span data-stu-id="d36df-113">See [**D3DX11\_EFFECT\_TYPE\_DESC**](d3dx11-effect-type-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d36df-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d36df-114">Return value</span></span>

<span data-ttu-id="d36df-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d36df-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d36df-116">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="d36df-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d36df-117">備註</span><span class="sxs-lookup"><span data-stu-id="d36df-117">Remarks</span></span>

<span data-ttu-id="d36df-118">效果變數描述包含效果類型的名稱、注釋、語義、旗標和緩衝區位移的相關資料。</span><span class="sxs-lookup"><span data-stu-id="d36df-118">The effect-variable description contains data about the name, annotations, semantic, flags and buffer offset of the effect type.</span></span>

> [!Note]  
> <span data-ttu-id="d36df-119">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="d36df-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d36df-120">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d36df-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d36df-121">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="d36df-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d36df-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d36df-122">Requirements</span></span>



| <span data-ttu-id="d36df-123">需求</span><span class="sxs-lookup"><span data-stu-id="d36df-123">Requirement</span></span> | <span data-ttu-id="d36df-124">值</span><span class="sxs-lookup"><span data-stu-id="d36df-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d36df-125">標頭</span><span class="sxs-lookup"><span data-stu-id="d36df-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d36df-126"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="d36df-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d36df-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="d36df-127">Library</span></span><br/> | <dl> <span data-ttu-id="d36df-128"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="d36df-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d36df-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d36df-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d36df-130">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="d36df-130">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

 






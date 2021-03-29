---
title: 'ID3DX11EffectTechnique GetDesc 方法 (D3dx11effect .h) '
description: 取得技術描述。
ms.assetid: ed82d873-0540-4aa8-ac0f-198852b886ad
keywords:
- GetDesc 方法 Direct3D 11
- GetDesc 方法 Direct3D 11，ID3DX11EffectTechnique 介面
- ID3DX11EffectTechnique 介面 Direct3D 11，GetDesc 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b847bd8381ec7d190931c04e5940f713676ff0b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992166"
---
# <a name="id3dx11effecttechniquegetdesc-method"></a><span data-ttu-id="05d25-106">ID3DX11EffectTechnique：： GetDesc 方法</span><span class="sxs-lookup"><span data-stu-id="05d25-106">ID3DX11EffectTechnique::GetDesc method</span></span>

<span data-ttu-id="05d25-107">取得技術描述。</span><span class="sxs-lookup"><span data-stu-id="05d25-107">Get a technique description.</span></span>

## <a name="syntax"></a><span data-ttu-id="05d25-108">語法</span><span class="sxs-lookup"><span data-stu-id="05d25-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_TECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="05d25-109">參數</span><span class="sxs-lookup"><span data-stu-id="05d25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05d25-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="05d25-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="05d25-111">類型： **[ **D3DX11 \_ 技術 \_ DESC**](d3dx11-technique-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="05d25-111">Type: **[**D3DX11\_TECHNIQUE\_DESC**](d3dx11-technique-desc.md)\***</span></span>

<span data-ttu-id="05d25-112">技術描述的指標 (參閱 [**D3DX11 \_ 技術 \_ DESC**](d3dx11-technique-desc.md)) 。</span><span class="sxs-lookup"><span data-stu-id="05d25-112">A pointer to a technique description (see [**D3DX11\_TECHNIQUE\_DESC**](d3dx11-technique-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05d25-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="05d25-113">Return value</span></span>

<span data-ttu-id="05d25-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="05d25-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="05d25-115">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="05d25-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="05d25-116">備註</span><span class="sxs-lookup"><span data-stu-id="05d25-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="05d25-117">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="05d25-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="05d25-118">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="05d25-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="05d25-119">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="05d25-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="05d25-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="05d25-120">Requirements</span></span>



| <span data-ttu-id="05d25-121">需求</span><span class="sxs-lookup"><span data-stu-id="05d25-121">Requirement</span></span> | <span data-ttu-id="05d25-122">值</span><span class="sxs-lookup"><span data-stu-id="05d25-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05d25-123">標頭</span><span class="sxs-lookup"><span data-stu-id="05d25-123">Header</span></span><br/>  | <dl> <span data-ttu-id="05d25-124"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="05d25-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="05d25-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="05d25-125">Library</span></span><br/> | <dl> <span data-ttu-id="05d25-126"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="05d25-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05d25-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05d25-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05d25-128">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="05d25-128">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

 






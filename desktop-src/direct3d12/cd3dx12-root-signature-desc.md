---
title: 'CD3DX12_ROOT_SIGNATURE_DESC 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 根簽章 \_ \_ \_ DESC 結構。
ms.assetid: A3B820C1-51E8-4E35-A67F-2C4BE82A6B7F
keywords:
- CD3DX12_ROOT_SIGNATURE_DESC 結構
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f89f9cd0f5ad9be08af1fa9c2556ebfbd4fcff1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992538"
---
# <a name="cd3dx12_root_signature_desc-structure"></a><span data-ttu-id="597d1-104">CD3DX12 \_ 根簽章 \_ \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="597d1-104">CD3DX12\_ROOT\_SIGNATURE\_DESC structure</span></span>

<span data-ttu-id="597d1-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 根簽章 \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) 結構。</span><span class="sxs-lookup"><span data-stu-id="597d1-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="597d1-106">語法</span><span class="sxs-lookup"><span data-stu-id="597d1-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_SIGNATURE_DESC  : public D3D12_ROOT_SIGNATURE_DESC{
       CD3DX12_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       CD3DX12_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init(D3D12_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="597d1-107">成員</span><span class="sxs-lookup"><span data-stu-id="597d1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="597d1-108">**CD3DX12 \_ 根簽章 \_ \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="597d1-108">**CD3DX12\_ROOT\_SIGNATURE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="597d1-109">建立 CD3DX12 根簽章 DESC 的新、未初始化的實例 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="597d1-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="597d1-110">**明確 CD3DX12 的根簽章 \_ \_ \_ DESC (const D3D12 \_ root \_ signature \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="597d1-110">**explicit CD3DX12\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="597d1-111">建立 CD3DX12 根簽章 desc 的新實例 \_ \_ \_ ，並使用另一個 [**D3D12 根簽章 \_ \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="597d1-111">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initialized with the contents of another [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="597d1-112">**CD3DX12 \_ 根簽章 \_ \_ DESC (UINT NUMPARAMETERS、const D3D12 \_ 根 \_ 參數 \* \_ pParameters、UINT numStaticSamplers = 0、const D3D12 \_ 靜態取樣器 \_ \_ DESC \* \_ pStaticSamplers = Null、D3D12 根簽章 \_ \_ \_ 旗標旗標 = D3D12 根簽章旗標 \_ \_ \_ \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="597d1-112">**CD3DX12\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="597d1-113">建立 CD3DX12 根簽章 DESC 的新實例 \_ \_ ，並 \_ 初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="597d1-113">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="597d1-114">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="597d1-114">UINT numParameters</span></span>

<span data-ttu-id="597d1-115">[**D3D12 \_根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="597d1-115">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="597d1-116"> (opt) UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="597d1-116">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="597d1-117"> (opt) [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null</span><span class="sxs-lookup"><span data-stu-id="597d1-117">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="597d1-118"> (opt) [**D3D12 \_ 根 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 簽章旗標旗標 = D3D12 根簽章旗標 \_ \_ \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="597d1-118">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="597d1-119">**CD3DX12 \_ 根目錄 \_ 簽名 \_ DESC (CD3DX12 \_ 預設)**</span><span class="sxs-lookup"><span data-stu-id="597d1-119">**CD3DX12\_ROOT\_SIGNATURE\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="597d1-120">建立 CD3DX12 根簽章 DESC 的新實例 \_ \_ \_ ，並以預設參數初始化。</span><span class="sxs-lookup"><span data-stu-id="597d1-120">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initialized with default parameters.</span></span>

``` syntax
CD3DX12_ROOT_SIGNATURE_DESC(0,NULL,0,NULL,D3D12_ROOT_SIGNATURE_FLAG_NONE)
```

</dd> <dt>

<span data-ttu-id="597d1-121">**內嵌 Init (UINT numParameters、const D3D12 \_ 根 \_ 參數 \* \_ pParameters、UINT numStaticSamplers = 0、const D3D12 \_ 靜態 \_ 取樣器 \_ DESC \* \_ pStaticSamplers = Null、D3D12 根簽章 \_ \_ \_ 旗標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="597d1-121">**inline Init(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="597d1-122">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="597d1-122">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="597d1-123">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="597d1-123">UINT numParameters</span></span>

<span data-ttu-id="597d1-124">[**D3D12 \_根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="597d1-124">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="597d1-125"> (opt) UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="597d1-125">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="597d1-126"> (opt) [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null</span><span class="sxs-lookup"><span data-stu-id="597d1-126">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="597d1-127"> (opt) [**D3D12 \_ 根 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 簽章旗標旗標 = D3D12 根簽章旗標 \_ \_ \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="597d1-127">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="597d1-128">**靜態內嵌 Init (D3D12 \_ 根簽章 \_ \_ DESC &DESC、uint NUMPARAMETERS、const D3D12 \_ 根 \_ 參數 \* \_ pParameters、uint numStaticSamplers = 0、const D3D12 \_ 靜態取樣器 \_ \_ DESC \* \_ pStaticSamplers = Null、D3D12 根簽章 \_ \_ \_ 旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="597d1-128">**static inline Init(D3D12\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="597d1-129">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="597d1-129">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="597d1-130">[**D3D12 \_根 \_ 特徵標記 \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &DESC</span><span class="sxs-lookup"><span data-stu-id="597d1-130">[**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &desc</span></span>

<span data-ttu-id="597d1-131">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="597d1-131">UINT numParameters</span></span>

<span data-ttu-id="597d1-132">[**D3D12 \_根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="597d1-132">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="597d1-133"> (opt) UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="597d1-133">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="597d1-134"> (opt) [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null</span><span class="sxs-lookup"><span data-stu-id="597d1-134">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="597d1-135"> (opt) [**D3D12 \_ 根 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 簽章旗標旗標 = D3D12 根簽章旗標 \_ \_ \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="597d1-135">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="597d1-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="597d1-136">Requirements</span></span>



| <span data-ttu-id="597d1-137">需求</span><span class="sxs-lookup"><span data-stu-id="597d1-137">Requirement</span></span> | <span data-ttu-id="597d1-138">值</span><span class="sxs-lookup"><span data-stu-id="597d1-138">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="597d1-139">標頭</span><span class="sxs-lookup"><span data-stu-id="597d1-139">Header</span></span><br/> | <dl> <span data-ttu-id="597d1-140"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="597d1-140"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="597d1-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="597d1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="597d1-142">**D3D12 \_ 根目錄 \_ 簽名 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="597d1-142">**D3D12\_ROOT\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)
</dt> <dt>

[<span data-ttu-id="597d1-143">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="597d1-143">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






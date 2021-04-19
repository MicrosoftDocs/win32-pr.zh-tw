---
title: 'CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 版本的根簽章 \_ \_ \_ \_ DESC 結構。
ms.assetid: 4505C1CE-CAA5-4092-B990-75740A2B194C
keywords:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC 結構
topic_type:
- apiref
api_name:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 695b60fef5aba124ce4e6f2ff729fdb9362c7b2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981990"
---
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a><span data-ttu-id="581c6-104">CD3DX12 已建立版本的根簽章 \_ \_ \_ \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="581c6-104">CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC structure</span></span>

<span data-ttu-id="581c6-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 版本的根簽章 \_ \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) 結構。</span><span class="sxs-lookup"><span data-stu-id="581c6-105">A helper structure to enable easy initialization of a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="581c6-106">語法</span><span class="sxs-lookup"><span data-stu-id="581c6-106">Syntax</span></span>


```C++
struct CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC  : public D3D12_VERSIONED_ROOT_SIGNATURE_DESC{
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_VERSIONED_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC1 &o);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init_1_0(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_0(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void inline Init_1_1(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_1(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="581c6-107">成員</span><span class="sxs-lookup"><span data-stu-id="581c6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="581c6-108">**CD3DX12 建立版本的根簽章 \_ \_ \_ \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="581c6-108">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="581c6-109">針對 CD3DX12 版本的根簽章 DESC，建立新的、未初始化的實例 \_ \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="581c6-109">Creates a new, uninitialized, instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="581c6-110">**明確 CD3DX12 設定版本的根簽章 \_ \_ \_ \_ desc (const D3D12 已建立版本的根簽章 \_ \_ \_ \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="581c6-110">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="581c6-111">建立 CD3DX12 版本根簽章 desc 的新實例 \_ \_ \_ \_ ，並以 [**D3D12 版本的根簽章 \_ \_ \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="581c6-111">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="581c6-112">**明確 CD3DX12 設定版本的根簽章 \_ \_ \_ \_ desc (const D3D12 根簽章 \_ \_ \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="581c6-112">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="581c6-113">建立 CD3DX12 版本根簽章 desc 的新實例 \_ \_ \_ \_ ，並以 [**D3D12 根簽章 \_ \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="581c6-113">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="581c6-114">**明確 CD3DX12 \_ 版本設定根簽章 \_ \_ \_ DESC (const D3D12 \_ root \_ signature \_ DESC1 &o)**</span><span class="sxs-lookup"><span data-stu-id="581c6-114">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="581c6-115">建立 CD3DX12 版本根簽章 DESC 的新實例 \_ \_ \_ \_ ，並以 [**D3D12 根簽章 \_ \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="581c6-115">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_ROOT\_SIGNATURE\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="581c6-116">**CD3DX12 建立版本的根簽章 \_ \_ \_ \_ DESC (UINT numParameters、const D3D12 \_ ROOT \_ PARAMETER \* \_ PPARAMETERS、UINT numStaticSamplers = 0、CONST D3D12 \_ 靜態 \_ 取樣器 \_ DESC \* \_ PSTATICSAMPLERS = Null、D3D12 根簽章 \_ \_ \_ 旗標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="581c6-116">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="581c6-117">建立 CD3DX12 版本根簽章 DESC 的新實例 \_ \_ ，並 \_ \_ 初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="581c6-117">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="581c6-118">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="581c6-118">UINT numParameters</span></span>

<span data-ttu-id="581c6-119">const [**D3D12 \_ 根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="581c6-119">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="581c6-120">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="581c6-120">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="581c6-121">const [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null</span><span class="sxs-lookup"><span data-stu-id="581c6-121">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="581c6-122">[**D3D12 \_根簽章 \_ \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="581c6-122">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="581c6-123">**CD3DX12 建立版本的根簽章 \_ \_ \_ \_ DESC (UINT numParameters、const D3D12 \_ 根 \_ PARAMETER1 \* \_ PPARAMETERS、UINT numStaticSamplers = 0、CONST D3D12 \_ 靜態 \_ 取樣器 \_ DESC \* \_ PSTATICSAMPLERS = Null、D3D12 根簽章 \_ \_ \_ 旗標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="581c6-123">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="581c6-124">建立 CD3DX12 版本根簽章 DESC 的新實例 \_ \_ ，並 \_ \_ 初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="581c6-124">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="581c6-125">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="581c6-125">UINT numParameters</span></span>

<span data-ttu-id="581c6-126">const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="581c6-126">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="581c6-127">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="581c6-127">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="581c6-128">const [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null</span><span class="sxs-lookup"><span data-stu-id="581c6-128">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="581c6-129">[**D3D12 \_根簽章 \_ \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="581c6-129">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="581c6-130">**CD3DX12 已建立版本的根簽章 \_ \_ \_ \_ DESC (CD3DX12 \_ 預設)**</span><span class="sxs-lookup"><span data-stu-id="581c6-130">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="581c6-131">建立 CD3DX12 版本根簽章 DESC 的新實例 \_ \_ \_ \_ ，並以預設參數初始化：</span><span class="sxs-lookup"><span data-stu-id="581c6-131">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the default parameters:</span></span>

<span data-ttu-id="581c6-132">UINT numParameters = 0</span><span class="sxs-lookup"><span data-stu-id="581c6-132">UINT numParameters = 0</span></span>

<span data-ttu-id="581c6-133">const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters = Null</span><span class="sxs-lookup"><span data-stu-id="581c6-133">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters = NULL</span></span>

<span data-ttu-id="581c6-134">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="581c6-134">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="581c6-135">const [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null</span><span class="sxs-lookup"><span data-stu-id="581c6-135">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="581c6-136">[**D3D12 \_根簽章 \_ \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="581c6-136">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="581c6-137">**內嵌 Init \_ 1 \_ 0 (UINT numParameters、const D3D12 \_ 根 \_ 參數 \* \_ pParameters、UINT numStaticSamplers = 0、const D3D12 \_ 靜態 \_ 取樣器 \_ DESC \* \_ pStaticSamplers = Null、D3D12 根簽章 \_ \_ \_ 旗標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="581c6-137">**inline Init\_1\_0(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="581c6-138">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="581c6-138">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="581c6-139">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="581c6-139">UINT numParameters</span></span>

<span data-ttu-id="581c6-140">const [**D3D12 \_ 根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="581c6-140">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="581c6-141">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="581c6-141">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="581c6-142">const [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null</span><span class="sxs-lookup"><span data-stu-id="581c6-142">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="581c6-143">[**D3D12 \_根簽章 \_ \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="581c6-143">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="581c6-144">**靜態內嵌 Init \_ 1 \_ 0 (D3D12 已建立版本的根簽章 \_ \_ \_ \_ DESC &DESC、uint numParameters、CONST D3D12 \_ 根 \_ 參數 \* \_ pParameters、uint numStaticSamplers = 0、CONST D3D12 \_ 靜態 \_ 取樣器 \_ DESC \* \_ pStaticSamplers = Null、D3D12 根簽章 \_ \_ \_ 旗標 = D3D12 根 \_ \_ \_ \_ 簽章旗標無)**</span><span class="sxs-lookup"><span data-stu-id="581c6-144">**static inline Init\_1\_0(D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="581c6-145">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="581c6-145">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="581c6-146">[**D3D12 \_已建立版本的根簽章 \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span><span class="sxs-lookup"><span data-stu-id="581c6-146">[**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span></span>

<span data-ttu-id="581c6-147">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="581c6-147">UINT numParameters</span></span>

<span data-ttu-id="581c6-148">const [**D3D12 \_ 根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="581c6-148">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="581c6-149">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="581c6-149">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="581c6-150">const [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null</span><span class="sxs-lookup"><span data-stu-id="581c6-150">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="581c6-151">[**D3D12 \_根簽章 \_ \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="581c6-151">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="581c6-152">**內嵌 Init \_ 1 \_ 1 (UINT numParameters、const D3D12 \_ ROOT \_ PARAMETER1 \* \_ pParameters、UINT numStaticSamplers = 0、const D3D12 \_ 靜態 \_ 取樣器 \_ DESC \* \_ pStaticSamplers = Null、D3D12 根簽章 \_ \_ \_ 旗標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="581c6-152">**inline Init\_1\_1(UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="581c6-153">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="581c6-153">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="581c6-154">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="581c6-154">UINT numParameters</span></span>

<span data-ttu-id="581c6-155">const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="581c6-155">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="581c6-156">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="581c6-156">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="581c6-157">const [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null</span><span class="sxs-lookup"><span data-stu-id="581c6-157">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="581c6-158">[**D3D12 \_根簽章 \_ \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="581c6-158">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="581c6-159">**靜態內嵌 Init \_ 1 \_ 1 (D3D12 已建立版本的根簽章 \_ \_ \_ \_ DESC &DESC、uint numParameters、CONST D3D12 \_ 根 \_ PARAMETER1 \* \_ pParameters、uint numStaticSamplers = 0、CONST D3D12 \_ 靜態 \_ 取樣器 \_ DESC \* \_ pStaticSamplers = Null、D3D12 根簽章 \_ \_ \_ 旗標 = D3D12 根 \_ \_ \_ \_ 簽章旗標無)**</span><span class="sxs-lookup"><span data-stu-id="581c6-159">**static inline Init\_1\_1(D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="581c6-160">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="581c6-160">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="581c6-161">[**D3D12 \_已建立版本的根簽章 \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span><span class="sxs-lookup"><span data-stu-id="581c6-161">[**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span></span>

<span data-ttu-id="581c6-162">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="581c6-162">UINT numParameters</span></span>

<span data-ttu-id="581c6-163">const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="581c6-163">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="581c6-164">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="581c6-164">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="581c6-165">const [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null</span><span class="sxs-lookup"><span data-stu-id="581c6-165">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="581c6-166">[**D3D12 \_根簽章 \_ \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="581c6-166">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="581c6-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="581c6-167">Requirements</span></span>



| <span data-ttu-id="581c6-168">需求</span><span class="sxs-lookup"><span data-stu-id="581c6-168">Requirement</span></span> | <span data-ttu-id="581c6-169">值</span><span class="sxs-lookup"><span data-stu-id="581c6-169">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="581c6-170">標頭</span><span class="sxs-lookup"><span data-stu-id="581c6-170">Header</span></span><br/> | <dl> <span data-ttu-id="581c6-171"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="581c6-171"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="581c6-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="581c6-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="581c6-173">**D3D12 已建立版本的根簽章 \_ \_ \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="581c6-173">**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[<span data-ttu-id="581c6-174">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="581c6-174">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






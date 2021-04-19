---
title: 'CD3DX12_STATIC_SAMPLER_DESC 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 靜態 \_ 取樣器 \_ DESC 結構。
ms.assetid: C402415D-7BD5-4E23-82C9-B29B0B5669B8
keywords:
- CD3DX12_STATIC_SAMPLER_DESC 結構
topic_type:
- apiref
api_name:
- CD3DX12_STATIC_SAMPLER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d6b10749f7a56d928e0a4218d534cc2a8ec4fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982193"
---
# <a name="cd3dx12_static_sampler_desc-structure"></a><span data-ttu-id="134b5-104">CD3DX12 \_ 靜態 \_ 取樣器 \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="134b5-104">CD3DX12\_STATIC\_SAMPLER\_DESC structure</span></span>

<span data-ttu-id="134b5-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 靜態取樣器 \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) 結構。</span><span class="sxs-lookup"><span data-stu-id="134b5-105">A helper structure to enable easy initialization of a [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="134b5-106">語法</span><span class="sxs-lookup"><span data-stu-id="134b5-106">Syntax</span></span>


```C++
struct CD3DX12_STATIC_SAMPLER_DESC  : public D3D12_STATIC_SAMPLER_DESC{
       CD3DX12_STATIC_SAMPLER_DESC();
       explicit CD3DX12_STATIC_SAMPLER_DESC(const D3D12_STATIC_SAMPLER_DESC &o);
       CD3DX12_STATIC_SAMPLER_DESC(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void static inline Init(D3D12_STATIC_SAMPLER_DESC &samplerDesc, UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="134b5-107">成員</span><span class="sxs-lookup"><span data-stu-id="134b5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="134b5-108">**CD3DX12 \_ 靜態 \_ 取樣器 \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="134b5-108">**CD3DX12\_STATIC\_SAMPLER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="134b5-109">建立 CD3DX12 靜態取樣器 DESC 的新、未初始化的實例 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="134b5-109">Creates a new, uninitialized, instance of a CD3DX12\_STATIC\_SAMPLER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="134b5-110">**明確 CD3DX12 \_ 靜態 \_ 取樣器 \_ DESC (const D3D12 \_ static 取樣器 \_ \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="134b5-110">**explicit CD3DX12\_STATIC\_SAMPLER\_DESC(const D3D12\_STATIC\_SAMPLER\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="134b5-111">建立 CD3DX12 靜態取樣器 desc 的新實例 \_ \_ \_ ，並以另一個 [**D3D12 \_ 靜態 \_ 取樣器 \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="134b5-111">Creates a new instance of a CD3DX12\_STATIC\_SAMPLER\_DESC, initialized with the contents of another [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="134b5-112">**CD3DX12 \_ 靜態 \_ 取樣 \_ 器 DESC (UINT shaderRegister，D3D12 \_ filter filter = D3D12 \_ FILTER \_ 各向異性，D3D12 \_ 材質 \_ address \_ MODE addressU = D3D12 \_ 材質 \_ address \_ mode \_ wrap，D3D12 \_ 材質 \_ address \_ mode addressV = D3D12 \_ 材質 \_ address \_ mode \_ Wrap，D3D12 \_ 紋理 \_ 位址 \_ 模式 ADDRESSW = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ WRAP，FLOAT MIPLODBIAS = 0，UINT maxAnisotropy = 16，D3D12 \_ 比較 \_ func comparisonFunc = D3D12 \_ 比較 \_ func \_ 小於 \_ 等於，D3D12 \_ 靜態 \_ 框線 \_ 色彩邊框型 = D3D12 \_ 靜態 \_ 框線色彩不 \_ \_ 透明 \_ 白色，float minLOD = 0。 f，float maxLOD = D3D12 的 \_ \_ 最大值，D3D12 \_ 著色器可見度 shaderVisibility = \_ \_ \_ \_ 0)**</span><span class="sxs-lookup"><span data-stu-id="134b5-112">**CD3DX12\_STATIC\_SAMPLER\_DESC(UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="134b5-113">建立 CD3DX12 靜態取樣器 DESC 的新實例 \_ \_ ，並 \_ 初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="134b5-113">Creates a new instance of a CD3DX12\_STATIC\_SAMPLER\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="134b5-114">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="134b5-114">UINT shaderRegister</span></span>

<span data-ttu-id="134b5-115"> (opt) [**D3D12 \_ 篩選**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) 條件 = D3D12 \_ 篩選 \_ 條件</span><span class="sxs-lookup"><span data-stu-id="134b5-115">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="134b5-116"> (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行</span><span class="sxs-lookup"><span data-stu-id="134b5-116">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="134b5-117"> (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行</span><span class="sxs-lookup"><span data-stu-id="134b5-117">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="134b5-118"> (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行</span><span class="sxs-lookup"><span data-stu-id="134b5-118">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="134b5-119"> (opt) FLOAT mipLODBias = 0</span><span class="sxs-lookup"><span data-stu-id="134b5-119">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="134b5-120"> (opt) UINT maxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="134b5-120">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="134b5-121"> (opt) [**D3D12 \_ 比較 \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12 \_ 比較 \_ func \_ 小於 \_ 相等</span><span class="sxs-lookup"><span data-stu-id="134b5-121">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="134b5-122"> (opt) [**D3D12 \_ 靜態 \_ 框線 \_ 色彩邊框型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) = D3D12 \_ 靜態 \_ 框線色彩不 \_ \_ 透明 \_ 白色</span><span class="sxs-lookup"><span data-stu-id="134b5-122">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="134b5-123"> (opt) FLOAT minLOD = 0 f</span><span class="sxs-lookup"><span data-stu-id="134b5-123">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="134b5-124"> (opt) FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX</span><span class="sxs-lookup"><span data-stu-id="134b5-124">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="134b5-125"> (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)shaderVisibility = D3D12 \_ 著色器 \_ 可見度 \_</span><span class="sxs-lookup"><span data-stu-id="134b5-125">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="134b5-126"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="134b5-126">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="134b5-127">**靜態內嵌 Init (D3D12 \_ 靜態 \_ 取樣 \_ 器 DESC &SamplerDesc、UINT shaderRegister、D3D12 \_ FILTER filter = D3D12 \_ FILTER 非 \_ 等、D3D12 \_ 紋理 \_ 位址 \_ 模式 addressU = D3D12 \_ 紋理 \_ 位址 \_ 模式 \_ wrap、D3D12 \_ 材質 \_ 位址 \_ 模式 addressV = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行、D3D12 \_ 紋理 \_ 位址 \_ 模式 ADDRESSW = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ WRAP，FLOAT MIPLODBIAS = 0，UINT maxAnisotropy = 16，D3D12 \_ 比較 \_ func comparisonFunc = D3D12 \_ 比較 \_ func \_ 小於 \_ 等於，D3D12 \_ 靜態 \_ 框線 \_ 色彩邊框型 = D3D12 \_ 靜態 \_ 框線色彩不 \_ \_ 透明 \_ 白色，float minLOD = 0。 f，float maxLOD = D3D12 的 \_ \_ 最大值，D3D12 \_ 著色器 \_ 可見度 shaderVisibility = \_ \_ \_ 0)**</span><span class="sxs-lookup"><span data-stu-id="134b5-127">**static inline Init(D3D12\_STATIC\_SAMPLER\_DESC &samplerDesc, UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="134b5-128">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="134b5-128">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="134b5-129">[**D3D12 \_靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc</span><span class="sxs-lookup"><span data-stu-id="134b5-129">[**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc</span></span>

<span data-ttu-id="134b5-130">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="134b5-130">UINT shaderRegister</span></span>

<span data-ttu-id="134b5-131"> (opt) [**D3D12 \_ 篩選**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) 條件 = D3D12 \_ 篩選 \_ 條件</span><span class="sxs-lookup"><span data-stu-id="134b5-131">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="134b5-132"> (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行</span><span class="sxs-lookup"><span data-stu-id="134b5-132">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="134b5-133"> (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行</span><span class="sxs-lookup"><span data-stu-id="134b5-133">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="134b5-134"> (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行</span><span class="sxs-lookup"><span data-stu-id="134b5-134">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="134b5-135"> (opt) FLOAT mipLODBias = 0</span><span class="sxs-lookup"><span data-stu-id="134b5-135">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="134b5-136"> (opt) UINT maxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="134b5-136">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="134b5-137"> (opt) [**D3D12 \_ 比較 \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12 \_ 比較 \_ func \_ 小於 \_ 相等</span><span class="sxs-lookup"><span data-stu-id="134b5-137">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="134b5-138"> (opt) [**D3D12 \_ 靜態 \_ 框線 \_ 色彩邊框型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) = D3D12 \_ 靜態 \_ 框線色彩不 \_ \_ 透明 \_ 白色</span><span class="sxs-lookup"><span data-stu-id="134b5-138">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="134b5-139"> (opt) FLOAT minLOD = 0 f</span><span class="sxs-lookup"><span data-stu-id="134b5-139">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="134b5-140"> (opt) FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX</span><span class="sxs-lookup"><span data-stu-id="134b5-140">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="134b5-141"> (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)shaderVisibility = D3D12 \_ 著色器 \_ 可見度 \_</span><span class="sxs-lookup"><span data-stu-id="134b5-141">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="134b5-142"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="134b5-142">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="134b5-143">**內嵌 Init (UINT shaderRegister、D3D12 \_ filter filter = D3D12 \_ FILTER \_ 各向異性、D3D12 \_ 材質 \_ address \_ mode addressU = D3D12 \_ 材質 \_ Address \_ MODE \_ WRAP、D3D12 \_ 材質 \_ address \_ Mode addressV = D3D12 \_ 材質 \_ address \_ Mode \_ wrap、D3D12 \_ 紋理 \_ 位址 \_ 模式 addressW = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ WRAP，FLOAT MipLODBias = 0，UINT maxAnisotropy = 16，D3D12 \_ 比較 \_ func comparisonFunc = D3D12 \_ 比較 \_ func \_ 小於 \_ 等於，D3D12 \_ 靜態 \_ 框線 \_ 色彩邊框型 = D3D12 \_ 靜態 \_ 框線色彩不 \_ \_ 透明 \_ 白色，float minLOD = 0。 f，float maxLOD = D3D12 的 \_ \_ 最大值，D3D12 \_ 著色器 \_ 可見度 shaderVisibility = \_ \_ \_ 0)**</span><span class="sxs-lookup"><span data-stu-id="134b5-143">**inline Init(UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="134b5-144">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="134b5-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="134b5-145">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="134b5-145">UINT shaderRegister</span></span>

<span data-ttu-id="134b5-146"> (opt) [**D3D12 \_ 篩選**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) 條件 = D3D12 \_ 篩選 \_ 條件</span><span class="sxs-lookup"><span data-stu-id="134b5-146">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="134b5-147"> (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行</span><span class="sxs-lookup"><span data-stu-id="134b5-147">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="134b5-148"> (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行</span><span class="sxs-lookup"><span data-stu-id="134b5-148">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="134b5-149"> (opt) [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ 材質 \_ 位址 \_ 模式 \_ 換行</span><span class="sxs-lookup"><span data-stu-id="134b5-149">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="134b5-150"> (opt) FLOAT mipLODBias = 0</span><span class="sxs-lookup"><span data-stu-id="134b5-150">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="134b5-151"> (opt) UINT maxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="134b5-151">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="134b5-152"> (opt) [**D3D12 \_ 比較 \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12 \_ 比較 \_ func \_ 小於 \_ 相等</span><span class="sxs-lookup"><span data-stu-id="134b5-152">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="134b5-153"> (opt) [**D3D12 \_ 靜態 \_ 框線 \_ 色彩邊框型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) = D3D12 \_ 靜態 \_ 框線色彩不 \_ \_ 透明 \_ 白色</span><span class="sxs-lookup"><span data-stu-id="134b5-153">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="134b5-154"> (opt) FLOAT minLOD = 0 f</span><span class="sxs-lookup"><span data-stu-id="134b5-154">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="134b5-155"> (opt) FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX</span><span class="sxs-lookup"><span data-stu-id="134b5-155">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="134b5-156"> (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)shaderVisibility = D3D12 \_ 著色器 \_ 可見度 \_</span><span class="sxs-lookup"><span data-stu-id="134b5-156">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="134b5-157"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="134b5-157">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="134b5-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="134b5-158">Requirements</span></span>



| <span data-ttu-id="134b5-159">需求</span><span class="sxs-lookup"><span data-stu-id="134b5-159">Requirement</span></span> | <span data-ttu-id="134b5-160">值</span><span class="sxs-lookup"><span data-stu-id="134b5-160">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="134b5-161">標頭</span><span class="sxs-lookup"><span data-stu-id="134b5-161">Header</span></span><br/> | <dl> <span data-ttu-id="134b5-162"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="134b5-162"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="134b5-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="134b5-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="134b5-164">**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="134b5-164">**D3D12\_STATIC\_SAMPLER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)
</dt> <dt>

[<span data-ttu-id="134b5-165">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="134b5-165">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






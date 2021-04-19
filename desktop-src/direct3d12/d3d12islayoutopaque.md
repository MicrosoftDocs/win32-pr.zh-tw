---
title: 'D3D12IsLayoutOpaque 函式 (D3dx12) '
description: 指出版面配置是否為不透明。
ms.assetid: 43B46A18-A725-4999-BD97-108032793A95
keywords:
- D3D12IsLayoutOpaque 函式
topic_type:
- apiref
api_name:
- D3D12IsLayoutOpaque
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971c44688e57dd1081d33a4a077a8dcadcb89abf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000221"
---
# <a name="d3d12islayoutopaque-function"></a><span data-ttu-id="b1935-104">D3D12IsLayoutOpaque 函式</span><span class="sxs-lookup"><span data-stu-id="b1935-104">D3D12IsLayoutOpaque function</span></span>

<span data-ttu-id="b1935-105">指出版面配置是否為不透明。</span><span class="sxs-lookup"><span data-stu-id="b1935-105">Indicates whether the layout is opaque.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1935-106">語法</span><span class="sxs-lookup"><span data-stu-id="b1935-106">Syntax</span></span>


```C++
bool inline D3D12IsLayoutOpaque(
   D3D12_TEXTURE_LAYOUT Layout
);
```



## <a name="parameters"></a><span data-ttu-id="b1935-107">參數</span><span class="sxs-lookup"><span data-stu-id="b1935-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1935-108">*版面配置*</span><span class="sxs-lookup"><span data-stu-id="b1935-108">*Layout*</span></span> 
</dt> <dd>

<span data-ttu-id="b1935-109">類型： **[ **D3D12 \_ 材質 \_ 版面** 配置](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**</span><span class="sxs-lookup"><span data-stu-id="b1935-109">Type: **[**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**</span></span>

<span data-ttu-id="b1935-110">要檢查的版面配置，作為 [**D3D12 \_ 材質 \_ 版面**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)配置。</span><span class="sxs-lookup"><span data-stu-id="b1935-110">The layout to check, as a [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1935-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1935-111">Return value</span></span>

<span data-ttu-id="b1935-112">類型： **bool**</span><span class="sxs-lookup"><span data-stu-id="b1935-112">Type: **bool**</span></span>

<span data-ttu-id="b1935-113">指出配置是否不透明的 **布林** 值。</span><span class="sxs-lookup"><span data-stu-id="b1935-113">A **bool** that indicates whether the layout is opaque.</span></span> <span data-ttu-id="b1935-114">如果配置是 D3D12 \_ 材質配置 \_ \_ 未知或 D3D12 \_ 材質配置 \_ \_ 64kb \_ 未定義 \_ SWIZZLE，則為不透明的版面配置。</span><span class="sxs-lookup"><span data-stu-id="b1935-114">A layout is opaque if it is D3D12\_TEXTURE\_LAYOUT\_UNKNOWN or D3D12\_TEXTURE\_LAYOUT\_64KB\_UNDEFINED\_SWIZZLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1935-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1935-115">Requirements</span></span>



| <span data-ttu-id="b1935-116">需求</span><span class="sxs-lookup"><span data-stu-id="b1935-116">Requirement</span></span> | <span data-ttu-id="b1935-117">值</span><span class="sxs-lookup"><span data-stu-id="b1935-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b1935-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b1935-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b1935-119"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1935-119"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="b1935-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="b1935-120">Library</span></span><br/> | <dl> <span data-ttu-id="b1935-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1935-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="b1935-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b1935-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="b1935-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1935-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1935-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1935-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1935-125">D3D12 的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="b1935-125">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 






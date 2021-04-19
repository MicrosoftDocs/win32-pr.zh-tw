---
title: 'D3D12GetFormatPlaneCount 函式 (D3dx12) '
description: 針對指定的虛擬配接器 (ID3D12Device) ，取得指定之 DXGI 格式的平面數目。
ms.assetid: CD21F6F9-A9AA-4CE8-A430-57C70326CB4B
keywords:
- D3D12GetFormatPlaneCount 函式
topic_type:
- apiref
api_name:
- D3D12GetFormatPlaneCount
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfc2e88c162068de2b97c9df5071398e2fab068
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997369"
---
# <a name="d3d12getformatplanecount-function"></a><span data-ttu-id="c8a46-104">D3D12GetFormatPlaneCount 函式</span><span class="sxs-lookup"><span data-stu-id="c8a46-104">D3D12GetFormatPlaneCount function</span></span>

<span data-ttu-id="c8a46-105">針對指定的虛擬配接器 (**ID3D12Device**) ，取得指定之 DXGI 格式的平面數目。</span><span class="sxs-lookup"><span data-stu-id="c8a46-105">Gets the number of planes for the specified DXGI format for the specified virtual adapter (an **ID3D12Device**).</span></span>

## <a name="syntax"></a><span data-ttu-id="c8a46-106">語法</span><span class="sxs-lookup"><span data-stu-id="c8a46-106">Syntax</span></span>


```C++
UINT8 inline D3D12GetFormatPlaneCount(
  _In_ ID3D12Device *pDevice,
       DXGI_FORMAT  Format
);
```



## <a name="parameters"></a><span data-ttu-id="c8a46-107">參數</span><span class="sxs-lookup"><span data-stu-id="c8a46-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8a46-108">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8a46-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8a46-109">類型： **[ **ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***</span><span class="sxs-lookup"><span data-stu-id="c8a46-109">Type: **[**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***</span></span>

<span data-ttu-id="c8a46-110">虛擬配接器 (用來取得平面計數的 [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)) 。</span><span class="sxs-lookup"><span data-stu-id="c8a46-110">The virtual adapter (an [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)) for which to get the plane count.</span></span>

</dd> <dt>

<span data-ttu-id="c8a46-111">*格式*</span><span class="sxs-lookup"><span data-stu-id="c8a46-111">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="c8a46-112">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="c8a46-112">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="c8a46-113">要取得平面計數的 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 。</span><span class="sxs-lookup"><span data-stu-id="c8a46-113">The [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) for which to get the plane count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8a46-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8a46-114">Return value</span></span>

<span data-ttu-id="c8a46-115">類型： **UINT8**</span><span class="sxs-lookup"><span data-stu-id="c8a46-115">Type: **UINT8**</span></span>

<span data-ttu-id="c8a46-116">指定之虛擬配接器上指定格式的平面計數。</span><span class="sxs-lookup"><span data-stu-id="c8a46-116">The plane count for the specified format on the specified virtual adapter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8a46-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8a46-117">Requirements</span></span>



| <span data-ttu-id="c8a46-118">需求</span><span class="sxs-lookup"><span data-stu-id="c8a46-118">Requirement</span></span> | <span data-ttu-id="c8a46-119">值</span><span class="sxs-lookup"><span data-stu-id="c8a46-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a46-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c8a46-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c8a46-121"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8a46-121"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="c8a46-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="c8a46-122">Library</span></span><br/> | <dl> <span data-ttu-id="c8a46-123"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8a46-123"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="c8a46-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c8a46-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="c8a46-125"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8a46-125"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8a46-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8a46-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8a46-127">**D3D12 \_ 功能 \_ 資料 \_ 格式 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="c8a46-127">**D3D12\_FEATURE\_DATA\_FORMAT\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info)
</dt> <dt>

[<span data-ttu-id="c8a46-128">**CheckFeatureSupport**</span><span class="sxs-lookup"><span data-stu-id="c8a46-128">**CheckFeatureSupport**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
</dt> <dt>

[<span data-ttu-id="c8a46-129">D3D12 的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="c8a46-129">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 


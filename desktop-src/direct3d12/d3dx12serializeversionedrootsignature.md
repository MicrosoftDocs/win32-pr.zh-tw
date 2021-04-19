---
title: 'D3DX12SerializeVersionedRootSignature 函式 (D3dx12) '
description: 有助於啟用根簽章1.1 功能（如果有的話），而且不需要維護兩個程式碼路徑來建立根簽章。 此 helper 方法會在版本1.1 不受支援時，重建版本1.0 的根簽章。
ms.assetid: 0F6BA6C1-9A33-4E99-BF34-4A0358E7427D
keywords:
- D3DX12SerializeVersionedRootSignature 函式
topic_type:
- apiref
api_name:
- D3DX12SerializeVersionedRootSignature
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70a9d0424f7f7a7f89edde18273c5d1fa22fae28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992699"
---
# <a name="d3dx12serializeversionedrootsignature-function"></a><span data-ttu-id="d2114-105">D3DX12SerializeVersionedRootSignature 函式</span><span class="sxs-lookup"><span data-stu-id="d2114-105">D3DX12SerializeVersionedRootSignature function</span></span>

<span data-ttu-id="d2114-106">有助於啟用根簽章1.1 功能（如果有的話），而且不需要維護兩個程式碼路徑來建立根簽章。</span><span class="sxs-lookup"><span data-stu-id="d2114-106">Helps enable root signature 1.1 features when they are available, and does not require maintaining two code paths for building root signatures.</span></span> <span data-ttu-id="d2114-107">此 helper 方法會在版本1.1 不受支援時，重建版本1.0 的根簽章。</span><span class="sxs-lookup"><span data-stu-id="d2114-107">This helper method reconstructs a version 1.0 root signature when version 1.1 is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2114-108">語法</span><span class="sxs-lookup"><span data-stu-id="d2114-108">Syntax</span></span>


```C++
HRESULT inline D3DX12SerializeVersionedRootSignature(
  _In_      const D3D12_VERSIONED_ROOT_SIGNATURE_DESC *pRootSignatureDesc,
                  D3D_ROOT_SIGNATURE_VERSION          MaxVersion,
  _Out_           ID3DBlob                            **ppBlob,
  _Out_opt_       ID3DBlob                            **ppErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="d2114-109">參數</span><span class="sxs-lookup"><span data-stu-id="d2114-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2114-110">*pRootSignatureDesc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d2114-110">*pRootSignatureDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2114-111">類型： **CONST D3D12 已建立版本的根簽章 \_ \_ \_ \_ DESC \***</span><span class="sxs-lookup"><span data-stu-id="d2114-111">Type: **const D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC\***</span></span>

<span data-ttu-id="d2114-112">指定 [**D3D12 \_ 版本的 \_ 根 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) 簽章 DESC，其中包含任何版本之根簽章的描述。</span><span class="sxs-lookup"><span data-stu-id="d2114-112">Specifies a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) that contains a description of any version of a root signature.</span></span>

</dd> <dt>

<span data-ttu-id="d2114-113">*Odata-maxversion*</span><span class="sxs-lookup"><span data-stu-id="d2114-113">*MaxVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="d2114-114">類型： **D3D \_ 根 \_ \_** 簽章版本</span><span class="sxs-lookup"><span data-stu-id="d2114-114">Type: **D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>

<span data-ttu-id="d2114-115">指定支援的 [**D3D 根簽章 \_ \_ \_ 版本**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)上限。</span><span class="sxs-lookup"><span data-stu-id="d2114-115">Specifies the maximum supported [**D3D\_ROOT\_SIGNATURE\_VERSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version).</span></span>

</dd> <dt>

<span data-ttu-id="d2114-116">*ppBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d2114-116">*ppBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2114-117">類型： **ID3DBlob \* \***</span><span class="sxs-lookup"><span data-stu-id="d2114-117">Type: **ID3DBlob\*\***</span></span>

<span data-ttu-id="d2114-118">記憶體區塊的指標，該區塊會接收指向 [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) 介面的指標，您可以用來存取序列化的根簽章。</span><span class="sxs-lookup"><span data-stu-id="d2114-118">A pointer to a memory block that receives a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the serialized root signature.</span></span>

</dd> <dt>

<span data-ttu-id="d2114-119">*ppErrorBlob* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="d2114-119">*ppErrorBlob* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2114-120">類型： **ID3DBlob \* \***</span><span class="sxs-lookup"><span data-stu-id="d2114-120">Type: **ID3DBlob\*\***</span></span>

<span data-ttu-id="d2114-121">記憶體區塊的指標，該區塊會接收您可以用來存取序列化程式錯誤訊息的 [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) 介面指標，如果沒有任何錯誤，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d2114-121">A pointer to a memory block that receives a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access serializer error messages, or **NULL** if there are no errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2114-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2114-122">Return value</span></span>

<span data-ttu-id="d2114-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2114-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d2114-124">如果成功，則傳回 **\_ [確定]** ，否則會傳回其中一個 [Direct3D 12 傳回碼](d3d12-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="d2114-124">Returns **S\_OK** if successful; otherwise, returns one of the [Direct3D 12 Return Codes](d3d12-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d2114-125">備註</span><span class="sxs-lookup"><span data-stu-id="d2114-125">Remarks</span></span>

<span data-ttu-id="d2114-126">這個函式的發行與 Windows 10 年度更新版 (14393) 一致。</span><span class="sxs-lookup"><span data-stu-id="d2114-126">This function was released to coincide with the Windows 10 Anniversary Update (14393).</span></span> <span data-ttu-id="d2114-127">若要支援此之前的 Windows 10 版本，請使用此函式需要設定 d3d12 以進行 *延遲載入*。</span><span class="sxs-lookup"><span data-stu-id="d2114-127">In order to support Windows 10 versions prior to this, use of this function requires d3d12.lib be set up for *delay loading*.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2114-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2114-128">Requirements</span></span>



| <span data-ttu-id="d2114-129">需求</span><span class="sxs-lookup"><span data-stu-id="d2114-129">Requirement</span></span> | <span data-ttu-id="d2114-130">值</span><span class="sxs-lookup"><span data-stu-id="d2114-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d2114-131">標頭</span><span class="sxs-lookup"><span data-stu-id="d2114-131">Header</span></span><br/>  | <dl> <span data-ttu-id="d2114-132"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2114-132"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="d2114-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="d2114-133">Library</span></span><br/> | <dl> <span data-ttu-id="d2114-134"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2114-134"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="d2114-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d2114-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="d2114-136"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2114-136"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2114-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2114-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2114-138">**D3D12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="d2114-138">**D3D12SerializeVersionedRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature)
</dt> <dt>

[<span data-ttu-id="d2114-139">D3D12 的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="d2114-139">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 


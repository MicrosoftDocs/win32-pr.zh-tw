---
description: 從 ID3DXPRTCompBuffer 壓縮的資料緩衝區，將每個樣本的主體元件分析 (PCA) 投影係數。
ms.assetid: 149098c2-35ca-46e9-a13a-94906c95cfd9
title: 'ID3DXPRTCompBuffer：： ExtractPCA 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractPCA
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ef949e9f88a843f4636643dadd7d00ffd94d98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000575"
---
# <a name="id3dxprtcompbufferextractpca-method"></a><span data-ttu-id="2ae55-103">ID3DXPRTCompBuffer：： ExtractPCA 方法</span><span class="sxs-lookup"><span data-stu-id="2ae55-103">ID3DXPRTCompBuffer::ExtractPCA method</span></span>

<span data-ttu-id="2ae55-104">從 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 壓縮的資料緩衝區，將每個樣本的主體元件分析 (PCA) 投影係數。</span><span class="sxs-lookup"><span data-stu-id="2ae55-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ae55-105">語法</span><span class="sxs-lookup"><span data-stu-id="2ae55-105">Syntax</span></span>


```C++
HRESULT ExtractPCA(
  [in] UINT  StartPCA,
  [in] UINT  NumExtract,
  [in] FLOAT *pPCACoefficients
);
```



## <a name="parameters"></a><span data-ttu-id="2ae55-106">參數</span><span class="sxs-lookup"><span data-stu-id="2ae55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ae55-107">*StartPCA* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2ae55-107">*StartPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae55-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ae55-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ae55-109">開始從緩衝區解壓縮的 PCA 投射係數索引。</span><span class="sxs-lookup"><span data-stu-id="2ae55-109">Starting index for PCA projection coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2ae55-110">*NumExtract* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2ae55-110">*NumExtract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae55-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ae55-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ae55-112">要從緩衝區中解壓縮的 PCA 投射係數數目。</span><span class="sxs-lookup"><span data-stu-id="2ae55-112">Number of PCA projection coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2ae55-113">*pPCACoefficients* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2ae55-113">*pPCACoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae55-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ae55-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2ae55-115">寫入叢集主體元件分析 (CPCA) 係數之位置的指標。</span><span class="sxs-lookup"><span data-stu-id="2ae55-115">Pointer to the location where clustered principal component analysis (CPCA) coefficients are written.</span></span> <span data-ttu-id="2ae55-116">寫入的資料大小是 (數目的樣本數目) \* (的 PCA 係數數) 。</span><span class="sxs-lookup"><span data-stu-id="2ae55-116">The size of the data written is (Number of Samples) \* (Number of PCA Coefficients).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ae55-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ae55-117">Return value</span></span>

<span data-ttu-id="2ae55-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ae55-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ae55-119">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="2ae55-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2ae55-120">如果方法失敗，則會傳回下列值。</span><span class="sxs-lookup"><span data-stu-id="2ae55-120">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ae55-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ae55-121">Requirements</span></span>



| <span data-ttu-id="2ae55-122">需求</span><span class="sxs-lookup"><span data-stu-id="2ae55-122">Requirement</span></span> | <span data-ttu-id="2ae55-123">值</span><span class="sxs-lookup"><span data-stu-id="2ae55-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ae55-124">標頭</span><span class="sxs-lookup"><span data-stu-id="2ae55-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2ae55-125"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ae55-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2ae55-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="2ae55-126">Library</span></span><br/> | <dl> <span data-ttu-id="2ae55-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ae55-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2ae55-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ae55-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ae55-129">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="2ae55-129">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 

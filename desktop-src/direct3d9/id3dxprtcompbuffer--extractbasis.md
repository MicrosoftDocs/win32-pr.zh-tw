---
description: 從 ID3DXPRTCompBuffer 壓縮的資料緩衝區中，針對指定的叢集，將 mean 和主體元件分析 (PCA) 基礎向量。
ms.assetid: dcb1372f-2c8f-4d18-9840-5982b2ed0d6e
title: 'ID3DXPRTCompBuffer：： ExtractBasis 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractBasis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ebedef91c9f3d1e277a099ffd295903e9ba77ba8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998586"
---
# <a name="id3dxprtcompbufferextractbasis-method"></a><span data-ttu-id="7a0c0-103">ID3DXPRTCompBuffer：： ExtractBasis 方法</span><span class="sxs-lookup"><span data-stu-id="7a0c0-103">ID3DXPRTCompBuffer::ExtractBasis method</span></span>

<span data-ttu-id="7a0c0-104">從 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 壓縮的資料緩衝區中，針對指定的叢集，將 mean 和主體元件分析 (PCA) 基礎向量。</span><span class="sxs-lookup"><span data-stu-id="7a0c0-104">Extracts the mean and principal component analysis (PCA) basis vectors for a given cluster from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a0c0-105">語法</span><span class="sxs-lookup"><span data-stu-id="7a0c0-105">Syntax</span></span>


```C++
HRESULT ExtractBasis(
  [in]      UINT  Cluster,
  [in, out] FLOAT *pClusterBasis
);
```



## <a name="parameters"></a><span data-ttu-id="7a0c0-106">參數</span><span class="sxs-lookup"><span data-stu-id="7a0c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a0c0-107">叢集 \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a0c0-107">*Cluster* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a0c0-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a0c0-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7a0c0-109">將解壓縮其基礎的叢集。</span><span class="sxs-lookup"><span data-stu-id="7a0c0-109">Cluster for which the basis will be extracted.</span></span>

</dd> <dt>

<span data-ttu-id="7a0c0-110">*pClusterBasis* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="7a0c0-110">*pClusterBasis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a0c0-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7a0c0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7a0c0-112">叢集之基礎向量資料陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="7a0c0-112">Pointer to an array of basis vector data for Cluster.</span></span> <span data-ttu-id="7a0c0-113">儲存的 FLOAT 資料大小將會是： (1 + 每個叢集的 PCA 向量數目) \* (係數數目) \* (色頻數目) </span><span class="sxs-lookup"><span data-stu-id="7a0c0-113">The size of the FLOAT data stored will be: (1 + Number of PCA vectors per cluster) \* (Number of coefficients) \* (Number of color channels)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a0c0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a0c0-114">Return value</span></span>

<span data-ttu-id="7a0c0-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7a0c0-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7a0c0-116">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="7a0c0-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7a0c0-117">如果方法失敗，則會傳回下列值。</span><span class="sxs-lookup"><span data-stu-id="7a0c0-117">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a0c0-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a0c0-118">Requirements</span></span>



| <span data-ttu-id="7a0c0-119">需求</span><span class="sxs-lookup"><span data-stu-id="7a0c0-119">Requirement</span></span> | <span data-ttu-id="7a0c0-120">值</span><span class="sxs-lookup"><span data-stu-id="7a0c0-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a0c0-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7a0c0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7a0c0-122"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="7a0c0-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7a0c0-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="7a0c0-123">Library</span></span><br/> | <dl> <span data-ttu-id="7a0c0-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a0c0-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7a0c0-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a0c0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a0c0-126">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="7a0c0-126">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 

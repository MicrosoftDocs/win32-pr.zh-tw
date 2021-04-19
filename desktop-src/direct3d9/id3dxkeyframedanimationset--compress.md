---
description: 將動畫中的動畫轉換成壓縮格式，並傳回儲存壓縮資料之緩衝區的指標。
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: 'ID3DXKeyframedAnimationSet：：壓縮方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.Compress
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd3a278760f2598df52d251a9e3558a72f954ceb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986126"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a><span data-ttu-id="8e36e-103">ID3DXKeyframedAnimationSet：：壓縮方法</span><span class="sxs-lookup"><span data-stu-id="8e36e-103">ID3DXKeyframedAnimationSet::Compress method</span></span>

<span data-ttu-id="8e36e-104">將動畫中的動畫轉換成壓縮格式，並傳回儲存壓縮資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="8e36e-104">Transforms animations in an animation set into a compressed format and returns a pointer to the buffer that stores the compressed data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e36e-105">語法</span><span class="sxs-lookup"><span data-stu-id="8e36e-105">Syntax</span></span>


```C++
HRESULT Compress(
  [in]  DWORD        Flags,
  [in]  FLOAT        Lossiness,
  [in]  LPD3DXFRAME  pHierarchy,
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a><span data-ttu-id="8e36e-106">參數</span><span class="sxs-lookup"><span data-stu-id="8e36e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e36e-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="8e36e-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e36e-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e36e-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e36e-109">其中一個 [**D3DXCOMPRESSION \_ 旗標**](./d3dxcompression-flags.md) 值，這些值會定義用於儲存壓縮動畫集資料的壓縮模式。</span><span class="sxs-lookup"><span data-stu-id="8e36e-109">One of the [**D3DXCOMPRESSION\_FLAGS**](./d3dxcompression-flags.md) values that define the compression mode used for storing compressed animation set data.</span></span> <span data-ttu-id="8e36e-110">D3DXCOMPRESS \_ 預設值是目前唯一支援的值。</span><span class="sxs-lookup"><span data-stu-id="8e36e-110">D3DXCOMPRESS\_DEFAULT is the only value currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="8e36e-111">*Lossiness* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8e36e-111">*Lossiness* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e36e-112">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e36e-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e36e-113">所需的壓縮遺失比例，範圍介於0到1之間。</span><span class="sxs-lookup"><span data-stu-id="8e36e-113">Desired compression loss ratio, in the range from 0 to 1.</span></span>

</dd> <dt>

<span data-ttu-id="8e36e-114">*pHierarchy* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8e36e-114">*pHierarchy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e36e-115">類型： **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="8e36e-115">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="8e36e-116">[**D3DXFRAME**](d3dxframe.md)轉換框架階層的指標。</span><span class="sxs-lookup"><span data-stu-id="8e36e-116">Pointer to a [**D3DXFRAME**](d3dxframe.md) transformation frame hierarchy.</span></span> <span data-ttu-id="8e36e-117">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8e36e-117">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8e36e-118">*ppCompressedData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8e36e-118">*ppCompressedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e36e-119">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e36e-119">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8e36e-120">指向 [**ID3DXBuffer**](id3dxbuffer.md) 壓縮動畫集之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="8e36e-120">Address of a pointer to the [**ID3DXBuffer**](id3dxbuffer.md) compressed animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e36e-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e36e-121">Return value</span></span>

<span data-ttu-id="8e36e-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8e36e-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8e36e-123">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="8e36e-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8e36e-124">如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="8e36e-124">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e36e-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e36e-125">Requirements</span></span>



| <span data-ttu-id="8e36e-126">需求</span><span class="sxs-lookup"><span data-stu-id="8e36e-126">Requirement</span></span> | <span data-ttu-id="8e36e-127">值</span><span class="sxs-lookup"><span data-stu-id="8e36e-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e36e-128">標頭</span><span class="sxs-lookup"><span data-stu-id="8e36e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="8e36e-129"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="8e36e-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8e36e-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="8e36e-130">Library</span></span><br/> | <dl> <span data-ttu-id="8e36e-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e36e-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8e36e-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e36e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e36e-133">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="8e36e-133">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 

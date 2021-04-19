---
description: 將裝訂邊套用至 FLOAT 材質緩衝區。
ms.assetid: 822483d7-ae62-498a-bce7-3a925ab21c04
title: 'ID3DXTextureGutterHelper：： ApplyGuttersFloat 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00ee6eac7328ee5f6adceb5b3966c222509237b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982025"
---
# <a name="id3dxtexturegutterhelperapplyguttersfloat-method"></a><span data-ttu-id="53d30-103">ID3DXTextureGutterHelper：： ApplyGuttersFloat 方法</span><span class="sxs-lookup"><span data-stu-id="53d30-103">ID3DXTextureGutterHelper::ApplyGuttersFloat method</span></span>

<span data-ttu-id="53d30-104">將裝訂邊套用至 FLOAT 材質緩衝區。</span><span class="sxs-lookup"><span data-stu-id="53d30-104">Applies gutters to a FLOAT texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="53d30-105">語法</span><span class="sxs-lookup"><span data-stu-id="53d30-105">Syntax</span></span>


```C++
HRESULT ApplyGuttersFloat(
  [in] FLOAT *pDataIn,
  [in] UINT  *NumCoeffs,
  [in] UINT  *Width,
  [in] UINT  *Height
);
```



## <a name="parameters"></a><span data-ttu-id="53d30-106">參數</span><span class="sxs-lookup"><span data-stu-id="53d30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53d30-107">*pDataIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53d30-107">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53d30-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="53d30-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="53d30-109">FLOAT 材質資料緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="53d30-109">Pointer to a buffer of FLOAT texture data.</span></span>

</dd> <dt>

<span data-ttu-id="53d30-110">*NumCoeffs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53d30-110">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53d30-111">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="53d30-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="53d30-112">記憶體中用來儲存範例的每個顏色通道的純量數目。</span><span class="sxs-lookup"><span data-stu-id="53d30-112">Number of scalars per color channel used in memory to store samples.</span></span> <span data-ttu-id="53d30-113">每個材質都包含 NumCoeffs 浮點值。</span><span class="sxs-lookup"><span data-stu-id="53d30-113">Each texel contains NumCoeffs FLOAT values.</span></span>

</dd> <dt>

<span data-ttu-id="53d30-114">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53d30-114">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53d30-115">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="53d30-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="53d30-116">從 [**ID3DXTextureGutterHelper：： GetWidth**](id3dxtexturegutterhelper--getwidth.md)取得之材質的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="53d30-116">Width of the texture, in pixels, obtained from [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d30-117">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53d30-117">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53d30-118">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="53d30-118">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="53d30-119">從 [**ID3DXTextureGutterHelper：： GetHeight**](id3dxtexturegutterhelper--getheight.md)取得的材質高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="53d30-119">Height of the texture, in pixels, obtained from [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53d30-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="53d30-120">Return value</span></span>

<span data-ttu-id="53d30-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="53d30-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="53d30-122">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="53d30-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="53d30-123">如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="53d30-123">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="53d30-124">備註</span><span class="sxs-lookup"><span data-stu-id="53d30-124">Remarks</span></span>

<span data-ttu-id="53d30-125">[**類別2材質**](id3dxtexturegutterhelper.md) 是藉由重新取樣類別1和4材質所產生。</span><span class="sxs-lookup"><span data-stu-id="53d30-125">[**Class 2 texels**](id3dxtexturegutterhelper.md) are generated by resampling class 1 and 4 texels.</span></span>

## <a name="requirements"></a><span data-ttu-id="53d30-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="53d30-126">Requirements</span></span>



| <span data-ttu-id="53d30-127">需求</span><span class="sxs-lookup"><span data-stu-id="53d30-127">Requirement</span></span> | <span data-ttu-id="53d30-128">值</span><span class="sxs-lookup"><span data-stu-id="53d30-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53d30-129">標頭</span><span class="sxs-lookup"><span data-stu-id="53d30-129">Header</span></span><br/>  | <dl> <span data-ttu-id="53d30-130"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="53d30-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="53d30-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="53d30-131">Library</span></span><br/> | <dl> <span data-ttu-id="53d30-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="53d30-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="53d30-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53d30-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53d30-134">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="53d30-134">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 

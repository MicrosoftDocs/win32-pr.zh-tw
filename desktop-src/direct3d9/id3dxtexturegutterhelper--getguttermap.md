---
description: 接收材質類別值，指出根據每個材質位置的材質類別。
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: 'ID3DXTextureGutterHelper：： GetGutterMap 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d973e716c598eaceaf7f75e6694a35691df4266
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982024"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a><span data-ttu-id="7a62e-103">ID3DXTextureGutterHelper：： GetGutterMap 方法</span><span class="sxs-lookup"><span data-stu-id="7a62e-103">ID3DXTextureGutterHelper::GetGutterMap method</span></span>

<span data-ttu-id="7a62e-104">接收材質類別值，指出根據每個材質位置的材質類別。</span><span class="sxs-lookup"><span data-stu-id="7a62e-104">Receives a texel class value that indicates texel class according to each texel's location.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a62e-105">語法</span><span class="sxs-lookup"><span data-stu-id="7a62e-105">Syntax</span></span>


```C++
HRESULT GetGutterMap(
  [in, out] BYTE *pGutterData
);
```



## <a name="parameters"></a><span data-ttu-id="7a62e-106">參數</span><span class="sxs-lookup"><span data-stu-id="7a62e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a62e-107">*pGutterData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="7a62e-107">*pGutterData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a62e-108">類型： **[**位元組**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7a62e-108">Type: **[**BYTE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7a62e-109">材質類別的指標。</span><span class="sxs-lookup"><span data-stu-id="7a62e-109">Pointer to the texel class.</span></span> <span data-ttu-id="7a62e-110">可能的材質類別如下所示。</span><span class="sxs-lookup"><span data-stu-id="7a62e-110">Possible texel classes are as follows.</span></span> <span data-ttu-id="7a62e-111">沒有材質類別3。</span><span class="sxs-lookup"><span data-stu-id="7a62e-111">There is no texel class 3.</span></span>



| <span data-ttu-id="7a62e-112">材質類別</span><span class="sxs-lookup"><span data-stu-id="7a62e-112">Texel Class</span></span> | <span data-ttu-id="7a62e-113">材質位置</span><span class="sxs-lookup"><span data-stu-id="7a62e-113">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a62e-114">0</span><span class="sxs-lookup"><span data-stu-id="7a62e-114">0</span></span>           | <span data-ttu-id="7a62e-115">不正確點;將不會使用材質。</span><span class="sxs-lookup"><span data-stu-id="7a62e-115">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="7a62e-116">1</span><span class="sxs-lookup"><span data-stu-id="7a62e-116">1</span></span>           | <span data-ttu-id="7a62e-117">在三角形內。</span><span class="sxs-lookup"><span data-stu-id="7a62e-117">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="7a62e-118">2</span><span class="sxs-lookup"><span data-stu-id="7a62e-118">2</span></span>           | <span data-ttu-id="7a62e-119">在裝訂邊內。</span><span class="sxs-lookup"><span data-stu-id="7a62e-119">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="7a62e-120">4</span><span class="sxs-lookup"><span data-stu-id="7a62e-120">4</span></span>           | <span data-ttu-id="7a62e-121">內部裝訂邊;材質將會評估為 [**ID3DXTextureGutterHelper：： ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md)、 [**ID3DXTextureGutterHelper：： ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)或 [**ID3DXTextureGutterHelper：： ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) 方法中的完整範例。</span><span class="sxs-lookup"><span data-stu-id="7a62e-121">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a62e-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a62e-122">Return value</span></span>

<span data-ttu-id="7a62e-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7a62e-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7a62e-124">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="7a62e-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7a62e-125">如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="7a62e-125">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="7a62e-126">備註</span><span class="sxs-lookup"><span data-stu-id="7a62e-126">Remarks</span></span>

<span data-ttu-id="7a62e-127">應用程式必須配置和管理 pGutterData，其大小指定為：</span><span class="sxs-lookup"><span data-stu-id="7a62e-127">The application must allocate and manage pGutterData, with size given by:</span></span>


```
texture width * texture height * sizeof(BYTE)
```



<span data-ttu-id="7a62e-128">紋理寬度和高度是由 [**ID3DXTextureGutterHelper：： GetWidth**](id3dxtexturegutterhelper--getwidth.md) 和 [**ID3DXTextureGutterHelper：： GetHeight**](id3dxtexturegutterhelper--getheight.md)傳回。</span><span class="sxs-lookup"><span data-stu-id="7a62e-128">Texture width and height are returned by [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md) and [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a62e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a62e-129">Requirements</span></span>



| <span data-ttu-id="7a62e-130">需求</span><span class="sxs-lookup"><span data-stu-id="7a62e-130">Requirement</span></span> | <span data-ttu-id="7a62e-131">值</span><span class="sxs-lookup"><span data-stu-id="7a62e-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a62e-132">標頭</span><span class="sxs-lookup"><span data-stu-id="7a62e-132">Header</span></span><br/>  | <dl> <span data-ttu-id="7a62e-133"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="7a62e-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7a62e-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="7a62e-134">Library</span></span><br/> | <dl> <span data-ttu-id="7a62e-135"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a62e-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7a62e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a62e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a62e-137">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="7a62e-137">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 

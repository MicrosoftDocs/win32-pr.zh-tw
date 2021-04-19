---
description: 設定材質類別值，指出根據每個材質位置的材質類別。
ms.assetid: cb2e6afb-4b6a-4b01-aaa8-1fd2d1f2bfa1
title: 'ID3DXTextureGutterHelper：： SetGutterMap 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d3c0b7c7e33664f3e078eca82a6f39b1294992a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992741"
---
# <a name="id3dxtexturegutterhelpersetguttermap-method"></a><span data-ttu-id="340ce-103">ID3DXTextureGutterHelper：： SetGutterMap 方法</span><span class="sxs-lookup"><span data-stu-id="340ce-103">ID3DXTextureGutterHelper::SetGutterMap method</span></span>

<span data-ttu-id="340ce-104">設定材質類別值，指出根據每個材質位置的材質類別。</span><span class="sxs-lookup"><span data-stu-id="340ce-104">Sets a texel class value that indicates texel class according to each texel's location.</span></span>

## <a name="syntax"></a><span data-ttu-id="340ce-105">語法</span><span class="sxs-lookup"><span data-stu-id="340ce-105">Syntax</span></span>


```C++
HRESULT SetGutterMap(
  [in] BYTE *pGutterData
);
```



## <a name="parameters"></a><span data-ttu-id="340ce-106">參數</span><span class="sxs-lookup"><span data-stu-id="340ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="340ce-107">*pGutterData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="340ce-107">*pGutterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="340ce-108">類型： **[**位元組**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="340ce-108">Type: **[**BYTE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="340ce-109">材質類別的指標。</span><span class="sxs-lookup"><span data-stu-id="340ce-109">Pointer to the texel class.</span></span> <span data-ttu-id="340ce-110">可能的材質類別如下所示。</span><span class="sxs-lookup"><span data-stu-id="340ce-110">Possible texel classes are as follows.</span></span> <span data-ttu-id="340ce-111">沒有材質類別3。</span><span class="sxs-lookup"><span data-stu-id="340ce-111">There is no texel class 3.</span></span>



| <span data-ttu-id="340ce-112">材質類別</span><span class="sxs-lookup"><span data-stu-id="340ce-112">Texel Class</span></span> | <span data-ttu-id="340ce-113">材質位置</span><span class="sxs-lookup"><span data-stu-id="340ce-113">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="340ce-114">0</span><span class="sxs-lookup"><span data-stu-id="340ce-114">0</span></span>           | <span data-ttu-id="340ce-115">不正確點;將不會使用材質。</span><span class="sxs-lookup"><span data-stu-id="340ce-115">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="340ce-116">1</span><span class="sxs-lookup"><span data-stu-id="340ce-116">1</span></span>           | <span data-ttu-id="340ce-117">在三角形內。</span><span class="sxs-lookup"><span data-stu-id="340ce-117">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="340ce-118">2</span><span class="sxs-lookup"><span data-stu-id="340ce-118">2</span></span>           | <span data-ttu-id="340ce-119">在裝訂邊內。</span><span class="sxs-lookup"><span data-stu-id="340ce-119">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="340ce-120">4</span><span class="sxs-lookup"><span data-stu-id="340ce-120">4</span></span>           | <span data-ttu-id="340ce-121">內部裝訂邊;材質將會評估為 [**ID3DXTextureGutterHelper：： ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md)、 [**ID3DXTextureGutterHelper：： ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)或 [**ID3DXTextureGutterHelper：： ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) 方法中的完整範例。</span><span class="sxs-lookup"><span data-stu-id="340ce-121">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="340ce-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="340ce-122">Return value</span></span>

<span data-ttu-id="340ce-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="340ce-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="340ce-124">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="340ce-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="340ce-125">如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="340ce-125">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="340ce-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="340ce-126">Requirements</span></span>



| <span data-ttu-id="340ce-127">需求</span><span class="sxs-lookup"><span data-stu-id="340ce-127">Requirement</span></span> | <span data-ttu-id="340ce-128">值</span><span class="sxs-lookup"><span data-stu-id="340ce-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="340ce-129">標頭</span><span class="sxs-lookup"><span data-stu-id="340ce-129">Header</span></span><br/>  | <dl> <span data-ttu-id="340ce-130"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="340ce-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="340ce-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="340ce-131">Library</span></span><br/> | <dl> <span data-ttu-id="340ce-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="340ce-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="340ce-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="340ce-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="340ce-134">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="340ce-134">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 

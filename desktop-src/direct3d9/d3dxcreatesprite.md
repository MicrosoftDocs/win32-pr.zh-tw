---
description: 建立與特定裝置相關聯的 sprite 物件。 Sprite 物件是用來在螢幕上繪製2D 影像。
ms.assetid: 1611073f-0590-415a-8ea5-dc1d224f20b9
title: 'D3DXCreateSprite 函式 (D3dx9core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSprite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1e16feb2ff07f10703c5243ebeaaee3a2a15e7f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997397"
---
# <a name="d3dxcreatesprite-function"></a><span data-ttu-id="68d5e-104">D3DXCreateSprite 函式</span><span class="sxs-lookup"><span data-stu-id="68d5e-104">D3DXCreateSprite function</span></span>

<span data-ttu-id="68d5e-105">建立與特定裝置相關聯的 sprite 物件。</span><span class="sxs-lookup"><span data-stu-id="68d5e-105">Creates a sprite object which is associated with a particular device.</span></span> <span data-ttu-id="68d5e-106">Sprite 物件是用來在螢幕上繪製2D 影像。</span><span class="sxs-lookup"><span data-stu-id="68d5e-106">Sprite objects are used to draw 2D images to the screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="68d5e-107">語法</span><span class="sxs-lookup"><span data-stu-id="68d5e-107">Syntax</span></span>


```C++
HRESULT D3DXCreateSprite(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXSPRITE      *ppSprite
);
```



## <a name="parameters"></a><span data-ttu-id="68d5e-108">參數</span><span class="sxs-lookup"><span data-stu-id="68d5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68d5e-109">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68d5e-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68d5e-110">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="68d5e-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="68d5e-111">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，與 sprite 相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="68d5e-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="68d5e-112">*ppSprite* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="68d5e-112">*ppSprite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68d5e-113">類型： **[ **LPD3DXSPRITE**](id3dxsprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="68d5e-113">Type: **[**LPD3DXSPRITE**](id3dxsprite.md)\***</span></span>

<span data-ttu-id="68d5e-114">[**ID3DXSprite**](id3dxsprite.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="68d5e-114">Address of a pointer to an [**ID3DXSprite**](id3dxsprite.md) interface.</span></span> <span data-ttu-id="68d5e-115">此介面可讓使用者存取 sprite 函數。</span><span class="sxs-lookup"><span data-stu-id="68d5e-115">This interface allows the user to access sprite functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68d5e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="68d5e-116">Return value</span></span>

<span data-ttu-id="68d5e-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="68d5e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="68d5e-118">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="68d5e-118">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="68d5e-119">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="68d5e-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="68d5e-120">備註</span><span class="sxs-lookup"><span data-stu-id="68d5e-120">Remarks</span></span>

<span data-ttu-id="68d5e-121">此介面可以用來在相關聯裝置的螢幕空間中繪製兩個維度影像。</span><span class="sxs-lookup"><span data-stu-id="68d5e-121">This interface can be used to draw two dimensional images in screen space of the associated device.</span></span>

## <a name="requirements"></a><span data-ttu-id="68d5e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="68d5e-122">Requirements</span></span>



| <span data-ttu-id="68d5e-123">需求</span><span class="sxs-lookup"><span data-stu-id="68d5e-123">Requirement</span></span> | <span data-ttu-id="68d5e-124">值</span><span class="sxs-lookup"><span data-stu-id="68d5e-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68d5e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="68d5e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="68d5e-126"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="68d5e-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="68d5e-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="68d5e-127">Library</span></span><br/> | <dl> <span data-ttu-id="68d5e-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="68d5e-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68d5e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68d5e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68d5e-130">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="68d5e-130">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 

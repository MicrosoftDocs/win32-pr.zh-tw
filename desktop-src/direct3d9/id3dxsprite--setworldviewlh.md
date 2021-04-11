---
description: 為 sprite 設定左手的世界視圖轉換。 在 billboarding 或排序 sprite 之前，需要呼叫此方法。
ms.assetid: 70f1181d-41f9-4663-91e0-8df94bce4eed
title: 'ID3DXSprite：： SetWorldViewLH 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewLH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 397c3803f6d4e445f74a8b24a61e86e72e471648
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196320"
---
# <a name="id3dxspritesetworldviewlh-method"></a><span data-ttu-id="c568c-104">ID3DXSprite：： SetWorldViewLH 方法</span><span class="sxs-lookup"><span data-stu-id="c568c-104">ID3DXSprite::SetWorldViewLH method</span></span>

<span data-ttu-id="c568c-105">為 sprite 設定左手的世界視圖轉換。</span><span class="sxs-lookup"><span data-stu-id="c568c-105">Sets the left-handed world-view transform for a sprite.</span></span> <span data-ttu-id="c568c-106">在 billboarding 或排序 sprite 之前，需要呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="c568c-106">A call to this method is required before billboarding or sorting sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="c568c-107">語法</span><span class="sxs-lookup"><span data-stu-id="c568c-107">Syntax</span></span>


```C++
HRESULT SetWorldViewLH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a><span data-ttu-id="c568c-108">參數</span><span class="sxs-lookup"><span data-stu-id="c568c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c568c-109">*pWorld* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c568c-109">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c568c-110">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c568c-110">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c568c-111">包含世界轉換之 [**D3DXMATRIX**](d3dxmatrix.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="c568c-111">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a world transform.</span></span> <span data-ttu-id="c568c-112">如果是 **Null**，則會使用身分識別矩陣進行世界轉換。</span><span class="sxs-lookup"><span data-stu-id="c568c-112">If **NULL**, the identity matrix is used for the world transform.</span></span>

</dd> <dt>

<span data-ttu-id="c568c-113">*pView* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c568c-113">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c568c-114">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c568c-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c568c-115">包含視圖轉換之 [**D3DXMATRIX**](d3dxmatrix.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="c568c-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a view transform.</span></span> <span data-ttu-id="c568c-116">如果是 **Null**，則會使用標識矩陣進行視圖轉換。</span><span class="sxs-lookup"><span data-stu-id="c568c-116">If **NULL**, the identity matrix is used for the view transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c568c-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="c568c-117">Return value</span></span>

<span data-ttu-id="c568c-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c568c-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c568c-119">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c568c-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c568c-120">如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="c568c-120">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="c568c-121">備註</span><span class="sxs-lookup"><span data-stu-id="c568c-121">Remarks</span></span>

<span data-ttu-id="c568c-122">如果您要使用 [D3DXSprite \_ \_ 佈告欄](d3dxsprite.md)、D3DXSprite SORT depth [](id3dxsprite--setworldviewrh.md) \_ \_ \_ \_ FRONTTOBACK 或 D3DXSprite \_ \_ \_ \_ [**：： Begin**](id3dxsprite--begin.md)中的 BACKTOFRONT SORT Depth ID3DXSprite 旗標值來呈現 sprite，則需要呼叫此方法 (或 ID3DXSprite：： SetWorldViewRH) 。</span><span class="sxs-lookup"><span data-stu-id="c568c-122">A call to this method (or to [**ID3DXSprite::SetWorldViewRH**](id3dxsprite--setworldviewrh.md)) is required if the sprite will be rendered with the [D3DXSprite\_\_BILLBOARD](d3dxsprite.md), D3DXSprite\_\_SORT\_DEPTH\_FRONTTOBACK, or D3DXSprite\_\_SORT\_DEPTH\_BACKTOFRONT flag value in [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c568c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c568c-123">Requirements</span></span>



| <span data-ttu-id="c568c-124">需求</span><span class="sxs-lookup"><span data-stu-id="c568c-124">Requirement</span></span> | <span data-ttu-id="c568c-125">值</span><span class="sxs-lookup"><span data-stu-id="c568c-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c568c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c568c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c568c-127"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="c568c-127"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="c568c-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="c568c-128">Library</span></span><br/> | <dl> <span data-ttu-id="c568c-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c568c-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c568c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c568c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c568c-131">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="c568c-131">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 





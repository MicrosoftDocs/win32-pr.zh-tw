---
description: 取得 sprite 轉換。
ms.assetid: d91f2776-ee87-42b3-998b-fccea178cee2
title: 'ID3DXSprite：： GetTransform 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 646fa3574c3b9be788ad32ef402a7ca2051d04de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035372"
---
# <a name="id3dxspritegettransform-method"></a><span data-ttu-id="df679-103">ID3DXSprite：： GetTransform 方法</span><span class="sxs-lookup"><span data-stu-id="df679-103">ID3DXSprite::GetTransform method</span></span>

<span data-ttu-id="df679-104">取得 sprite 轉換。</span><span class="sxs-lookup"><span data-stu-id="df679-104">Gets the sprite transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="df679-105">語法</span><span class="sxs-lookup"><span data-stu-id="df679-105">Syntax</span></span>


```C++
HRESULT GetTransform(
  [in] D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a><span data-ttu-id="df679-106">參數</span><span class="sxs-lookup"><span data-stu-id="df679-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df679-107">*pTransform* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df679-107">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df679-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="df679-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="df679-109">[**D3DXMATRIX**](d3dxmatrix.md)的指標，其中包含原始世界空間中 sprite 的轉換。</span><span class="sxs-lookup"><span data-stu-id="df679-109">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a transform of the sprite from the original world space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df679-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="df679-110">Return value</span></span>

<span data-ttu-id="df679-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df679-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df679-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="df679-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="df679-113">如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="df679-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="df679-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="df679-114">Requirements</span></span>



| <span data-ttu-id="df679-115">需求</span><span class="sxs-lookup"><span data-stu-id="df679-115">Requirement</span></span> | <span data-ttu-id="df679-116">值</span><span class="sxs-lookup"><span data-stu-id="df679-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df679-117">標頭</span><span class="sxs-lookup"><span data-stu-id="df679-117">Header</span></span><br/>  | <dl> <span data-ttu-id="df679-118"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="df679-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="df679-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="df679-119">Library</span></span><br/> | <dl> <span data-ttu-id="df679-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="df679-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="df679-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df679-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df679-122">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="df679-122">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 





---
description: 應用程式會使用 ID3DXEffectPool 介面來識別要在效果間共用的參數。 請參閱複製和共用 (Direct3D 9) 中的參數共用。 此介面沒有任何方法。
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: 'ID3DXEffectPool 介面 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectPool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893116d7e99bd720f098a8b536f1ad4fd02563ab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386430"
---
# <a name="id3dxeffectpool-interface"></a><span data-ttu-id="07f09-105">ID3DXEffectPool 介面</span><span class="sxs-lookup"><span data-stu-id="07f09-105">ID3DXEffectPool interface</span></span>

<span data-ttu-id="07f09-106">應用程式會使用 **ID3DXEffectPool** 介面來識別要在效果間共用的參數。</span><span class="sxs-lookup"><span data-stu-id="07f09-106">Applications use the **ID3DXEffectPool** interface to identify parameters that are going to be shared across effects.</span></span> <span data-ttu-id="07f09-107">請參閱 [複製和共用 (Direct3D 9) ](cloning-and-sharing.md)中的參數共用。</span><span class="sxs-lookup"><span data-stu-id="07f09-107">See parameter sharing in [Cloning and Sharing (Direct3D 9)](cloning-and-sharing.md).</span></span> <span data-ttu-id="07f09-108">此介面沒有任何方法。</span><span class="sxs-lookup"><span data-stu-id="07f09-108">This interface has no methods.</span></span>

## <a name="members"></a><span data-ttu-id="07f09-109">成員</span><span class="sxs-lookup"><span data-stu-id="07f09-109">Members</span></span>

<span data-ttu-id="07f09-110">**ID3DXEffectPool** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="07f09-110">The **ID3DXEffectPool** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="07f09-111">備註</span><span class="sxs-lookup"><span data-stu-id="07f09-111">Remarks</span></span>

<span data-ttu-id="07f09-112">ID3DXEffectPool 介面是藉由呼叫 [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md)來取得。</span><span class="sxs-lookup"><span data-stu-id="07f09-112">The ID3DXEffectPool interface is obtained by calling [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).</span></span>

<span data-ttu-id="07f09-113">LPD3DXEFFECTPOOL 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="07f09-113">The LPD3DXEFFECTPOOL type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
```



## <a name="requirements"></a><span data-ttu-id="07f09-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="07f09-114">Requirements</span></span>



| <span data-ttu-id="07f09-115">需求</span><span class="sxs-lookup"><span data-stu-id="07f09-115">Requirement</span></span> | <span data-ttu-id="07f09-116">值</span><span class="sxs-lookup"><span data-stu-id="07f09-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07f09-117">標頭</span><span class="sxs-lookup"><span data-stu-id="07f09-117">Header</span></span><br/>  | <dl> <span data-ttu-id="07f09-118"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="07f09-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="07f09-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="07f09-119">Library</span></span><br/> | <dl> <span data-ttu-id="07f09-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="07f09-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="07f09-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07f09-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07f09-122">效果介面</span><span class="sxs-lookup"><span data-stu-id="07f09-122">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 

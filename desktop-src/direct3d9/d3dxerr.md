---
description: D3DXERR 列舉：錯誤會以負數值表示，而且無法合併。
ms.assetid: 2318278e-e1e1-4cd8-a5ce-5c99f3bc47ba
title: 'D3DXERR 列舉 (D3dx9) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXERR
api_type:
- HeaderDef
api_location:
- d3dx9.h
ms.openlocfilehash: 1c1dd03500a493b30d7c1d3bfdfdf800b65a6d82
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094300"
---
# <a name="d3dxerr-enumeration"></a><span data-ttu-id="61342-103">D3DXERR 列舉</span><span class="sxs-lookup"><span data-stu-id="61342-103">D3DXERR enumeration</span></span>

<span data-ttu-id="61342-104">錯誤會以負數值表示，而且無法合併。</span><span class="sxs-lookup"><span data-stu-id="61342-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="61342-105">以下是 D3DX 公用程式程式庫隨附的方法可傳回的值清單。</span><span class="sxs-lookup"><span data-stu-id="61342-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="61342-106">如需每個可傳回值的清單，請參閱個別的方法描述。</span><span class="sxs-lookup"><span data-stu-id="61342-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="61342-107">這些清單不一定完整。</span><span class="sxs-lookup"><span data-stu-id="61342-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="61342-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="61342-108">Syntax</span></span>


```C++
enum _D3DXERR {
  D3DXERR_CANNOTMODIFYINDEXBUFFER, 
  D3DXERR_INVALIDMESH, 
  D3DXERR_CANNOTATTRSORT, 
  D3DXERR_SKINNINGNOTSUPPORTED, 
  D3DXERR_TOOMANYINFLUENCES, 
  D3DXERR_INVALIDDATA, 
  D3DXERR_LOADEDMESHASNODATA, 
  D3DXERR_DUPLICATENAMEDFRAGMENT, 
  D3DXERR_CANNOTREMOVELASTITEM 

};
```



## <a name="constants"></a><span data-ttu-id="61342-109">常數</span><span class="sxs-lookup"><span data-stu-id="61342-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="61342-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR \_ CANNOTMODIFYINDEXBUFFER**</span><span class="sxs-lookup"><span data-stu-id="61342-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR\_CANNOTMODIFYINDEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="61342-111">無法修改索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="61342-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="61342-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR \_ INVALIDMESH**</span><span class="sxs-lookup"><span data-stu-id="61342-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR\_INVALIDMESH**</span></span>
</dt> <dd>

<span data-ttu-id="61342-113">網格無效。</span><span class="sxs-lookup"><span data-stu-id="61342-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="61342-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR \_ CANNOTATTRSORT**</span><span class="sxs-lookup"><span data-stu-id="61342-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR\_CANNOTATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="61342-115">屬性排序 (D3DXMESHOPT \_ ATTRSORT) 不支援做為優化技術。</span><span class="sxs-lookup"><span data-stu-id="61342-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="61342-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR \_ SKINNINGNOTSUPPORTED**</span><span class="sxs-lookup"><span data-stu-id="61342-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR\_SKINNINGNOTSUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="61342-117">不支援 [外觀]。</span><span class="sxs-lookup"><span data-stu-id="61342-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="61342-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR \_ TOOMANYINFLUENCES**</span><span class="sxs-lookup"><span data-stu-id="61342-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR\_TOOMANYINFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="61342-119">指定了太多影響。</span><span class="sxs-lookup"><span data-stu-id="61342-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="61342-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR \_ INVALIDDATA**</span><span class="sxs-lookup"><span data-stu-id="61342-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR\_INVALIDDATA**</span></span>
</dt> <dd>

<span data-ttu-id="61342-121">資料無效。</span><span class="sxs-lookup"><span data-stu-id="61342-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="61342-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR \_ LOADEDMESHASNODATA**</span><span class="sxs-lookup"><span data-stu-id="61342-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR\_LOADEDMESHASNODATA**</span></span>
</dt> <dd>

<span data-ttu-id="61342-123">網格沒有任何資料。</span><span class="sxs-lookup"><span data-stu-id="61342-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="61342-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR \_ DUPLICATENAMEDFRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="61342-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR\_DUPLICATENAMEDFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="61342-125">具有該名稱的片段已經存在。</span><span class="sxs-lookup"><span data-stu-id="61342-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="61342-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR \_ CANNOTREMOVELASTITEM**</span><span class="sxs-lookup"><span data-stu-id="61342-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR\_CANNOTREMOVELASTITEM**</span></span>
</dt> <dd>

<span data-ttu-id="61342-127">無法刪除最後一個專案。</span><span class="sxs-lookup"><span data-stu-id="61342-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61342-128">備註</span><span class="sxs-lookup"><span data-stu-id="61342-128">Remarks</span></span>

<span data-ttu-id="61342-129">設備碼 \_ FACDD 可用來產生錯誤碼，如下列宏所示。</span><span class="sxs-lookup"><span data-stu-id="61342-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="61342-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="61342-130">Requirements</span></span>



| <span data-ttu-id="61342-131">需求</span><span class="sxs-lookup"><span data-stu-id="61342-131">Requirement</span></span> | <span data-ttu-id="61342-132">值</span><span class="sxs-lookup"><span data-stu-id="61342-132">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="61342-133">標頭</span><span class="sxs-lookup"><span data-stu-id="61342-133">Header</span></span><br/> | <dl> <span data-ttu-id="61342-134"><dt>D3dx9。h</dt></span><span class="sxs-lookup"><span data-stu-id="61342-134"><dt>D3dx9.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61342-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61342-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61342-136">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="61342-136">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 





---
title: 'D3DX11_ERR 列舉 (D3DX11 .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 錯誤會以負數值表示，而且無法合併。
ms.assetid: d042621d-a20b-4945-b6aa-714a451aa88a
keywords:
- D3DX11_ERR 列舉 Direct3D 11
- LPD3DX11_ERR 列舉指標 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_ERR
api_location:
- D3DX11.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0607bd495bad4bdeacf66ae593670dbe3ad0d2e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992365"
---
# <a name="d3dx11_err-enumeration"></a><span data-ttu-id="dbfc8-106">D3DX11 \_ ERR 列舉</span><span class="sxs-lookup"><span data-stu-id="dbfc8-106">D3DX11\_ERR enumeration</span></span>

> [!Note]  
> <span data-ttu-id="dbfc8-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="dbfc8-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="dbfc8-108">錯誤會以負數值表示，而且無法合併。</span><span class="sxs-lookup"><span data-stu-id="dbfc8-108">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="dbfc8-109">以下是 D3DX 公用程式程式庫隨附的方法可傳回的值清單。</span><span class="sxs-lookup"><span data-stu-id="dbfc8-109">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="dbfc8-110">如需每個可傳回值的清單，請參閱個別的方法描述。</span><span class="sxs-lookup"><span data-stu-id="dbfc8-110">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="dbfc8-111">這些清單不一定完整。</span><span class="sxs-lookup"><span data-stu-id="dbfc8-111">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbfc8-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbfc8-112">Syntax</span></span>


```C++
typedef enum D3DX11_ERR { 
  D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX11_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX11_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX11_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX11_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX11_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX11_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX11_ERR, *LPD3DX11_ERR;
```



## <a name="constants"></a><span data-ttu-id="dbfc8-113">常數</span><span class="sxs-lookup"><span data-stu-id="dbfc8-113">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dbfc8-114"><span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11 \_ ERR \_ 無法 \_ 修改 \_ 索引 \_ 緩衝區**</span><span class="sxs-lookup"><span data-stu-id="dbfc8-114"><span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11\_ERR\_CANNOT\_MODIFY\_INDEX\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="dbfc8-115">無法修改索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="dbfc8-115">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="dbfc8-116"><span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11 \_ 錯誤 \_ 無效 \_ 網格**</span><span class="sxs-lookup"><span data-stu-id="dbfc8-116"><span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11\_ERR\_INVALID\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="dbfc8-117">網格無效。</span><span class="sxs-lookup"><span data-stu-id="dbfc8-117">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="dbfc8-118"><span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11 \_ ERR \_ 無法 \_ \_ 進行 ATTR 排序**</span><span class="sxs-lookup"><span data-stu-id="dbfc8-118"><span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11\_ERR\_CANNOT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="dbfc8-119">屬性排序 (D3DXMESHOPT \_ ATTRSORT) 不支援做為優化技術。</span><span class="sxs-lookup"><span data-stu-id="dbfc8-119">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="dbfc8-120"><span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**\_ \_ \_ 不支援 D3DX11 錯誤的外觀 \_**</span><span class="sxs-lookup"><span data-stu-id="dbfc8-120"><span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**D3DX11\_ERR\_SKINNING\_NOT\_SUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="dbfc8-121">不支援 [外觀]。</span><span class="sxs-lookup"><span data-stu-id="dbfc8-121">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dbfc8-122"><span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11 \_ 錯誤 \_ 太 \_ 多 \_ 影響**</span><span class="sxs-lookup"><span data-stu-id="dbfc8-122"><span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11\_ERR\_TOO\_MANY\_INFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="dbfc8-123">指定了太多影響。</span><span class="sxs-lookup"><span data-stu-id="dbfc8-123">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="dbfc8-124"><span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11 \_ 錯誤 \_ 的 \_ 資料無效**</span><span class="sxs-lookup"><span data-stu-id="dbfc8-124"><span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11\_ERR\_INVALID\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="dbfc8-125">資料無效。</span><span class="sxs-lookup"><span data-stu-id="dbfc8-125">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="dbfc8-126"><span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**D3DX11 \_ 錯誤 \_ 載入 \_ 網格 \_ \_ 沒有任何 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="dbfc8-126"><span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**D3DX11\_ERR\_LOADED\_MESH\_HAS\_NO\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="dbfc8-127">網格沒有任何資料。</span><span class="sxs-lookup"><span data-stu-id="dbfc8-127">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="dbfc8-128"><span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**D3DX11 \_ 錯誤的 \_ 重複 \_ 命名 \_ 片段**</span><span class="sxs-lookup"><span data-stu-id="dbfc8-128"><span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**D3DX11\_ERR\_DUPLICATE\_NAMED\_FRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="dbfc8-129">具有該名稱的片段已經存在。</span><span class="sxs-lookup"><span data-stu-id="dbfc8-129">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="dbfc8-130"><span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11 \_ ERR \_ 無法 \_ 移除 \_ 最後一個 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="dbfc8-130"><span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11\_ERR\_CANNOT\_REMOVE\_LAST\_ITEM**</span></span>
</dt> <dd>

<span data-ttu-id="dbfc8-131">無法刪除最後一個專案。</span><span class="sxs-lookup"><span data-stu-id="dbfc8-131">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbfc8-132">備註</span><span class="sxs-lookup"><span data-stu-id="dbfc8-132">Remarks</span></span>

<span data-ttu-id="dbfc8-133">設備碼 \_ FACDD 可用來產生錯誤碼，如下列宏所示。</span><span class="sxs-lookup"><span data-stu-id="dbfc8-133">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="dbfc8-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbfc8-134">Requirements</span></span>



| <span data-ttu-id="dbfc8-135">需求</span><span class="sxs-lookup"><span data-stu-id="dbfc8-135">Requirement</span></span> | <span data-ttu-id="dbfc8-136">值</span><span class="sxs-lookup"><span data-stu-id="dbfc8-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dbfc8-137">標頭</span><span class="sxs-lookup"><span data-stu-id="dbfc8-137">Header</span></span><br/> | <dl> <span data-ttu-id="dbfc8-138"><dt>D3DX11。h</dt></span><span class="sxs-lookup"><span data-stu-id="dbfc8-138"><dt>D3DX11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbfc8-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbfc8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbfc8-140">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="dbfc8-140">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 






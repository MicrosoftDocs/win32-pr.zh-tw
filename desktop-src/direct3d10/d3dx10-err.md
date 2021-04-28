---
description: D3DX10_ERR 列舉：錯誤會以負數值表示，而且無法合併。
ms.assetid: 4149ce6d-e87a-4003-b123-5555c6b3b086
title: 'D3DX10_ERR 列舉 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ERR
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 520abae0409dd4214106363d7ffde0cfb5c81ff1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094349"
---
# <a name="d3dx10_err-enumeration"></a><span data-ttu-id="09031-103">D3DX10 \_ ERR 列舉</span><span class="sxs-lookup"><span data-stu-id="09031-103">D3DX10\_ERR enumeration</span></span>

<span data-ttu-id="09031-104">錯誤會以負數值表示，而且無法合併。</span><span class="sxs-lookup"><span data-stu-id="09031-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="09031-105">以下是 D3DX 公用程式程式庫隨附的方法可傳回的值清單。</span><span class="sxs-lookup"><span data-stu-id="09031-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="09031-106">如需每個可傳回值的清單，請參閱個別的方法描述。</span><span class="sxs-lookup"><span data-stu-id="09031-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="09031-107">這些清單不一定完整。</span><span class="sxs-lookup"><span data-stu-id="09031-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="09031-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="09031-108">Syntax</span></span>


```C++
typedef enum D3DX10_ERR { 
  D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX10_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX10_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX10_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX10_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX10_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX10_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX10_ERR, *LPD3DX10_ERR;
```



## <a name="constants"></a><span data-ttu-id="09031-109">常數</span><span class="sxs-lookup"><span data-stu-id="09031-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="09031-110"><span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10 \_ ERR \_ 無法 \_ 修改 \_ 索引 \_ 緩衝區**</span><span class="sxs-lookup"><span data-stu-id="09031-110"><span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10\_ERR\_CANNOT\_MODIFY\_INDEX\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="09031-111">無法修改索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="09031-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="09031-112"><span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**D3DX10 \_ 錯誤 \_ 無效 \_ 網格**</span><span class="sxs-lookup"><span data-stu-id="09031-112"><span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**D3DX10\_ERR\_INVALID\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="09031-113">網格無效。</span><span class="sxs-lookup"><span data-stu-id="09031-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="09031-114"><span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**D3DX10 \_ ERR \_ 無法 \_ \_ 進行 ATTR 排序**</span><span class="sxs-lookup"><span data-stu-id="09031-114"><span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**D3DX10\_ERR\_CANNOT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="09031-115">屬性排序 (D3DXMESHOPT \_ ATTRSORT) 不支援做為優化技術。</span><span class="sxs-lookup"><span data-stu-id="09031-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="09031-116"><span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**\_ \_ \_ 不支援 D3DX10 錯誤的外觀 \_**</span><span class="sxs-lookup"><span data-stu-id="09031-116"><span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**D3DX10\_ERR\_SKINNING\_NOT\_SUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="09031-117">不支援 [外觀]。</span><span class="sxs-lookup"><span data-stu-id="09031-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="09031-118"><span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10 \_ 錯誤 \_ 太 \_ 多 \_ 影響**</span><span class="sxs-lookup"><span data-stu-id="09031-118"><span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10\_ERR\_TOO\_MANY\_INFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="09031-119">指定了太多影響。</span><span class="sxs-lookup"><span data-stu-id="09031-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="09031-120"><span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**D3DX10 \_ 錯誤 \_ 的 \_ 資料無效**</span><span class="sxs-lookup"><span data-stu-id="09031-120"><span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**D3DX10\_ERR\_INVALID\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="09031-121">資料無效。</span><span class="sxs-lookup"><span data-stu-id="09031-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="09031-122"><span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**D3DX10 \_ 錯誤 \_ 載入 \_ 網格 \_ \_ 沒有任何 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="09031-122"><span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**D3DX10\_ERR\_LOADED\_MESH\_HAS\_NO\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="09031-123">網格沒有任何資料。</span><span class="sxs-lookup"><span data-stu-id="09031-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="09031-124"><span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3DX10 \_ 錯誤的 \_ 重複 \_ 命名 \_ 片段**</span><span class="sxs-lookup"><span data-stu-id="09031-124"><span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3DX10\_ERR\_DUPLICATE\_NAMED\_FRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="09031-125">具有該名稱的片段已經存在。</span><span class="sxs-lookup"><span data-stu-id="09031-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="09031-126"><span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10 \_ ERR \_ 無法 \_ 移除 \_ 最後一個 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="09031-126"><span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10\_ERR\_CANNOT\_REMOVE\_LAST\_ITEM**</span></span>
</dt> <dd>

<span data-ttu-id="09031-127">無法刪除最後一個專案。</span><span class="sxs-lookup"><span data-stu-id="09031-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09031-128">備註</span><span class="sxs-lookup"><span data-stu-id="09031-128">Remarks</span></span>

<span data-ttu-id="09031-129">設備碼 \_ FACDD 可用來產生錯誤碼，如下列宏所示。</span><span class="sxs-lookup"><span data-stu-id="09031-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="09031-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="09031-130">Requirements</span></span>



| <span data-ttu-id="09031-131">需求</span><span class="sxs-lookup"><span data-stu-id="09031-131">Requirement</span></span> | <span data-ttu-id="09031-132">值</span><span class="sxs-lookup"><span data-stu-id="09031-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="09031-133">標頭</span><span class="sxs-lookup"><span data-stu-id="09031-133">Header</span></span><br/> | <dl> <span data-ttu-id="09031-134"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="09031-134"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09031-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09031-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09031-136">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="09031-136">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 





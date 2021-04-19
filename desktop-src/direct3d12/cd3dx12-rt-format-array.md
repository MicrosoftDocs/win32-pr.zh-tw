---
title: 'CD3DX12_RT_FORMAT_ARRAY 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ RT \_ 格式 \_ 陣列結構。
ms.assetid: E890DD33-599F-4B20-BD15-2734867788E5
keywords:
- CD3DX12_RT_FORMAT_ARRAY 結構
topic_type:
- apiref
api_name:
- CD3DX12_RT_FORMAT_ARRAY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05b7ae9e51d2d6b2a43f45dc83bda2074f6b734
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993911"
---
# <a name="cd3dx12_rt_format_array-structure"></a><span data-ttu-id="343cb-104">CD3DX12 \_ RT \_ 格式 \_ 陣列結構</span><span class="sxs-lookup"><span data-stu-id="343cb-104">CD3DX12\_RT\_FORMAT\_ARRAY structure</span></span>

<span data-ttu-id="343cb-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ RT \_ 格式 \_ 陣列**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) 結構。</span><span class="sxs-lookup"><span data-stu-id="343cb-105">A helper structure to enable easy initialization of a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="343cb-106">語法</span><span class="sxs-lookup"><span data-stu-id="343cb-106">Syntax</span></span>


```C++
struct CD3DX12_RT_FORMAT_ARRAY  : public D3D12_RT_FORMAT_ARRAY{
  CD3DX12_RT_FORMAT_ARRAY CD3DX12_RT_FORMAT_ARRAY();
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const D3D12_RT_FORMAT_ARRAY& o);
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const DXGI_FORMAT* pFormats, UINT NumFormats);
                          operator const D3D12_RT_FORMAT_ARRAY&() const;
};
```



## <a name="members"></a><span data-ttu-id="343cb-107">成員</span><span class="sxs-lookup"><span data-stu-id="343cb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="343cb-108">**CD3DX12 \_ RT \_ 格式 \_ 陣列 ()**</span><span class="sxs-lookup"><span data-stu-id="343cb-108">**CD3DX12\_RT\_FORMAT\_ARRAY()**</span></span>
</dt> <dd>

<span data-ttu-id="343cb-109">建立新的、未初始化的 CD3DX12 \_ RT \_ 格式陣列實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="343cb-109">Creates a new, uninitialized, instance of a CD3DX12\_RT\_FORMAT\_ARRAY.</span></span>

</dd> <dt>

<span data-ttu-id="343cb-110">**明確的 CD3DX12 \_ rt \_ 格式 \_ 陣列 (const D3D12 \_ RT \_ 格式 \_ 陣列& o)**</span><span class="sxs-lookup"><span data-stu-id="343cb-110">**explicit CD3DX12\_RT\_FORMAT\_ARRAY(const D3D12\_RT\_FORMAT\_ARRAY& o)**</span></span>
</dt> <dd>

<span data-ttu-id="343cb-111">建立 CD3DX12 \_ RT 格式陣列的新實例 \_ \_ ，並以從 [**D3D12 \_ RT \_ 格式 \_ 陣列**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) 結構複製而來的值進行初始化。</span><span class="sxs-lookup"><span data-stu-id="343cb-111">Creates a new instance of a CD3DX12\_RT\_FORMAT\_ARRAY, initialized with values copied from a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> <dt>

<span data-ttu-id="343cb-112">**明確 \_ 的 CD3DX12 RT \_ 格式 \_ 陣列 (const DXGI \_ Format \* pFormats，UINT NumFormats)**</span><span class="sxs-lookup"><span data-stu-id="343cb-112">**explicit CD3DX12\_RT\_FORMAT\_ARRAY(const DXGI\_FORMAT\* pFormats, UINT NumFormats)**</span></span>
</dt> <dd>

<span data-ttu-id="343cb-113">建立 CD3DX12 \_ RT 格式陣列的新實例 \_ \_ ，並以參數清單中傳遞的值進行初始化。</span><span class="sxs-lookup"><span data-stu-id="343cb-113">Creates a new instance of a CD3DX12\_RT\_FORMAT\_ARRAY, initialized with the values passed in the parameter list.</span></span> <span data-ttu-id="343cb-114">*PFormats* 參數所指定的陣列內容會複製到成員陣列 **RTFormats** 中。</span><span class="sxs-lookup"><span data-stu-id="343cb-114">Contents of the array specified by the *pFormats* parameter are copied into the member array **RTFormats**.</span></span> <span data-ttu-id="343cb-115">*PFormats* 指定的陣列會假設其大小與 **RTFormats** 相同。</span><span class="sxs-lookup"><span data-stu-id="343cb-115">The array specified by *pFormats* is assumed to have the same size as **RTFormats**.</span></span>

</dd> <dt>

<span data-ttu-id="343cb-116">**operator const D3D12 \_ RT \_ 格式 \_ 陣列& () const**</span><span class="sxs-lookup"><span data-stu-id="343cb-116">**operator const D3D12\_RT\_FORMAT\_ARRAY&() const**</span></span>
</dt> <dd>

<span data-ttu-id="343cb-117">隱含轉換成 [**D3D12 \_ RT \_ 格式 \_ 陣列**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) 結構。</span><span class="sxs-lookup"><span data-stu-id="343cb-117">Implicit conversion to a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span> <span data-ttu-id="343cb-118">因為 D3D12 \_ RT \_ 格式 \_ 陣列是 CD3DX12 深度樣板 DESC1 的基礎類型 \_ \_ \_ ，所以物件只會以 const D3D12 \_ RT \_ 格式陣列參考的形式傳回 \_ 本身。</span><span class="sxs-lookup"><span data-stu-id="343cb-118">Because D3D12\_RT\_FORMAT\_ARRAY is the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, the object is simply returned as a const D3D12\_RT\_FORMAT\_ARRAY reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="343cb-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="343cb-119">Requirements</span></span>



| <span data-ttu-id="343cb-120">需求</span><span class="sxs-lookup"><span data-stu-id="343cb-120">Requirement</span></span> | <span data-ttu-id="343cb-121">值</span><span class="sxs-lookup"><span data-stu-id="343cb-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="343cb-122">標頭</span><span class="sxs-lookup"><span data-stu-id="343cb-122">Header</span></span><br/> | <dl> <span data-ttu-id="343cb-123"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="343cb-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="343cb-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="343cb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="343cb-125">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="343cb-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="343cb-126">**D3D12 \_ RT \_ 格式 \_ 陣列**</span><span class="sxs-lookup"><span data-stu-id="343cb-126">**D3D12\_RT\_FORMAT\_ARRAY**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 






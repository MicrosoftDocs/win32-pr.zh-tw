---
title: 'CommandListCast 函式 (D3dx12) '
description: 這個函式範本會將任何命令清單的常數指標轉換成 ID3D12CommandList 的 const 指標。
ms.assetid: 63719AA1-2119-456C-9D23-13933D38AFA9
keywords:
- CommandListCast 函式
topic_type:
- apiref
api_name:
- CommandListCast
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a740258f74975fecac3e1a4df2412f1fae92f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985907"
---
# <a name="commandlistcast-function"></a><span data-ttu-id="7d8a2-104">CommandListCast 函式</span><span class="sxs-lookup"><span data-stu-id="7d8a2-104">CommandListCast function</span></span>

<span data-ttu-id="7d8a2-105">這個函式範本會將任何命令清單的常數指標轉換成 ID3D12CommandList 的 const 指標。</span><span class="sxs-lookup"><span data-stu-id="7d8a2-105">This function template casts a constant pointer to any command list into a const pointer to an ID3D12CommandList.</span></span>

<span data-ttu-id="7d8a2-106">這項轉換適用于將強型別命令清單指標傳遞至 [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)。</span><span class="sxs-lookup"><span data-stu-id="7d8a2-106">This cast is useful for passing strongly-typed command list pointers into [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span></span>

## <a name="syntax"></a><span data-ttu-id="7d8a2-107">語法</span><span class="sxs-lookup"><span data-stu-id="7d8a2-107">Syntax</span></span>


```C++
ID3D12CommandList * const * inline CommandListCast(
   t_CommandListType * const * pp
);
```



## <a name="parameters"></a><span data-ttu-id="7d8a2-108">參數</span><span class="sxs-lookup"><span data-stu-id="7d8a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d8a2-109">*Pp*</span><span class="sxs-lookup"><span data-stu-id="7d8a2-109">*pp*</span></span> 
</dt> <dd>

<span data-ttu-id="7d8a2-110">類型： **t \_ CommandListType \* const \***</span><span class="sxs-lookup"><span data-stu-id="7d8a2-110">Type: **t\_CommandListType \* const \***</span></span>

<span data-ttu-id="7d8a2-111">要轉換的強型別命令清單。</span><span class="sxs-lookup"><span data-stu-id="7d8a2-111">The strongly-typed command list to cast.</span></span>

<span data-ttu-id="7d8a2-112">範本引數 **t \_ CommandListType** 指定任何強型別命令清單物件。</span><span class="sxs-lookup"><span data-stu-id="7d8a2-112">The template argument **t\_CommandListType** specifies any strongly-typed command list object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d8a2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d8a2-113">Return value</span></span>

<span data-ttu-id="7d8a2-114">類型： **ID3D12CommandList \* const \***</span><span class="sxs-lookup"><span data-stu-id="7d8a2-114">Type: **ID3D12CommandList \* const \***</span></span>

<span data-ttu-id="7d8a2-115">強型別命令清單重新解譯為 [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)。</span><span class="sxs-lookup"><span data-stu-id="7d8a2-115">The strongly-typed command list, reinterpreted as an [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).</span></span>

## <a name="remarks"></a><span data-ttu-id="7d8a2-116">備註</span><span class="sxs-lookup"><span data-stu-id="7d8a2-116">Remarks</span></span>

<span data-ttu-id="7d8a2-117">CommandListCast 會執行 **重新解譯 \_ 轉換**。</span><span class="sxs-lookup"><span data-stu-id="7d8a2-117">CommandListCast performs a **reinterpret\_cast**.</span></span> <span data-ttu-id="7d8a2-118">只要遵守命令清單的 const 性質，轉換就有效。</span><span class="sxs-lookup"><span data-stu-id="7d8a2-118">The cast is valid as long as the const-ness of the command list is respected.</span></span>

<span data-ttu-id="7d8a2-119">CommandListCast 函式定義如下：</span><span class="sxs-lookup"><span data-stu-id="7d8a2-119">The CommandListCast function is defined as the following:</span></span>


```C++
template <typename t_CommandListType>
inline ID3D12CommandList * const * CommandListCast(t_CommandListType * const * pp)
{
    return reinterpret_cast<ID3D12CommandList * const *>(pp);
}
          
```



## <a name="requirements"></a><span data-ttu-id="7d8a2-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d8a2-120">Requirements</span></span>



| <span data-ttu-id="7d8a2-121">需求</span><span class="sxs-lookup"><span data-stu-id="7d8a2-121">Requirement</span></span> | <span data-ttu-id="7d8a2-122">值</span><span class="sxs-lookup"><span data-stu-id="7d8a2-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7d8a2-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7d8a2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7d8a2-124"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d8a2-124"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="7d8a2-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="7d8a2-125">Library</span></span><br/> | <dl> <span data-ttu-id="7d8a2-126"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d8a2-126"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="7d8a2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7d8a2-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="7d8a2-128"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d8a2-128"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d8a2-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d8a2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d8a2-130">D3D12 的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="7d8a2-130">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 






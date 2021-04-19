---
title: 'D3DX12GetBaseSubobjectType 函式 (D3dx12) '
description: 傳回子物件類型，這個物件對應至傳入之子物件類型的基類。
ms.assetid: 3744B042-094C-4EA4-8185-A018B728D843
keywords:
- D3DX12GetBaseSubobjectType 函式
topic_type:
- apiref
api_name:
- D3DX12GetBaseSubobjectType
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b39f1c61be682d55512772bef1258aecdb009a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988168"
---
# <a name="d3dx12getbasesubobjecttype-function"></a><span data-ttu-id="cb3b1-104">D3DX12GetBaseSubobjectType 函式</span><span class="sxs-lookup"><span data-stu-id="cb3b1-104">D3DX12GetBaseSubobjectType function</span></span>

<span data-ttu-id="cb3b1-105">傳回子物件類型，這個物件對應至傳入之子物件類型的基類。</span><span class="sxs-lookup"><span data-stu-id="cb3b1-105">Returns the subobject type that corresponds to the base class of the passed-in subobject type.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb3b1-106">語法</span><span class="sxs-lookup"><span data-stu-id="cb3b1-106">Syntax</span></span>


```C++
D3D12_PIPELINE_STATE_SUBOBJECT_TYPE inline D3DX12GetBaseSubobjectType(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE SubobjectType
);
```



## <a name="parameters"></a><span data-ttu-id="cb3b1-107">參數</span><span class="sxs-lookup"><span data-stu-id="cb3b1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb3b1-108">*SubobjectType*</span><span class="sxs-lookup"><span data-stu-id="cb3b1-108">*SubobjectType*</span></span> 
</dt> <dd>

<span data-ttu-id="cb3b1-109">類型： **D3D12 \_ 管線 \_ 狀態 \_ \_** 子物件類型</span><span class="sxs-lookup"><span data-stu-id="cb3b1-109">Type: **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>

<span data-ttu-id="cb3b1-110">列舉值，指定您感興趣的子物件類型。</span><span class="sxs-lookup"><span data-stu-id="cb3b1-110">An enumeration value that specifies the subobject type that you're interested in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb3b1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb3b1-111">Return value</span></span>

<span data-ttu-id="cb3b1-112">類型： **D3D12 \_ 管線 \_ 狀態 \_ \_** 子物件類型</span><span class="sxs-lookup"><span data-stu-id="cb3b1-112">Type: **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>

<span data-ttu-id="cb3b1-113">如果 *SubobjectType* 對應至衍生自另一個子物件資料類型的子物件資料類型，則會傳回基底子物件資料類型的子物件類型。否則，會傳回傳入的子物件類型。</span><span class="sxs-lookup"><span data-stu-id="cb3b1-113">If *SubobjectType* corresponds to a subobject data type that is derived from another subobject data type, the subobject type of the base subobject data type is returned; otherwise, the passed-in subobject type is returned.</span></span> <span data-ttu-id="cb3b1-114">例如，如果傳入 **D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型 \_ 深度 \_ STENCIL1** ，則會傳回 **D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型 \_ 深度 \_** 樣板。</span><span class="sxs-lookup"><span data-stu-id="cb3b1-114">For example, if **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL1** is passed in, then **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb3b1-115">備註</span><span class="sxs-lookup"><span data-stu-id="cb3b1-115">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cb3b1-116">需求</span><span class="sxs-lookup"><span data-stu-id="cb3b1-116">Requirements</span></span>



| <span data-ttu-id="cb3b1-117">需求</span><span class="sxs-lookup"><span data-stu-id="cb3b1-117">Requirement</span></span> | <span data-ttu-id="cb3b1-118">值</span><span class="sxs-lookup"><span data-stu-id="cb3b1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cb3b1-119">標頭</span><span class="sxs-lookup"><span data-stu-id="cb3b1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cb3b1-120"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb3b1-120"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="cb3b1-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="cb3b1-121">Library</span></span><br/> | <dl> <span data-ttu-id="cb3b1-122"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb3b1-122"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="cb3b1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cb3b1-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="cb3b1-124"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb3b1-124"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb3b1-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb3b1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb3b1-126">D3D12 的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="cb3b1-126">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 






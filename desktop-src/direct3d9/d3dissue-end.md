---
description: 此宏會建立問題用來發出查詢結束的值。
ms.assetid: 9ced932a-5d98-4bf8-aa11-06560f53546d
title: 'D3DISSUE_END (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DISSUE_END
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 7a448346bdc5dcfbbca4cf0d55273bdadc2fdcbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323011"
---
# <a name="d3dissue_end"></a><span data-ttu-id="db3ba-103">D3DISSUE \_ 結束</span><span class="sxs-lookup"><span data-stu-id="db3ba-103">D3DISSUE\_END</span></span>

<span data-ttu-id="db3ba-104">此宏會建立 [**問題**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) 用來發出查詢結束的值。</span><span class="sxs-lookup"><span data-stu-id="db3ba-104">This macro creates a value used by [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) to issue a query end.</span></span>

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a><span data-ttu-id="db3ba-105">參數</span><span class="sxs-lookup"><span data-stu-id="db3ba-105">Parameters</span></span>





 

## <a name="remarks"></a><span data-ttu-id="db3ba-106">備註</span><span class="sxs-lookup"><span data-stu-id="db3ba-106">Remarks</span></span>

<span data-ttu-id="db3ba-107">此宏會將查詢狀態變更為未收到信號。</span><span class="sxs-lookup"><span data-stu-id="db3ba-107">This macro changes the query state to nonsignaled.</span></span>

<span data-ttu-id="db3ba-108">D3DISSUE \_ END 對下列查詢類型有效。</span><span class="sxs-lookup"><span data-stu-id="db3ba-108">D3DISSUE\_END is valid for the following query types.</span></span>

-   <span data-ttu-id="db3ba-109">D3DQUERYTYPE \_ VCACHE</span><span class="sxs-lookup"><span data-stu-id="db3ba-109">D3DQUERYTYPE\_VCACHE</span></span>
-   <span data-ttu-id="db3ba-110">D3DQUERYTYPE \_ ResourceManager</span><span class="sxs-lookup"><span data-stu-id="db3ba-110">D3DQUERYTYPE\_ResourceManager</span></span>
-   <span data-ttu-id="db3ba-111">D3DQUERYTYPE \_ VERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="db3ba-111">D3DQUERYTYPE\_VERTEXSTATS</span></span>
-   <span data-ttu-id="db3ba-112">D3DQUERYTYPE \_ 事件</span><span class="sxs-lookup"><span data-stu-id="db3ba-112">D3DQUERYTYPE\_EVENT</span></span>
-   <span data-ttu-id="db3ba-113">D3DQUERYTYPE \_ 遮蔽</span><span class="sxs-lookup"><span data-stu-id="db3ba-113">D3DQUERYTYPE\_OCCLUSION</span></span>

## <a name="requirements"></a><span data-ttu-id="db3ba-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="db3ba-114">Requirements</span></span>



| <span data-ttu-id="db3ba-115">需求</span><span class="sxs-lookup"><span data-stu-id="db3ba-115">Requirement</span></span> | <span data-ttu-id="db3ba-116">值</span><span class="sxs-lookup"><span data-stu-id="db3ba-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db3ba-117">標頭</span><span class="sxs-lookup"><span data-stu-id="db3ba-117">Header</span></span><br/> | <dl> <span data-ttu-id="db3ba-118"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="db3ba-118"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db3ba-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db3ba-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db3ba-120">巨集</span><span class="sxs-lookup"><span data-stu-id="db3ba-120">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="db3ba-121">**D3DISSUE \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="db3ba-121">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md)
</dt> <dt>

[<span data-ttu-id="db3ba-122">**D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="db3ba-122">**D3DQUERYTYPE**</span></span>](./d3dquerytype.md)
</dt> </dl>

 

 

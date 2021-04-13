---
description: 此宏會建立問題用來發出查詢開始的值。
ms.assetid: 21b8a2b0-d18f-4412-b655-3a913b7312ee
title: 'D3DISSUE_BEGIN (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DISSUE_BEGIN
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 90d932176a70159d31a239a9a37422b474acb485
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323008"
---
# <a name="d3dissue_begin"></a><span data-ttu-id="1a1ba-103">D3DISSUE \_ 開始</span><span class="sxs-lookup"><span data-stu-id="1a1ba-103">D3DISSUE\_BEGIN</span></span>

<span data-ttu-id="1a1ba-104">此宏會建立 [**問題**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) 用來發出查詢開始的值。</span><span class="sxs-lookup"><span data-stu-id="1a1ba-104">This macro creates a value used by [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) to issue a query begin.</span></span>

``` syntax
#define D3DISSUE_BEGIN (1 << 1)
```

## <a name="remarks"></a><span data-ttu-id="1a1ba-105">備註</span><span class="sxs-lookup"><span data-stu-id="1a1ba-105">Remarks</span></span>

<span data-ttu-id="1a1ba-106">D3DISSUE \_ BEGIN 對下列查詢類型有效。</span><span class="sxs-lookup"><span data-stu-id="1a1ba-106">D3DISSUE\_BEGIN is valid for the following query type.</span></span>

-   <span data-ttu-id="1a1ba-107">D3DQUERYTYPE \_ 遮蔽</span><span class="sxs-lookup"><span data-stu-id="1a1ba-107">D3DQUERYTYPE\_OCCLUSION</span></span>

## <a name="requirements"></a><span data-ttu-id="1a1ba-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a1ba-108">Requirements</span></span>



| <span data-ttu-id="1a1ba-109">需求</span><span class="sxs-lookup"><span data-stu-id="1a1ba-109">Requirement</span></span> | <span data-ttu-id="1a1ba-110">值</span><span class="sxs-lookup"><span data-stu-id="1a1ba-110">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a1ba-111">標頭</span><span class="sxs-lookup"><span data-stu-id="1a1ba-111">Header</span></span><br/> | <dl> <span data-ttu-id="1a1ba-112"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="1a1ba-112"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a1ba-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a1ba-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a1ba-114">巨集</span><span class="sxs-lookup"><span data-stu-id="1a1ba-114">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="1a1ba-115">**D3DISSUE \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="1a1ba-115">**D3DISSUE\_END**</span></span>](d3dissue-end.md)
</dt> <dt>

[<span data-ttu-id="1a1ba-116">**D3DGETDATA \_ FLUSH**</span><span class="sxs-lookup"><span data-stu-id="1a1ba-116">**D3DGETDATA\_FLUSH**</span></span>](d3dgetdata-flush.md)
</dt> <dt>

[<span data-ttu-id="1a1ba-117">**D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="1a1ba-117">**D3DQUERYTYPE**</span></span>](./d3dquerytype.md)
</dt> </dl>

 

 

---
description: 4x4 資料列主要矩陣。
ms.assetid: 2253f486-7bb6-4966-b3ec-dba47e53e372
title: 'D3DMATRIX 結構 (D3DX10Math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATRIX
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 1df0d2171e828b14fba87f6587c604146360d0e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323172"
---
# <a name="d3dmatrix-structure"></a><span data-ttu-id="dd4b8-103">D3DMATRIX 結構</span><span class="sxs-lookup"><span data-stu-id="dd4b8-103">D3DMATRIX structure</span></span>

<span data-ttu-id="dd4b8-104">4x4 資料列主要矩陣。</span><span class="sxs-lookup"><span data-stu-id="dd4b8-104">A 4x4 row-major matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd4b8-105">語法</span><span class="sxs-lookup"><span data-stu-id="dd4b8-105">Syntax</span></span>


```C++
typedef struct D3DMATRIX {
  float m[4][4];
} D3DMATRIX, *LPD3DMATRIX;
```



## <a name="members"></a><span data-ttu-id="dd4b8-106">成員</span><span class="sxs-lookup"><span data-stu-id="dd4b8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dd4b8-107">**m \[ 4 \] \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="dd4b8-107">**m\[4\]\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="dd4b8-108">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="dd4b8-108">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="dd4b8-109">4x4 資料列主要矩陣。</span><span class="sxs-lookup"><span data-stu-id="dd4b8-109">The 4x4 row-major matrix.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd4b8-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd4b8-110">Requirements</span></span>



| <span data-ttu-id="dd4b8-111">需求</span><span class="sxs-lookup"><span data-stu-id="dd4b8-111">Requirement</span></span> | <span data-ttu-id="dd4b8-112">值</span><span class="sxs-lookup"><span data-stu-id="dd4b8-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd4b8-113">標頭</span><span class="sxs-lookup"><span data-stu-id="dd4b8-113">Header</span></span><br/> | <dl> <span data-ttu-id="dd4b8-114"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="dd4b8-114"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd4b8-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd4b8-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd4b8-116">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="dd4b8-116">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 





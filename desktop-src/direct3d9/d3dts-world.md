---
description: 識別要設定為世界轉換矩陣的轉換矩陣。
ms.assetid: 2bf7ac8a-43d8-460e-a400-3b33e96441db
title: 'D3DTS_WORLD 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLD
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3c8f0ac30230a747fba34d9962791b4b331d647
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976473"
---
# <a name="d3dts_world-macro"></a><span data-ttu-id="b41f6-103">D3DTS \_ WORLD 宏</span><span class="sxs-lookup"><span data-stu-id="b41f6-103">D3DTS\_WORLD macro</span></span>

<span data-ttu-id="b41f6-104">識別要設定為世界轉換矩陣的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="b41f6-104">Identifies the transformation matrix being set as the world transformation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b41f6-105">語法</span><span class="sxs-lookup"><span data-stu-id="b41f6-105">Syntax</span></span>


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLD(void);
```



## <a name="parameters"></a><span data-ttu-id="b41f6-106">參數</span><span class="sxs-lookup"><span data-stu-id="b41f6-106">Parameters</span></span>

<span data-ttu-id="b41f6-107">這個宏沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b41f6-107">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b41f6-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b41f6-108">Return value</span></span>

<span data-ttu-id="b41f6-109">[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)相當於 [**D3DTS \_ WORLDMATRIX (0)**](./d3dts-worldmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="b41f6-109">A [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) equivalent to [**D3DTS\_WORLDMATRIX(0)**](./d3dts-worldmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b41f6-110">備註</span><span class="sxs-lookup"><span data-stu-id="b41f6-110">Remarks</span></span>

<span data-ttu-id="b41f6-111">這個宏是為了加速將現有應用程式移植到 Direct3D 9 的目的而提供。</span><span class="sxs-lookup"><span data-stu-id="b41f6-111">This macro is provided to facilitate porting existing applications to Direct3D 9.</span></span>

## <a name="requirements"></a><span data-ttu-id="b41f6-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="b41f6-112">Requirements</span></span>



| <span data-ttu-id="b41f6-113">需求</span><span class="sxs-lookup"><span data-stu-id="b41f6-113">Requirement</span></span> | <span data-ttu-id="b41f6-114">值</span><span class="sxs-lookup"><span data-stu-id="b41f6-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b41f6-115">標頭</span><span class="sxs-lookup"><span data-stu-id="b41f6-115">Header</span></span><br/> | <dl> <span data-ttu-id="b41f6-116"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="b41f6-116"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b41f6-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b41f6-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b41f6-118">巨集</span><span class="sxs-lookup"><span data-stu-id="b41f6-118">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="b41f6-119">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="b41f6-119">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="b41f6-120">**D3DTS \_ WORLDMATRIX**</span><span class="sxs-lookup"><span data-stu-id="b41f6-120">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 

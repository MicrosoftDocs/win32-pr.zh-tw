---
description: 在效果中建立程式材質填充的版本權杖。 D3DXFillxxxTX 函數會使用這個宏。
ms.assetid: b11b6229-27a3-4813-9642-9e33bcd0da7a
title: 'D3DXTX_VERSION (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTX_VERSION
api_type:
- HeaderDef
api_location:
- D3DX9Shader.h
ms.openlocfilehash: 05b034a48635e3a5a6d1a3dbdfbabd0fe2933b5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992712"
---
# <a name="d3dxtx_version"></a><span data-ttu-id="112ae-104">D3DXTX \_ 版本</span><span class="sxs-lookup"><span data-stu-id="112ae-104">D3DXTX\_VERSION</span></span>

<span data-ttu-id="112ae-105">在效果中建立程式材質填充的版本權杖。</span><span class="sxs-lookup"><span data-stu-id="112ae-105">Version token that creates a procedural texture filler in effects.</span></span> <span data-ttu-id="112ae-106">D3DXFillxxxTX 函數會使用這個宏。</span><span class="sxs-lookup"><span data-stu-id="112ae-106">This macro is used by the D3DXFillxxxTX functions.</span></span>

``` syntax
#define D3DXTX_VERSION (_Major, _Minor) (('T' << 24) | ('X' << 16) | ((_Major) << 8) | (_Minor))
```

## <a name="return-value"></a><span data-ttu-id="112ae-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="112ae-107">Return Value</span></span>

<span data-ttu-id="112ae-108">宏會傳回程序的材質版本戳記。</span><span class="sxs-lookup"><span data-stu-id="112ae-108">The macro returns the procedural texture version token.</span></span>

## <a name="requirements"></a><span data-ttu-id="112ae-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="112ae-109">Requirements</span></span>



| <span data-ttu-id="112ae-110">需求</span><span class="sxs-lookup"><span data-stu-id="112ae-110">Requirement</span></span> | <span data-ttu-id="112ae-111">值</span><span class="sxs-lookup"><span data-stu-id="112ae-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="112ae-112">標頭</span><span class="sxs-lookup"><span data-stu-id="112ae-112">Header</span></span><br/> | <dl> <span data-ttu-id="112ae-113"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="112ae-113"><dt>D3DX9Shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="112ae-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="112ae-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="112ae-115">巨集</span><span class="sxs-lookup"><span data-stu-id="112ae-115">Macros</span></span>](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[<span data-ttu-id="112ae-116">**D3DXFillTextureTX**</span><span class="sxs-lookup"><span data-stu-id="112ae-116">**D3DXFillTextureTX**</span></span>](d3dxfilltexturetx.md)
</dt> <dt>

[<span data-ttu-id="112ae-117">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="112ae-117">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> <dt>

[<span data-ttu-id="112ae-118">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="112ae-118">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 





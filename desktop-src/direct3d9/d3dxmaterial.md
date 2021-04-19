---
description: 傳回儲存在 Direct3D (. x) 檔案中的材質資訊。
ms.assetid: dfa021ba-61d8-4f99-9bbb-0cfbe11b787d
title: 'D3DXMATERIAL 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 89079b716a8c5808255b2bc660f1d364bb97315f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976456"
---
# <a name="d3dxmaterial-structure"></a><span data-ttu-id="7a01a-103">D3DXMATERIAL 結構</span><span class="sxs-lookup"><span data-stu-id="7a01a-103">D3DXMATERIAL structure</span></span>

<span data-ttu-id="7a01a-104">傳回儲存在 Direct3D (. x) 檔案中的材質資訊。</span><span class="sxs-lookup"><span data-stu-id="7a01a-104">Returns material information saved in Direct3D (.x) files.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a01a-105">語法</span><span class="sxs-lookup"><span data-stu-id="7a01a-105">Syntax</span></span>


```C++
typedef struct D3DXMATERIAL {
  D3DMATERIAL9 MatD3D;
  LPSTR        pTextureFilename;
} D3DXMATERIAL, *LPD3DXMATERIAL;
```



## <a name="members"></a><span data-ttu-id="7a01a-106">成員</span><span class="sxs-lookup"><span data-stu-id="7a01a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a01a-107">**MatD3D**</span><span class="sxs-lookup"><span data-stu-id="7a01a-107">**MatD3D**</span></span>
</dt> <dd>

<span data-ttu-id="7a01a-108">類型： **[ **D3DMATERIAL9**](d3dmaterial9.md)**</span><span class="sxs-lookup"><span data-stu-id="7a01a-108">Type: **[**D3DMATERIAL9**](d3dmaterial9.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a01a-109">描述材質屬性的 [**D3DMATERIAL9**](d3dmaterial9.md)結構。</span><span class="sxs-lookup"><span data-stu-id="7a01a-109">[**D3DMATERIAL9**](d3dmaterial9.md) structure that describes the material properties.</span></span>

</dd> <dt>

<span data-ttu-id="7a01a-110">**pTextureFilename**</span><span class="sxs-lookup"><span data-stu-id="7a01a-110">**pTextureFilename**</span></span>
</dt> <dd>

<span data-ttu-id="7a01a-111">類型： **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="7a01a-111">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="7a01a-112">指定材質檔案名的字串指標。</span><span class="sxs-lookup"><span data-stu-id="7a01a-112">Pointer to a string that specifies the file name of the texture.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a01a-113">備註</span><span class="sxs-lookup"><span data-stu-id="7a01a-113">Remarks</span></span>

<span data-ttu-id="7a01a-114">[**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md)和 [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md)函式會傳回 **D3DXMATERIAL** 結構的陣列，為網格中的每個材質指定材質色彩和材質的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a01a-114">The [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) and [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) functions return an array of **D3DXMATERIAL** structures that specify the material color and name of the texture for each material in the mesh.</span></span> <span data-ttu-id="7a01a-115">然後需要應用程式才能載入紋理。</span><span class="sxs-lookup"><span data-stu-id="7a01a-115">The application is then required to load the texture.</span></span>

<span data-ttu-id="7a01a-116">LPD3DXMATERIAL 型別定義為 **D3DXMATERIAL** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7a01a-116">The LPD3DXMATERIAL type is defined as a pointer to the **D3DXMATERIAL** structure.</span></span>


```
typedef struct D3DXMATERIAL* LPD3DXMATERIAL;
```



## <a name="requirements"></a><span data-ttu-id="7a01a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a01a-117">Requirements</span></span>



| <span data-ttu-id="7a01a-118">需求</span><span class="sxs-lookup"><span data-stu-id="7a01a-118">Requirement</span></span> | <span data-ttu-id="7a01a-119">值</span><span class="sxs-lookup"><span data-stu-id="7a01a-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a01a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="7a01a-120">Header</span></span><br/> | <dl> <span data-ttu-id="7a01a-121"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="7a01a-121"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a01a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a01a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a01a-123">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="7a01a-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="7a01a-124">**D3DXLoadMeshFromX**</span><span class="sxs-lookup"><span data-stu-id="7a01a-124">**D3DXLoadMeshFromX**</span></span>](d3dxloadmeshfromx.md)
</dt> <dt>

[<span data-ttu-id="7a01a-125">**D3DXLoadMeshFromXof**</span><span class="sxs-lookup"><span data-stu-id="7a01a-125">**D3DXLoadMeshFromXof**</span></span>](d3dxloadmeshfromxof.md)
</dt> </dl>

 

 





---
description: 包含成員結構資訊的 helper 結構。
ms.assetid: 2fbe5e97-047e-48bf-9413-dd297632288a
title: 'D3DXSHADER_STRUCTMEMBERINFO 結構 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_STRUCTMEMBERINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 01782331459956c0878b46861db0d4f11e19c7dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322827"
---
# <a name="d3dxshader_structmemberinfo-structure"></a><span data-ttu-id="d4348-103">D3DXSHADER \_ STRUCTMEMBERINFO 結構</span><span class="sxs-lookup"><span data-stu-id="d4348-103">D3DXSHADER\_STRUCTMEMBERINFO structure</span></span>

<span data-ttu-id="d4348-104">包含成員結構資訊的 helper 結構。</span><span class="sxs-lookup"><span data-stu-id="d4348-104">A helper structure containing member structure information.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4348-105">語法</span><span class="sxs-lookup"><span data-stu-id="d4348-105">Syntax</span></span>


```C++
typedef struct D3DXSHADER_STRUCTMEMBERINFO {
  DWORD Name;
  DWORD TypeInfo;
} D3DXSHADER_STRUCTMEMBERINFO, *LPD3DXSHADER_STRUCTMEMBERINFO;
```



## <a name="members"></a><span data-ttu-id="d4348-106">成員</span><span class="sxs-lookup"><span data-stu-id="d4348-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d4348-107">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d4348-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="d4348-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4348-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4348-109">從這個結構開頭算起的位移（以位元組為單位），指向包含結構成員名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="d4348-109">Offset from the beginning of this structure, in bytes, to the string that contains the structure member name.</span></span>

</dd> <dt>

<span data-ttu-id="d4348-110">**TypeInfo**</span><span class="sxs-lookup"><span data-stu-id="d4348-110">**TypeInfo**</span></span>
</dt> <dd>

<span data-ttu-id="d4348-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4348-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4348-112">從這個結構開頭算起的位移（以位元組為單位），指向包含型別資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="d4348-112">Offset from the beginning of this structure, in bytes, to the string that contains the type information.</span></span> <span data-ttu-id="d4348-113">請參閱 [**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)。</span><span class="sxs-lookup"><span data-stu-id="d4348-113">See [**D3DXSHADER\_TYPEINFO**](d3dxshader-typeinfo.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4348-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4348-114">Requirements</span></span>



| <span data-ttu-id="d4348-115">需求</span><span class="sxs-lookup"><span data-stu-id="d4348-115">Requirement</span></span> | <span data-ttu-id="d4348-116">值</span><span class="sxs-lookup"><span data-stu-id="d4348-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4348-117">標頭</span><span class="sxs-lookup"><span data-stu-id="d4348-117">Header</span></span><br/> | <dl> <span data-ttu-id="d4348-118"><dt>D3dx9shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4348-118"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4348-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4348-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4348-120">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="d4348-120">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="d4348-121">**D3DXSHADER \_ TYPEINFO**</span><span class="sxs-lookup"><span data-stu-id="d4348-121">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> </dl>

 

 

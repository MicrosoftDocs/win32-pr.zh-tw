---
description: 效果資料類型。 資料會包含在 D3DXEFFECTDEFAULT 的 pValue 成員中。
ms.assetid: d698ad6e-2ce2-48d6-90be-49bc08f172a9
title: 'D3DXEFFECTDEFAULTTYPE 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULTTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: ffd31167d712a8270011c061cd6328aa9214352e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992717"
---
# <a name="d3dxeffectdefaulttype-enumeration"></a><span data-ttu-id="28a64-104">D3DXEFFECTDEFAULTTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="28a64-104">D3DXEFFECTDEFAULTTYPE enumeration</span></span>

<span data-ttu-id="28a64-105">效果資料類型。</span><span class="sxs-lookup"><span data-stu-id="28a64-105">Effect data types.</span></span> <span data-ttu-id="28a64-106">資料會包含在 [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)的 pValue 成員中。</span><span class="sxs-lookup"><span data-stu-id="28a64-106">The data is contained in the pValue member of [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="28a64-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="28a64-107">Syntax</span></span>


```C++
typedef enum D3DXEFFECTDEFAULTTYPE { 
  D3DXEDT_STRING      = 1,
  D3DXEDT_FLOATS      = 2,
  D3DXEDT_DWORD       = 3,
  D3DXEDT_FORCEDWORD  = 0x7fffffff
} D3DXEFFECTDEFAULTTYPE, *LPD3DXEFFECTDEFAULTTYPE;
```



## <a name="constants"></a><span data-ttu-id="28a64-108">常數</span><span class="sxs-lookup"><span data-stu-id="28a64-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="28a64-109"><span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**D3DXEDT \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="28a64-109"><span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**D3DXEDT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="28a64-110">資料型別是以 Null 結束的 ASCII 文字字串。</span><span class="sxs-lookup"><span data-stu-id="28a64-110">The data type is a NULL-terminated ASCII text string.</span></span>

</dd> <dt>

<span data-ttu-id="28a64-111"><span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**D3DXEDT \_ 浮動**</span><span class="sxs-lookup"><span data-stu-id="28a64-111"><span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**D3DXEDT\_FLOATS**</span></span>
</dt> <dd>

<span data-ttu-id="28a64-112">資料類型是 float 類型的陣列。</span><span class="sxs-lookup"><span data-stu-id="28a64-112">The data type is an array of type float.</span></span> <span data-ttu-id="28a64-113">陣列中的 float 類型數目是由 [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)中的 NumBytes 指定。</span><span class="sxs-lookup"><span data-stu-id="28a64-113">The number of float types in the array is specified by NumBytes in [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span></span>

</dd> <dt>

<span data-ttu-id="28a64-114"><span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**D3DXEDT \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="28a64-114"><span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**D3DXEDT\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="28a64-115">資料類型是 DWORD。</span><span class="sxs-lookup"><span data-stu-id="28a64-115">The data type is a DWORD.</span></span>

</dd> <dt>

<span data-ttu-id="28a64-116"><span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**D3DXEDT \_ FORCEDWORD**</span><span class="sxs-lookup"><span data-stu-id="28a64-116"><span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**D3DXEDT\_FORCEDWORD**</span></span>
</dt> <dd>

<span data-ttu-id="28a64-117">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="28a64-117">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="28a64-118">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="28a64-118">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="28a64-119">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="28a64-119">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28a64-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="28a64-120">Requirements</span></span>



| <span data-ttu-id="28a64-121">需求</span><span class="sxs-lookup"><span data-stu-id="28a64-121">Requirement</span></span> | <span data-ttu-id="28a64-122">值</span><span class="sxs-lookup"><span data-stu-id="28a64-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28a64-123">標頭</span><span class="sxs-lookup"><span data-stu-id="28a64-123">Header</span></span><br/> | <dl> <span data-ttu-id="28a64-124"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="28a64-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28a64-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28a64-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28a64-126">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="28a64-126">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 





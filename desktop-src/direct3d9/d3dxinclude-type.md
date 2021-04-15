---
description: 描述 include 檔的位置。
ms.assetid: a15d363e-0d82-44a9-816b-edf2f60540b3
title: 'D3DXINCLUDE_TYPE 列舉 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINCLUDE_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 51a4ed41203a9f78ee5fef747f088e9def9033c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514589"
---
# <a name="d3dxinclude_type-enumeration"></a><span data-ttu-id="aa9f6-103">D3DXINCLUDE \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="aa9f6-103">D3DXINCLUDE\_TYPE enumeration</span></span>

<span data-ttu-id="aa9f6-104">描述 include 檔的位置。</span><span class="sxs-lookup"><span data-stu-id="aa9f6-104">Describes the location for the include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa9f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa9f6-105">Syntax</span></span>


```C++
typedef enum D3DXINCLUDE_TYPE { 
  D3DXINC_LOCAL        = 0,
  D3DXINC_SYSTEM       = 1,
  D3DXINC_FORCE_DWORD  = 0x7fffffff
} D3DXINCLUDE_TYPE, *LPD3DXINCLUDE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="aa9f6-106">常數</span><span class="sxs-lookup"><span data-stu-id="aa9f6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="aa9f6-107"><span id="D3DXINC_LOCAL"></span><span id="d3dxinc_local"></span>**D3DXINC \_ 本機**</span><span class="sxs-lookup"><span data-stu-id="aa9f6-107"><span id="D3DXINC_LOCAL"></span><span id="d3dxinc_local"></span>**D3DXINC\_LOCAL**</span></span>
</dt> <dd>

<span data-ttu-id="aa9f6-108">在本機專案中查看 include 檔案。</span><span class="sxs-lookup"><span data-stu-id="aa9f6-108">Look in the local project for the include file.</span></span>

</dd> <dt>

<span data-ttu-id="aa9f6-109"><span id="D3DXINC_SYSTEM"></span><span id="d3dxinc_system"></span>**D3DXINC \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="aa9f6-109"><span id="D3DXINC_SYSTEM"></span><span id="d3dxinc_system"></span>**D3DXINC\_SYSTEM**</span></span>
</dt> <dd>

<span data-ttu-id="aa9f6-110">查看 include 檔案的系統路徑。</span><span class="sxs-lookup"><span data-stu-id="aa9f6-110">Look in the system path for the include file.</span></span>

</dd> <dt>

<span data-ttu-id="aa9f6-111"><span id="D3DXINC_FORCE_DWORD"></span><span id="d3dxinc_force_dword"></span>**D3DXINC \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="aa9f6-111"><span id="D3DXINC_FORCE_DWORD"></span><span id="d3dxinc_force_dword"></span>**D3DXINC\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="aa9f6-112">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="aa9f6-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="aa9f6-113">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="aa9f6-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="aa9f6-114">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="aa9f6-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa9f6-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa9f6-115">Requirements</span></span>



| <span data-ttu-id="aa9f6-116">需求</span><span class="sxs-lookup"><span data-stu-id="aa9f6-116">Requirement</span></span> | <span data-ttu-id="aa9f6-117">值</span><span class="sxs-lookup"><span data-stu-id="aa9f6-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa9f6-118">標頭</span><span class="sxs-lookup"><span data-stu-id="aa9f6-118">Header</span></span><br/> | <dl> <span data-ttu-id="aa9f6-119"><dt>D3dx9shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="aa9f6-119"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa9f6-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa9f6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9f6-121">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="aa9f6-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




